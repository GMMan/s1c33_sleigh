Epson S1C33 Ghidra Processor
============================

This is a Ghidra SLEIGH processor for Epson's S1C33 PE Core 32-bit RISC
processor.

Features
--------
- Disassembly of all C33 PE instructions, including extended instructions
- P-code implemented for all of the instructions
- Custom pseudo-instructions added for two-register `xadd`, `xsub`, `xcmp`,
  `xand`, `xoor`, and `xxor`
- Default compiler spec follows gcc33 / E0C33 Family C Compiler ABI
  (arguments in r12-r15, return in r10/r11, r8 reserved as global pointer)
- Original r6-r9 / r4 ABI retained as compiler id `legacy`
- Invalid encodings decode as `und` and return instead of aborting the
  decompiler

Build
-----

Compile the language with Ghidra's SLEIGH compiler, then copy this
directory to `Ghidra/Processors/S1C33` (or install it as an extension)
and restart Ghidra:

    <ghidra>/support/sleigh -a data/languages

Language id is `S1C33:LE:32:PE`. Compiler ids: `default` and `gcc33`
share the gcc33 spec; `legacy` is the previous r6-r9 / r4 ABI.

TODOs
-----
- Potentially simplify extended instruction constructors
- Recheck pack rules
