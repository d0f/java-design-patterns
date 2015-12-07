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

* an object structure contains many classes of objects with differing interfaces, and you want to perform operations on these objects that depend on their concrete classes
* many distinct and unrelated operations need to be performed on objects in an object structure, and you want to avoid "polluting" their classes with these operations. Visitor lets you keep related operations together by defining them in one class. When the object structure is shared by many applications, use Visitor to put operations in just those applications that need them
* the classes defining the object structure rarely change, but you often want to define new operations over the structure. Changing the object structure classes requires redefining the interface to all visitors, which is potentially costly. If the object structure classes change often, then it's probably better to define the operations in those classes

**Real world examples:**

* [Apache Wicket](https://github.com/apache/wicket) component tree, see [MarkupContainer](https://github.com/apache/wicket/blob/b60ec64d0b50a611a9549809c9ab216f0ffa3ae3/wicket-core/src/main/java/org/apache/wicket/MarkupContainer.java)

**Credits**

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
