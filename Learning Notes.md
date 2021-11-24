# Basic Notes

## 类基础

Java程序的基本组成单元：类

**类包含**：属性、方法

每一个应用程序需要包含一个main()方法，含有main()方法的类被成为主类。

Java文件名需要和类名称同名，**Java大小写敏感**

### 示例

```java
pubilic class Book{
	private String name;

	//权限修饰符 返回值类型 方法名(参数){ }
	public String getName(){   //方法
		int id = 0;
		setName("JAVA");
		return id + this.name
	}

	private void setName(String name){
		this.name = name;
	}
	
	Public Book getBook(){
		return this;
	}
}
```



## main()方法

main()方法是类体中的主方法



```java
package hello; 			//包声明
import java.util.Scanner;

public class test {		//定义（创建）类
	public static void main(String[] args) {  //主方法
//main()方法的参数：权限修饰符、静态修饰符、返回值修饰符    字符串类型的数组

		Scanner in = new Scanner(System.in);
		System.out.println(in.nextLine());
	}
}
```



## I/O

```java
//Output:
System.out.prinln("Print Here."); //'prinln' means Print Line

//Input:
import java.util.Scanner; 

Scanner in = new Scanner(System.in);
System.out.println(in.nextLine());
```

## 对象





## 字符串

Java将字符串作为对象来管理

```java
String st = new String("Hello!");
```









# Part1.类与对象

## 1.1 用类制造对象

- 对象 是 实体，需要被创建，可以拿来做事情

- 类 是 规范，根据类的定义来创建对象

**关系**：类定义了对象，每一个具体的对象都是类的实体。

对象：[ 操作 ( 数据 ) ]	-->	将数据与对数据的操作放在一起，即“封装”。

## 1.2 定义类

`structname b = new structname();`

用 new 实例化（创建）对象；定义b为对象变量，来管理类。

## 1.3 成员变量和成员函数

### 变量

本地变量：定义在函数内部的变量

- 生存期与作用域均在函数内部

成员变量：定义在函数外部的变量

- 生存期在对象new(创建)后才存在，不关心什么时候消失
-  作用域是类内部的成员函数

### 调用函数

函数通过变量来调用

- 在成员函数外部：使用 . 运算符调用某个对象的函数
- 在成员函数内部：直接调用自己（this）的其他函数

`b.insert()`

在调用中临时建立了insert()与b之间的关系，让insert()内部的成员变量指向b的成员变量

### this

在成员函数中，this是一个特殊固有的本地变量，表达了调用这个函数的那个对象

~~~java
void test(){
System.out.println(value);
System.out.println(this.value);
//均在函数内部，两者相同
}
~~~

```java
public class set{
	int a = 0;
	
	void test(){
		this.a = a; //若不加this. 则为a = a无法区分哪个a是内部或外部的
        //此时this.a与a各指向不用
	}
}
```

## 1.4 对象初始化

### 成员变量定义初始化

- 没有给出初始值的成员变量会自动获得一个0值，表示没有管理任何对象，也可以主动给null值

### 构造函数

如果一个成员函数的名字和类的名字完全相同，则在创建这个类的每一个对象的时候会自动调用这个函数，

即构造函数。（在构造的时候会被自动调用的函数）

```java
public class test{
	int va = 0;
    int st = 0;
	
	test()	//构造函数
	{
    	st = 0;    
 	}
	
	test(int st)	//重载
	{
        this.st = st;
	}
}
```

# Part2.对象交互

## 对象交互







