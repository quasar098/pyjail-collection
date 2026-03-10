# pyjail collection

## why

i love pyjails

## todo ctfs

make github issue if a ctf has some good pyjails and they should be added here

- amateurs ctf, 2023 and 2024

## pyjails

|title|source|description/tldr|
|-|-|-|
|Picklection|HITCON CTF 2022|get `eval` in plain sight in collections module using pickle|
|V O I D|HITCON CTF 2022|bytecode overwrite oob stuff (?)|
|[minijail](./chals/minijail)|ImaginaryCTF Round 9|eval with only the print builtin in 37 bytes|
|[tax evasion](./chals/tax-evasion)|ImaginaryCTF Round 11|python audit hook function overwrite|
|[how r u](./chals/how-r-u)|ImaginaryCTF Round 12|python2.7 non-raw input is dangerous asf|
|[Fickle Pickles](./chals/fickle-pickles)|ImaginaryCTF Round 13|weird pickle challenge|
|[prison](./chals/prison)|ImaginaryCTF Round 18|standard no builtins escape but with blacklist|
|[Stackless Jail](./chals/stackless-jail)|ImaginaryCTF Round 23|read sys environ with only stack size 1 from dis.code\_info|
|[Nameless Jail](./chals/nameless-jail)|ImaginaryCTF Round 24|use dictionary instead of multiple variables|
|[\_](./chals/_)|ImaginaryCTF Round 25|use `*` for unpacking a file object|
|[dont-repeat-yourself](./chals/dont-repeat-yourself)|ImaginaryCTF Round 28|only use each char once|
|[No Comment](./chals/no-comment)|ImaginaryCTF Round 32|abuse `\r` in input function|
|[decorated](./chals/decorated)|ImaginaryCTF Round 33|use decorators on functions|
|[Breaking in the jail](./chals/breaking-in-the-jail)|ImaginaryCTF Round 34|pickle jail, chain pickle modules with some dependencies to eventually get to os|
|Revenge is best served pickled|ImaginaryCTF Round 34|todo|
|[My Little Jail](./chals/my-little-jail)|ImaginaryCTF Round 35|overwrite global `any` with `all` to bypass blocklist|
|[PyCryptoJail](./chals/pycryptojail)|ImaginaryCTF Round 36|discrete logarithm and nfkc normalization abuse|
|[Exceptional Pyjail](./chals/exceptional-pyjail)|ImaginaryCTF Round 37|use stderr instead of stdout|
|[Safe Pickle](./chals/safe-pickle)|ImaginaryCTF Round 38|vulnerability-ish in [picklescan](https://github.com/mmaitre314/picklescan)|
|[pickle-madness](./chals/pickle-madness)|ImaginaryCTF Round 43|bash jail disguised as pickle jail|
|[Low Security Jail](./chals/low-security-jail)|ImaginaryCTF Round 44|eval blacklist overwrite|
|[pygolf](./chals/pygolf)|ImaginaryCTF Round 44|NFKC normalization op|
|[pickle overflow](./chals/pickle-overflow)|ImaginaryCTF Round 49|utf8 str encoded can be longer than 2 bytes per char|
|[pygolf 2](./chals/pygolf-2)|ImaginaryCTF Round 49|use only 25 "non-space" chars and no jail essentials also|
|[cipherjail](./chals/cipherjail)|ImaginaryCTF Round 50|monoalphabetic substitution cipher pyjail|
|[cipherjail2](./chals/cipherjail2)|ImaginaryCTF Round 50|monoalphabetic substitution cipher pyjail 2|
|Completely new challenge|ImaginaryCTF Round 50|golf a generator frame escape with no dunders, todo|
|modjail|ImaginaryCTF Round 53|abuse `#` padding with slightly shifted input of bytes_to_long, todo|
|modjail2|ImaginaryCTF Round 53|only ascii input, use LLL, todo|
|modjail3|ImaginaryCTF Round 53|weird numbers repr constraint, use LLL again, todo|
|electronic jail|ImaginaryCTF Round 54|4x email parsing inject a payload|
|another gambling jail|ImaginaryCTF Round 56|todo|
|pygolf4|ImaginaryCTF Round 56|fuzz a leak of `v` through stderr, sol `v(*1)`|
|Real Gambling Jail|ImaginaryCTF Round 56|always check py version by using Dockerfile hash|
|[You shall not call!](./chals/you-shall-not-call)|ImaginaryCTF 2023|BUILD opcode abuse into unpickler attr overwrite with cheese-ish|
|[You shall not call Revenge](./chals/you-shall-not-call-revenge)|ImaginaryCTF 2023|BUILD opcode abuse into unpickler attr overwrite|
|[Get and set](./chals/get-and-set)|ImaginaryCTF 2023|pydash (almost) arbitrary get and set|
|[pyquinejailgolf](./chals/pyquinejailgolf)|amateursCTF 2024|todo|
|[pyquinejailgolf 2](./chals/pyquinejailgolf-2)|amateursCTF 2024|todo|
|[Just Another Pickle Jail](./chals/just-another-pickle-jail)|Sekai CTF 2023|todo|
|[introspection](./chals/introspection)|angstromCTF 2024|find discrepancies between pickle c impl and python impl (python2)|
|[llama jail](./chals/llama-jail)|vsCTF 2024|bypass ast visitor when ast.iter_child_nodes|
|[llama jail revenge](./chals/llama-jail-revenge)|vsCTF 2024|attributeerror obj trick|
|calc|ImaginaryCTF 2024|bypass audit hook with signal|
|ok-nice|ImaginaryCTF 2024|division by 0 side channel|
|ASTea|UIUCTF 2024|bypass simple ast thingy|
|prison|ifCTF 2023 finals|todo|
|[repickle](./chals/repickle)|CyberSpace CTF 2024|abuse bug in pickler|
|parseltongue|jailCTF 2024|todo|
|[smiley-faiss](./chals/smiley-faiss)|jailCTF 2024|build opcode abuse|
|parity 1|jailCTF 2024|todo|
|parity 2|jailCTF 2024|todo|
|MMM|jailCTF 2024|todo|
|filter'd|jailCTF 2024|todo|
|charredcoal|jailCTF 2024|todo|
|what numbers?|jailCTF 2024|todo|
|polyglo7quine|jailCTF 2024|todo|
|what flag?|jailCTF 2024|todo|
|respy evil challenge|jailCTF 2024|todo|
|void|jailCTF 2024|todo|
|respy nice challenge|jailCTF 2024|todo|
|functional programming|jailCTF 2024|todo|
|jellyjail|jailCTF 2024|todo|
|lost in transit|jailCTF 2024|todo|
|computer-monitor|jailCTF 2024|todo|
|pickled magic|jailCTF 2024|todo|
|stupid crypto chall|jailCTF 2024|todo|
|get and call|jailCTF 2024|todo|
|no nonsense|jailCTF 2024|todo|
|last message|jailCTF 2024|todo|
|axed|TCP1P CTF 2024|python2 `__metaclass__` abuse|
|sym|TCP1P CTF 2024|todo|
|typically not a revenge|TCP1P CTF 2024|sys & builtins nuked, `a-zA-Z._[]` allowed|
|functional|TCP1P CTF 2024|challenge copied from jailctf but with rce|
|RSAjail-1|Blue Water CTF 2024|todo|
|RSAjail-2|Blue Water CTF 2024|todo|
|RSAjail-3|Blue Water CTF 2024|todo|
|Prison Reform|diceCTF 2023|match case for arb getattr|
|unipickle|diceCTF quals 2024|pickle with utf8 valid bytes|
|diligent-auditor|diceCTF quals 2024|overwrite audit hook stuff with ctypes|
|IRS|diceCTF quals 2024|bypass c audit hook with pwn|
|gentleman|BuckeyeCTF 2024|novel technique with `inp.format()` + arb file write causes rce through ctypes cdll getitem|
|1linepyjail|SECCON quals 2024|use help to import anything for subclasses usage|
|Don't Sandbox Python 1|UofTCTF 2025|use numpy module attributes to get to dangerous stuffs|
|Don't Sandbox Python 2|UofTCTF 2025|todo (it is a 0day)|
|Don't Sandbox Python 3|UofTCTF 2025|todo (it is a 0day)|
|[Paper Viper](./chals/paper-viper)|KalmarCTF 2025|follow up to "Dont't Sandbox Python" series in UofTCTF, abusing numpy `genfromtxt`|
|SSPJ|Srdnlen CTF 2025|`.lower()` filter bypass and `__getattr__` module attr overwrite with import|
|Another Impossible Escape|Srdnlen CTF 2025|func default dict abuse and use of `gc` module to recover deleted flag|
|snecko's lair|LACTF 2025|overwrite `__code__` bytecode of `evaluate_value` of 3.14+ TypeAliasType|
|farquaad|LACTF 2025|no `E` or `e`|
|vibe-coding|b01lers CTF 2025|todo|
|shakespearejail|b01lers CTF 2025|todo|
|/>>=jail|b01lers CTF 2025|todo|
|prismatic|b01lers CTF 2025|todo|
|emacs-jail|b01lers CTF 2025|todo|
|monochromatic|b01lers CTF 2025|todo|
|evaldle|UMDCTF 2025|todo|
|Comments Only|UIUCTF 2025|python3 detecting file as zip and running it (zipimporter) abuse|
|yaps|DiceCTF 2026|pickle/cpickle divergence in py3.15+ bc of dict/array memo in cpickle|
|pytecoding|DiceCTF 2026|COPY out of bounds x bytecode golf|
