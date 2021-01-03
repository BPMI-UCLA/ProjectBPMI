# ProjectBPMI

### 声明
这个repo是为了维护BPMI UCLA官方网站所有内容而创建的。网站建设基于[Hugo](https://gohugo.io)建站框架，模版以[Portio](https://themes.gohugo.io/portio-hugo/)为原型进行的魔改，以适应社团网站需要。

需要了解Hugo和Portio主题更多特性请访问其官网。

### 快速开始

**这篇文档可以教会你如何更新Post以及发布网站更新内容，欲要修改其他内容请来微信群喊一声**

假设你已经按照[Hugo官方快速开始教程](https://gohugo.io/getting-started/quick-start/)安装了Hugo在本机，第一步先选择合适的位置下载本Repo：

```
git clone https://github.com/BPMI-UCLA/ProjectBPMI.git
```
下载完成之后，使用Terminal进入这个文件夹

```
cd [刚才的下载路径]
cd ProjectBPMI
```

这个时候，运行指令`hugo`会自动根据现有内容发布静态网站到`./public`文件夹，届时可以把该文件夹内容push到隔壁repo上，完成网站发布。

### 更新文章
由于Hugo的限制（便利），所有文章均以Markdown格式文档保存使用，文件内容在`ProjectBPMI/content/posts`。

创建新文章，可以使用Hugo自带指令实现（记得查看当前路径是否在ProjectBPMI中），注意文件标题不得存在除`-`以外的任何特殊符号。
```
hugo new content/posts/title-of-your-new-post.md
```
此时，一个新的Markdown文件就被创建完成。使用你喜欢的文本编辑器进行编辑该文件。

值得注意的是，每一篇文章的文件开头会有类似这样的一段代码，除`draft`外的项目都不可缺失，新文档会缺少图片信息，请根据以下模版补充进去。

```
---
title: "Article Title"
date: 2021-01-02T19:45:05-08:00
featureImage: images/folder/pic.jpg
postImage: images/folder/another-pic.png
draft: true
---
```

其中，`title`决定文章标题；`date`是文章发布时间，注意：**如果是未来的时间，网站生成时不会有该文章**；
`featureImage`为预览图，尺寸为宽320，高370（可等比例缩放）注意：**预览图为必须插入的内容，不然无法显示文章**，`postImage`是文章内开头插图，任意大小，推荐使用横版；
`draft`为文章发布状态，设置true则保存为草稿，不会发布（可使用此功能实现历史文章隐藏），否则设置为false或者删除该行来实现发布。

图片均保存在`ProjectBPMI/static/images`，可以自行创建文件夹在images保存需要的图片，使用图片路径的时候只需从`images/`开始写即可，例如现有一张图片名为`a.jpg`保存在`static/images/img/a.jpg`，
使用图片仅需指明路径为`images/img/a.jpg`即可

### 之后呢？

使用`hugo`生成新的静态网站到public，然后进入public文件夹
```
git add .
git commit -m "Your commit message"
git push
```
过一分钟左右，新的网站内容就会被发布在 bpmi-ucla.github.com
