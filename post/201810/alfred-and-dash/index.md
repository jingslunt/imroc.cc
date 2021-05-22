---
title: "极客工具之 Alfred 与 Dash"
subtitle: "效率神器，macOS 专属"

# Date published
date: 2018-10-21T07:00:00+08:00

# Date updated
lastmod: "2018-10-21T07:00:00+08:00"

draft: false

# Show this page in the Featured widget?
featured: false

authors:
- admin

tags:
- geek
- macOS

---

{{% toc %}}


## Alfred
使用 Alfred 可以让你在 macOS 程序间自由切换、快速查找或打开文件、调起浏览器进行网页搜索、 还可以做计算器。 另外，还有许多其它搜索功能以及付费的工作流特性，Powerpack 就是 Alfred 工作流模块，需要付费才能使用，不过，我觉得免费的功能已经完全够用了， 而且很简洁，功能太多咱也学不过来。
#### 下载安装
Alfred 官网是 [https://www.alfredapp.com/](https://www.alfredapp.com/)
#### 禁用自带的 Spotlight
macOS 自带了搜索工具 Spotlight, 但是功能相对于 Alfred 就弱爆了，它默认的快捷键是 `cmd+space`，我们最好禁用它，进入 `系统偏好设置-键盘-快捷键-聚焦`，然后取消勾选 `显示“聚焦”搜索`

![alfred setting](https://res.cloudinary.com/imroc/image/upload/v1540031377/blog/geek/alfred-disable-spotlight.png)

并且将 Alfred 的热键也设为 `cmd+space`

![alfred setting](https://res.cloudinary.com/imroc/image/upload/v1540031375/blog/geek/alfred-setting.png)
#### 程序间快速切换
我们之前常用的程序切换方式有：
- cmd+tab 和 shift+cmd+tab 切换程序
- 在触摸板三根手指上滑打开调度中心，结合三根手指左右滑切换桌面，然后选择要切换的程序

它们的缺点很明显，程序窗口所在的位置不一定是固定的，需要观察一下才能找到，而且如果打开的程序非常多，找起来就更麻烦。如果用 Alfred， 则只需输入能匹配程序名称部分的简短字母就能找到（如果程序含中文名，使用拼音也能搜到)， 再按下回车就能切换到指定程序上，比如切换到 `Google Chrome`，只需要输入 `chr` 就能定位到 Chrome 浏览器。

![search app](https://res.cloudinary.com/imroc/image/upload/v1540031373/blog/geek/alfred-search-app.png)

#### 快速查找和打开文件或目录
Alfred 还支持很多指令，`find` 是在磁盘找到文件，回车后就将搜到的文件或目录显示在 Finder 中，搜索是瞬间完成的，灰常灰常快。

![aflred find](https://res.cloudinary.com/imroc/image/upload/v1540031373/blog/geek/alfred-find.png)

`open` 命令与 `find` 类似，唯一的区别是 `open` 会将文件直接通过默认的打开方式打开而不是显示在 `Finder` 中。

#### 计算器
偶尔我们需要做些数学计算，打开自带的计算器太麻烦，而且功能很弱，面对复杂的数学表达式输入显得不够直观简单，利用 Alfred 可以直接输入可读性很好的运算表达式，非常直观简单。

![aflred calculator](https://res.cloudinary.com/imroc/image/upload/v1540031373/blog/geek/alfred-calculator.png)

#### 网页搜索
没有输入命令的情况下，如果你的输入无法找到对应的程序，默认就会推荐到网页搜索

![aflred search web](https://res.cloudinary.com/imroc/image/upload/v1540031376/blog/geek/alfred-search-web.png)

你也可以一开始就指定用某个搜索引擎搜索，比如谷歌默认用的 `gg` 命令

![aflred search google](https://res.cloudinary.com/imroc/image/upload/v1540031373/blog/geek/alfred-search-google.png)

你还可以自定义搜索引擎，比如百度、淘宝、京东、Github 等，以添加 Github 为例，打开 Alfred 的 `Preferences-Features-Web Search-Add Custom Search`， 各选项填写如下：

- Search URL: https://github.com/search?q={query}
- Title: Search with Github for {query}
- Keyword: gh

![aflred custom search](https://res.cloudinary.com/imroc/image/upload/v1540031374/blog/geek/alfred-custom-search.png)

`{query}` 是会填充的搜索词变量，随便在 Github 搜索一个关键词，然后复制 url ，将搜索词替换为 `{query}` 就得到 `Search URL` 了，其它搜索引擎的 `Search URL` 也同理可得。

现在在 Alfred 中输入 `gh` 命令就可以搜索 Github 项目了，如果希望搜索的时候显示 Github 的 logo，可以自己把 logo 图片文件拖到上图设置右侧方框处。

## Dash
很多人应该都知道 Dash ，程序员看文档的神器，但其实它还有一个功能: `Snippets`，这才是我频繁使用它的原因。它可以让你不受编辑器约束，在任意可以输入的地方都快速输入代码片段或者叫做文本模板，避免重复输入，提高效率。我会举一些实际使用的例子让你知道它为什么这么爽。

#### 下载安装
Dash 的官网是 https://kapeli.com/dash

#### 确保 Dash 权限
进入 `系统偏好设置-键盘-快捷键-服务`，确保搜索下面的 `Look Up in Dash` 是勾选状态

![dash setting](https://res.cloudinary.com/imroc/image/upload/v1540031374/blog/geek/dash-setting.png)

#### 添加 Snippet
进入 Dash 的 Snippets，我们尝试添加一个，就拿我经常要输入的命令的举例

![dash snippets](https://res.cloudinary.com/imroc/image/upload/v1540031375/blog/geek/dash-snippets.png)

新建了一个名字是 `kx.` 的 `Snippet`，不管我们在哪输入了这个名字，他都会触发这个 `Snippet`，我习惯用 "." 号来触发，所以在名字默认都加了 "."

来看下使用效果

![dash demo](https://res.cloudinary.com/imroc/image/upload/v1540031374/blog/geek/dash-demo.gif)

除了方便我们快速输入常用而又冗长的命令之外，你还可以把常用的服务器 ip 也做成 `Snippet`，起个容易记得名字，这样你的服务器 ip 很多也不怕了， 不需要查服务器 ip 列表，直接输入 `Snippet` 名称。你也可以把你的公钥也做成 `Snippet`，这样就可以很方便把公钥输入到服务器的 `~/.ssh/authorized_keys` ，以便让我们不输入密码就可以登录服务器。当然你写代码的时候还可以用它来键入代码片段，不过它和 vscode 兼容性有点不好，有时会输入不想要的字符。我建议代码片段功能就用编辑器或 IDE 自带的，功能更加丰富点。

## 推荐系统快捷键
- 在 `系统偏好设置-键盘-修饰键` 把 `大写锁定键` 映射为 `Control` 键，因为 ctrl 用的实在太频繁了，自带的键盘和其它普通的键盘的 ctrl 键位不好按，像 hhkb 这种键盘的 ctrl 键本身就在普通键盘的大写锁定键位置，所以就不用映射。
- 在 `系统偏好设置-键盘-调度中心`，将 `向左移动一个空间` 快捷键绑定为 `ctrl+,`，`向右移动一个空间` 快捷键绑定为 `ctrl+.`。这样多个桌面空间之间的切换也很方便了，快捷键也不会跟其它软件冲突。


最后，我还录了一个视频供大家参考学习：

<embed src="https://imgcache.qq.com/tencentvideo_v1/playerv3/TPout.swf?max_age=86400&v=20161117&vid=f075714x4s9&auto=0" allowFullScreen="true" quality="high" width="900" height="700" align="middle" allowScriptAccess="always" type="application/x-shockwave-flash"></embed>