# 全新的一个开始(进入应用阶段)
之前是单文件多类，现在是项目的方式

# 第四章 Applet及其应用
1. Applet概述
2. Applet类
3. Applet程序和HTML文件
4. Applet的应用

## Applet概述
### Java程序的两种基本形式
	- Java Application
	- Java Applet
### 一个小例子
没有main函数，继承自Applet
```java
import java.applet.Applet;
import java.awt.Graphics;

public class Exam4_1 extends Applet {
	String str;
	public void int() {
		str = "";
	}
	public void paint(Graphic g) {
		g.drawString(str, 100, 100);
	}
}
```
Java开发一般都是从基础类进行继承，然后进行override
### servlet
和Applet是一对
### switch
主要就是在页面上针对全屏幕进行响应的快捷方法

###HTML文件
Applet以HTML作为载体

## Applet类
继承关系`java,lang.Object <- java.awt.Component <- java.awt.Container <- java.awt.Panel <- java.applet.Applet`
默认情况下，Applet使用FlowLayout布局管理器
### 主要方法
1. init()
	- 初始化
	- 第一次加载时候调用，仅执行一次
2. start()
	- 启动Applet主线程执行
	- 重启时也被调用(reload或返回)
3. paint()
	- 将结果输出/绘制到界面上
	- 将自动调用(启动后/窗口改变/repaint()调用)
4. stop()
	- 暂停Applet执行
5. destroy()
	- 终止Applet程序执行，释放占用资源
把经常变动的部分放在HTML里面，文本比字节码易于更改。

### 绘制图形
1. 设置字体
2. 设置颜色
3. 绘制文本
4. 绘制几何图形

### 演示图像
动画
	- 创建Image类的对象数组
	- drawImage()
	- Thread.sleep()
	- drawImage()
