# 策略模式

## 概述

策略模式定义了一系列算法，并把每一个算法封装起来，使得这些封装起来的算法可以相互替换。

策略模式是对象行为型模式，这个模式通过对算法的封装来解耦算法的使用和算法的实现，并委派给不同的对象对这些算法进行管理。

## 特点

## 结构

策略模式的主要角色如下：

- 抽象策略类：通常是一个接口或者一个抽象类。里头给出所有具体策略类所需要的接口
- 具体策略类：实现抽象策略类给出的接口，提供算法的具体实现
- 环境类：持有一个具体策略类的引用，并供客户端调用

## 优缺点

- ### 优点
  
  - 具体策略类之间可以自由切换：因为每个具体策略类其实都实现了同样的一个接口，因此使得他们可以自由切换。
  - 易于扩展：增加一个新的策略，只需要添加一个具体策略类，满足“开闭原则”。避开了if-else逻辑。
  
- ### 缺点

  - 客户端必须要知道具体策略类都有哪些，然后自己决定使用哪个具体策略类
  - 会造成很多具体策略类的产生（可以使用享元模式解决创建对象的数量问题）

## 适用场景

- 一个系统需要动态地选择多个算法中的某一个，这个时候可以将每个算法封装成具体策略类。
- 一个类定义了多个行为，并且这些行为在类中是以条件语句的方式出现的，这个时候可以将每个行为封装成具体策略类。
  