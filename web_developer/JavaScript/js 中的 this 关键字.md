this的指向看是 哪个对象 调用执行的这个函数，

**方法调用**：

- 当一个函数作为对象的方法调用时，`this` 指向那个对象。

```
const myObject = {
    myMethod: function() {
        return this;
    }
};

myObject.myMethod(); // `this` 指向 myObject

```

**箭头函数**：

- 箭头函数不绑定自己的 `this`，它们继承 `this` 值自其所在的上下文。
```
const myObject = {
    myArrowFunction: () => {
        return this;
    }
};

myObject.myArrowFunction(); // 在浏览器中，这将返回 window 对象


```

## 箭头函数声明和普通函数声明的区别

```
function getName(){ 
	console.log(this.name); 
} 
let getName2 = () =>{
	console.log(this.name);
} 

这两种声明函数的方法有什么区别
```

在你的例子中，第一种是使用普通的函数声明方式，而第二种是使用箭头函数声明方式。这两种方式有一些重要的区别，主要涉及到它们对 `this` 关键字的处理和作用域。

1. **普通函数声明：**
    
    javascriptCopy code
    
    `function getName() {     console.log(this.name); }`
    
    - 在普通函数中，`this` 的值在运行时取决于调用该函数的方式。如果函数是作为对象的方法调用的，`this` 将指向该对象；如果函数是独立调用的，`this` 将指向全局对象（在浏览器环境中通常是 `window`）。
    - 普通函数可以通过 `call`、`apply` 或者 `bind` 来显式设置 `this`。
2. **箭头函数声明：**
    
    javascriptCopy code
    
    `let getName2 = () => {     console.log(this.name); }`
    
    - 箭头函数没有自己的 `this`，它继承自外围作用域。箭头函数捕获的是在创建时外层最近的普通函数的 `this` 值，而不是在调用时的 `this` 值。
    - 因此，箭头函数通常更适合在不需要动态绑定 `this` 的场景，比如在回调函数或闭包中使用。

示例：



```
let obj = {
	name: 'John',     
	getName: getName,     
	getName2: getName2 
};  
obj.getName();   // 输出: John  (this 指向 obj 对象) 
obj.getName2();  // 输出: undefined  (this 指向全局对象或 undefined，因为箭头函数没有自己的 this)
```

总体来说，选择使用普通函数还是箭头函数取决于你的需求。如果需要动态绑定 `this` 或者在对象上调用方法，通常使用普通函数更合适。如果希望继承外部作用域的 `this`，并且不需要动态绑定，可以使用箭头函数。



## 箭头函数
箭头函数中：this 是静态的，this始终指向函数声明时所在作用域下的 this 的值。

```JavaScript
function getName(){
    console.log(this.name);
}
let getName2 = () =>{
    console.log(this.name);
}
// 设置 window 对象的 name 属性
window.name = '张三'
const person = {
    name:'小张'
}
// 直接调用
getName() //张三
getName2() //张三
//call 方法调用
getName.call(person) //小张
getName2.call(person) //张三 箭头函数是静态的，始终指向开始时的第一个值

```

## `bind`方法
`bind` 是 `Function` 类型的原生方法之一。这个方法的主要作用是创建一个新的函数，其 `this` 值会被绑定到指定的对象，而且在调用时无论如何都不会改变。

`bind` 方法的基本语法是：


`const newFunction = originalFunction.bind(thisArg[, arg1[, arg2[, ...]]]);`

- `originalFunction` 是要绑定上下文的原始函数。
- `thisArg` 是新函数运行时 `this` 关键字绑定的对象。
- `arg1, arg2, ...` 是可选的参数，它们会预先传递给原始函数。

`bind` 方法返回一个新的函数，可以在稍后的时间点调用。这个新函数的 `this` 值已经被固定为 `thisArg`，无论它是如何被调用的。

javascriptCopy code

`const obj = { value: 42 };  function printValue() {   console.log(this.value); }  const boundFunction = printValue.bind(obj); boundFunction(); // 输出: 42`

在这个例子中，`printValue.bind(obj)` 创建了一个新的函数 `boundFunction`，当调用 `boundFunction` 时，`this` 将始终指向 `obj` 对象。

`bind` 方法在事件处理函数、定时器和实现函数式编程中经常被使用，它允许明确指定函数在运行时的上下文，避免了在函数内部使用 `this` 时出现意外的结果。

## `call` 方法
在JavaScript中，`call` 是函数对象的一个方法，用于在调用函数时显式设置函数体内的 `this` 值，并且允许传递参数列表。这允许你借用（或调用）一个对象的方法并临时设置它的 `this` 值。

`call` 方法的基本语法如下：



`functionName.call(thisArg, arg1, arg2, ...);`

- `functionName`: 要调用的函数名。
- `thisArg`: 设置函数体内的 `this` 值的对象。
- `arg1, arg2, ...`: 传递给函数的参数。

下面是一个简单的例子：



```javascript
// 定义一个对象
var person = {
  firstName: 'John',
  lastName: 'Doe',
  fullName: function() {
    return this.firstName + ' ' + this.lastName;
  }
};

// 定义另一个对象
var anotherPerson = {
  firstName: 'Jane',
  lastName: 'Doe'
};
```

// 使用 call 方法调用 person 对象的 fullName 方法，并设置 this 为 anotherPerson
var result = person.fullName.call(anotherPerson);

console.log(result);  // 输出: Jane Doe


在这个例子中，`call` 方法允许我们在 `person.fullName` 方法中设置 `this` 为 `anotherPerson` 对象，从而借用 `person.fullName` 方法来获取 `anotherPerson` 的全名。

`call` 方法还可以用于传递参数，例如：


```JavaScript
function greet(greeting) {
  console.log(greeting + ' ' + this.firstName + ' ' + this.lastName);
}

var person = {
  firstName: 'John',
  lastName: 'Doe'
};

// 使用 call 方法调用 greet 函数，并传递参数
greet.call(person, 'Hello');  // 输出: Hello John Doe

```

这个例子中，`call` 方法将 `this` 设置为 `person` 对象，并传递了 `'Hello'` 作为参数。


