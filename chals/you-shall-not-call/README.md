# You shall not call!

## challenge

Never have I seen a pickle, worming its way out of a jail, whose exploitation did not rely upon the calling of some nefarious function. Thus, I hereby declare: there shall be no call heeded within this domain anymore. It is for I yearn the secure confinement of pickles; and shall not stand their escape.

```py
#!/usr/bin/env python3

import __main__
import pickle
import io

# Security measure -- forbid calls
for op in ['reduce', 'inst', 'obj', 'newobj', 'newobj_ex']: #pickle.REDUCE, pickle.INST, pickle.OBJ, pickle.NEWOBJ, pickle.NEWOBJ_EX]:
    id = getattr(pickle, op.upper())[0]
    delattr(pickle._Unpickler, pickle._Unpickler.dispatch[id].__name__)
    pickle._Unpickler.dispatch[id] = lambda _: print("Stop right there, you heineous criminal!") or exit()

# Security measure -- remove dangerous class and method
del pickle.Unpickler
del pickle._Unpickler.find_class

# Security measure -- overload unpickler with an actually secure class
class SecureUnpickler(pickle._Unpickler):
    def find_class(self, _: str, name: str) -> object:
        # Security measure -- prevent access to dangerous elements
        for x in ['exe', 'os', 'break', 'set', 'eva', 'help', 'sys', 'load', 'open', 'dis']:
            if x in name:
                print("Smuggling contraband in broad daylight?! Guards!")
                break
        # Security measure -- only the main module is a valid lookup target
        else:
            return getattr(__main__, name)

# Security measure -- remove dangerous magic
for k in list(globals()):
    if '_' in k and k not in ['__main__', '__builtins__']:
        del globals()[k]

# Security measure -- remove dangerous magic
__builtins__ = { k: getattr(__builtins__, k) for k in dir(__builtins__) if '_' not in k }

# My jail is very secure!
data = io.BytesIO(bytes.fromhex(input('$ ')))
SecureUnpickler(data).load()
```

## intended solution

see [you-shall-not-call-revenge](../you-shall-not-call-revenge)

## unintended solution

we can abuse the fact that there is a file named `flag.txt` in a known location and it just requires a file read. although `help` was blocked, we can abuse `license` because it is a `_Printer` object

```py
>>> type(license)
<class '_sitebuiltins._Printer'>
```

we can just overwrite the `_Printer__filenames` with `['flag.txt']` to win

```
>>> license._Printer__filenames = ['flag.txt']
>>> license()
flag flag flag flag
```

so first we can just do a standard module-submodule extension sort of thing with `__main__.__main__` and `__main__.__builtins__` because the dunder builtins object is a dict (we can use build to do arb setattr with that)

then, once we have `license`, we can just overwrite the attribute `_Printer__filenames` with `['flag.txt']`. then, we can call print on license by overwriting `self.append` and using the GET opcode

too lazy to make a poc but it works, trust
