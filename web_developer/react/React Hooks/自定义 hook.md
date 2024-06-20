#### 1、react中自定义hook的目的是什么
在React中，自定义Hook的目的是为了将组件逻辑抽象出来，使其可重用。自定义Hook可以让你在不增加组件的复杂度的情况下，将状态逻辑和副作用逻辑从组件中提取出来，这样可以更好地组织代码，使得代码更加清晰、可维护，并且可以提高代码的复用性。


#### 2、自定义hook的函数体中可以使用其他hook吗
 
自定义Hook的函数体中可以使用其他Hook。

事实上，自定义Hook本身就是由React的基本Hook组成的。React的基本Hook，如useState、useEffect、useContext等，都可以在自定义Hook中被调用和使用。

例如，你可以在自定义Hook中使用useState来管理状态，使用useEffect来处理副作用，使用useContext来访问React的Context等等。这样可以让你在自定义Hook中使用React提供的所有功能，使得自定义Hook更加灵活和强大。

