#  静态代码块，构造代码块，局部代码块

---

#### 执行顺序:

* 静态 - 构造代码块 - 构造方法 - 局部

#### 用途:

* 静态代码块:只会被执行一次,一般用于初始化项目

  * > 静态代码块
    > 1，在类第一次加载时就加载到内存中并一直驻存，
    > 并全局共享,直到类消失静态资源才消失
    > 2，并且静态资源只被加载一次
  
* 构造代码块:用来抽取构造方法中的共性代码

* 局部代码块:用来控制变量的作用范围,出了括号就失效.变量范围越小越好.

-----

# 子类不能调用曾父类的成员变量.除非父类的成员变量是 super.曾父类的成员变量 赋值的/

> ```java
> 
> //这个不叫多态.有方法重写才叫多态
> Zeng z=New Zi(); 
> sout(zi.num)
>     
> class Zeng{
>  int num=1;
> }
> class Fu extends  Zeng{
>  int num=2 ;
>  int num2=super.num;//只能父类也super.曾父类的成员变量 去赋值
> }
> class Zi extends Fu{
>  int num=3;
>  public void show() {
>      int num=4;
>      int num2= super.num2;
>      System.out.println(num2);
>      System.out.println(super.num);
>      System.out.println(this.num);
>      System.out.println(num);
>  }
> }
> ```

---

# 子类构造会调用父类的构造,父类没写就调默认的构造

```java
class F {
    int i;
    F() {
        System.out.println("FFFFFFF");
    }
}

public class Z extends F{
    int i;
    Z() {
        System.out.println("ZZZZZZZZ");
    }
    public static void main(String[] args) {
        Z z = new Z();
        //FFFFFFF
        //ZZZZZZZZ

    }
}
```

# 有关继承的代码块和构造方法的执行顺序

```java
//A静态代码块
//B静态代码块
//A构造代码块
//A的构造方法
//B造代码块
//B构造方法
public class OOPTest {
    public static void main(String[] args) {
        B b = new B();

    }
}
class A{
    static {
        System.out.println("A静态代码块");
    }
    {
        System.out.println("A构造代码块");
    }
    public A() {
        System.out.println("A的构造方法");
    }
}
class B extends A{
    static {
        System.out.println("B静态代码块");
    }
    {
        System.out.println("B造代码块");
    }
    public B() {
        super();
        System.out.println("B构造方法");
    }
}

```



# 子类继承父类,重写的那个方法还能重载吗?

> ## 可以

# 重载返回值类型不一样也是重载

---

# 父类最好还是加上无参构造,怕你子类构造时忘了给super传参



