[English](README.md)

# VSCode 8051/8052 汇编语言支持

本插件为 Visual Studio Code 增加了 8051/8052 汇编的语法高亮和智能提示功能。

## 语法高亮

- 以分号(`;`)起始的注释
- 双引号(`"`)字符串(可区分转义字符)
- 各种进制的数字
    - 16进制不区分大小写
    - 2进制不区分大小写，支持用下划线(`_`)分段，即：`0b1010_0101`
    - 10进制专门避开了以美元符(`$`)结尾的数字(通常用作内部跳转地址的标号)
    - 以单引号(`'`)包裹的单个字符也当作数字处理
- 8051/8052 汇编语言助记符
- 常用基础内置寄存器：
    - 目前只支持`A`，`ACC`，`AB`，`B`，`C`，`DPH`，`DPL`，`DPTR`，`PSW`，`SP`，`R0`~`R7`和`AR0`~`AR7`
- 常见通用汇编伪指令：
    - 数据定义：`.org`，`.db`，`.dw`，`.ds`，`.equ`，`.set`，`.end`，`.include`等
    - 条件编译：`.if`……`.else`……`.endif`等
    - 宏定义：`macro`……`endm`等
    - 重复迭代：`rept`……`endr`、`irp`、`irpc`等

## 安装方法

### 从 Marketplace 安装
1. 打开 Visual Studio Code
2. 按 `Ctrl+Shift+X`（Mac 上按 `Cmd+Shift+X`）打开扩展视图
3. 搜索 "8052 Assembly" 或 "asm8052"
4. 点击安装

### 从 VSIX 文件安装
1. 从 [Releases](https://github.com/hsrzq/VSCode-ASM8052/releases) 下载 `.vsix` 文件
2. 打开 Visual Studio Code
3. 按 `Ctrl+Shift+P`（Mac 上按 `Cmd+Shift+P`）打开命令面板
4. 输入 "Extensions: Install from VSIX..." 并选择
5. 选择下载的 `.vsix` 文件

## 开源协议

本项目采用 [Apache License 2.0](LICENSE) 开源协议。
