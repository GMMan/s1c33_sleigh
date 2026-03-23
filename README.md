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

TODOs
-----
- Validate proper implementation of P-code
- Potentially simplify extended instruction constructors
- Recheck pack rules
