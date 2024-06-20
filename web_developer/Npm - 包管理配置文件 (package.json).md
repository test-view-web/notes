## 一、package.json 基础使用
npm 规定，在项目根目录中，必须提供一个叫做 package.json 的包管理配置文件，npm是前端开发人员广泛使用的包管理工具，项目中通过package.json来管理项目中所依赖的npm包的配置。package.json就是一个json文件，除了能够描述项目的包依赖外，允许我们使用“语义化版本规则”指明你项目依赖包的版本，让你的构建更好地与其他开发者分享，便于重复使用。

本文主要从最近的实践出发，结合最新的npm和node的版本，介绍一下package.json中一些常见的配置以及如何写一个规范的package.json

#### package.json 包含的内容
>1）项目的名称、版本号、描述等；
   2）项目中都用到了哪些包；
   3）哪些包只在开发期间会用到；
   4）哪些包在开发和部署时都需要用到；
   快速创建 package.json

#### CommonJS规范

1. node_modules文件详解：包实际上是一个存档文件，即一个目录直接打包为.zip或tar.gz格式的文件，安装后解压还原为目录。完全符合CommonJS规范的包目录应该包含如下这些文件

　　1、package.json：包描述文件

　　2、bin：用于存放可执行二进制文件的目录

　　3、lib：用于存放JavaScript代码的目录

　　4、doc：用于存放文档的目录

　　5、test：用于存放单元测试用例的代码
#### npm 使用常见误区
npm 包管理工具提供一个快捷命令：`` ​​npm init -y`` ​​，可以在执行命令时所处的目录中，创建 package.json 这个包管理配置文件：


注意：

1. 上述命令，只能在英文的目录下成功运行！所以，在项目文件夹的名称一定要使用英文命名，不要使用中文，不能出现空格。

2. 运行 `npm install` 命令安装包的时候，npm 包管理工具会自动把 包的名称和版本号，记录到 package.json 中。

3. 运行 `npm unstall` 命令，来卸载指定的包： 
- 提示：安装包能简写成  npm install => npm i ，卸载包不能简写；
####  package-lock.json


我们发现在npm init的时候，不仅生成了package.json文件，还生成了package-lock.json文件。那么为什么存在package.json的清空下，还需要生成package-lock.json文件呢。本质上package-lock.json文件是为了锁版本，在package.json中指定的子npm包比如：react: "^16.0.0"，在实际安装中，只要高于react的版本都满足package.json的要求。这样就使得根据同一个package.json文件，两次安装的子依赖版本不能保证一致。

而package-lock文件如下所示，子依赖dependency1就详细的指定了其版本。起到lock版本的作用。

#### devDependencies 节点

1. 如果某些包只在项目开发阶段会用到，在项目上线后用不到了，则建议把这些包记录到 devDependencies 节点中。与之对应的，某些包在开发和项目上线后都需要用到，则建议把这些包记录到 dependencies 节点中。这两个节点，也只有这一点的区别。

使用如下命令，将包记录到 devDependencies 节点中：

```
npm install [包名] --save-dev
```

或简写：

```
 npm i [包名] -D
```

 提示：包名(moment)和参数(--save-dev) 的位置可以互换，语法比较随意；

示例：

```
 npm i webpack -D
```



#### 在导包的时候，要注意包的版本
每个包都有自己的 package.json ，在其中包含版本信息，如果是逆向得到的源码，node_modules 中一般不包含 package.json ，此时就需要找许可证 或者 代码注释来自己判断版本。（看的时候不注意，遇到的时候不会查）

#### 导入本地依赖包
## 二、package.json常用属性
#### 1. script
在npm中使用script标签来定义脚本，每当制定npm run的时候，就会自动创建一个shell脚本，这里需要注意的是，npm run新建的这个 Shell，会将本地目录的node_modules/.bin子目录加入PATH变量。

这意味着，当前目录的node_modules/.bin子目录里面的所有脚本，都可以直接用脚本名调用，而不必加上路径。比如，当前项目的依赖里面有 esbuild，只要直接写esbuild xxx 就可以了。
``` json
{
// ...
"scripts": {
"build": "esbuild index.js",
}
}
{
// ...
"scripts": {
"build": "./node_modules/.bin/esbuild index.js"
}
}
```

上面两种写法是等价的。


#### 2. bin

bin属性用来将可执行文件加载到全局环境中，指定了bin字段的npm包，一旦在全局安装，就会被加载到全局环境中，可以通过别名来执行该文件。

比如@bytepack/cli的npm包：

``` json
"bin": {
    "bytepack": "./bin/index.js"
 },
```
一旦在全局安装了@bytepack/cli，就可以直接通过bytepack来执行相应的命令，比如

```
bytepack -v
//显示1.11.0
```
如果非全局安装，那么会自动连接到项目的node_module/.bin目录中。与前面介绍的script标签中所说的一致，可以直接用别名来使用。


#### 3. package.json 必须配置（name）和（version）
[注意]对于nodejs来说，版本号的小数位代表为这个版本的稳定性，偶数位为稳定版本(0.6.x、0.8.x……)，奇数位为非稳定版本(0.7.x、0.9.x……)。一般地，开发时要使用最新的稳定版本


## [三、为npm设置代理](http://www.manongjc.com/detail/55-befrkgtjjiwjvxl.html)

```
$ npm config set proxy http://server:port
$ npm config set https-proxy http://server:port
```

如果代理需要认证的话可以这样来设置。

```
$ npm config set proxy http://username:password@server:port
$ npm config set https-proxy http://username:pawword@server:port
```

如果代理不支持https的话需要修改npm存放package的网站地址。

```
$ npm config set registry "http://registry.npmjs.org/"
```

[原乐耶园网页地址](https://www.leyeah.com/article/package-json-relies-detailed-environment-related-properties-697372)
[原博客园网页](https://www.cnblogs.com/terrymin/p/15639502.html)
