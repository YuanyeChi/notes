- Java的新变化
	- 互联网技术
		- 脚本语言
	- 从Java9开始
		- Applet不再更新和使用
		- Java Web Start
	- Java Web Start
		- Java 5.0中就包含了
		- Java Network Launching Protocol(jnlp) 放在前端跑 避免了复杂的安装和升级
		- 所有jnlp都必须打成jar包

# 第五章 图形用户界面设计
1. 概述
2. 事件处理
3. 基本控制组件
4. 布局设计
5. 常用容器组件

## 概述
- Java GUI的发展
	- AWT 没法放弃AWT的原因是里面有事件响应机制
	- Swing
	- JFC
- Java FX
	基于Java的rich Internet applications的实现技术

## 界面的构成
只需要三种控件label textbox button 
menubar
### 一些特定的Java类
	- java.awt
	- java.swing
awt是重量级，swing是轻量级，swing可以跨平台运行
	- javafx.scene.control
### 容器组件(container):可包含其他组件
	- Dialog，Frame，Window
	- 一般用途容器: Panel，ScrollPane
	- 特定用途容器:InternalFrame
自己写的话顶层用frame，分区用panel
### 非容器组件
	- button，checkbox，scrollbar，choice，canvas
## 图形用户界面的实现
1. 选取组建
2. 设计布局
3. 响应事件
4. 应用原则
MVC是高度抽象的结果 model view control，java中将view和control放在一起变成model delegate
> adaptor，如果只想实现接口中的部分功能，系统会自动把其他抽象方法变成具体的空方法，这样就不用重写其他方法了
