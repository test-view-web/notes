https://blog.csdn.net/weixin_60401853/article/details/129825597

1. 调用父类的成员变量
2. 调用父类的成员方法
3. 调用父类的构造方法（有参）
super关键字是Java中的一个引用变量，它可以用来引用父类的成员变量、成员方法和构造方法。具体来说，super可以用于以下几个方面：

#### 1. 引用父类的成员变量
在Java中，如果父类和子类都有同名的成员变量，那么在子类中使用该变量时，会默认使用子类的变量。如果要引用父类的同名变量，可以使用super关键字。例如：

class Animal {
    String name = "animal";
}
 
class Dog extends Animal {
    String name = "dog";
 
    void printNames() {
        System.out.println(name); // 输出 "dog"
        System.out.println(super.name); // 输出 "animal"
    }
}
在上面的例子中，Dog类继承了Animal类，并定义了一个同名变量name。在printNames方法中，使用this.name会输出子类的name值"dog"，而使用super.name则会输出父类的name值"animal"。

#### 2. 引用父类的成员方法
在子类中可以通过super关键字来调用父类的成员方法。例如：

class Animal {
    void speak() {
        System.out.println("I'm an animal");
    }
}
 
class Dog extends Animal {
    void speak() {
        System.out.println("I'm a dog");
        super.speak(); // 调用父类的speak方法
    }
}
在上面的例子中，Dog类继承了Animal类，并重写了speak方法。在重写的speak方法中，使用super.speak()来调用父类的speak方法，从而实现在子类中添加额外的逻辑同时保留父类的行为。

#### 3. 调用父类的构造方法
在Java中，子类的构造方法默认会调用父类的无参构造方法，但如果父类没有无参构造方法，那么就需要使用super关键字来调用父类的其他构造方法。例如：

class Animal {
    String name;
 
    Animal(String name) {
        this.name = name;
    }
}
 
class Dog extends Animal {
    int age;
 
    Dog(String name, int age) {
        super(name); // 调用父类的构造方法
        this.age = age;
    }
}
在上面的例子中，Animal类定义了一个有参构造方法，而Dog类继承了Animal类并定义了自己的有参构造方法。在Dog类的构造方法中，使用super(name)来调用父类的构造方法，并将name参数传递给父类的构造方法，从而完成了子类和父类之间的构造方法调用。
————————————————
版权声明：本文为CSDN博主「就叫你天选之人啦」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/weixin_60401853/article/details/129825597