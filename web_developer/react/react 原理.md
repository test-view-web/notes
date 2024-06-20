#### ReactDOM.render()
`ReactDOM.render()` 是 React 中用于将 React 元素渲染到 DOM 的方法。它是 React DOM 提供的一个重要函数，通常用于将整个应用程序的根组件渲染到页面上。

### 基本用法：



``` jsx
import React from 'react';
import ReactDOM from 'react-dom';

const App = () => (
  <div>
    <h1>Hello, React!</h1>
    <p>This is a simple React app.</p>
  </div>
);

// 将根组件渲染到页面上的指定元素中
ReactDOM.render(<App />, document.getElementById('root'));


```
在上述示例中：

- `App` 是一个简单的 React 组件。
- `ReactDOM.render(<App />, document.getElementById('root'))` 将 `App` 组件渲染到具有 `id` 为 `'root'` 的 DOM 元素中。

### 参数：

`ReactDOM.render()` 接收两个参数：

1. **第一个参数：** React 元素或组件，用于渲染到页面上。
    
2. **第二个参数：** 一个 DOM 元素，表示渲染的目标容器。
    

### 注意事项：

1. **只能调用一次：** 通常，`ReactDOM.render()` 只应该在应用程序的入口文件中调用一次。它负责渲染整个应用程序的根组件。子组件的更新和渲染由 React 自动处理。
    
2. **根 DOM 元素：** 第二个参数应该是一个有效的 DOM 元素，表示你想要将 React 应用程序渲染到的位置。在上述示例中，`document.getElementById('root')` 返回具有 `'root'` id 的元素。
    
3. **组件的挂载：** `ReactDOM.render()` 将 React 组件挂载到指定的 DOM 元素上，从而启动组件的生命周期。
    
4. **动态更新：** 一旦应用程序启动，React 将负责处理组件状态和属性的变化，并在需要时动态更新 DOM。
    

总的来说，`ReactDOM.render()` 是启动 React 应用程序的入口点，它将根组件渲染到指定的 DOM 元素上。