---
published:true
title: How Spring Works
layout: default
---

What is Spring? - is a simple question which gets so many different responses. I will try to explain what is it and how it works under the hood. 

Spring is an enterprise Java framework. It contains some useful classes that you can use in your Java projects. But some of those classes will remove a lot of boilerplate code. These are the classes that manage most of the objects in your project. 

eg: If you are working with class that needs database access. Generally, you create a connection in constructor and maintain it as class variable and use that connection to do SQL with JDBC. This is good enough for small projects. If you have a projects with tens of tables (each has it's own Java class) and if you need to write the same logic ?? We quickly realize there is lot of repeated code. We can have a global connection object which is messy. Other option is to have connection class as singleton. 

Here you need to design and implement the connection class as "Singleton". There are so many issues like this in large-scale projects which can be solved by Spring. Spring has a "container" which is like a layer on top of JVM which takes care of all your classes and objects. In this case, you can make the connection class as "singleton" with simple annotation and use it in all those classes without even passing it to constructor of those classes. Spring container manages all of this.

But what is Spring container? How it works?

Spring container, also called as Spring IoC container is a pretty good Java class that maintains all other Java classes/objects in your code. It can be explained as simple as that. In order to do that, you need to let the container know where your classes are. You can do that by XML or Java annotations or Java config classes. All we need to do is to let the container know where your classes are. Spring has many options with which you can wire your components. I mean, from previous example, database connection can be wired into each of the DAO (Data Access Object) classes. We'll see how we can do that shortly.

It works by reading from XML that you specified or with annotation based configuration. It creates all the objects and maintains them in it's own object space. When your code needs some object, you ask Spring container to get it for you. No more "new Object()". It makes the code very clean and maintainable. By this time, you still don't understand how it's going to help you.

Because Spring is useful for large scale projects, unless you write or maintain a large project, it feels counter-intuitive to use Spring instead of writing our own code to create objects.

< To be continued.. >

