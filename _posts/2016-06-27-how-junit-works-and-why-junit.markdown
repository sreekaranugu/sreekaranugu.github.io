---
published: true
title: How JUnit Works and Why JUnit
layout: post
---
JUnit is de-facto standard of Java unit testing. But it's awkward for me that I don't understand why do we need it and how it works under the hood. So here is what I found.

Can't we test the output manually with equals method and  have a main class which runs all these tests and maintains record? Let's see what we need to do:

1.  Write test methods and return proper error messages and codes when tests fail/pass. 
2. Run these methods by using a main class
3. If we need to add more tests in future we need to add them to this main class
4. If we need to run it within eclipse, we need to add a custom run configuration.
5. No other tool can integrate into out test cases to show us how much is coverage etc. 

This is hell lot of work to do with each project. We can clearly see that there is ot of boiler plate code involved. Especially you need to write "equals" methods for all primitive types and collection types and custom types and throw an error with appropriate description.

How JUnit solves all these problems:

1. JUnit has assert methods to compare and return appropriate error messages and codes.
2. Main class is called "runner" in JUnit terminology and frameworks like Spring extended this runner class to initialize their environment and run test cases properly. It is powerful mechanism.
3. You can annotate your methods with @Test and your classes with @TestSuite and they are automatically detected with reflection.
4. Eclipse has very good support for JUnit and it automatically works with Maven/Gradle configurations to run tests. 
5. Third party tools can integrate into our code and show us various other reports about our test coverage etc.

This is why JUnit is used. You can certainly write your test cases but it's not going to make anything better.