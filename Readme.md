---

Title: 关于 FarBox 模板 GrayshadeM 的使用说明
Date: 2013-07-13 10:28
Tags: FarBox 主题 模板 说明文档

---

#关于 FarBox 模板 GrayshadeM 的使用说明

搬迁到 FarBox 后，一直想自己做个模板，奈何一直没有时间。  
近日看到 [Rock](http://rock.farbox.com/ "Rock 的博客") 制作的从 Octopress 模板 [Greyshade](http://shashankmehta.in/archive/2012/greyshade.html "Octopress 模板： Greyshade") 移植过来的 FarBox 模板，甚是喜爱，但发现有不少地方不方便自定义，幸好 Rock 提供了模板代码([GitHub](https://github.com/roccox/farbox_temp.git "Rock 从 Octopress 移植的 Greyshade 主题")),于是 Clone 一份，于 2013年07月12日 晚上开始修改，听着 豆瓣FM 的 [程序猿之音](http://douban.fm/?cid=1001343 "豆瓣FM - 程序猿之音") ，学习 FarBox 主题的制作文档，大约折腾了三个多小时，在次日凌晨 2 点多时完成初版，将其命名为 GrayshadeM 。

##模板功能说明

- 页面宽度自适应，兼容移动设备，如 iPad 、 iPhone
- 自动识别 links.md 、 about.md 为 Links 与 About 页面
- 文章与照片页面，自动识别 comment_js.md 的第三方社交评论或者用 FarBox 的评论系统

##网站自定义参数配置

如果需要修改本模板的自定义项，需要在网站目录（比如 `FarBox/My Blog/` ）下放置一个名为 `site.md` 的文件，如下是一个范例：

    title: IF404
    subtitle: 折腾模板的地方
    author: 枫叶向风
    authorinfo: 枫叶向风：手艺人、爱喵可是老婆不让养、已婚胖子、业余作家、伪程序员、技术不算太宅、在光明的迷途中寻找出路
    somethingtitle: 一些说明
    something: 可自定义统计代码、Gravatar头像和一些社交链接。
    gravatar: your@email.com
    facebook: http://facebook.com
    google: http://plus.google.com
    twitter: http://twitter.com
    github: http://github.com
    linkedin: http://linkedin.com
    pinterest: http://pinterest.com
    delicious: http://delicious.com
    pinboard: http://pinboard.com
    instagram: http://instagram.com
    weibo: http://weibo.com
    qq: http://t.qq.com
    douban: http://douban.com
    fanfou: http://fanfou.com
    zhihu: http://zhihu.com
    rss: /feed
    analytics: <script type="text/javascript">var _gaq=_gaq||[];_gaq.push(['_setAccount','UA-xxxxxxx-x']);_gaq.push(['_trackPageview']);(function(){var ga=document.createElement('script');ga.type='text/javascript';ga.async=true;ga.src=('https:'==document.location.protocol?'https://ssl':'http://www')+'.google-analytics.com/ga.js';var s=document.getElementsByTagName('script')[0];s.parentNode.insertBefore(ga,s)})();</script>

格式说明：

**title**
> 添加该属性，网站左侧将显示博客名称。

**subtitle**
> 添加该属性，网站左侧博客名称下方将显示网站副标题。

**author**
> 添加该属性，网站底部将显示版权信息，包含作者笔名。

**authorinfo**
> 添加该属性，网站左侧将显示作者自我介绍。

**somethingtitle**
> 添加该属性，网站左侧将显示补充描述文字的标题。

**something**
> 添加该属性，网站左侧将显示补充描述文字，建议不要太长。注意：只有该属性存在时， `somethingtitle` 才能显示。

**gravatar**
> 添加该属性，填入在 Gravatar 注册的邮箱，将显示作者的 Gravatar 头像。

**社交链接**
> 目前支持 Facebook、Google+、Twitter、GitHub、Linkedin、Pinterest、Delicious、Pinboard、Instagram、新浪微博、腾讯微博、豆瓣、饭否、知乎、RSS订阅 。对应属性请参考上面的范例。  
> 默认显示为不同颜色圆形图案，如果要显示 Logo ，可在博客文件夹中新建 `\images\social\` 文件夹，放入和属性相同名字的 png 文件，注意图片尺寸不要超过 30x30 。我已存放一份在 GitHub 中，显示效果可以参考我的[主题折腾专用博客](http://if404template.farbox.com/ "IF404主题折腾专用博客")。

**统计代码**
> 添加 `analytics` 属性，将统计代码**压缩成一行**放入。

**关于网站的 Favicon 图标**
> 如果要添加自定义的 Favicon 图标，请直接将 `favicon.png` 文件放在根目录下。

##文章自定义属性

**Link属性**
> 格式： `Link: http://www.google.com`  
> 文章头部加入 `Link` 属性后，在首页、存档等页面中，该文章标题前会出现“[链接]”标记，点击标题链接将访问自定义的链接，而不是访问该文章内容页，右下角的“阅读全文”也会变成“访问链接”。  
> 该功能相当于轻博客中的“链接”。

**Url属性**
> 格式： `Url: a-link`  
> 文章头部加入 `Url` 属性后，可自定义该文章访问链接地址，比如文章 `a-url-link.md` 的默认访问链接为 `xxx.farbox.com/post/a-url-link` ，添加该属性后变成 `xxx.farbox.com/post/a-link` 。

##其他功能
**独立文件 isaid.md**

有时候想说些话，但单独新建个文件的话日子久了文件会变很多，于是我做了个独立文件 `isaid.md` ，每次想吐槽什么或者发一句话内容，就更新到这个文件中。另外，也可以直接放入微博秀代码。下面是使用方法：
> 在根目录新建一个 `isaid.md` 文件。头部主要属性包括：`title`、`status`  
> `title` 属性将决定网站左侧导航栏的地方显示什么文字，比如我设置 `title: 闲言碎语` ，左侧即可显示“闲言碎语”。  
> `status` 属性是为了避免这个文件的内容出现在正常文章列表中，只要随便设置不等于 `public`、`secret`、`private`的值即可，比如我设置 `status: isaid` 。当然，如果你觉得没关系，这个属性可以不设置。  
> 可以直接放入微博秀的代码，比如我的[主题折腾专用博客](http://if404template.farbox.com/isaid.md)

##版本更新记录
- 2013-07-13 创建主题。
- 2013-07-14 发觉正文和标签之间太靠近了，有点怪，秉承“感觉怪就赶紧改改”的精神（病），于是在 post.thml 中两者之间加了个 `</br>` 。
- 2013-07-14 经@taresky 提醒，发现在列表页中，“下一页”没和“上一页”、“存档”水平对齐，修改 paginator.html 代码后修复成功。
- 2013-07-14 添加 FontAwesome 字体，个别地方会显示类似图片其实是字符的图案，比如“上一页”“下一页”旁边的箭头。
- 2013-07-15 发现相册整个样式排版有问题，都堆在左边了，修改了 file.html 和 file-list.html 两个文件，让相册也显示在中间了，不过样式还没调整，所以依然很难看，而且感觉探测文件和显示的逻辑上有点不对，另外找时间调整看看。目前的显示效果可以在这里查看：[模板折腾处-相册](http://if404template.farbox.com/folder/ "模板折腾处-相册")
- 2013-07-16 今天翻旧文时发现刚搬进 FarBox 时写的文章《[正式把博客搬到 Farbox](http://blog.if404.com/post/life/2013-05-22-zheng-shi-ba-bo-ke-ban-daofarbox)》中，提到要把以前以状态形式发布的内容放到一个文件中，在新主题里调用显示。加上话痨症又犯了，于是利用午休时间做了一个，期间多次犯二，在 FarBox 团队的帮助下搞清楚了。通过在根目录创建 `isaid.md` 并设定相关参数即可在左侧导航中出现相关链接。既可以隔三差五更新内容，也可以放入微博秀代码。
- 2013-07-20 修复在*分类(category.html)*和*归档(archive.html)*页面中，跳转外链的文章链接没有指向外链的 bug 。
- 2013-07-21 修复在*分类(category.html)*和*标签(tags.html)*页面中，网页标题显示有误的 bug ，感谢 @taresky 童鞋的反馈。同时将*标签(tags.html)*和*文章(post.html)*页面中的“Tags:”汉化为中文。
- 2013-07-23 修复因 *feed.html* 文件引起的在 Feedly 等订阅工具中，文章访问链接显示不全和图片无法显示的问题。