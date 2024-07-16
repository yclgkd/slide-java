---
# try also 'default' to start simple
theme: default
favicon: /img/favicon.png
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://images.unsplash.com/photo-1484417894907-623942c8ee29?q=80&w=2664&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
# some information about your slides, markdown enabled
title: Java 急速入门
info: false
author: Brian Yao<me@brianyao.tech>
# keywords field for exported PDF, comma-delimited.
keywords: Java 急速入门
# apply any unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
  enabled: dev
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
presenter: dev
record: dev
---



<!-- <div class="flex items-center justify-center">
  <img src="/img/Java.svg" class="w-70">
</div> -->

# ***Java 急速入门***

## 2024/6/20

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
image: James.png
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
image: IDEA.png

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

新建一个名为 Hello.java 的文件（<span v-mark.red>**文件名必须和类名一致**</span>）

```java {1|2|all}
public class Hello {
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

--- #10
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

--- #11
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

--- #12
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

--- #13
transition: fade-in
---

# Java 数据类型

```java {all|3-5|7-8|all}
public class AllPrimitiveTypesExample {
    public static void main(String[] args) {
        final byte byteValue = 127; // 字节类型，final 表示常量，一旦赋值就不能再修改
        final short shortValue; // 短整型，没有初始化可以在后面赋值
        shortValue = 32767; // 赋值后不可以再修改
        int intValue = 2147483647; // 整数类型
        long longValue = 9223372036854775807L; // 长整型，注意结尾的 L 表示是 long 类型，避免使用小写 l，造成误解
        float floatValue = 3.14f; // 单精度浮点数，注意结尾的 f 表示是 float 类型，大写 F 也可以
        double doubleValue = 3.14159; // 双精度浮点数
        boolean booleanValue = true; // 布尔类型
        char charValue = 'A'; // 字符类型

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

--- #14
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

--- #15
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

--- #16
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
<v-click>
需要注意的是，强制类型转换可能会造成数据丢失，例如：
</v-click>

<v-click>
````md magic-move
```java
int intValue = 2147483647;
// byte 类型的范围是 -128 到 127
byte byteValue = (byte) intValue;
System.out.println("强制类型转换: " + byteValue);
```
```java
int intValue = 2147483647;
// byte 类型的范围是 -128 到 127
byte byteValue = (byte) intValue;
System.out.println("强制类型转换: " + byteValue); // 结果是 -1，因为 byte 类型的范围是 -128 到 127
```
```java
int intValue = 2147483647;
// byte 类型的范围是 -128 到 127
byte byteValue = (byte) intValue;
System.out.println("强制类型转换: " + byteValue); // 结果是 -1，因为 byte 类型的范围是 -128 到 127
// 2147483647 的二进制表示是 01111111 11111111 11111111 11111111
// 截取最后一个字节就是 11111111，它代表的是一个有符号的 8 位二进制数，在二进制补码表示中表示 -1
```
````
</v-click>


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

--- #17
transition: fade-in
---

# Java 中的数组

```java {3-6|8-11|13-14|16-21|all}
public class ArrayExample {
    public static void main(String[] args) {
      // 数组的第一种定义方式
      int[] intArray = new int[10];
      String[] stringArray = new String[1];
      boolean boolArray[] = new boolean[100];

      // 数组的第二种定义方式
      int[] y = {9000, 1000, 1337};
      String names[] = {"Bob", "John", "Fred", "Juan Pedro"};
      boolean bools[] = {true, false, false};

      // 多维数组的声明和初始化
      int[][] matrix = {{1, 2, 3},{4, 5, 6},{7, 8, 9}};

      // 访问数组元素
      System.out.println("intArray @ 0: " + intArray[0]);

      // 修改数组元素
      intArray[1] = 1;
      System.out.println("intArray @ 1: " + intArray[1]); // => 1
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

--- #18
transition: fade-in
---

# Java 中的 if 判断

````md magic-move
```java {all|13-22}
public class IfStatementExample {
    public static void main(String[] args) {
        // 声明一个字符串变量并赋值为 null
        String str = null;

        // 使用 if 判断语句检查字符串是否为空
        if (str == null) {
            System.out.println("字符串为空");
        } else {
            System.out.println("字符串不为空");
        }

        // 尝试比较字符串 str 和 "Hello"，会抛出空指针异常
        try {
            if (str.equals("Hello")) { // 这里会抛出 NullPointerException
                System.out.println("字符串内容相同");
            } else {
                System.out.println("字符串内容不同");
            }
        } catch (NullPointerException e) {
            System.out.println("发生空指针异常：字符串为 null");
        }
    }
}
```
```java
public class IfStatementExample {
    public static void main(String[] args) {
        // 声明一个字符串变量并赋值为 null
        String str = null;

        // 使用 if 判断语句检查字符串是否为空
        if (str == null) {
            System.out.println("字符串为空");
        } else {
            System.out.println("字符串不为空");
        }
  
        // 使用 && 运算符避免空指针异常
        if (str != null && str.equals("Hello")) {
            System.out.println("字符串内容相同");
        } else {
            System.out.println("字符串内容不同");
        }
    }
}
```
````

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

--- #19
transition: fade-in
---

# Java 中的循环

````md magic-move
```java
public class LoopExample {
    public static void main(String[] args) {
        // while 循环
        int j = 0;
        while (j < 5) {
            System.out.println("while 循环: " + j);
            j++;
        }

        // do-while 循环
        int k = 0;
        do {
            System.out.println("do-while 循环: " + k);
            k++;
        } while (k < 5);
    }
}
```
```java
public class LoopExample {
    public static void main(String[] args) {
        // for 循环
        for (int i = 0; i < 5; i++) {
            System.out.println("for 循环: " + i);
        }
        
        // 使用标签跳出循环
        outer:
        for (int i = 0; i < 10; i++) {
          for (int j = 0; j < 10; j++) {
            if (i == 5 && j ==5) {
              // 使用标签跳出外层循环
              break outer;
            }
          }
        }

        // for each 循环遍历数组
        int[] ns = { 1, 4, 9, 16, 25 };
        for (int n : ns) {
            System.out.println(n);
        }
    }
}
```
```java
public class LoopExample {
    public static void main(String[] args) {
       for (int i=1; i<=10; i++) {
            System.out.println("i = " + i);
            for (int j=1; j<=10; j++) {
                System.out.println("j = " + j);
                if (j >= i) {
                    break;
                }
            }
            // break跳到这里
            System.out.println("breaked");
        }
    }
}
```
```java
public class LoopExample {
    public static void main(String[] args) {
       int sum = 0;
        for (int i=1; i<=10; i++) {
            System.out.println("begin i = " + i);
            if (i % 2 == 0) {
                continue; // continue语句会结束本次循环
            }
            sum = sum + i;
            System.out.println("end i = " + i);
        }
        System.out.println(sum); // 25
    }
}
```
````

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

--- #20
transition: fade-in
---

# Java 中的 Switch 语句
<v-click>使用switch时，如果遗漏了break，就会造成严重的逻辑错误，而且不易在源代码中发现错误。从Java 12开始，switch语句升级为更简洁的表达式语法，使用类似模式匹配（Pattern Matching）的方法，保证只有一种路径会被执行，并且不需要break语句</v-click>
````md magic-move
```java {all}
public class Main {
    public static void main(String[] args) {
        int option = 2;
        switch (option) {
        case 1:
            System.out.println("Selected 1");
            break;
        case 2:
        case 3:
            System.out.println("Selected 2, 3");
            break;
        default:
            System.out.println("Not selected");
            break;
        }
    }
}
```
```java
// switch表达式
public class Main {
    public static void main(String[] args) {
        String fruit = "orange";
        int opt = switch (fruit) {
            // case 语句返回值，这里不需要 break，因为 switch 语句会自动结束
            case "apple" -> 1;
            case "pear", "mango" -> 2;
            // 如果需要复杂的语句块，可以使用 {} 包裹
            default -> {
                int code = fruit.hashCode();
                yield code; // switch语句返回值
            }
        };
        System.out.println("opt = " + opt);
    }
}
```
````

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

--- #21
transition: fade-in
layout: section
---

# 面向对象编程

<div class="flex flex-row">
  <img src="/img/OOP1.png">
  <img src="/img/OOP2.png">
</div>

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

--- #22
transition: fade-in
---

# Java 类中的成员变量和方法

````md magic-move
```java {all|3,9-24|4,10-12,20-23|5,13-14|6,13-14,15-19|all}
public class Main {
    public static void main(String[] args) {
        Person ming = new Person();
        ming.setName("Xiao Ming"); // 设置name
        ming.age = 18; // 设置age
        System.out.println(ming.getName() + ", " + ming.age);
    }
}
class Person {
    // 不带作用域修饰符，表示包访问权限，即同一个包中的其他类可以访问
    // 作用域修饰符 private 表示私有，外部无法访问，只有本类内部可以访问
    private String name;
    // 作用域修饰符 public 表示公开的，外部可以访问
    public int age;
    // public 表示公开的，外部可以调用
    public String getName() {
        // this 指向当前实例，这里因为没有冲突 this 可以省略
        return this.name;
    }
    public void setName(String name) {
        // 如果有局部变量和字段重名，那么局部变量优先级更高，就必须加上this，少了 this 就是局部变量
        this.name = name;
    }
}
```
```java {10-17|1-8}
public class Main {
    public static void main(String[] args) {
        // 调用静态方法不需要实例
        Person.setNumber(99);
        // 类名.静态字段来访问静态对象
        System.out.println(Person.number);
    }
}

class Person {
    // 静态字段属于所有实例“共享”的字段，实际上是属于class的字段
    public static int number;
    // 静态方法属于class而不属于实例，因此，静态方法内部，无法访问this变量，也无法访问实例字段，它只能访问静态字段
    public static void setNumber(int value) {
        number = value;
    }
}
```
```java
public class Main {
    public static void main(String[] args) {
        System.out.println(sum(1, 2, 3, 4, 5)); // 15
    }
    // 方法中的可变参数
    public static int sum(int... ns) {
        int sum = 0;
        // 可变参数在方法内部是一个数组，可以用for each循环遍历
        for (int n : ns) {
            sum = sum + n;
        }
        return sum;
    }
}
```
````

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

--- #23
transition: fade-in
---

# Java 类中的构造方法

````md magic-move
```java {all|3,13-17,8-9|4,10-12|all}
public class Main {
    public static void main(String[] args) {
        Person p1 = new Person("Xiao Ming", 15); // 调用带参数的构造方法
        Person p2 = new Person(); // 调用无参数构造方法
    }
}
class Person {
    private String name; // 默认初始化为null
    private int age; // 默认初始化为0
    // 无参数构造方法，也叫默认构造方法，如果什么构造方法都不写，编译器会自动加上一个无参数构造方法
    public Person() {
    }
    // 带参数的构造方法，可以初始化name和age，初始化后优先级高于默认值；如果有多个构造方法，可以根据参数个数和类型区分
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return this.name;
    }
    public int getAge() {
        return this.age;
    }
}
```
```java {4}
public class Main {
    public static void main(String[] args) {
        Person p1 = new Person("Xiao Ming", 15); // 既可以调用带参数的构造方法
        Person p2 = new Person(); // 类中只有带参数的构造方法，那么还可以调用无参数构造方法吗❓️🕵‍♀
    }
}
class Person {
    private String name; // 默认初始化为null
    private int age; // 默认初始化为0
    // 带参数的构造方法，可以初始化name和age，初始化后优先级高于默认值；如果有多个构造方法，可以根据参数个数和类型区分
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return this.name;
    }
    public int getAge() {
        return this.age;
    }
}
```
````

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

--- #24
transition: fade-in
---

# Java 类中的方法重载

方法名相同，功能类似，但各自的参数不同，称为方法<span v-mark.circle.red>重载</span>（Overload）
  
```java
public class Main {
    public static void main(String[] args) {
        System.out.println(sum(1, 2)); // 3
        System.out.println(sum(1, 2, 3)); // 6
        System.out.println(sum(1, 2, 3, 4)); // 10
    }
    // 方法重载
    public int sum(int a, int b) {
        return a + b;
    }
    public int sum(int a, int b, int c) {
        return a + b + c;
    }
    public int sum(int a, int b, int c, int d) {
        return a + b + c + d;
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

--- #25
transition: fade-in
---

# Java 类中的继承

````md magic-move
```java{1|1-14|15|15-24}
class sealed Person permits Student { // 使用 sealed 修饰类，表示这个类只能被 Student 继承
    private String name;
    private int age;
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return this.name;
    }
    public int getAge() {
        return this.age;
    }
}
class final Student extends Person { // 子类继承了父类所有的字段和方法，注意：构造方法不会被继承且子类不能继承父类的私有字段和方法
    private int score;
    public Student(String name, int age, int score) {
        super(name, age); // 调用父类的构造方法，初始化name和age，这里必须写在第一行
        this.score = score;
    }
    public int getScore() {
        return this.score;
    }
}
```
```java{2|22-24}
class sealed Person permits Student { // 使用 sealed 修饰类，表示这个类只能被 Student 继承
    protected String name;
    private int age;
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return this.name;
    }
    public int getAge() {
        return this.age;
    }
}
class final Student extends Person { // 子类继承了父类所有的字段和方法，注意：构造方法不会被继承且子类不能继承父类的私有字段和方法
    private int score;
    public Student(String name, int age, int score) {
        super(name, age); // 调用父类的构造方法，初始化name和age，这里必须写在第一行
        this.score = score;
    }
    // ...
    public void hello() {
        System.out.println("Hello, " + super.name); // super 一个指向父类实例的特殊引用，这里用this也可以
    }
}
```
```java{15-25}
class Person {
    private String name;
    private int age;
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return this.name;
    }
    public int getAge() {
        return this.age;
    }
}
class final Student extends Person { // 子类继承了父类所有的字段和方法，注意：构造方法不会被继承且子类不能继承父类的私有字段和方法
    private int score;
    public Student(String name, int age, int score) {
        // 如果没有调用父类的构造方法，编译器会自动加上
        // super();
        this.score = score;
    }
    public int getScore() {
        return this.score;
    }
}
```
```java{15-25}
class Person { // 使用 sealed 修饰类，表示这个类只能被 Student 继承
    private String name;
    private int age;
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return this.name;
    }
    public int getAge() {
        return this.age;
    }
}
class final Student extends Person { // 子类继承了父类所有的字段和方法，注意：构造方法不会被继承且子类不能继承父类的私有字段和方法
    private int score;
    public Student(String name, int age, int score) {
        // ❌️ 编译错误，因为父类没有无参数构造方法
        // super(); 编译器会自动加上
        this.score = score;
    }
    public int getScore() {
        return this.score;
    }
}
```
```java {1-6}
public class Main {
    public static void main(String[] args) {
        Student s = new Student("Xiao Ming", 12, 89);
        System.out.println(s.getName() + ", " + s.getAge() + ", " + s.getScore());
    }
}
// ...
class final Student extends Person { // 子类继承了父类所有的字段和方法，注意：构造方法不会被继承且子类不能继承父类的私有字段和方法
    private int score;
    public Student(String name, int age, int score) {
        super(name, age); // 调用父类的构造方法，初始化name和age，这里必须写在第一行，如果没有写，编译器会自动加上 super()
        this.score = score;
    }
    public int getScore() {
        return this.score;
    }
}
```
````

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

--- #26
transition: fade-in
---

# Java 类中的向上转型和向下转型

````md magic-move
```java
public class Main {
    public static void main(String[] args) {
        Person p = new Student("Xiao Ming", 12, 89); // 向上转型
        System.out.println(p.getName() + ", " + p.getAge());
        Student s = (Student) p; // 向下转型
        System.out.println(s.getName() + ", " + s.getAge() + ", " + s.getScore());
    }
}
```
```java
// 向下转型失败
public class Main {
    public static void main(String[] args) {
        Person p = new Person("Xiao Ming", 12);
        Student s = (Student) p; // ❌️ 编译通过，运行时会抛出 ClassCastException 异常
        System.out.println(s.getName() + ", " + s.getAge() + ", " + s.getScore());
    }
}
```
```java
// 安全的向下转型
public class Main {
    public static void main(String[] args) {
        Person p = new Student("Xiao Ming", 12, 89);
        if (p instanceof Student) { // 判断 p 是否是 Student 的实例
            Student s = (Student) p; // 向下转型
            System.out.println(s.getName() + ", " + s.getAge() + ", " + s.getScore());
        }
    }
}
```
```java
// 安全的向下转型
public class Main {
    public static void main(String[] args) {
        Person p = new Student("Xiao Ming", 12, 89);
        // 从Java 14开始，判断instanceof后，可以直接转型为指定变量，避免再次强制转型
        if (p instanceof Student s) { // 判断 p 是否是 Student 的实例
            System.out.println(s.getName() + ", " + s.getAge() + ", " + s.getScore());
        }
    }
}
```
````

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

--- #27
transition: fade-in
---

# Java 类中的方法重写

方法重写是指子类重新定义父类的方法，方法名、参数列表和返回值类型都必须与父类中的方法一致

````md magic-move
```java
class Person {
    public void run() {
        System.out.println("Person run");
    }
}
class Student extends Person {
    // @Override 注解表示这个方法是重写父类的方法，如果方法名写错或者参数列表不一致，编译器会报错
    @Override // 重写父类的方法
    public void run() {
        System.out.println("Student run");
    }
}
public class Main {
    public static void main(String[] args) {
        Person p = new Student();
        p.run(); // Student run
    }
}
```
```java
class Person {
    public void run() {
        System.out.println("Person run");
    }
}
class Student extends Person {
    @Override // 重写父类的方法
    public void run() {
        System.out.println("Student run");
    }
    public void study() {
        System.out.println("Student study");
    }
}
public class Main {
    public static void main(String[] args) {
        Person p = new Student();
        p.run(); // Student run
        // ❌️ 编译错误，因为父类引用不能调用子类特有的方法
        // p.study();
    }
}
```
```java
class Person {
    public void run() {
        System.out.println("Person run");
    }
    public final void hello() { // final 修饰的方法不能被重写
        System.out.println("Person hello");
    }
}
class Student extends Person {
    @Override // 重写父类的方法
    public void run(String s) { // ❌️ 编译错误，因为父类没有 run(String s) 方法，方法签名不同
        System.out.println("Student run");
    }
    @Override
    public void study() { // ❌️ 编译错误，因为父类没有 study 方法
        System.out.println("Student study");
    }
    @Override
    public void hello() { // ❌️ 编译错误，因为父类的 hello 方法被 final 修饰，不能被重写
        System.out.println("Student hello");
    }
}
```
````

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

--- #28
transition: fade-in
---

# 方法重写和方法重载的区别

| 方法重载(Overload) | 方法重写(Override) |
| --- | --- |
| 方法名相同，参数列表不同 | 方法名相同，参数列表相同 |
| 返回值类型通常是相同的 | 返回值类型必须相同 |
| 可以在同一个类中 | 一般在父类和子类中 |
| 编译器根据参数列表选择调用 | 运行时根据对象类型选择调用 |
| 重载是静态绑定 | 重写是动态绑定 |

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

--- #29
transition: fade-in
---

# Java 中的多态

- 多态是指同一个方法调用，由于对象不同可能会有不同的行为，即一个引用变量指向不同类型的对象，调用相同方法时会产生不同的行为。 
- 多态的实现需要<span v-mark.red>继承</span>、<span v-mark.red>方法重写(Override)</span>和<span v-mark.red>父类引用指向子类对象(向上转型)</span>
- 多态的好处是可以使程序变得更加灵活，可以在不修改原有代码的情况下增加新的功能

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

--- #30
transition: fade-in
---

# Java 中的多态

````md magic-move
```java
// 给一个有普通收入、工资收入和享受国务院特殊津贴的小伙伴算税
// 普通收入
class Income {
    protected double income;
    public Income(double income) {
        this.income = income;
    }
    public double getTax() {
        return income * 0.1; // 税率10%
    }
}
// 工资收入
class Salary extends Income {
    public Salary(double income) {
        super(income);
    }
    @Override
    public double getTax() {
        if (income <= 5000) {
            return 0;
        }
        return (income - 5000) * 0.2;
    }
}
```
```java
// 给一个有普通收入、工资收入和享受国务院特殊津贴的小伙伴算税
// 普通收入
class Income {
    protected double income;
    public Income(double income) {
        this.income = income;
    }
    public double getTax() {
        return income * 0.1; // 税率10%
    }
}
// ...
// 国务院特殊津贴
class StateCouncilSpecialAllowance extends Income {
    public StateCouncilSpecialAllowance(double income) {
        super(income);
    }
    @Override
    public double getTax() {
        return 0;
    }
}
```
```java
public class Main {
    public static void main(String[] args) {
        // 给一个有普通收入、工资收入和享受国务院特殊津贴的小伙伴算税:
        Income[] incomes = new Income[] {
            new Income(3000),
            new Salary(7500),
            new StateCouncilSpecialAllowance(15000)
        };
        System.out.println(totalTax(incomes));
    }

    public static double totalTax(Income... incomes) {
        double total = 0;
        for (Income income: incomes) {
            total = total + income.getTax();
        }
        return total;
    }
}
```
````

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

--- #31
transition: fade-in
---

# Java 中的抽象类

<v-clicks>

- 抽象类是不能被实例化的类，只能被继承
- 抽象类中可以包含抽象方法，抽象方法是没有方法体的方法，只有方法声明，没有方法体
- 抽象类中的抽象方法**必须**被子类实现，否则子类也必须是抽象类
- 抽象类中可以包含普通方法，普通方法有方法体，但是抽象类中至少有一个抽象方法
- 抽象类中可以包含成员变量，构造方法，静态方法等
- 抽象类中的构造方法不能用来实例化对象，只能被子类调用，用来初始化子类的实例

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

--- #32
transition: fade-in
---

# Java 中的抽象类

````md magic-move
```java
// 抽象类
abstract class Person {
    private String name;
    public Person(String name) {
        this.name = name;
    }
    public String getName() {
        return this.name;
    }
    // 抽象方法
    public abstract int getAge();
}
// 继承抽象类
class Student extends Person {
    private int age;
    public Student(String name, int age) {
        super(name);
        this.age = age;
    }
    // 实现抽象方法
    @Override
    public int getAge() {
        return this.age;
    }
}
```
```java
public class Main {
    public static void main(String[] args) {
        Person p = new Student("Xiao Ming", 12);
        System.out.println(p.getName() + ", " + p.getAge());
    }
}
```
````

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


--- #33
transition: fade-in
---

# Java 中的接口

<v-clicks>

- 接口是抽象方法的集合，接口中的方法都是抽象方法，没有方法体
- 接口中的方法默认是 public abstract，可以省略
- 接口中不能有实例字段，但可以有静态常量字段，字段默认是 public static final，可以省略
- 接口中的方法不能有方法体，不能有构造方法，因为接口不是类
- 接口可以继承多个接口
- 一个类可以实现多个接口，但只能继承一个类

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

--- #34
transition: fade-in
---

# Java 中的接口

````md magic-move
```java {1-4|5-12}
interface Person {
    // 接口中的方法默认是 public abstract，可以省略
    void run();
}
// 实现接口
class Student implements Person {
    // 实现接口的方法
    @Override
    public void run() {
        System.out.println("Student run");
    }
}
```
```java {5-7|9|10-14|15-18}
interface Person {
    // 接口中的方法默认是 public abstract，可以省略
    void run();
}
interface Hello {
    void hello();
}
// 实现多个接口
class Student implements Person, Hello {
    // 实现接口的方法
    @Override
    public void run() {
        System.out.println("Student run");
    }
    @Override
    public void hello() {
        System.out.println("Hello");
    }
}
```
```java {5-6}
interface Person {
    // 接口中的方法默认是 public abstract，可以省略
    void run();
}
// 接口继承接口
interface Hello extends Person {
    void hello();
}
// 实现接口
class Student implements Hello {
    // 实现接口的方法
    @Override
    public void run() {
        System.out.println("Student run");
    }
    @Override
    public void hello() {
        System.out.println("Hello");
    }
}
```
```java {8-12|3-4}
public class Main {
    public static void main(String[] args) {
        Person p = new Student("Xiao Ming");
        p.run();
    }
}
interface Person {
    String getName();
    String ACTION = "run"; // 接口中的字段默认是 public static final，可以省略
    default void run() { // 接口中的默认方法
        System.out.println(getName() + ACTION);
    }
}
class Student implements Person {
    private String name;
    public Student(String name) {
        this.name = name;
    }
    public String getName() {
        return this.name;
    }
}
```
````

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

<!-- 实现类可以不必覆写default方法。default方法的目的是，当我们需要给接口新增一个方法时，会涉及到修改全部子类。如果新增的是default方法，那么子类就不必全部修改，只需要在需要覆写的地方去覆写新增方法。 -->

--- #35
transition: fade-in
---

# Java 中的接口和抽象类的区别

| 特点                   | 接口                               | 抽象类                             |
|----------------------|------------------------------------|------------------------------------|
| 定义关键字           | `interface`                        | `abstract class`                   |
| 继承                 | 继承一个或多个接口                    | 可以继承一个抽象类，同时实现多个接口   |
| 构造方法             | 不能有构造方法                       | 可以有构造方法，供子类调用              |
| 方法                 | 可以包含抽象方法、默认方法、静态方法   | 可以包含抽象方法、普通方法、静态方法     |
| 成员变量             | 只能是静态常量，不能有实例变量      | 可以有各种类型的成员变量                |
| 扩展性               | 更灵活，易于替换和扩展                | 更具体，包含部分实现，可作为子类的模板    |


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


--- #36
transition: fade-in
---

# Java 面向抽象编程

<v-clicks>

- 上层代码只定义规范，例如使用接口或抽象类
- 不需要子类就可以实现业务逻辑（正常编译）
- 具体的业务逻辑由不同的子类实现，调用者并不关心，利用的是多态性，向上转型
- 降低耦合度，提高代码的灵活性和可维护性

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

--- #37
transition: fade-in
layout: end
---

# 谢谢观看😃

该幻灯片可以在👉[java-tutorial.vercel.app](https://java-tutorial.vercel.app)上查看
