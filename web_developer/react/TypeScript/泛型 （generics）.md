在 TypeScript 中，`echo` 函数的目的是接收一个参数并将其返回。下面是一个简单的 TypeScript 示例：
```typescript
function echo(arg){
	return arg
}

const result = echo（123）
```

https://www.runoob.com/typescript/ts-function.html
![[TypeScript 函数 _ 菜鸟教程.html]]

![[Pasted image 20240304233744.png]]

泛型（Generics）是一种编程语言特性，允许在定义函数、类、接口等时使用占位符来表示类型，而不是具体的类型。

![[TypeScript 泛型 _ 菜鸟教程.html]]



![[Pasted image 20240308125942.png]]
hello 是函数的引用，指定 hello 所指的函数的参数props的类型为 IHelloProps , 此时在使用Hello 函数时会获得函数验证，并且在敲代码 props. 的时候会 获得代码补全提示

![[Pasted image 20240308131311.png]]
React.FC 是 react 预先定义的泛型接口，在第七行的代码中调用该接口，调用时传入一个

`React.FC<>` 后面的尖括号 `<>` 中接受一个泛型参数，用于指定组件的 props 类型。在 TypeScript 中，这个泛型参数可以是任何合法的类型，通常是一个对象类型或者一个包含组件 props 的接口。这个泛型参数是可选的，如果不传入泛型参数，则默认为一个空对象 `{}`。

例如，假设有一个简单的组件，props 包含一个 `name` 属性，你可以这样使用 `React.FC<>`：

```typescript
interface FunctionComponent<P = {}> {

        (props: P, context?: any): ReactNode;

        /**

         * Used to declare the types of the props accepted by the

         * component. These types will be checked during rendering

         * and in development only.

         *

         * We recommend using TypeScript instead of checking prop

         * types at runtime.

         *

         * @see {@link https://react.dev/reference/react/Component#static-proptypes React Docs}

         */

        propTypes?: WeakValidationMap<P> | undefined;

        /**

         * @deprecated

         *

         * Lets you specify which legacy context is consumed by

         * this component.

         *

         * @see {@link https://legacy.reactjs.org/docs/legacy-context.html Legacy React Docs}

         */

        contextTypes?: ValidationMap<any> | undefined;

        /**

         * Used to define default values for the props accepted by

         * the component.

         *

         * @see {@link https://react.dev/reference/react/Component#static-defaultprops React Docs}

         *

         * @example

         *

         * ```tsx

         * type Props = { name?: string }

         *

         * const MyComponent: FC<Props> = (props) => {

         *   return <div>{props.name}</div>

         * }

         *

         * MyComponent.defaultProps = {

         *   name: 'John Doe'

         * }

         * ```

         */

        defaultProps?: Partial<P> | undefined;

        /**

         * Used in debugging messages. You might want to set it

         * explicitly if you want to display a different name for

         * debugging purposes.

         *

         * @see {@link https://legacy.reactjs.org/docs/react-component.html#displayname Legacy React Docs}

         *

         * @example

         *

         * ```tsx

         *

         * const MyComponent: FC = () => {

         *   return <div>Hello!</div>

         * }

         *

         * MyComponent.displayName = 'MyAwesomeComponent'

         * ```

         */

        displayName?: string | undefined;

    }
```
其中，React.FunctionComponent \<IHelloProps\> 中<>的内容是 泛型标识符

```
const LikeButton : React.FC = () => { 

  }
```
这个语句是用 TypeScript 编写 React 组件时的一种常见写法，它有以下作用：

1. **定义组件类型**：`React.FC` 是 React 提供的一个泛型类型，用于表示函数组件。使用 `React.FC` 可以明确告诉 TypeScript，这是一个函数组件。

2. **指定组件的 Props 类型**：在 TypeScript 中，通过泛型 `<T>` 来指定组件的 Props 类型。在这种情况下，`React.FC` 可以接受一个泛型参数，用于定义组件的 Props 类型。例如，如果要定义一个 Props 包含 `name` 属性的组件，可以写成 `React.FC<{ name: string }>`

`const LikeButton: React.FC = () => { }` 的作用是定义了一个名为 `LikeButton` 的函数组件，该组件没有任何 Props。这意味着在组件内部，您可以直接使用 `props` 参数，而不需要额外定义 Props 类型。 ^b7b596


在泛型中，通常使用一些约定俗成的标识符，比如常见的 `T`（表示 Type）、`U`、`V` 等，但实际上你可以使用任何标识符。

T: 代表 "Type"，是最常见的泛型类型参数名。

