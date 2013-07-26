key: FarBox-Template-GrayshadeM-2013072601
title: FarBox模板：GrayshadeM
domain: http://blog.if404.com

- 2013-07-13 创建主题
- 2013-07-14 发觉正文和标签之间太靠近了，有点怪，秉承“感觉怪就赶紧改改”的精神（病），于是在 post.thml 中两者之间加了个 `</br>` 。
- 2013-07-14 经@taresky 提醒，发现在列表页中，“下一页”没和“上一页”、“存档”水平对齐，修改 paginator.html 代码后修复成功。
- 2013-07-14 添加FontAwesome字体，个别地方会显示类似图片其实是字符的图案，比如“上一页”“下一页”旁边的箭头。
- 2013-07-15 发现相册整个样式排版有问题，都堆在左边了，修改了 file.html 和 file-list.html 两个文件，让相册也显示在中间了，不过样式还没调整，所以依然很难看，而且感觉探测文件和显示的逻辑上有点不对，另外找时间调整看看。目前的显示效果可以在这里查看：[模板折腾处-相册](http://if404template.farbox.com/folder/ "模板折腾处-相册")
- 2013-07-16 今天翻旧文时发现刚搬进 FarBox 时写的文章《[正式把博客搬到 Farbox](http://blog.if404.com/post/life/2013-05-22-zheng-shi-ba-bo-ke-ban-daofarbox)》中，提到要把以前以状态形式发布的内容放到一个文件中，在新主题里调用显示。加上话痨症又犯了，于是利用午休时间做了一个，期间多次犯二，在 FarBox 团队的帮助下搞清楚了。通过在根目录创建 `isaid.md` 并设定相关参数即可在左侧导航中出现相关链接。既可以隔三差五更新内容，也可以放入微博秀代码。
- 2013-07-20 修复在*分类(category.html)*和*归档(archive.html)*页面中，跳转外链的文章链接没有指向外链的 bug 。
- 2013-07-21 修复在*分类(category.html)*和*标签(tags.html)*页面中，网页标题显示有误的 bug ，感谢 @taresky 童鞋的反馈。同时将*标签(tags.html)*和*文章(post.html)*页面中的“Tags:”汉化为中文。
- 2013-07-23 修复因 *feed.html* 文件引起的在 Feedly 等订阅工具中，文章访问链接显示不全和图片无法显示的问题。
- 2013-07-26 修改 *post.html* 文件，方便用户通过在 *site.md* 中加入 `socialshare` 属性，添加 JiaThis 等社交分享按钮。