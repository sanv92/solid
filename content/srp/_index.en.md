+++
title = "SRP (Single Responsibility Principle)"
description = "SRP (Single Responsibility Principle)"
chapter = true
weight = 1
pre = "<b>1. </b>"
+++

## SRP (Single Responsibility Principle)
---
![srp](srp.jpg)
The single responsibility principle is a computer programming principle that states that every module or class should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class. All its services should be narrowly aligned with that responsibility.

---

#### The principle of SRP can be used when:
- too much is allowed to the class object

- any change in the logic of the object's behavior leads to changes in other places of the application

- you have to test, fix errors, even if a third party is responsible for their performance

- not so simple to separate and apply a class in another area of the application, since it will pull unnecessary dependencies

---

#### Bad:
![srp_wrong_design](srp_wrong_design.png)

#### Good:
![srp_design](srp_design.png)

---
#### Read More:
- https://github.com/SanderV1992/SOLID-examples/tree/master/src/srp/good
- <a href="https://ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF_%D0%B5%D0%B4%D0%B8%D0%BD%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D0%B9_%D0%BE%D1%82%D0%B2%D0%B5%D1%82%D1%81%D1%82%D0%B2%D0%B5%D0%BD%D0%BD%D0%BE%D1%81%D1%82%D0%B8">https://ru.wikipedia.org/</a>
