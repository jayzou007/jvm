
# 类文件结构

## JVM 的“无关性”
- 平台无关性：任何操作系统都能运行 Java 代码
- 语言无关性： JVM 能运行除 Java 以外的其他代码

Java 源代码首先需要使用 Javac 编译器编译成 .class 文件，然后由 JVM 执行 .class 文件，从而程序开始运行。

JVM 只认识 .class 文件，它不关心是何种语言生成了 .class 文件，只要 .class 文件符合 JVM 的规范就能运行。
目前已经有 JRuby、Jython、Scala 等语言能够在 JVM 上运行。它们有各自的语法规则，不过它们的编译器
都能将各自的源码编译成符合 JVM 规范的 .class 文件，从而能够借助 JVM 运行它们。

> Java 语言中的各种变量、关键字和运算符号的语义最终都是由多条字节码命令组合而成的，
因此字节码命令所能提供的语义描述能力肯定会比 Java 语言本身更加强大。
因此，有一些 Java 语言本身无法有效支持的语言特性，不代表字节码本身无法有效支持。

## Class 文件结构
class 文件时二进制文件，它的内容具有严格的规范，文件中没有任何空格，全都是连续的0/1。class 文件
中的所有内容被分为两种类型：无符号数、表。

Append something here...