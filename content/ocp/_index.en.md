+++
title = "OCP (Open Closed Principle)"
description = "OCP (Open Closed Principle)"
chapter = true
weight = 2
pre = "<b>2. </b>"
+++

## OCP (Open Closed Principle)
---
![ocp](ocp.jpg)
Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.

#### The principle of OCP suggests that software entities must be:
- should be open for extension:
    this means, that module can be extended. When applications requirements change,
    we are able to expand the module.

    In other words, we have the ability to extend classes, making them more functional.
    At the same time, the behavior of the old methods does not change,
    and class itself is not changing to.

- closed for modification:
    after the expansion of the entity behavior,
    no changes should be made to the code that uses these entities.

---

#### This is especially important for code in a production environment:
- any changes in the source code requires a revision of the entire code,
    where this entity / class is used.

- revision of unit testing and other similar procedures.

---

If code follows this principle, therefore does not require such effort.

---
#### Read More:
- https://github.com/SanderV1992/SOLID-examples/tree/master/src/ocp/good
- <a href="https://ru.wikipedia.org/wiki/%D0%9F%D1%80%D0%B8%D0%BD%D1%86%D0%B8%D0%BF_%D0%BE%D1%82%D0%BA%D1%80%D1%8B%D1%82%D0%BE%D1%81%D1%82%D0%B8/%D0%B7%D0%B0%D0%BA%D1%80%D1%8B%D1%82%D0%BE%D1%81%D1%82%D0%B8">https://ru.wikipedia.org/</a>
