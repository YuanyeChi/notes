## 事件模型
事件源->触发事件
listener<-接收事件

### 事件处理
- 事件分类
	1. ActionListener
		public void actionPerformed(ActionEvent e)
	2. WindowListener 
		WindowOpened, WindowClosing...
	3. MouseListener
		mouseClicked, mousePressed, mouseReleased
	4. MouseMotionListener
		mouseDragged, mouseMoved

### 事件类型MVC
- 控件所在的容器中完成布局view
- 数据对象，程序的关键点model
- 控件.addtypeListener(对象implements interface)<control>
多个事件监听接口定义了多个方法具体到每个控件，并不需要定义多有的实现
Java提供了adaptor

### 标签和按钮
- 按钮Button
	- 创建按钮
		- public Button()
		- public Button(String label)
	- 常用方法
		- public String getLabel()
		- public void setLabel(String label)
		- public void setActionCommand(String s)
		- public void getActionCommand(String s)
	- 事件响应
		- java.awt.event.ActionListener(接口)
		- void actionPerformed(ActionEvent e)
### 文本框和文本区
### 单复选框和列表
- 单选按钮组
	- 创建单选按钮组
	- 常用方法
	- 事件响应
### List
	- 创建列表
	- 常用方法
	- 事件响应
### canvas
- 一个控窗口，用于绘制图形的选择

### 布局管理
	- 两种简单布局
		- FlowLayout
			- 所有组件从左往右排成一行
			- 一行排满后转到下一行从左向右排
			- 居中，左对齐，右对齐
		- GridLayout
			- 限定行列，如果都是0行0列，那就是flowLayout
	- 两种特定用途布局
		- BorderLayout
		- CardLayout
	- 两种灵活布局
### 容器
	- 常用方法
		- 添加组件
		- 获取指定的组件	
		- 移除组件
		- 设置容器布局
		- 刷新组建 repaint
	- Panel
		- 无边框容器
		- 默认FlowLayout
		- Applet子类
	- 
