## Java程序的种类
1. Java小应用程序(Java Applet)
	- 在Web浏览器(container)中运行(内嵌Java虚拟机)，专门针对网络应用程序打造
2. Java应用程序(Java Application)
	- 独立的Java程序,所有的东西都是类
	- 程序入口方法 `public static void main(String[] args) {...}`

## Java Script 和 Java 的关系
- 嵌入在HTML文件中的脚本语言(netscape首提html)
- 特定标记 `<script language=javascript>...</script>`
- 不是java
- Netscape引入的javascript
- AS3
- EMC联盟

# Java应用程序
- Java源程序文件，扩展名是".java"
- 生成可执行Java字节码程序，扩展名为".class"

## 程序命名
- Java原程序名与程序内部的公有类(public class)名称必须一致
也就是说，一个Java文件中只能有一个公共类
```
class MyClass {
	...
}
```
文件名必须为MyClass.java

## 注解方式(Comments)
1. /** ~~~ */ 文档注解，从源程序提炼出来产生javadoc注解文档
2. /* ~~~ */ 程序内的任意位置
3. //　单行注解

## main Method
1. 每个Java程序必须有且只能有一个方法，程序执行的入口
2. 格式固定
`public static void main(String[] args)`

## 引入类和包
- 引入特定的类(Class)
```
import java.applet.Applet
import java.awt.Graphics
```
- 引入整个包(package)
```
import java.applet.*;
import java.awt.*;
```
默认引入java.lang，包含基本的输入输出

# Java语法基础
## 词法规则
> 所有的语言都是串行的单词流(有规律的字符流)
### 程序设计语言中的五类符号(所有的程序语言)
- 关键字(保留字)
- 标识符
- 分隔符(体现出了Java和C的区别，逗号在C中是连接符)
- 常量数据
- 运算符

### Java程序的运行体系
- source code(.java file)
- javac: Lexical Analysis & Parsing(语义分析) + Type-checking -> Byte code(.class file)
Java编译器对源代码进行语法分析和类型校验，生成字节码文件
- Java(JVM): Verification(essentially repeating static checks) + (Interpretation OR Compilation + Loading + Executing)
hotspot 

### 关键字 和 保留字(true, false, null)

### 标识符
- 字母，特殊符号，数字
- 第一个符号不能为数字
- 不能为关键字、true、false、null
- 区分大小写
- 一般约定：
	- 表示**常量**的标识符全部大写 `RED`
	- 表示**类名**的标识符用大写字母开始 如`MyCar`
	- 表示**公有方法和实例变量**的标识符用小写字母开始，后面描述性词以大写开始 如`getCurrentValue`
	- 表示**私有或局部变量**的标识符全部用小写字母，如`next_value`

### 分隔符
- 空白符
	- 空格、换行符、制表符
- 分号
	-标识语句结束
- 逗号
	- 变量之间的分隔
- 冒号
	- ?: / switch循环的case语句
- 花括号
	- 类体、方法、复合语句

## 数据类型
- 基本数据类型
	- 数字(number)
		- 整型(Integer)
			1. byte 一个字节
			2. short 两个字节 
			3. int 四个字节
			4. long 八个字节
		- 实型
			1. float 4字节
			2. double 8字节
	- 字符(char) 两个字节 unicode字符 \u0000 ~ \uffff u代表16进制
	- 布尔(boolean):true false(**为了保证不消耗过多的计算资源，Java不支持进行任何形式的类型转换!!!**)
- 符合数据类型
	- 数组(Array),类(cass),接口(interface)
## 常量数据表示
- 示例
	1. int i = 178
	2. long I = 8864L (8864L)
	3. double d1 = 37.266
	4. double d2 = 37.266D (37.266d)
	5. double d3 = 26.77e3
	6. float f = 87.363F 

# 大作业
要在web里面使用
最好是做成app






计算机本身就是方便人类，为别人提供便利，繁杂的留给自己
dos命令`tree`
