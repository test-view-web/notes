App.js
```jsx
import logo from './logo.svg';

import './App.css';

import NameCard from './components/NameCard'

  

function App() {

  return (

    <div className="App">

      <header className="App-header">

        <img src={logo} className="App-logo" alt="logo" />

        <p>

          Edit <code>src/App.js</code> and save to reload.

        </p>

        <a

          className="App-link"

          href="https://reactjs.org"

          target="_blank"

          rel="noopener noreferrer"

        >

          Learn React

        </a>

      </header>

      <NameCard name = "king" number = "132456" isHuman/>

    </div>

  );

}
export default App;
```
  
NameCard.js

```jsx
import React from 'react'

class NameCard extends React.Component{

    render(){

        const {name,number,isHuman,tags} =this.props

        return(

            <div>

                <h4>{name}</h4>

                <ul>

                    <li>电话{number}</li>

                    <li>{isHuman? '人类' : '外星生物'}</li>

                </ul>

            </div>

        )

    }

}

export default NameCard
```
  


在这个 React 应用中，`NameCard` 组件是 `App` 组件的子组件。在 `App.js` 文件中，通过以下代码引入并使用了 `NameCard` 组件：



`<NameCard name="king" number="132456" isHuman/>`

这意味着 `NameCard` 组件被嵌套在 `App` 组件中，因此 `NameCard` 是 `App` 的子组件。在 React 中，父组件可以将属性传递给子组件，而这些属性可以在子组件中通过 `props` 访问和使用。

在 `NameCard.js` 文件中，通过 `this.props` 来访问在 `App.js` 中传递给 `NameCard` 组件的属性：



`const { name, number, isHuman, tags } = this.props;`

这样，`NameCard` 组件就能够显示 `App` 组件传递的属性，并以相应的方式渲染内容。
![[传递props和state给子组件 (2).html]]

在 React 中，子组件和父组件是组件之间关系的概念，它们用于描述组件的层级结构和相互之间的嵌套关系。

1. **子组件（Child Component）：**
    
    - 子组件是在另一个组件内部定义的组件。
    - 它接收父组件传递给它的数据（通过 `props`）并渲染相应的内容。
    - 子组件可以包含在父组件的 JSX 中，形成层级结构。
2. **父组件（Parent Component）：**

- 父组件是包含其他组件（包括子组件）的组件。
- 它可以传递数据、状态以及函数给子组件，以影响子组件的行为和显示。
- 父组件可以包含多个子组件，形成一个组件树。