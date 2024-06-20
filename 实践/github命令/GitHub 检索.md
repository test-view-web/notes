

## **搜索指定语言**

比如我们需要搜索vue项目或者java指定语言项目，

语言过滤：使用**“language:”**筛选器来限制搜索结果的编程语言。例如，**“language:python”**。

![](https://pic3.zhimg.com/80/v2-e85a7365264c68a10d717682f0d4e46a_720w.webp)

这样我们搜索出来的都是关于指定Java语言的项目

![](https://pic1.zhimg.com/80/v2-5b99d7bc672dafd87fa8e4da17131474_720w.webp)

## **strats排序搜索**

星级排序：使用`“stars:>”`筛选器来按星级排序结果。例如，“stars:>10”将只显示星级大于10的项目。

![](https://pic3.zhimg.com/80/v2-10e82e95e68677acf055f85fae879cf6_720w.webp)

## **更新时间搜索**

更新频率：使用**“pushed:>”**筛选器来按更新日期排序结果。例如，“pushed:>2021-01-01”将只显示自2021年1月1日以来更新的项目。

![](https://pic1.zhimg.com/80/v2-768f49e64d212c2c2bd6f13400976b24_720w.webp)

## **更多搜索**

1. 贡献者搜索：使用**“involves:”**筛选器来查找包含指定用户的项目。例如，“involved:username”将列出该用户最近参与的项目。
2. README搜索：使用**“in:name,description,readme”**筛选器来搜索项目名称、描述和README文件的所有内容。例如，“in:name,description,readme python”将搜索所有包含“python”关键词的项目。
3. Forks搜索：使用**“forks:”**筛选器来搜索特定数量的分支。例如，“forks:>200”将只显示拥有200个以上分支的项目。
4. 按关注者数排序：使用**“followers:>”**筛选器按关注者数排序结果。例如，“followers:>100”将只显示其关注者超过100个的项目。
5. 按许可证搜索：使用**“license:”**筛选器来搜索特定类型的许可证。例如，“license:MIT”将只显示使用MIT许可证的项目。

## **高级搜索**

1. 按关键字排除结果：使用“-”符号来排除不感兴趣的项目。例如，“machine learning -tensorflow”将排除诸如“tensorflow”之类的项目。
2. 按文件类型搜索：使用“filename:”筛选器按文件类型搜索。例如，“filename:app.js”将只显示名为“app.js”的文件的项目。
3. 按领域搜索：在关键词后添加特定领域的词汇可以缩小搜索范围。例如，“machine learning healthcare”将返回与医疗保健领域相关的机器学习项目。
4. 根据项目活动搜索：使用“activity:”筛选器来根据提交、问题、推送和挑战等活动搜索项目。例如，“activity:pushed”将只显示最近有推送行为的项目。
5. 根据开发者类型搜索：使用“user:”筛选器来搜索具有特定开发者类型的项目。例如，“user:github”将只显示由GitHub组织创建的项目。
6. 使用通配符：使用“_”来匹配任何字符，并帮助在不确定的情况下搜索项目。例如，“docker_api”将搜索带有“Docker”的所有项目，并将返回所有包含“api”的项目。
7. 按项目大小搜索：使用“size:”筛选器按项目大小搜索。例如，“size:>5000”将只显示大于5,000KB的项目。
8. 聚焦特定领域：使用 GitHub Topics 搜索功能可以聚焦特定领域的项目。例如，通过搜索 "Topic: React" 可以找到和 React 相关的所有项目。
9. 使用高级搜索语法：高级搜索语法可以帮助你更加细致地筛选出符合你要求的项目。例如，使用 "user:username" 搜索 Github 上特定用户的项目。
10. 使用 [http://Shields.io](https://link.zhihu.com/?target=http%3A//Shields.io)：[http://shields.io](https://link.zhihu.com/?target=http%3A//shields.io) 可以帮你为项目生成一些标签，用于显示项目的关键信息，例如项目的版本、许可证信息、followers 数量等等，这些标签可以帮助你更快地了解项目。
11. 使用 Repository-metadata： "repo-metadata" 库可让你以格式化的方式检索您可能需要的项目元数据，包括包含在 readme 文件中的关键字，以及项目成员的名称和邮件地址。

## **可视化搜索**

当然这些是我们直接通过搜索语法进行搜索的，我们也可以在github上通过可视化界面进行搜索

![](https://pic3.zhimg.com/80/v2-a415d1e1da7769351176b8b913a8c846_720w.webp)

点击这个搜搜索条件去搜索

![](https://pic1.zhimg.com/80/v2-cfd3cc919eef1c1327ee648031b957dc_720w.webp)

## **github必备插件**

## **October**

在GitHub浏览项目代码时，常常感到不太方便。每次点击文件后，整个项目文件列表都会被隐藏，想查看其它文件就必须回退后再次进入。如果文件夹结构很复杂，查找起来就非常麻烦。

不过，有一款叫做octotree的工具可以很好地解决这个问题。它在GitHub页面的左上角添加了一个按钮，当你点击它时，就会展开一个菜单，显示整个项目的文件夹结构。通过octotree，你可以非常方便地浏览或下载单个源文件。

[下载地址](https://link.zhihu.com/?target=https%3A//link.juejin.cn/%3Ftarget%3Dhttps%253A%252F%252Fchrome.google.com%252Fwebstore%252Fdetail%252Foctotree%252Fbkhaagjahfmjljalopjnoealnfndnagc%253Futm_source%253Dchrome-ntp-icon)

当我们安装成功后github项目左侧就会有这个展开目录结构

![](https://pic1.zhimg.com/80/v2-220d176615787b3a90fcc6d1d79a0134_720w.webp)

![](https://pic1.zhimg.com/80/v2-c6ebc81e02898e6ae18b0bc9eb024ab4_720w.webp)

## **sourcegraph**

如果你认为octotree已经很好地解决了上述问题，那么你一定会喜欢sourcegraph。sourcegraph类似一个Web IDE，让浏览GitHub的代码成为一种全新的体验。

只需单击仓库主页上的sourcegraph按钮，你就能跳转至sourcegraph官网，通过该网站可以实现更深入的代码探究。

sourcegraph允许你对代码进行全文搜索、代码跳转、引用查找等功能，让你在快速阅读代码时受益匪浅。此外，sourcegraph还提供一些其他工具，可用于分析代码质量、评估代码可读性等方面的问题。总之，使用sourcegraph，你可以以一种更加高效的方式探索GitHub的代码库。

[下载地址](https://link.zhihu.com/?target=https%3A//link.juejin.cn/%3Ftarget%3Dhttps%253A%252F%252Fchrome.google.com%252Fwebstore%252Fdetail%252Fsourcegraph%252Fdgjhfomjieaadpoljlnidmbgkdffpack%253Futm_source%253Dchrome-ntp-icon)

安装完成后点击这里

![](https://pic4.zhimg.com/80/v2-66ea2239166043392778de64da4a7aa7_720w.webp)

到了sourcegraph，网页就变成了熟悉的类似本地IDE的界面了

![](https://pic2.zhimg.com/80/v2-103954f4f38809cd0407bc108c1719f1_720w.webp)

变量定义、函数调用、代码搜索、查看文件提交记录等等功能都有，实在是太方便了

## **github-file-icon**

如果你经常访问GitHub，你可能已经注意到，GitHub上展示的文件图标相当单调，这使得不同类型的文件难以区分。但是，有一个叫做github-file-icon的插件可以帮助你解决这个问题。这个插件提供了一套非常炫酷的文件图标，使文件看起来更加直观，方便区分不同类型的文件。

不仅如此，github-file-icon还可以自动识别不同语言和框架的项目，并展示相应的图标，例如Java、Python、React等。这样，用户可以一眼识别文件类型，而无需依靠文件名后缀。  
总体而言，github-file-icon插件提供了一种更好的文件浏览体验，使你能够更好地识别和管理你的代码库。

[下载地址](https://link.zhihu.com/?target=https%3A//link.juejin.cn/%3Ftarget%3Dhttps%253A%252F%252Fchrome.google.com%252Fwebstore%252Fdetail%252Fgithub-file-icons%252Fkkokonbjllgdmblmbichgkkikhlcnekp%253Futm_source%253Dchrome-ntp-icon)

![](https://pic2.zhimg.com/80/v2-884b1580f544e8b2b424bb0c7cc8b349_720w.webp)

难能可贵的是，github-file-icon能够和Octotree完美结合

  
[https://images.soboys.cn/202305051827842.png](https://link.zhihu.com/?target=https%3A//images.soboys.cn/202305051827842.png)

![](https://pic2.zhimg.com/80/v2-6b186b51e3530d849bdfbed626c11ac5_720w.webp)

## **Git History**

git history可以让我们更优雅的查看commit历史记录，能以时间轴的方式展现代码的演进变化。选择repository中的一个文件，就能看到

![](https://pic3.zhimg.com/80/v2-0483bb5110ee48dc1daf953b3892adda_720w.webp)

![](https://pic4.zhimg.com/80/v2-32cb20947710428a435dfd45c9712ea3_720w.webp)

## **isometric-contributions**

除了上述提到的工具，在GitHub上还有一款非常有趣的Chrome扩展程序叫做Isometric Contributions。

该扩展程序可以将你每天的contributions数目转化为颜色不一的立体柱状图，并给出自己的统计数据。通过该扩展程序，每天的提交记录使用图表展示，可以让你更加直观地看到自己的贡献状况。

而针对这些数据，Isometric Contributions还会将你一年内的提交状况、最忙的一天提交数目等统计出来，使你更清楚地了解自己的工作量。在普通的Github贡献表与等距像素艺术版之间切换，每个提交的数量和次数都用图形化的方式展示，非常有趣且具有成就感。总之，这个插件可以让你更加直观地看到自己的代码贡献状况，并享受到提交记录的美好视觉呈现。

[下载地址](https://link.zhihu.com/?target=https%3A//link.juejin.cn/%3Ftarget%3Dhttps%253A%252F%252Fchrome.google.com%252Fwebstore%252Fdetail%252Fisometric-contributions%252Fmjoedlfflcchnleknnceiplgaeoegien%252Frelated%253Futm_source%253Dchrome-ntp-icon)

![](https://pic2.zhimg.com/80/v2-5d3465fe9e62d2cceef526f53e8b6b05_720w.webp)

今天给大家带来的是 **在 GitHub 上如何精准搜索的神仙技巧**。

**普通的搜索**

相信一般人搜索项目时，都是直接搜索技术栈相关的项目。

高级一点的搜索，会根据 最匹配、最多 Star 来进行排序、选择相应的语言、选择仓库或者代码来进行筛选。

  

![](https://pic1.zhimg.com/80/v2-fd101133af700070f6ff258b711b946c_720w.webp)

  

如果你只会用以上的功能，那你知道的仅仅是 GitHub 搜索的冰山一角！

GitHub 的搜索是非常强大的！下面介绍更高级的搜索技巧。

**搜索语法**

搜索 GitHub 时，你可以构建匹配特定数字和单词的查询。

**01、查询大于或小于另一个值的值**

您可以使用 `>`、`>=`、`<` 和 `<=` 搜索大于、大于等于、小于以及小于等于另一个值的值。

![](https://pic1.zhimg.com/80/v2-4be1bb2640167129d050da602c1241e4_720w.webp)

您还可以使用 范围查询 搜索大于等于或小于等于另一个值的值。

![](https://pic4.zhimg.com/80/v2-f95c7cc2a7f5d08098d6fce3b0882f37_720w.webp)

**02、查询范围之间的值**

您可以使用范围语法 `*n*..*n*` 搜索范围内的值，其中第一个数字 _n_ 是最低值，而第二个是最高值。

![](https://pic3.zhimg.com/80/v2-871143cf6940d039d66f4c5b2e2fa9be_720w.webp)

**03、查询日期**

您可以通过使用 `>`、`>=`、`<`、`<=` 和 范围查询 搜索早于或晚于另一个日期，或者位于日期范围内的日期。

日期格式必须遵循 [ISO8601]标准，即 `YYYY-MM-DD`（年-月-日）。

![](https://pic3.zhimg.com/80/v2-da367c1b87aa9f04a768c68eaf11a1e2_720w.webp)

  

您也可以在日期后添加可选的时间信息 `THH:MM:SS+00:00`，以便按小时、分钟和秒进行搜索。 这是 `T`，随后是 `HH:MM:SS`（时-分-秒）和 UTC 偏移 (`+00:00`)。

![](https://pic4.zhimg.com/80/v2-935a52a83ba982a2b1c2fd2a3007b61b_720w.webp)

**04、排除特定结果**

您可以使用 `NOT` 语法排除包含特定字词的结果。 `NOT` 运算符只能用于字符串关键词， 不适用于数字或日期。

![](https://pic4.zhimg.com/80/v2-0f1625c9431c1774b6cb39d932e7d177_720w.webp)

缩小搜索结果范围的另一种途径是排除特定的子集。 您可以为任何搜索限定符添加 `-` 前缀，以排除该限定符匹配的所有结果。

![](https://pic3.zhimg.com/80/v2-5a01db948c494fff023ce89a4602f50a_720w.webp)

**05、对带有空格的查询使用引号**

如果搜索含有空格的查询，您需要用引号将其括起来。 例如：

- [cats NOT “hello world”](https://link.zhihu.com/?target=https%3A//github.com/search%3Futf8%3D%25E2%259C%2593%26q%3Dcats%2BNOT%2B%2522hello%2Bworld%2522%26type%3DRepositories) 匹配含有 “vue” 字样但不含有 “hello world” 字样的仓库。
- [build label:“bug fix”](https://link.zhihu.com/?target=https%3A//github.com/search%3Futf8%3D%25E2%259C%2593%26q%3Dbuild%2Blabel%253A%2522bug%2Bfix%2522%26type%3DIssues) 匹配具有标签 “bug fix”、含有 “build” 字样的议题。

某些非字母数字符号（例如空格）会从引号内的代码搜索查询中删除，因此结果可能出乎意料。

**06、使用用户名的查询**

如果搜索查询包含需要用户名的限定符，例如 `user`、`actor` 或 `assignee`，您可以使用任何 GitHub 用户名指定特定人员，或使用 `@me` 指定当前用户。

![](https://pic4.zhimg.com/80/v2-7a622c54ebac3a8ecede406ef87d2137_720w.webp)

`@me` 只能与限定符一起使用，而不能用作搜索词，例如 `@me main.workflow`。

**高级的搜索**

**07、按仓库名称、说明或自述文件内容搜索**

通过 `in` 限定符，您可以将搜索限制为仓库名称、仓库说明、自述文件内容或这些的任意组合。

如果省略此限定符，则只搜索仓库名称和说明。

![](https://pic3.zhimg.com/80/v2-f672fd4e685dde8ad08b0108dc5b461a_720w.webp)

  

![](https://pic2.zhimg.com/80/v2-637f65a6bb49c1af00f3fd1f2c17c8ed_720w.webp)

  

**08、在用户或组织的仓库内搜索**

要在 `特定用户或组织` 拥有的所有仓库中搜索，您可以使用 `user` 或 `org` 限定符。

![](https://pic4.zhimg.com/80/v2-97c2ac9c5f5d99aba2dfd4474ec3003f_720w.webp)

**09、按仓库大小搜索**

`size` 限定符使用 [大于、小于和范围限定符](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/understanding-the-search-syntax) 查找匹配特定大小（以千字节为单位）的仓库。

![](https://pic2.zhimg.com/80/v2-b6cecc2e0bc0f4cb057bf3cce79c8b5d_720w.webp)

  

![](https://pic1.zhimg.com/80/v2-c8bd588bb0c733c66d6f6194f02187c8_720w.webp)

  

**10、按关注者数量搜索**

您可以使用 `followers` 限定符以及[大于、小于和范围限定符](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/understanding-the-search-syntax)基于仓库拥有的关注者数量过滤仓库。

![](https://pic2.zhimg.com/80/v2-2ac9188442d21f9ab171d93f268d1aad_720w.webp)

  

![](https://pic4.zhimg.com/80/v2-ee6fd8a6cffe1330efba08b761258c1b_720w.webp)

  

![](https://pic4.zhimg.com/80/v2-d2f7a14b3f29d3d7bec78f3864744ea3_720w.webp)

  

**11、按复刻数量搜索**

`forks` 限定符使用[大于、小于和范围限定符](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/understanding-the-search-syntax)指定仓库应具有的复刻数量。

![](https://pic4.zhimg.com/80/v2-59a2e3b068a527a01b427da2f6f9dfeb_720w.webp)

  

![](https://pic1.zhimg.com/80/v2-2d455b6bc5a8aa54dc8ba6a1be98a7f8_720w.webp)

  

**12、按星号数量搜索**

您可以使用 [大于、小于和范围限定符](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/understanding-the-search-syntax) 基于仓库具有的 [星标](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/saving-repositories-with-stars) 数量搜索仓库

![](https://pic4.zhimg.com/80/v2-759812b880f68bd843e454b2ce3b2a43_720w.webp)

  

![](https://pic4.zhimg.com/80/v2-2e6d19bcda6daa2f9d6b6e4d3b257a4f_720w.webp)

  

**13、按仓库创建或上次更新时间搜索**

你可以基于创建时间或上次更新时间过滤仓库。

- 对于仓库创建，您可以使用 `created` 限定符；
- 要了解仓库上次更新的时间，您要使用 `pushed` 限定符。 `pushed` 限定符将返回仓库列表，按仓库中任意分支上最近进行的提交排序。

两者均采用日期作为参数。 日期格式必须遵循 ISO8601 标准，即 `YYYY-MM-DD`（年-月-日）。

也可以在日期后添加可选的时间信息 `THH:MM:SS+00:00`，以便按小时、分钟和秒进行搜索。 这是 `T`，随后是 `HH:MM:SS`（时-分-秒）和 UTC 偏移 (`+00:00`)。

日期支持 `大于、小于和范围限定符`。

  

![](https://pic2.zhimg.com/80/v2-514a3d0ac391f684aba61c9e91421d79_720w.webp)

  

![](https://pic1.zhimg.com/80/v2-8297c2ab7201c1177b0d74c2b9d4f6d8_720w.webp)

  

**14、按语言搜索**

您可以基于其编写采用的主要语言搜索仓库。

![](https://pic4.zhimg.com/80/v2-86083f9242bdfd9d7d7b3e0f3e488047_720w.webp)

![](https://pic4.zhimg.com/80/v2-061264399ec4a57a449e38b2f3f0080f_720w.webp)

  

**15、按主题搜索**

您可以查找归类为特定 [主题](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/classifying-your-repository-with-topics) 的所有仓库。

![](https://pic1.zhimg.com/80/v2-07fd54d9bda02d40c17ee87f5322bfb0_720w.webp)

  

估计又有很多人不知道 GitHub 上有话题一说的吧。

![](https://pic1.zhimg.com/80/v2-b36a3e371858b126e50fab50140a3900_720w.webp)

![](https://pic4.zhimg.com/80/v2-143254922fb9c133a4bfec06edbd97d7_720w.webp)

  

**16、按主题数量搜索**

您可以使用 `topics` 限定符以及 [大于、小于和范围限定符]按应用于仓库的 [主题] 数量搜索仓库。

![](https://pic2.zhimg.com/80/v2-d14ab54acfdc4b30e3c092bcab6ccf29_720w.webp)

  

![](https://pic2.zhimg.com/80/v2-d8bc0c54f7aefb481ab4d557006bb95d_720w.webp)

  

**17、使用可视界面搜索**

还可以使用 [search](https://link.zhihu.com/?target=https%3A//github.com/search) page 或 [advanced search](https://link.zhihu.com/?target=https%3A//github.com/search/advanced) page 搜索 GitHub 哦。

这种搜索方式，估计就更少人知道了吧。

[advanced search](https://link.zhihu.com/?target=https%3A//github.com/search/advanced) page 提供用于构建搜索查询的可视界面。

您可以按各种因素过滤搜索，例如仓库具有的星标数或复刻数。 在填写高级搜索字段时，您的查询将在顶部搜索栏中自动构建。

  

![动图封面](https://pic4.zhimg.com/v2-c107760f53fb2b4f3de3847f7cbb297f_b.jpg)

  

**18、按许可搜索**

您可以按其[许可](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/licensing-a-repository)搜索仓库。 您必须使用[许可关键词](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/licensing-a-repository/%23searching-github-by-license-type)按特定许可或许可系列过滤仓库。

![](https://pic3.zhimg.com/80/v2-71be025d6824c11554ee07e726970c76_720w.webp)

  

**19、按公共或私有仓库搜索**

您可以基于仓库是公共还是私有来过滤搜索。

![](https://pic3.zhimg.com/80/v2-2fab0c9e92271b0041e57bf0ad1372ca_720w.webp)

  

**20、按公共或私有仓库搜索**

您可以根据仓库是否为镜像以及托管于其他位置托管来搜索它们。

![](https://pic4.zhimg.com/80/v2-446f5b93e03a4c98c33ecbdb90db033f_720w.webp)

**21、基于仓库是否已存档搜索**

你可以基于仓库是否[已存档](https://link.zhihu.com/?target=https%3A//docs.github.com/cn/free-pro-team%40latest/articles/about-archiving-repositories)来搜索仓库。

![](https://pic4.zhimg.com/80/v2-d2e9a94eb93d1fe3dccbfe6272c3b5b7_720w.webp)

基于具有 `good first issue` 或 `help wanted` 标签的议题数量搜索

您可以使用限定符 `help-wanted-issues:>n` 和 `good-first-issues:>n` 搜索具有最少数量标签为 `help-wanted` 或 `good-first-issue` 议题的仓库。

![](https://pic1.zhimg.com/80/v2-896794de508f90d1faf56ff526df3d0c_720w.webp)

**学习**

其实，以上很多内容的都是来自于 GitHub 的官方文档，如果你还想学习更多技巧，请看

[GitHub 官方文档](https://link.zhihu.com/?target=https%3A//docs.github.com/cn) : [https://docs.github.com/cn](https://link.zhihu.com/?target=https%3A//docs.github.com/cn)

  

![](https://pic1.zhimg.com/80/v2-78639ae4c1b2320fb85f85a7d12fa240_720w.webp)

  

![](https://pic4.zhimg.com/80/v2-8e6c5147ddf1196943063096d48ce887_720w.webp)

  

觉得有用 ？喜欢就收藏，顺便点个赞吧，你的支持是我最大的鼓励！

---

优质文章传送门：

[慕课网：【良心推荐】一招搞定GitHub下载加速！5 赞同 · 1 评论文章![](https://pic1.zhimg.com/v2-6fe0df02fb49f502a259929dad5987ec_180x120.jpg)](https://zhuanlan.zhihu.com/p/347159788)

[慕课网：程序员如何阅读源码？（初级前端必看）7 赞同 · 0 评论文章![](https://pic3.zhimg.com/v2-7db24b9288bd166f509a31402056347e_180x120.jpg)](https://zhuanlan.zhihu.com/p/346842794)

[慕课网：没用过这些IDEA插件？怪不得写代码头疼121 赞同 · 5 评论文章![](https://pic4.zhimg.com/v2-0a8826e777be212be482fe1b23a0d15f_180x120.jpg)](https://zhuanlan.zhihu.com/p/342900760)

作者：天明夜尽

链接：[https://www.imooc.com/article/313250](https://link.zhihu.com/?target=https%3A//www.imooc.com/article/313250)

来源：慕课网

本文原创发布于慕课网 ，转载请注明出处，谢谢合作