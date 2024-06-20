#### 1.初识Ajax
// 1.Ajax 是什么 
// Ajax 是 Asynchronous JavaScript and XML (异步 JavaScript 和 XML)的简写 
// Ajax 中的异步:可以异步地向服务器发送请求，在等待响应的过程中，不会阻塞当前页面，浏览器可以做自己的事情。直到成功获取响应后，浏览器才开始处理响应数据 
// XML(可扩展标记语言)是前后端数据通信时传输数据的一种格式 
// XML 现在已经不怎么用了，现在比较常用的是JSON 
// Ajax 其实就是浏览器与服务器之间的一种异步通信方式
// 使用 Ajax 可以在不重新加载整个页面的情况下，对页面的某部分进行更新 
//1.慕课网注册检测 
//2.慕课网搜索提示


#### 2.Ajax的基本用法
// 1.XMLHttpRequest
// console.log(Ajax); 
// Ajax 想要实现浏览器与服务器之间的异步通信，需要依靠XMLHttpRequest，它是一个构造函数 
// 不论是 XMLHttpRequest，还是 Ajax，都没有和具体的某种数据格式绑定 
// 2.2.准备发送请求
// xhr.open( 
// 'HTTP 方法 GET、POST、PUT、DELETE', 
// '地址 URL https://www.imooc.com/api/http/search/suggest?words=js ./index.html./index.xml./index. 
txt', // true 
//); 
// 调用 open 并不会真正发送请求，而只是做好发送请求前的准备工作 
// 2.3.发送请求 
// 调用 send() 正式发送请求 
// xhr.send(); 
// send() 的参数是通过请求体携带的数据// xhr.send(null); 
// 2.4.监听事件，处理响应 
//当获取到响应后，会触发xhr对象的 readystatechange 事件，可以在该事件中对响应进行处理 
```html
xhr.onreadystatechange = () => {
 if (xhr.readyState !== 4) return; 
 // HTTP CODE 
 // 获取到响应后，响应的内容会自动填充xhr对象的属性 
 // xhr.status: HTTP 200 404 
 // xhr.statusText: HTTP OK Not Found 
 if ((xhr.status >= 200 && xhr.status < 300) || xhr.status === 304) {

 //console.log('正常使用响应数据');
 console.log(xhr.responseText); 
}
};
```

ChatGPT给出的示例：
```html
// 创建 XMLHttpRequest 对象
var xhr = new XMLHttpRequest();

// 设置响应的回调函数
xhr.onreadystatechange = function() {
    // 检查请求是否完成
    if (xhr.readyState !== 4) return;

    // 检查 HTTP 状态码来判断响应是否成功
    if (xhr.status >= 200 && xhr.status < 300 || xhr.status === 304) {
        // 请求成功，可以正常使用响应数据
        console.log(xhr.responseText);
    } else {
        // 请求失败，处理来自服务器的错误
        console.error('Failed to load data: ' + xhr.status + ' ' + xhr.statusText);
    }
};

// 配置请求的类型和 URL
xhr.open('GET', 'https://example.com/data', true);

// 发送请求
xhr.send();

```
// readystatechange 事件监听 readyState 这个状态的变化

// readystatechange 事件也可以配合 addEventListener 使 
用，不过要注意，IE6~8不支持 addEventListener 
// 为了兼容性，readystatechange 中不使用 this，而是直接使 
用xhr 
//由于兼容性的原因，最好放在 open 之前 

// 它的值从0~4，一共5个状态 
//O:未初始化。尚未调用open() 
// 1:启动。已经调用open()，但尚未调用 send() 
// 2:发送。已经调用send()，但尚未接收到响应 
// 3:接收。已经接收到部分响应数据 
// 4:完成。已经接收到全部响应数据，而且已经可以在浏览器中使用了 

#### 3.初识跨域

// 向一个域发送请求，如果要请求的域和当前域是不同域，就叫跨域 
// 不同域之间的请求，就是跨域请求 

 2. 什么是不同域，什么是同域 
// https(协议)://www.imooc.com(域名):443 (端口号)/course/list(路径) 
**// 协议、域名、端口号，任何一个不一样，就是不同域** 
// 与路径无关，路径一不一样无所谓 
// 不同域 
// https://www.imooc.com:443/course/list
// http://www.imooc.com:80/course/list 

// http://www.imooc.com:80/course/list
// http://m.imooc.com:80/course/list
// http://imooc.com:80/course/list 

// 同域 
// http://imooc.com:80 
// http://imooc.com:80/course/list 


 3. 跨域请求为什么会被阻止 
//阻止跨域请求，其实是浏览器本身的一种安全策略--同源策略 
//其他客户端或者服务器都不存在跨域被阻止的问题 

4. 跨域解决方案 
// CORS
// JSONP 
// 优先使用 CORS 跨域资源共享，如果浏览器不支持 CORS 的话，再使用JSONP 

// Access-Control-Allow-Origin: * 
//表明允许所有的域名来跨域请求它，*是通配符，没有任何限制 
//只允许指定域名的跨域请求 
// Access-Control-Allow-Origin: http://127.0.0.1:5500

// 使用CORS 跨域的过程 
//① 浏览器发送请求 
// ② 后端在响应头中添加 Access-Control-Allow-Origin 头信息 
//③ 浏览器接收到响应 
// ④ 如果是同域下的请求，浏览器不会额外做什么，这次前后端通信就圆满完成了 
//⑤ 如果是跨域请求，浏览器会从响应头中查找是否允许跨域访问 

// CORS 的兼容性 
// IE10 及以上版本的浏览器可以正常使用 CORS 
// JSONP 

// 1.JSONP 的原理 
// script 标签跨域不会被浏览器阻止 
// JSONP 主要就是利用script 标签，加载跨域文件 


