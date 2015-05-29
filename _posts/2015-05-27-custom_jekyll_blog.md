---
layout : post
title : "定制自己的Jekyll博客"
category : Hive
date : 2015-05-27 16:52:34
tags : [blog]
---


Jekyll中文官网：http://jekyllcn.com/

#初始化Blog

首先需要安装 ==ruby==。
>可以切换ruby的gem源，直接使用国外的gem源很慢

然后在命令行初始化一个Blog

```bash

$ gem install jekyll            #安装jekyll
$ jekyll new my-awesome-site    #初始化一个新的blog
$ cd my-awesome-site
~/my-awesome-site 
$ jekyll serve                  #在本地启动blog服务
# => Now browse to http://localhost:4000
```

#基础配置

##基础目录结构

http://jekyllcn.com/docs/structure/

一个基本的 Jekyll 网站的目录结构一般是像这样的：

```
.
├── _config.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.textile
|   └── on-simplicity-in-technology.markdown
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
|   └── 2009-04-26-barcamp-boston-4-roundup.textile
├── _site
└── index.html
```

##修改_config.yml


#插件安装
在主目录下新建一个目录 `_plugins`

##文章目录插件 jekyll-toc-generator
Github：https://github.com/dafi/jekyll-toc-generator


##语法高亮插件 SyntaxHighlighter
主页：http://alexgorbatchev.com/SyntaxHighlighter/
GitHub：https://github.com/alexgorbatchev/SyntaxHighlighter  

参考：
http://alfred-sun.github.io/blog/2014/12/15/Use-Syntaxhighlighter-for-Jekyll/


##归档插件 类别分类&时间归档
GitHub：https://github.com/shigeya/jekyll-category-archive-plugin
GitHub：https://github.com/shigeya/jekyll-monthly-archive-plugin

插件使用 Ruby 写成，放在 `_plugins` 目录下，有些 Jekyll 没有的功能，又不能 手动添加，因为页面的内容会随着文章日期类别的不同而不同，例如**分类功能**和**归档功能**， 这时，就需要使用插件自动生成一些页面和目录。

1. 分类 我的分类插件使用的是 jekyll-category-archive-plugin, 它会根据网站文章的分类信息，为每个类别生成一个页面。
使用方法是，把 plugins/categoryarchive_plugin.rb 放在 plugins 目录下， 把 _layouts/categoryarchive.html 放在 layouts 目录下， 这样，这个插件会在Jekyll解析网站时，生成相应categories目录，目录下是各个分类， 每个分类下都有一个 index.html 文件，这个文件是根据模板文件 `categoryarchive.html` 生成的，例如：

```ruby
_site/categories/
├── 工具
│   └── index.html
├── 思想
│   └── index.html
├── 技术
│   └── index.html
└── 源代码阅读
    └── index.html
```

然后，你就可以通过 http://username.github.io/blog/categories/工具/ 访问 工具类下的 index.html 文件。

2. 归档 我的归档插件使用的是 jekyll-monthly-archive-plugin,它会根据网站 _posts目录下的文章日期，为每个月生成一个页面。
使用方法同上。注意，这个插件在 jekyll-1.4.2 中可能会出错，在 jekyll-1.2.0 中没有错误。

#参考

1. http://blog.csdn.net/on_1y/article/details/19259435


