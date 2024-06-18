---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://images.unsplash.com/photo-1484417894907-623942c8ee29?q=80&w=2664&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
# some information about your slides, markdown enabled
title: Java 急速入门
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply any unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
---



<!-- <div class="flex items-center justify-center">
  <img src="/img/Java.svg" class="w-70">
</div> -->

# ***Java 急速入门***

## 2024/6/28

<style>
h1 {
  /*  字符笔画的宽和颜色  */
  -webkit-text-stroke: 3px #ffcb4e;
  /*  透明色  */
  color: rgba(0,0,0,0);
  /*  和 box-shadow 很像，给图像一个阴影  */
  filter: drop-shadow(0 0 3px rgb(249, 187, 3, 0.7)) drop-shadow(0 0 15px #f9bb03);
  /*  字母间更加紧凑  */
  letter-spacing: -.02em;
  margin: 0;
  padding: 20px 0;
  font-family: urbane-rounded;
  font-size: 100px;
}
h2 {
  color: #ff6859;
  text-shadow: 0 0 20px #ff6859;
  letter-spacing: -.02em;
  margin: 0;
  font-family: urbane-rounded;
}

</style>

--- #2
layout: center
---

# Java 介绍

<v-clicks>

- Java 是一种广泛使用的计算机编程语言，拥有跨平台、面向对象、泛型编程的特性。
- Java 由 Sun Microsystems 公司的 James Gosling 等人开发，并于 1995 年正式发布。
- Java 语言的特点是平台无关性，即一次编译，到处运行。
- Java 语言的应用领域非常广泛，包括企业级应用、移动应用、大数据分析等。
- Java 语言的发展非常迅速，目前最新版本是 Java 22。

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

</v-clicks>
<!-- Java介于编译型语言和解释型语言之间。编译型语言如C、C++，代码是直接编译成机器码执行，但是不同的平台（x86、ARM等）CPU的指令集不同，因此，需要编译出每一种平台的对应机器码。解释型语言如Python、Ruby没有这个问题，可以由解释器直接加载源码然后运行，代价是运行效率太低。而Java是将代码编译成一种“字节码”，它类似于抽象的CPU指令，然后，针对不同平台编写虚拟机，不同平台的虚拟机负责加载字节码并执行，这样就实现了“一次编写，到处运行”的效果。当然，这是针对Java开发者而言。对于虚拟机，需要为每个平台分别开发。为了保证不同平台、不同公司开发的虚拟机都能正确执行Java字节码，SUN公司制定了一系列的Java虚拟机规范。从实践的角度看，JVM的兼容性做得非常好，低版本的Java字节码完全可以正常运行在高版本的JVM上。 -->

--- #3
layout: image-right
image: /img/James.png
backgroundSize: 20em 80%
---

# Java 历史

<v-clicks>

- 1991年，Sun 公司的 James Gosling 等人开发了 Java 语言
- 1995年，Sun 公司正式发布 Java 1.0
- 2009年，Sun 公司被 Oracle 收购
- 2014年，Java 8发布

....

- 2024年，Java 22发布

</v-clicks>

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>


--- #4
transition: fade-in
---

# Java 流行度 

<img src="/img/GitHub.png"  class="w-full h-full shadow">

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>


--- #5
transition: fade-in
---

# Java 流行度 
<img src="/img/TIOBE.png" class="w-full h-auto shadow">

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>


<!-- TIOBE 是一家荷兰的软件公司，每月发布一次编程语言流行度排行榜 -->
--- #6
transition: fade-in
layout: two-cols-header
---

# 名词解释

::left::
- JDK：Java Development Kit
- JRE：Java Runtime Environment

<br/>

JDK 和 JRE 关系如下：

<img src="/img/JDK.png" class="w-full h-auto">

::right::

- Java SE：Standard Edition
- Java EE：Enterprise Edition
- Java ME：Micro Edition

三者的关系：

<img src="/img/JavaEE.png" class="w-2/3 h-auto">

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

<!-- 简单来说，Java SE就是标准版，包含标准的JVM和标准库，而Java EE是企业版，它只是在Java SE的基础上加上了大量的API和库，以便方便开发Web应用、数据库、消息服务等，Java EE的应用使用的虚拟机和Java SE完全相同。

Java ME就和Java SE不同，它是一个针对嵌入式设备的“瘦身版”，Java SE的标准库无法在Java ME上使用，Java ME的虚拟机也是“瘦身版”。

毫无疑问，Java SE是整个Java平台的核心，而Java EE是进一步学习Web应用所必须的。我们熟悉的Spring等框架都是Java EE开源生态系统的一部分。不幸的是，Java ME从来没有真正流行起来，反而是Android开发成为了移动平台的标准之一，因此，没有特殊需求，不建议学习Java ME。

因此我们推荐的Java学习路线图如下：

首先要学习Java SE，掌握Java语言本身、Java核心开发技术以及Java标准库的使用；

如果继续学习Java EE，那么Spring框架、数据库开发、分布式架构就是需要学习的；

如果要学习大数据开发，那么Hadoop、Spark、Flink这些大数据平台就是需要学习的，他们都基于Java或Scala开发；

如果想要学习移动开发，那么就深入Android平台，掌握Android App开发。 -->

--- #7
transition: fade-in
layout: image-left
image: /img/IDEA.png

---

# Java 环境搭建

- 下载 JDK https://www.oracle.com/java/technologies/downloads/
- 安装 JDK
- 设置环境变量
- 下载安装 IDEA
https://www.jetbrains.com/idea/download/

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

<!-- JDK 版本可以通过设置环境变量切换，学习的时候直接下社区版就够用 -->

--- #8
transition: fade-in
---

# Hello World

新建一个名为 HelloWorld.java 的文件（**文件名必须和类名一致**）

```java {1|2|all}
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

运行流程如下：
<img src="/img/compile.png" class="h-full w-auto">

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

<!-- 在 IDEA 中编译执行只需要点一下绿色的播放按钮，剩下的工作都由 IDEA 来做 -->

--- #9
transition: fade-in
---

# Java 输入与输出

```java {1-9|11-23|14-15|all}
// 使用 System.out.println() 输出，代表输出后换行
System.out.println("Hello World!");
// 输出多个变量
System.out.println("Integer: " + 10 + " Double: " + 3.14 + " Boolean: " + true);
// 使用 System.out.print() 输出，代表输出后不换行
System.out.print("Hello ");
System.out.print("World");
// 使用 System.out.printf() 输出，可以格式化输出
System.out.printf("pi = %.5f", Math.PI); // => pi = 3.14159
     
// 使用 System.in 读取用户输入
// 创建 Scanner 对象，用于接收用户输入，需要导入 java.util.Scanner 包
Scanner scanner = new Scanner(System.in);
// scanner.next() 和 scanner.nextLine() 方法用于接收用户输入的字符串，区别是 next() 遇到空格就结束，nextLine() 读取一整行
String name = scanner.nextLine();
// String name = scanner.nextLine();
// 下面的方法用于接收用户输入的不同类型的数据
byte numByte = scanner.nextByte();
int numInt = scanner.nextInt();
long numLong = scanner.nextLong();
float numFloat = scanner.nextFloat();
double numDouble = scanner.nextDouble();
boolean bool = scanner.nextBoolean();
```

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

--- #9
transition: fade-in
---

# Java 输入与输出

```java {1|3-4|5-14|15-16|17-18}
import java.util.Scanner;  // 导入Scanner类，用于接收输入

public class InputOutputExample {
    public static void main(String[] args) {
        // 创建Scanner对象，用于接收用户输入
        Scanner scanner = new Scanner(System.in);
        // 提示用户输入姓名
        System.out.print("请输入您的姓名: ");
        // 使用Scanner对象的nextLine()方法接收用户输入的字符串
        String name = scanner.nextLine();
        // 提示用户输入年龄
        System.out.print("请输入您的年龄: ");
        // 使用Scanner对象的nextInt()方法接收用户输入的整数
        int age = scanner.nextInt();
        // 输出结果
        System.out.println("您好，" + name + "！您的年龄是 " + age + " 岁。");
        // 关闭Scanner对象
        scanner.close();
    }
}
```

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

--- #10
transition: fade-in
---

# Java 数据类型

<img src="/img/DataTypes.png" class="h-auto w-4/5">

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

--- #11
transition: fade-in
---

# Java 数据类型

<img src="/img/DataTypeSize.png" class="h-auto w-full">

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

<!-- 这里的数据范围没必要记，使用的时候考虑临界情况 -->

--- #12
transition: fade-in
---

# Java 数据类型

```java {all|7,8|all}
public class AllPrimitiveTypesExample {
    public static void main(String[] args) {
        
        byte byteValue = 127;           // 字节类型
        short shortValue = 32000;       // 短整型
        int intValue = 2147483647;      // 整数类型
        long longValue = 9223372036854775807L; // 长整型，注意结尾的 L 表示是 long 类型，避免使用小写 l，造成误解
        float floatValue = 3.14f;       // 单精度浮点数，注意结尾的 f 表示是 float 类型，大写 F 也可以
        double doubleValue = 3.14159;   // 双精度浮点数
        boolean booleanValue = true;    // 布尔类型
        char charValue = 'A';           // 字符类型

        System.out.println("字节值: " + byteValue);
        System.out.println("短整型值: " + shortValue);
        System.out.println("整数值: " + intValue);
        System.out.println("长整型值: " + longValue);
        System.out.println("单精度浮点数值: " + floatValue);
        System.out.println("双精度浮点数值: " + doubleValue);
        System.out.println("布尔值: " + booleanValue);
        System.out.println("字符值: " + charValue);
    }
}
```

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

--- #13
transition: fade-in
---

# Java 运算符

<img src="/img/operator.png" class="w-[60%] h-auto">


<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

--- #14
transition: fade-in
---

# Java 类型转换

除法中的类型转换经典案例
```java
public class DivisionExample {
    public static void main(String[] args) {
        System.out.println("整数相除: " + 10/3); // 结果是 3，因为整数相除结果是整数
        System.out.println("整数和浮点数相除: " + 10/3.0); // 结果是 3.3333333333333335，因为整数和浮点数相除结果是浮点数
    }
}
```

Java 运算中如果参与运算的两个数类型不一致，会自动将较小的类型转换为较大的类型，但是有时候我们需要手动进行类型转换，即强制类型转换。

<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

--- #15
transition: fade-in
---

# Java 强制类型转换

```java
public class TypeConversionExample {
    public static void main(String[] args) {
        int intValue = 100;
        long longValue = intValue; // 自动类型转换
        System.out.println("自动类型转换: " + longValue);

        long longValue2 = 100;
        int intValue2 = (int) longValue2; // 强制类型转换
        System.out.println("强制类型转换: " + intValue2);
    }
}
```

需要注意的是，强制类型转换可能会造成数据丢失，例如：

```java
int intValue = 2147483647;
byte byteValue = (byte) intValue;
System.out.println("强制类型转换: " + byteValue); // 结果是 -1，因为 byte 类型的范围是 -128 到 127
// 2147483647 的二进制表示是 01111111 11111111 11111111 11111111
// 截取最后一个字节就是 11111111，它代表的是一个有符号的 8 位二进制数，在二进制补码表示中表示 -1
```


<style>
h1 {
    background-color: #2B90B6;
    background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>
