# Awesome Python Reversing

A curated list of awesome Python reversing libraries, tools and resources.

- [Disassemblers](#disassemblers)
- [Decompilers](#decompilers)
- [Debuggers](#debuggers)
- [Bytecode](#bytecode)
    - [Editors](#editors)
    - [Manual analysis](#manual-analysis)
- [Python internals](#python-internals)
- [Packers](#packers)
- [Extractors](#extractors)
- [Obfuscators](#obfuscators)
- [Deobfuscators](#deobfuscators)
- [Resources](#resources)


---

## Disassemblers

*Python bytecode disassemblers.*

* [dis](https://docs.python.org/3/library/dis.html) - The built-in Python disassembler.
* [xdis](https://github.com/rocky/python-xdis) - A Python cross-version bytecode library and disassembler.
* [pycdas](https://github.com/zrax/pycdc) - A disassembler and decompiler written in C++ aiming to support all Python versions.

## Decompilers

*Python bytecode decompilers.*

* [pylingual](https://github.com/syssec-utd/pylingual) ([web service](https://pylingual.io/)) - An AI decompiler for multiple, more recent, Python versions. Has built-in output checking and is in general one of the better decompilers out there.
* [decompile3](https://github.com/rocky/python-decompile3) - A Python decompiler aiming to support versions 3.7 - 3.8.
* [uncompyle6](https://github.com/rocky/python-uncompyle6) - A Python decompiler aiming to support versions 1.0 - 3.8 (including Dropbox's Python 2.5 bytecode and some PyPy bytecodes).
* [pycdc](https://github.com/zrax/pycdc) - A disassembler and decompiler written in C++ aiming to support all Python versions. This decompiler is known to be unstable.
* [pycdc (snippet decompiler)](https://github.com/extremecoders-re/python-snippet-decompiler) - This tool decompiles individual snippets of Python bytecode as opposed to entire binary files, aiming to help manual decompilation of binaries that are unsupported by state-of-the-art Python decompilers.
* [unpyc3.7-3.10](https://github.com/greyblue9/unpyc37-3.10) - A fork of a decompiler which aims to support versions 3.7 - 3.10.

## Debuggers

*Python source code/bytecode debuggers.*

* [pdb](https://docs.python.org/3/library/pdb.html) - The built-in Python interactive source debugger.
* [python3-trepan](https://github.com/rocky/python3-trepan) - A gdb-like debugger which supports both source code and bytecode debugging.
* [PyCharm's debugger](https://www.jetbrains.com/pycharm/) - PyCharm has its own debugger which is considered to be one of the best.

## Bytecode

### Editors

*Bytecode editors.*

* [pySpy](https://github.com/Svenskithesource/pySpy) - This tool aims to make viewing and editing bytecode easier. Only works properly for version 3.9.
* [xdis](https://github.com/rocky/python-xdis) - A Python cross-version bytecode library and disassembler. This library allows you to modify bytecode programmatically.

### Manual analysis

*Tools to assist with manual analysis of Python bytecode.*

* [PyInjector](https://github.com/call-042PE/PyInjector) - An injector for Windows that allows you to inject Python code into any Python process. It can be useful to expose variables, functions, grab code objects and many other things.
* [PythonForWindows](https://github.com/hakril/PythonForWindows) - This library allows you to interact with windows but also lets you inject Python code into another Python process without needing to inject a dll yourself.
* [x-python](https://github.com/rocky/x-python) - A Python implementation of the C interpreter. It can be useful to run bytecode instruction by instruction.
* [hypno](https://github.com/kmaork/hypno) - A cross-platform tool/library allowing to inject python code into a running python process. Can be installed through `pip`.
* [PyInjecto](https://github.com/BetterWayElectronics/PyInjecto) - Acts as an interactive CLI tool for injecting/analyzing Python processes. Allows you to start an exe and suspend it to inject Python code without being detected by some anti-debug protection. Allows you to use DLL injection or Hypno (see above).

## Python internals

*Tools to inspect or modify Python internals.*

* [inspect](https://docs.python.org/3/library/inspect.html) - A built-in library to inspect live objects. It gives information about objects like modules, classes, methods, functions, tracebacks, frame objects, and code objects. (Can be used along with [Python injectors](#manual-analysis))
* [CPython](https://github.com/python/cpython) - The CPython source code itself can often times be very useful to modify or trace.

## Packers

*Python packers that will package your Python project into an executable. This includes Python "compilers".*

* [PyInstaller](https://pyinstaller.org/) - PyInstaller is the most popular Python packager, supporting the platforms Windows, Linux and MacOS X.
* [py2exe](https://www.py2exe.org/) - py2exe can package Python projects to an executable for Windows.
* [Cython](https://cython.org/) - Cython is a superset of the Python language but can nonetheless compile Python code to a native program. It compiles the Python code to C code so any platform that has a C compiler should work.
* [Nuitka](https://github.com/Nuitka/Nuitka) - This is also a compiler for Python that can generate executables. It officially supports Linux, FreeBSD, NetBSD, MacOS X, and Windows (32bits/64 bits/ARM).

## Extractors

*Tools that can extract packed Python executables.*

* [pyinstxtractor](https://github.com/extremecoders-re/pyinstxtractor) - pyinstxtractor is the most popular extractor for PyInstaller. It supports almost all versions of PyInstaller. ([pyinstxtractor-ng](https://github.com/pyinstxtractor/pyinstxtractor-ng) and [pyinstxtractor-go](https://github.com/pyinstxtractor/pyinstxtractor-go) might be worth checking out aswell.)
* [unpy2exe](https://github.com/matiasb/unpy2exe) - unpy2exe is an extractor for py2exe but is not maintained anymore and likely will fail on newer versions of py2exe.
* [nuitka-extractor](https://github.com/extremecoders-re/nuitka-extractor) - An extractor for nuitka. This basically does the same thing as looking in the `temp` folder, but without actually running the executable.

## Obfuscators

*Python obfuscators.*

* [Pyarmor](https://github.com/dashingsoft/pyarmor) - This is by far the most popular Python obfuscator. It supports Python 2 and 3 on Windows, Linux and MacOS X.
* [Nuitka](https://github.com/Nuitka/Nuitka) - Nuitka isn't officially seen as an obfuscator but because it compiles Python code to C code it definitely helps with making the code harder to understand. The [commercial version](https://nuitka.net/doc/commercial.html) does have some extra protection features.
* [Cython](https://cython.org/) - Cython isn't officially seen as an obfuscator but because it compiles Python code to C code it definitely helps with making the code harder to understand.
* [Hyperion](https://github.com/billythegoat356/Hyperion) - This obfuscator is unique since it's one of the only ones that actually transforms your Python code. Since it returns plain Python source code it can be used on any platform that has Python available.
* [DIY PyArmor RFT](https://github.com/BetterWayElectronics/diy-pyarmor-rft-mode) - A Python source code renamer. This will attempt to rename as many names as it can without breaking the code. The project name comes from the PyArmor RFT mode, which also renames your code.

The following obfuscators all work in similar ways: marshalling the original Python code and hiding it behind multiple layers of `exec` statements with potentionally some encryption/decryption.

* [Specter](https://github.com/billythegoat356/Specter)
* [Kramer](https://github.com/billythegoat356/Kramer)
* [Berserker](https://github.com/billythegoat356/Berserker)
* [pyobfuscate](https://pyobfuscate.com/public/pyd2)
* [development tools's obfuscator](https://development-tools.net/python-obfuscator/)
* [Anubis](https://github.com/0sir1ss/Anubis)

## Deobfuscators

*Deobfuscators for Python obfuscators.*

* [PyArmor-Unpacker](https://github.com/Svenskithesource/PyArmor-Unpacker) - The most popular deobfuscator for the obfuscator Pyarmor. It only supports the free version of Pyarmor.
* [bonedensity](https://github.com/nesrak1/bonedensity) - A deobfuscator for the obfuscator PyArmor. Supports both the free and the paid Super mode.
* [Pyarmor-Static-Unpack-1shot](https://github.com/Lil-House/Pyarmor-Static-Unpack-1shot) - A deobfuscator for the obfuscator Pyarmor 8.0 and above. Supports both free and pro versions.
* [Hyperion-deobfuscator](https://github.com/xKiian/Hyperion-deobfuscator) - A deobfuscator for the obfuscator Hyperion.
* [nuitka-helper](https://github.com/goatmilkkk/nuitka-helper) - Not a deobfuscator but a tool that does symbol recovery for Nuitka samples. Read the blog post linked in the README.

## Resources

*Educational resources for Python reverse engineering.*

* [Python Reversing](https://blog.svenskithesource.be/)
* [Exploring code objects](https://late.am/post/2012/03/26/exploring-python-code-objects.html)
* [Python Stack Frames and Tail-Call Optimization](https://towardsdatascience.com/python-stack-frames-and-tail-call-optimization-4d0ea55b0542)
* [A Nuitka reverse engineering guide](https://goatmilkk.notion.site/Nuitka-a3ac9ee7f3f240f3baa345c17f2b8aa3)
