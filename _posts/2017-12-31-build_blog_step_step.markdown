---
layout: post
title:  "用GitHub Pages + jekyll 搭建博客"
date:   2017-12-31 10:12:11 +0800
categories: tutorial
---

最近又把博客改版了，顺便把之前的文章也删掉了（好像自己写过很多文章似的）。

之前用过几个jekyll主题，都是精挑细选的。其实还挺喜欢[Daktilo](https://github.com/kronik3r/daktilo)，既然喜欢，为什么要放弃?我也忘记了，大概看久了也会疲劳。

现在这个主题，是jekyll默认主题。其实这个主题也不是我理想中的效果，连个分类都没有，搞什么博客？连个评论都没有，搞什么博客？连个统计都没有，搞什么博客?现在很多主题都集成了这些，而且还有详细的配置说明，要想简单，找个自己喜欢的主题，配置下就ok了。然后就可以专心写博客，写博客很简单，在_posts目录下写就好了。而我之所以选择这个最简单的主题，就是想折腾一下，自己慢慢写一个有意思的主题出来。

至于怎么写主题，我现在也不太清楚，方法总是会有，不是吗？

## 静态博客
用GitHub Pages 和Jekyll 搭建的博客是静态博客，关于什么是静态博客以及为什么要使用静态博客，推荐听内核恐慌的第3期[静态网站生成器](https://kernelpanic.fm/3) ，其实听完这期应该就差不多可以去写Blog了。



## 关于GithubPage
既然使用GithubPage,就先了解为什么要使用GithubPage。[https://pages.github.com/](https://pages.github.com/) 这是GitHub Pages的官方页面。

> Websites for you and your projects. Hosted directly from your GitHub repository. Just edit, push, and your changes are live.

其实不用GitHub Pages 也行，不过用GitHub Pages 可以省很多事。很多情况是，花很多时间把博客搭建起来，然后写个Hello World 就不再写。而用GitHub Pages ,很简单，创建一个项目，只要写文章，提交，博客就会自动更新。这样就可以更加专注的写博客。

## 关于Jekyll
如果不想折腾的话，直接去[Jekyll thems ](http://jekyllthemes.org/)上找还可以的主题，按照主题的提示，克隆，修改配置文件，写文章，提交，就可以了，就这么简单。如果是选择困难症，那就多选选选呗。

我是想从头自己写个主题出来，所以就要重点看下[jekyll](https://jekyllrb.com/)咯。

> Transform your plain text into static websites and blogs.

所以jekyll的作用就是把你写的纯文本内容，转换成静态的网站和博客，转换成网站和博客后，还需要部署到服务器上，这就GitHub Pages 的作用了，不过GitHub Pages 已经集成了Jekyll。
 
用其他技术实现一个静态或动态网站，最后都会组成一个html页面，jekyll也一样，只不过用来写博客的语言简单一些，只要用标记语言写就可以了，比如markdown,HTML，然后jekyll再把文本和预先定义好的布局文件，样式和脚本组成HTML页面，所以写jekyll主题，主要是定义布局，样式和表现形式。
### jekyll快速入门
我用的是ubuntu,安装jekyll也是用的最简单的方式。

    sudo apt install jekyll 

然后再执行 

    jekyll new blog 

就可以得到一个jekyll 项目。 执行

    jekyll server  

就可以去浏览器上看博客效果了。

### jekyll 目录说明
通过```jekyll new ```生成的项目结构如下

{% highlight ruby %}
├── abount.md
├── _config.yml
├── css
|   ├── main.scss
├── feed.xml
├── _includes
|   ├── footer.html
|   └── header.html
└── index.html 
└── js
|   ├── html5shiv.js
|   ├── respond.js
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2018-01-01-welcome-to-jekyll.markdown
├── _sass
|   ├── _base.scss
|   └── _layout.scss
├── _site
{% endhighlight %}

从名字就可以看出各个文件及文件夹的作用。
- about.md 可以不要，可以写一些网站博客的介绍

- _config.yml,配置文件，很多主题主要改了这个配置文件就可以用了，内容很多，不同的主题可能有不同的配置，不必记住每个属性，也可以自定义属性。

- css 样式文件

- feed.xml 供Rss阅读器订阅。

- _includes 可重复使用的文件，比如博客的头部文件，底部文件。

{% highlight ruby %}
{ % include file.ext %}
{% endhighlight %}

- index.html 博客首页，要放在项目的根目录下，可以是markdown格式

- js JavaScript 文件

- _layouts 布局文件

- _posts 博客文件，在这个目录下写博客就可以了。

- _sass 会被组装到main.css 文件中

- _site jekyll 生成网站。

自己按这个目录结构建个同样的目录，也是可以的。比如阮一峰老师的这篇文章[搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)就是这样一步一步搭建出来的。要写主题的话，主要就是改css,_includes,index.html,js,_layouts等目录或文件。







