系统智能推荐，注意算法

# 面向对象特征
1. 基本概念
2. 类的定义
3. 对象
4. 类的继承和多态
5. 接口和包
6. 常用工具类

## 基本概念
- 机器语言
- 汇编语言 mov, push, add, call
- 第三代语言 高级语言以C为代表,面向过程
- 第四代语言 非过程化/面向对象的编程
- 语言的发展: 抽象的过程

### 面向对象(Object Oriented-OO)
- 面向对象编程(Object Oriented Programming-OOP)
> 成功语言的黏滞性，太过优秀导致更新比较困难(smalltalk)
- 五个基本概念
	1. 对象
	2. 类
	3. 封装性
	4. 继承性
	5. 多态性
**类相当于就是数据类型，对象相当于就是变量**，先声明后使用(实例化)

任何的类都只能是**部分数据**类型的抽象，随着对个体了解的越深入，抽象出来的就会越准确。
如果要开发一个行业的实际的应用，这个时候我们得到的系统都是从主观出发的，我们应该向行业的老法师请教。

## 类的定义
程序是对象的集合，而对象是类的实例化。
源程序就是一个个Java类。
类分三种：Java本身提供的类(核心API)， 第三方开发的类 以及 程序员自己提供的类

> 先封装，后继承共性的东西，在根据自己的需要进行个性化定制。(继往开来)

### 类的定义格式
#### 类头
`[类的修饰符] class 类名 [extends 父类名] [implements 接口名]`
#### 类的修饰符
- 封装性
1. public 可以被其他类使用
2. 无修饰(protected) 仅能在package中被调用

- 继承和多态
3. abstract 宣布该类不能被实例化(declares that the class cannot be instantiated)
4. final 宣布该类不能有子类 (cannot be subclassed)

### package的概念(对应于文件系统src下的路径)
> 现在集成化的开发环境中没有那么重要了
package org.jalpha 系统会自动给你生成,以当前的文件夹为起点
class test {}
1. 源文件位置`D:\\src\org\jalpha\test.java`
2. 编译方法1 `cd D:\src\org\jalpha\` `javac test.java`
3. 编译方法2 `cd D:\src\` `javac org\jalpha\test.java`
4. class位置`D:\\src\org\jalpha\test.class`
5. `cd D:\src\` `java org.jalpha.test`

### 类成员，变量
- 访问控制修饰符
	- 公共访问控制符-public
		- 被所有类访问
	- 默认访问控制符
		- 被同一包中其他类访问
	- 私有访问控制符 private
		- 被该类自身访问，就连生成的对象对其访问也属于外部
		- 所有类内部的数据域都应该是private，调用和修改都应该由public方法做到
		- 所有类内部的方法都是public
	- 保护访问控制符 protected
		- 访类自身、同一个包中的其他类、**其他包中的子类访问**
		- 保护态都是和继承连接在一起的
		- 有继承的时候与public一样，无继承的时候与private类似
- 非访问控制修饰符
	- 静态变量 static 属于类的变量
		- 针对静态变量，都会放在类的空间统一放置
		- 非静态就会放在本地堆中
	- 最终变量 final 值在程序的执行过程中不会改变
		- C++ 中的const
		- 在子类中貌似可以被覆盖
	- 易失变量 volatile	可能同时被多个线程所控制个修改
		- 多线程
### 类成员方法
	

