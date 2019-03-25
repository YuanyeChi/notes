switch 后面的选择类型是离散状态。
Java输入可以用 char c = (char) System.in.read();

### 跳转语句
#### `break`
break不带标号的语句，跳出当前循环。
break带标号的语句。
```java
public static void main(String[] args) {
	int j, k;
	Rep;
	for (j = 8; j > 1; j--) {
		for (k = 1; k <=9; k++) {
			break Rep;
		}
	}
}
```
#### `continue`
continue 同理

### 其他语句
- import
`import java.applet.Applet`被踢掉了
`javaFX`也被踢掉了
- package

### 控制台输入输出
- Scanner 类

## 数组
> 数组的类型可以是基本类型，类或接口
数组是一种特殊的对象
计算机处理应用程序是当做一个串行的字符读入的。先定义一个数组的类型可以帮助计算机率先处理。`int[] i`就比`int i[]`好。
实例化相当于就是把变量在内存空间中实体化。

```java
int[] a = {1, 2, 3, 4};
int[] b; int[] c = {1, 3, 5, 7};
b = a; c = a;
```
浅拷贝，相当于直接让a被b和c指向。

深拷贝
System.arraycopy
### 二维数组

## 命令行参数


# 第二讲 进入Java


