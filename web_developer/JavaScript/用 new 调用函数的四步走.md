
![[Pasted image 20240227180641.png]]
javascript构造函数调用所经历的步骤：  
1）创建一个新的对象；  
2）将构造函数的作用域赋给新对象（因此this指向了这个新对象）；  
3）执行构造函数中的代码（为这个新对象添加属性）；  
4）返回新对象


![[Pasted image 20240227193551.png]]
![[Pasted image 20240227193647.png]]


构造函数是面向对象编程中的一个重要概念，是指在创建一个新的对象时，用于初始化对象成员变量的一种方法。在JavaScript中，构造函数通常用于创建新的对象，而在Java中，构造函数通常用于初始化一个类的实例。

在JavaScript中，构造函数使用function关键字定义，并由一个或多个参数组成。这些参数被用于设置对象的属性，并返回一个新的对象。例如：

```JavaScript
function Person(name, age) {
this.name = name;
this.age = age;
}
```

在这个例子中，Person是一个构造函数，它接受两个参数name和age，并用它们来设置Person对象的name和age属性。要创建一个新的Person对象，可以使用new关键字：

```java
var john = new Person('John', 30);
```

在Java中，构造函数用于初始化一个类的实例。Java中的构造函数与JavaScript中的构造函数有些不同。Java中的构造函数由类名和一对括号组成。例如：

```java
public class Person {
private String name;
private int age;
public Person(String name, int age) {
this.name = name;
this.age = age;
}
}
```

在这个例子中，Person类有一个构造函数，它接受两个参数name和age，并用它们来设置Person对象的属性。要创建一个新的Person对象，可以使用new关键字：

```java
Person john = new Person('John', 30);
```

总的来说，JavaScript和Java中的构造函数都用于初始化对象的属性，但在语法上有所不同。JavaScript中的构造函数使用function关键字定义，而Java中的构造函数由类名和一对括号组成。

JavaScript 和 Java 中的 `new` 关键字有一些相似之处，但也存在一些重要的区别。

### 相似之处：

1. **用途**：
    - 在两种语言中，`new` 关键字都用于创建新的对象实例。

### 区别：

1. **语言类型**：
    
    - JavaScript 是一种动态类型的脚本语言，而 Java 是一种静态类型的编译语言。
2. **类的概念**：
    
    - 在 Java 中，`new` 通常用于实例化类。Java 中的类是一种数据结构，包含属性和方法。
    - 在 JavaScript 中，`new` 也用于实例化对象，但 JavaScript 中的类是一种基于原型的概念，不同于 Java 中的类。JavaScript 中的类更像是函数构造器或原型对象。
3. **原型链**：
    
    - JavaScript 中的 `new` 关键字会创建一个新的对象实例，并将该对象的原型链与构造函数的 `prototype` 属性相关联。
    - Java 中的 `new` 关键字创建的对象直接是指定类的实例，与原型链无关。
4. **构造函数**：
    
    - 在 JavaScript 中，使用 `new` 关键字调用的函数被称为构造函数，用于初始化新创建的对象。
    - 在 Java 中，`new` 关键字后面的表达式通常是类的构造函数，用于实例化类并初始化实例的状态。
5. **返回值**：
    
    - 在 JavaScript 中，构造函数默认返回新创建的对象实例。如果构造函数有显式返回值，且返回的是一个对象，则该对象将作为 `new` 表达式的结果返回；否则，将返回新创建的对象实例。
    - 在 Java 中，`new` 表达式的结果始终是新创建的对象实例。构造函数可以有返回值，但返回值不会影响 `new` 表达式的结果。

总的来说，尽管两者都使用 `new` 关键字来创建对象实例，但在语言类型、类的概念、原型链、构造函数和返回值等方面存在明显的区别。

![[Pasted image 20240227194809.png]]

  
Java 中的类和 JavaScript 中的类在很多方面都有相似之处，但也存在一些重要的区别。

### 相似之处：

1. **面向对象**：
    
    - Java 和 JavaScript 都支持面向对象编程（OOP），并且都使用类作为对象的模板。
2. **属性和方法**：
    
    - 在两种语言中，类可以包含属性（字段）和方法（函数）。
3. **实例化**：
    
    - 在两种语言中，类可以被实例化为对象，对象可以访问类中定义的属性和方法。

### 区别：

1. **语言类型**：
    
    - Java 是一种静态类型的编译语言，而 JavaScript 是一种动态类型的脚本语言。
2. **类的声明**：
    
    - 在 Java 中，类的声明是静态的，需要使用关键字 `class` 来声明类，类的结构在编译时确定。
    - 在 JavaScript 中，类的声明是动态的，可以使用关键字 `class` 声明类，也可以使用函数构造器或对象字面量等方式声明类，类的结构在运行时动态创建。
3. **继承**：
    
    - 在 Java 中，类的继承通过 `extends` 关键字实现，Java 支持单继承。
    - 在 JavaScript 中，类的继承可以通过原型链实现，JavaScript 支持原型链继承和组合继承。
4. **方法定义**：
    
    - 在 Java 中，类的方法通常被定义为类的一部分，通过关键字 `public`、`private`、`protected` 等修饰符来控制访问权限。
    - 在 JavaScript 中，类的方法通常定义在类的原型中，可以直接通过类的实例访问。
5. **构造函数**：
    
    - 在 Java 中，类的构造函数是一个特殊的方法，使用 `new` 关键字创建对象时会自动调用该构造函数。
    - 在 JavaScript 中，类的构造函数可以是类的一部分（通过 `constructor` 方法）或者单独定义，并且可以通过 `new` 关键字来实例化对象。
6. **访问控制**：
    
    - 在 Java 中，可以使用 `public`、`private`、`protected` 等访问修饰符来控制类的成员（属性和方法）的访问权限。
    - 在 JavaScript 中，可以使用 `public`、`private`、`protected` 等修饰符模拟访问控制，但实际上 JavaScript 中的属性和方法默认是公开的。

总的来说，Java 中的类和 JavaScript 中的类在语言类型、类的声明、继承、方法定义、构造函数和访问控制等方面存在较大的差异。

JavaScript 中实际上没有纯粹的类的概念，只有构造函数的概念，用构造函数起到类的作用