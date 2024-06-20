在非严格模式下，匿名函数中的 `this` 关键字将指向全局对象（在浏览器环境中通常是 `window` 对象），而不是函数被调用时的作用域。这可能会导致意外的行为，特别是在需要使用函数作为构造函数时。

如果你希望在函数内部使用正确的 `this` 值，可以考虑使用箭头函数，因为箭头函数的 `this` 值继承自外部作用域，而不是在函数被调用时绑定。

```
var myFunction = (name) => {
    this.name = name;
    // 函数体
};

```

和

```
var myFunction = function(name) { 
	this.name=name // 函数体 
};
```
虽然都是匿名函数，但是他们的this的指向的规则不一样
实例见“test1”
![[test1.html]]