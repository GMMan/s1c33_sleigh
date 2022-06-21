Epson S1C33 Ghidra Processor
============================

This is a Ghidra SLEIGH processor for Epson's S1C33 PE Core 32-bit RISC
processor.

Features
--------
- Disassembly of all C33 PE instructions, including extended instructions
- P-code implemented for most of the instructions

TODOs
-----
- Validate proper implementation of P-code
- Add flag packing/unpacking for direct `%psr` modifications
- Potentially simplify extended instruction constructors
- Recheck pack rules
