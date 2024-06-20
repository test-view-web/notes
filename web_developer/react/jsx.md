## jsx 是什么
它是一种语法糖-React.createElement() 
React.createElement() 返回 ReactElement 对象 
[react 中文官方教程关于 jsx 的部分](https://zh-hans.react.dev/learn/writing-markup-with-jsx)
## JSX 规则 [](https://zh-hans.react.dev/learn/writing-markup-with-jsx#the-rules-of-jsx "Link for JSX 规则")

#### 1. 只能返回一个根元素 [](https://zh-hans.react.dev/learn/writing-markup-with-jsx#1-return-a-single-root-element "Link for 1. 只能返回一个根元素")
#### 2. 标签必须闭合 [](https://zh-hans.react.dev/learn/writing-markup-with-jsx#2-close-all-the-tags "Link for 2. 标签必须闭合")

JSX 要求标签必须正确闭合。像 `<img>` 这样的自闭合标签必须书写成 `<img />`，而像 `<li>oranges` 这样只有开始标签的元素必须带有闭合标签，需要改为 `<li>oranges</li>`。
#### 3. 使用驼峰式命名法给 ~~所有~~ 大部分属性命名！ [](https://zh-hans.react.dev/learn/writing-markup-with-jsx#3-camelcase-salls-most-of-the-things "Link for this heading")

JSX 最终会被转化为 JavaScript，而 JSX 中的属性也会变成 JavaScript 对象中的键值对。在你自己的组件中，经常会遇到需要用变量的方式读取这些属性的时候。但 JavaScript 对变量的命名有限制。例如，变量名称不能包含 `-` 符号或者像 `class` 这样的保留字。

## JSX 的大括号内来编写 JavaScript
有时候，你可能想要在标签中添加一些 JavaScript 逻辑或者引用动态的属性。这种情况下，你可以在 JSX 的大括号内来编写 JavaScript。

在 JSX 中，只能在以下两种场景中使用大括号：

1. 用作 JSX 标签内的**文本**：`<h1>{name}'s To Do List</h1>` 是有效的，但是 `<{tag}>Gregorio Y. Zara's To Do List</{tag}>` 无效。
2. 用作紧跟在 `=` 符号后的 **属性**：`src={avatar}` 会读取 `avatar` 变量，但是 `src="{avatar}"` 只会传一个字符串 `{avatar}`。

## 使用 “双大括号”：JSX 中的 CSS 和 对象 [](https://zh-hans.react.dev/learn/javascript-in-jsx-with-curly-braces#using-double-curlies-css-and-other-objects-in-jsx "Link for 使用 “双大括号”：JSX 中的 CSS 和 对象")

除了字符串、数字和其它 JavaScript 表达式，你甚至可以在 JSX 中传递对象。对象也用大括号表示，例如 `{ name: "Hedy Lamarr", inventions: 5 }`。因此，为了能在 JSX 中传递，你必须用另一对额外的大括号包裹对象：`person={{ name: "Hedy Lamarr", inventions: 5 }}`。


所以当你下次在 JSX 中看到 `{{` 和 `}}`时，就知道它只不过是包在大括号里的一个对象罢了！

#### 函数体为什么要小括号



在 JavaScript 中，当使用箭头函数返回 JSX 或一个对象字面量时，通常需要用小括号将返回的内容包裹起来。这是因为在箭头函数中，花括号 `{}` 既可以表示函数体的开始，也可以表示一个对象字面量的开始。为了避免混淆，当你想直接从箭头函数返回 JSX 或对象时，你应该使用小括号。

例如，在您的代码中：



`tags.map((tag, index) => (     <span key={index}>{tag}</span> ))`

这里，小括号告诉 JavaScript 解释器，箭头函数的返回值是括号内的内容（即一个 JSX 元素），而不是一个要执行的代码块。如果不使用小括号，JavaScript 将尝试将花括号内的内容解释为语句，而不是要返回的对象或 JSX。