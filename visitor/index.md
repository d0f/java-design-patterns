---
layout: pattern
title: Visitor
folder: visitor
permalink: /patterns/visitor/
categories: Behavioral
tags:
 - Java
 - Difficulty-Expert
 - Gang Of Four
---

**Intent:** 表示在对象结构的元素上执行的操作。访问者可以让你定义一个新的操作，而不改变它操作的元素所在的类。

![alt text](./etc/visitor_1.png "Visitor")

**Applicability:** 使用访问者模式

* 一个对象结构包含了许多类的对象，它们继承不同的接口，并且你希望在它们的具体类上执行这些对象的操作。
* 许多不同的和不相关的操作需要在某个对象结构中某个对象进行对象，并且你想避免“污染”他们操作所在的类。访问者可以相关性的操作定义在同一个类中。当对象结构被许多应用程序共享时，可以在需要的时候使用访问这模式
* the classes defining the object structure rarely change, but you often want to define new operations over the structure. Changing the object structure classes requires redefining the interface to all visitors, which is potentially costly. If the object structure classes change often, then it's probably better to define the operations in those classes

**Real world examples:**

* [Apache Wicket](https://github.com/apache/wicket) component tree, see [MarkupContainer](https://github.com/apache/wicket/blob/b60ec64d0b50a611a9549809c9ab216f0ffa3ae3/wicket-core/src/main/java/org/apache/wicket/MarkupContainer.java)

**Credits**

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
