---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://images.unsplash.com/photo-1484417894907-623942c8ee29?q=80&w=2664&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
# some information about your slides, markdown enabled
title: Java 入门
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

# Java 快速入门

--- #2

# Java 介绍

<v-clicks>

- Java 是一种广泛使用的计算机编程语言，拥有跨平台、面向对象、泛型编程的特性。
- Java 由 Sun Microsystems 公司的 James Gosling 等人开发，并于 1995 年正式发布。
- Java 语言的特点是平台无关性，即一次编译，到处运行。
- Java 语言的应用领域非常广泛，包括企业级应用、移动应用、嵌入式系统、大数据分析等。
- Java 语言的发展非常迅速，目前最新版本是 Java 22。

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


--- #4
transition: fade-in
---

# Java 流行度 

<img src="/img/GitHub.png"  class="w-full h-full shadow">


--- #5
transition: fade-in
---

# Java 流行度 
<img src="/img/TIOBE.png" class="w-full h-auto shadow">



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