在 TypeScript 中，`<P = {}>` 这样的语法是泛型（Generics）的一种写法。在这个例子中，`FunctionComponent` 是一个接口，它是 React 函数组件的类型定义。

`<P = {}>` 中的 `<P>` 表示类型参数（Type Parameter），它允许你在接口中定义一个占位符，用来表示将来传入的 props 的类型。在这里，`P` 是一个泛型参数，它表示函数组件的 props 类型。

`= {}` 则是默认值的写法，表示如果没有明确指定泛型参数的类型，就默认为一个空对象 `{}`。

所以，`FunctionComponent<P = {}>` 的含义是：定义一个接口 `FunctionComponent`，它接受一个泛型参数 `P`，默认类型为一个空对象 `{}`。这样定义的接口可以用来描述一个接受特定类型 props 的 React 函数组件。

https://www.typescriptlang.org/docs/handbook/2/generics.html

![[Pasted image 20240308142052.png|https://www.bilibili.com/video/BV14Z4y1u7pi?p=51&spm_id_from=pageDriver&vd_source=54c4bb63799ad696ed0571b9fe25e6e0]]

![[Pasted image 20240308142254.png]]

![[React Generics Usage 4.html]]

但是typescript中的泛型接口被实现时不是需要接收一个类型吗，React.FC<>中为什么可以接受一个接口

ChatGPT

ChatGPT

你提出了一个很好的问题。实际上，在 TypeScript 中，泛型接口被实现时确实需要传入一个类型参数。然而，`React.FC<>` 并不是一个标准的泛型接口，而是一个类型别名（Type Alias），这使得它的用法略有不同。

类型别名在 TypeScript 中允许我们给复杂的类型取一个简短的名字，并且可以包含泛型参数。因此，`React.FC<>` 其实是一个具有泛型参数的类型别名。当你使用 `React.FC<>` 时，你所传入的参数会被用作组件的 props 类型。

事实上，`React.FC<>` 的定义类似于下面的代码：

typescriptCopy code

`type ReactFC<P = {}> = FunctionComponent<P>;`

其中 `FunctionComponent` 是一个泛型接口，定义了函数组件的类型。`React.FC<>` 其实是 `FunctionComponent<>` 的一个别名，它接受一个泛型参数 `P`，表示组件的 props 类型，默认值为一个空对象 `{}`。

因此，当你使用 `React.FC<>` 来定义组件时，你所传入的参数（例如接口或类型别名）会被用作组件的 props 类型。虽然 `React.FC<>` 看起来像一个普通的函数接口，但实际上它是一个具有泛型参数的类型别名，这使得它可以接受一个接口作为参数。




type FC<P = {}> = FunctionComponent``<P>``;当“const MyComponent: React.FC``<MyComponentProps> ``= (props) => { // 组件的实现 };”
时，P是什么

在这种情况下，P是一个泛型参数，用于表示组件的 props 类型。在 React.FC``<MyComponentProps>`` 中，MyComponentProps被用作 P的具体类型，因此 P 的类型就是 MyComponentProps，即组件接受的 props 类型。

换句话说，当你声明 ``const MyComponent: React.FC<MyComponentProps> ``时，你实际上是在声明一个名为 MyComponent的变量，它是一个函数组件，接受的 props 类型为MyComponentProps。在这个声明中，P被指定为 MyComponentProps，因此 props 参数的类型将会是 MyComponentProps。



但是MyComponentProps不是一个接口吗，为什么说它是类型



在 TypeScript 中，`interface` 和 `type`（类型别名）都用来描述对象的结构和类型。虽然在语法上有一些区别，但它们都可以用来定义对象类型。

在这种情况下，`MyComponentProps` 是一个接口，用于描述组件的 props 结构。虽然它是通过 `interface` 关键字定义的，但从概念上来说，接口也是一种类型，因此可以被称为类型。

因此，当说 `MyComponentProps` 是一个类型时，意思是它是一个描述对象类型的结构，可以被用来指定组件接受的 props 类型。虽然它是通过 `interface` 定义的，但它的作用与类型别名（`type`）类似，都可以用来描述对象的结构和类型。

``` typescript
import React from "react";

  

interface IHelloProps {

    message?:number;

}

  

// const Hello = (props:any) => {

//     return <h2>{props.message}</h2>

// }

const Hello: React.FC<IHelloProps>= (props) => {

    return <h2>{props.message}</h2>

}

  

Hello.defaultProps = {

    message:0

    // message: "this is the defaultProps for Hello.tsx"

}

  

export default Hello;
```


这里的``const Hello: React.FC<IHelloProps>``表明了Hello是一个'FC'，并且接受的参数的类型是'IHelloProps'