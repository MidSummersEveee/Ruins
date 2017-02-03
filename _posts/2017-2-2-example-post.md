---
layout: post
title: Interesting Facts about Variables' Intialization in Java
excerpt: "Thinking in Java一书谈到了一个有趣的事实"
modified: 2/2/2017, 21:31:35
tags: [intro, beginner, jekyll, tutorial]
comments: true
category: blog
---


*Thinking in Java*一书谈到了一个有趣的事实，即，若我们有一个包含其他类对象作为成员变量的类，那么，这些变量的初始化，会在构造方法执行之前就被完成。

```
class Tag {
	Tag(int maker) {
    	System.out.println("Tag(" + marker + ")"); 
    }
}
class Card {
	Tag t1 = new Tag(1);
    // Before constructor

    Card() {
    System.out.println("Card()");
    t3 = new Tag(33);
    // Re-initialize t3   }

    Tag t2 = new Tag(2);
    // After constructor

    void f() {
    	System.out.println("f()")
    	Tag t3 = new Tag(3);
    // At end
}

public class OrderOfInitialization {
	public static void main(String[] args) {
    	Card t = new Card();
        // Shows that construction is done
        }
}
```

本例中，尽管执行main函数之后，似乎应该会先执行Card类的构造函数，实质上，由于Card类包含了Tag类的对象成员，在创建对象Card类的实例时，Java会优先完成Card类的成员对象初始化，即现行生成三个Tag类的对象，初始化完毕后才会执行构造函数。

实际打印结果为：
```
Tag(1)
Tag(2)
Tag(3)
Card()
Tag(33)
f()
```
