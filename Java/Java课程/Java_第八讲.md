> 与C++不同的是，类的内部可以定义另外的类：嵌套类，C#甚至可以定义两个类名一样(partitial关键字)
## 类的定义格式
[类的修饰符]class 类名[extends 父类名][implements接口名] {
	[修饰符]类型 成员变量1;
	[修饰符]类型 成员变量2;

	[修饰符]类型 成员方法(参数1，参数2...) {
		方法体;
	}
	[修饰符]类型 成员方法(参数1，参数2...) {
		方法体;
	}
}
## 类的描述
### abstract
抽象类至少有一个方法只有定义没有实现的，那么自动变为抽象方法
所谓抽象方法就是定义了一个这样的抽象概念，具体实现是有具体类完成。
### final

## 类成员变量的访问
### 访问控制修饰符

### 非访问控制修饰符
- 静态变量static
	- 属于类的变量(已经具有可访问特性，不需要借助对象，是所有对象公有的)
- 最终变量final
	- 值在程序的执行过程中不会被改变(可以在子类中改变shadow，方法如果定义了final则不能被继承 )
- 易失变量volatile
	- 可能同时被多个线程所控制和修改

### 类成员方法的访问
- 非访问控制修饰符
	- 静态方法
		- 属于类的方法
	- 最终方法final
		- 不能被子类重新定义的方法
	- 抽象方法abstract
		- 只有方法说明，没有具体实现
	- 本地方法native
		- 以其他语言实现功能，现在也越来越少了，一般借助于框架。
	- 同步方法synchronized
		- 用于多线程程序的协调和同步

## 构造方法
- 默认构造方法
```java
class Apple {
	int color;
}
Apple a = new Apple();
```
- 对象实例的判断：null
```java
Apple a;
if (a == null) {
	System.out.println("");
}
```
- 再谈构造方法
```java
class Cmethod {
	Cmethod (boolean) {}
	public static void main(String args[]) {
		Cmethod c1 = new Cmethod();//第一行报错，没有相应的构造函数
		Cmethod c1 = new Cmethod(false);
	}
}
```
运行时系统自动赋予一个空构造方法，仅仅当该类没定义构造方法的情况下。

## static变量的初始化(在编译器完成)
```
class Smember {
	
}
```

## 设计模式的例子
- 单对象模型singleton
> 汽车工业中所有零件都是独一无二的
```java
class Singleton {
	private static Singleton me = new Singleton();
	public static Singleton getSingleton(){
		return me;
	}
	private Singleton() {}
	public static void mian(String args[]) {
		Singleton s1 = Singleton.getSingleton();
		Singleton s2 = Singleton.getSingleton();
		if (s1 == s2)
			System.out.println("s1 is s2");
		else 
}			System.out.println("s1 is not s2");
```
- sequence
#继承
> 满足is-a的关系,子类和父类的关系(extends)

## 重新定义父类已有的变量
	- 父类中同名的变量无效
	- 通过`super.变量`和`父类名.变量(static变量)`引用。
	- shadow下只能用上述方法调用，override也是，调用父类方法只能super

## 抽象类
- 抽象类想变成普通类，必须要在子类中进行完整的方法实现。
- 为了提升代码可扩展性，不要省略方法的abstract
- **抽象类在内存模型里就是个指针**,实际访问的时候就是指针指向的具体类。针对不同的对象所体现出来的不同的状态就是称之为**多态**。	

## 接口interface(do something)
> 接口是对abstract类的进一步扩展
- 接口中方法都是未实现的，一般没有成员变量。而抽象类则可以有具体方法。
- 目的是在实现接口的类之间建立一种协议。

## 接口和抽象类的方法
- 如果用了interface, 那么里面的变量都是public static final，接口就是C++的纯虚函数
- Java通过接口实现多继承。要增加新的操作途径，就引入新的接口。
- 有时候抽象类会很好用。

## 实例
```java
class Hero extends ActionChracter implements Canfight, Canswim, CanFly {
	public void swim(){};
	public void fly(){};
}
interface CanFight{
	fight(){};
}
interface CanSwim{
	swim(){};
}
interface CanFly{
	fly(){};
}

class ActionChracter {
	public void fight(){};
}
```
## 对象的使用
this是指当前对象本身。
- 当成员变量和局部变量重名时，在方法中使用this时，表示的是该方法所在类中的成员变量。
- 把自己当作参数传递时，也可以用this.
- 在构造函数中，通过this可以调用同一类中别的构造函数。

