---
layout: post
title: "关于搭建Octopress总结"
date: 2017-04-14 16:20:30 +0800
comments: true
categories: Octopress
---
这是我的第一篇博客，虽然功能还不太健全，但是最起码能用，后续再慢慢完善吧。已经迫不及待的发表我的第一篇博客啦～

搭建博客的初衷，不是想展示自己有多牛（PS：我还是小白一枚），只是看到大神们的博客实在养眼，便想拥有自己的博客。一方面能够对自己所学进行总结，另一方面也有助于提高自己的写作能力，我相信经过一段时间的积累，当回过头来看的时候，肯定会有很多的成就感。说白了就是自我价值的体现，我还是很喜欢这种感觉的。

好了废话不多说，第一篇文章自然是关于搭建博客过程的总结。网上已经有很多牛人的总结了，我这里只是对一些常用命令进行总结。方便后续进行查阅。

1.创建文章

`$ rake new_post\[title\]    #title为你的文章名，可随意更改`

很多博客中使用的是这个命令:rake new_post["title"]

但是我在执行时总是报错：

`zsh: no matches found: new_post[title]`

所以当我输入rake new_post时我按了tab键进行命令提示，就出来了rake new_post\[title\]这个命令，至于原因，我也不知道为什么。可能跟我用的shell有关系吧，我用的是zsh。不确定。
<!--more-->

当执行完创建文章的命令后，系统会在octopress/source/_posts目录下生成markdown文件，接下来你只要编辑这个文件就是在写一篇博客了。

`~/octopress/source/_posts (source*) $ ls
2017-04-14-guan-yu-da-jian-octopresszong-jie.markdown`

2.生成本地静态网站并进行预览

文章创建完之后，可以先进行本地预览。命令如下：

`$ rake generate`

`$ rake preview`

3.将静态网站同步至GitHub

如果你预览没问题的话，接下来就可以发布到GitHub了。

命令如下：

`$ rake deploy`

过一会，你访问自己的博客，就可以进行查看了。

4.将本地资源文件同步到 GitHub 中

如果你想将本地资源，如Markdown文件等内容，也同步至GitHub中的话，可以执行如下命令：

`$ git add .    #不要忘记后面的英文句号`

`$ git commit -m "comment"  #comment可随意更改`

`$ git push origin source`

先写到这里吧，后续再补充...
