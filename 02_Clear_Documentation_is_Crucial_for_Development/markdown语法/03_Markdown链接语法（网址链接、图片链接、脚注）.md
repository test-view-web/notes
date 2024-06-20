### 一、Markdown超链接语法
\[链接显示名\](\链接地址 "链接标题"\)

方括号和圆括号之间不需要隔空格。链接显示名是指该链接在预览窗口显示的内容，而链接标题是指当我们将鼠标悬停在该链接上时显示的内容，它并不是必须写的。注意链接标题要用双引号引起并且与链接地址间隔一个空格。举例如下：
`[Markdown链接语法]([https://markdown.com.cn/basic-syntax/](https://link.zhihu.com/?target=https%3A//markdown.com.cn/basic-syntax/)>links.html "标题")`

如果要插入的链接并不需要显示指定的显示名，而是直接以链接的形式显示的话，使用尖括号即可快速创建链接，举例如下：

> `<https://markdown.com.cn/basic-syntax/links.html>`

显示为：[https://markdown.com.cn/basic-syntax/links.html](https://link.zhihu.com/?target=https%3A//markdown.com.cn/basic-syntax/links.html)

注意，许多 Markdown 处理器会自动将 URL 作为链接，包括 VS Code。当我们直接书写一个网页链接时，比如：[https://markdown.com.cn/extended-syntax/automatic-url-linking.html](https://link.zhihu.com/?target=https%3A//markdown.com.cn/extended-syntax/automatic-url-linking.html)

处理器会自动将其转换成链接。如果想避免使用这一功能，可以通过将网址用反引号定义为代码来禁止： `https://markdown.com.cn/extended-syntax/automatic-url-linking.html`
### 二、Markdown图片链接语法

3）使用语法格式： 更多情况下我们使用特定的书写格式来导入图片，这更符合我们使用 Markdown 的初衷，也不容易出错。将图片导入Markdown的语法为：

>`![Alt Text](path/to/image.png)`

其中 Alt Text 表示插入的图片无法正常显示时图片显示的名称，之后的圆括号内书写的是图片所在的路径，建议使用相对路径，其中 / 开头的路径是相较与工作区根目录来处理的，而以 ./ 开始的路径或没有任何前缀的路径则是相较于当前文件开始处理的。

`
``[![error](/path/to/image_4.png)](https://baidu.com)``

[![error](/path/to/image_4.png)](https://baidu.com)
[原知乎网页](https://zhuanlan.zhihu.com/p/648801929 "一个标题")