# 多态

---

### 父类引用指向子类对象.编译看左,运行看右.

> 父亲提供的方法才能用,子类特有的功能用不了.
>
> 等于说子类重写了父类的方法  指向子类的父类对象才可以调用,

### 多态 成员变量只会看父类的.静态方法也是如此.

> 静态资源属于类,不存在重写现象,只是两个类中有同样声明的方法而已,不属于重写

# static

---



* ## 非静态能调用静态,因为要非静态是后创建的

* ## 静态不能调用非静态,理由同上.

* ## static 不能和super,this关键字一起用.理由同上上

# Final

---

* ## 被final修饰的类,无法被继承.也就是没有子类.

* ## 被final修饰的成员变量,不可以被修改

* ## 被final修饰的方法,子类不能被重写.