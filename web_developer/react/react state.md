![[Pasted image 20240108224856.png]]

state 中的值不能随便被更改，唯一更改的方法就是调用 setstate方法

## 不要直接修改 state

>  React 规定：class 组件的 `constructor` 构造函数是**唯一**可以给 `this.state` 赋值的地方。

  

**示例：**此代码不会重新渲染组件，且是个糟糕的写法

```
this.state.comment = 'Hello';
```

  

应该使用 `setState()`:

```
this.setState({comment: 'Hello'});
```

  

**Tips：**React 希望开发者将 `this.state` 看作是不可变的，将其视为已经被渲染了的值，即当前屏幕上显示的值。