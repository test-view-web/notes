## 效果
![[Pasted image 20231201212111.png|Obsidian 中带说明文字的图片。上方为图片，下方为说明文字（caption）。]]


#关键词 #图片注释
## 命令
说明文字是图片的替代文本（alt text)，即

```text
![This is the caption](image.png)
```

或者

```text
![[image.png|This is the caption]]
```


## 方法

- 新建一个 .txt 文件，并插入下面的代码；
- 修改文件后缀名 txt 为 css；
- 将 css 文件放到路径 `your vault/.vault/snippet` ，也可以在 `设置-外观-CSS snippets` 中打开；
- 在 `设置-外观-CSS snippets` 激活这个 `css` 脚本

  

```css
/* reading mode */
.image-embed[alt]:after {
    content: attr(alt);
    display: block;
    margin: 0.2rem 1rem 1rem 1rem;
    font-size: 90%;
    line-height: 1.4;
    color: var(--text-faint);
    text-align: center;

}
/* source view and live preview */
.image-embed[alt]:after {
    content: attr(alt);
    display: block;
    margin: 0.2rem 1rem 1rem 1rem;
    font-size: 90%;
    line-height: 1.4;
    color: var(--text-faint);
    text-align: center;
}
```


## 参考

[https://forum.obsidian.md/t/add](https://link.zhihu.com/?target=https%3A//forum.obsidian.md/t/adding-caption-to-images/16431/22%23possible-solution-editor-mode-preview-mode-1)

[原知乎网页地址](https://zhuanlan.zhihu.com/p/662633596)