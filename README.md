[简体中文](README.zh_CN.md)

# VSCode 8051/8052 Assembly Language Support

Syntax highlighting and IntelliSense for 8051/8052 assembly language in Visual Studio Code.

## Syntax Highlighting

- Comments starting with semicolon (`;`)
- Double quotation mark (`"`) strings (with escape character recognition)
- Numbers in various bases
    - Hexadecimal (case-insensitive)
    - Binary numbers are case-insensitive and support segmentation with underscores (`_`), i.e., `0b1010_0101`
    - Decimal excludes numbers ending with `$` (reserved for inside jump labels)
    - A single character enclosed in single quotation marks (`'`) is also treated as a number
- 8051/8052 assembly language mnemonics
- Common built-in registers:
    - Only supports `A`, `ACC`, `AB`, `B`, `C`, `DPH`, `DPL`, `DPTR`, `PSW`, `SP`, `R0`~`R7` and `AR0`~`AR7`
- Common assembly directives:
    - Data definition: `.org`, `.db`, `.dw`, `.ds`, `.equ`, `.set`, `.end`, `.include`, etc.
    - Conditional compilation: `.if`...`.else`...`.endif`, etc.
    - Macro definition: `macro`...`endm`, etc.
    - Repetitive iteration: `rept`...`endr`, `irp`, `irpc`, etc.
- [SDCC](https://sdcc.sourceforge.net) proprietary assembly directives:
    - Segments and symbol declaration: `.module`, `.area`, `.globl`, etc.
    - Flow control extensions: `iff`, `ift`, `iftf`, `ifxx`, etc.
    - Full directive reference: [asmlnk.txt](https://svn.code.sf.net/p/sdcc/code/trunk/sdcc/sdas/doc/asmlnk.txt)
- [Keil](https://www.keil.com) proprietary assembly directives

## Installation

### From Marketplace
1. Open Visual Studio Code
2. Press `Ctrl+Shift+X` (or `Cmd+Shift+X` on Mac) to open Extensions view
3. Search for "8052 Assembly" or "asm8052"
4. Click Install

### From VSIX File
1. Download the `.vsix` file from [Releases](https://github.com/hsrzq/VSCode-ASM8052/releases)
2. Open Visual Studio Code
3. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) to open Command Palette
4. Type "Extensions: Install from VSIX..." and select it
5. Choose the downloaded `.vsix` file

## License

Licensed under the [Apache License 2.0](LICENSE).
