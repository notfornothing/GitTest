# 异常

---

## 异常的继承关系:

### Throwable :--顶级父类

> ### Error:--系统错误，无法修复
>
> ### Exception: --可修复的错误



## try catch 和 throws 两种方式

---

# 抽象类 Abstract

* 被abstract**修饰的类叫抽象类.**
* 如果一个类中包含抽象方法(即方法被abstract修饰),那么这个类必须为抽象类.
* 但是一个抽象类不一定有抽象方法
* 抽象类不能实例化(即创建对象)
* 抽象类可以重写父类的抽象方法让其可以不抽象.或者自己就是个抽象类.
* **抽象方法不能有方法体**
* **抽象类中有构造方法**,他不能创造对象,其构造方法是为了创建子类对象使用
