在js的类中，this是没有自动绑定的，所以当你访问一个回调函数，那么这个函数中的this就没有绑定指定的类，所以会返回undefined

js中的bind方法 
![[传递props和state给子组件.html]]
https://www.imooc.com/video/17885
![[Pasted image 20240108232405.png]]
也可以使用es6中的箭头函数
![[Pasted image 20240108232906.png]]



https://www.bilibili.com/video/BV1Sp4y1U7FG/?vd_source=54c4bb63799ad696ed0571b9fe25e6e0
![[Pasted image 20240109164636.png]]普通函数的this是动态的,普通函数的this指针指向函数的调用者

箭头函数中的this 是在定义时就确定了，定义时，箭头函数属于object window，所以箭头函数中的this 指向window，window 是全局对象
