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
    qq2: http://wpa.qq.com/msgrd?v=3&uin=123456&site=qq&menu=yes
    qqqun: http://wp.qq.com/wpa/qunwpa?idkey=1234567890abcdefghijklmn
    qqqunname: QQ群名字
    weixin: 我叫微信
    douban: http://douban.com
    fanfou: http://fanfou.com
    zhihu: http://zhihu.com
    email: mailto:123@abc.com
    rss: /feed
    alipay: http://me.alipay.com/mapleobserver
	highlight: true
    analytics: <script type="text/javascript">var _gaq=_gaq||[];_gaq.push(['_setAccount','UA-xxxxxxx-x']);_gaq.push(['_trackPageview']);(function(){var ga=document.createElement('script');ga.type='text/javascript';ga.async=true;ga.src=('https:'==document.location.protocol?'https://ssl':'http://www')+'.google-analytics.com/ga.js';var s=document.getElementsByTagName('script')[0];s.parentNode.insertBefore(ga,s)})();</script>
	socialshare: <!-- JiaThis Button BEGIN --><div class="jiathis_style_24x24"><a class="jiathis_button_qzone"></a><a class="jiathis_button_tsina"></a><a class="jiathis_button_tqq"></a><a class="jiathis_button_weixin"></a><a class="jiathis_button_renren"></a><a href="http://www.jiathis.com/share" class="jiathis jiathis_txt jtico jtico_jiathis" target="_blank"></a><a class="jiathis_counter_style"></a></div><script type="text/javascript" src="http://v3.jiathis.com/code/jia.js?uid=1374815515868166" charset="utf-8"></script><!-- JiaThis Button END -->

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
> 目前支持 Facebook、Google+、Twitter、GitHub、Linkedin、Pinterest、Delicious、Pinboard、Instagram、新浪微博、腾讯微博、QQ、QQ群、微信、豆瓣、饭否、知乎、EMail、RSS订阅 。对应属性请参考上面的范例。

> 默认显示为不同颜色圆形图案，如果要显示 Logo ，可在博客文件夹中新建 `\images\social\` 文件夹，放入和属性相同名字的 png 文件，注意图片尺寸不要超过 30x30 。我已存放一份在 GitHub 中，显示效果可以参考我的[主题折腾专用博客](http://if404template.farbox.com/ "IF404主题折腾专用博客")。

**QQ社交链接 & QQ群社交链接**
> QQ社交链接属性为 `qq2` ，通过 [wp.qq.com](http://wp.qq.com/ "QQ在线状态") 获取代码，例如：  
> `<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=123456&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:123456:53" alt="点击这里给我发消息" title="点击这里给我发消息"/></a>`  
> 在属性中填入上述范例代码中的 `http://wpa.qq.com/msgrd?v=3&uin=123456&site=qq&menu=yes`  
> 该功能无法实现QQ在线离线状态的图片切换，点击社交图标即可弹出QQ对话窗口。  
> QQ群社交链接属性为 `qqqun` ，设置方法和QQ社交链接一样。  
> 另有 `qqqunname` 属性，可添加QQ群的群名称，鼠标覆盖社交图标时会显示。
> 显示效果可以参考我的[主题折腾专用博客](http://if404template.farbox.com/ "IF404主题折腾专用博客")。

**微信社交链接**
> 微信社交链接的属性为 `weixin` ，填入微信个人或者公众账号即可。  
> **务必要在 `images/social/` 文件夹中放入二维码文件，命名为 `weixinqrcode.png` ，二维码图片会被自动压缩或拉伸到 160 像素宽高的正方形图片。**  
> 鼠标覆盖微信图标时，会显示微信账号，同时*顶部作者头像会变成微信二维码图片*，移开鼠标则恢复显示头像。点击微信图标将在新窗口打开二维码图片，方便手机用户操作。  
> 显示效果可以参考我的[主题折腾专用博客](http://if404template.farbox.com/ "IF404主题折腾专用博客")。  

**支付宝付费功能**
> 通过添加 `alipay` 属性，可以在文章底部显示支付宝付款内容，网友若觉得文章有用，可以通过支付宝收款主页向博客作者付款。  
> 属性值为支付宝收款主页功能提供的链接，请通过支付宝获取，别直接填我的地址啊^_^

**代码高亮**
> 添加 `highlight` 属性，可以使文章中的代码高亮着色，属性值任意，比如 `true` 。有需要代码高亮的童鞋可以使用。
> 该功能利用 *Pygments* 功能实现，我采用的是 Pygments 的 monokai 样式，本模板控制代码高亮着色的 css 文件为 `highlight.css` 。  
> 效果参考[这里](http://if404template.farbox.com/post/fen-lei/test-highlight "代码高亮效果")。  
> 有兴趣自定义高亮样式的童鞋可以参考：  
> [Farbox 代码高亮语法](https://github.com/hepochen/FarBox-Doc/blob/master/docs/%E4%B9%A6%E5%86%99/%E4%BB%A3%E7%A0%81%E9%AB%98%E4%BA%AE.md "FarBox 代码高亮语法")
> [Pygments 代码高亮样式](http://pygments.org/ "Pygments 代码高亮样式")
> [Pygments CSS文件](https://github.com/richleland/pygments-css "Pygments CSS文件")

**统计代码**
> 添加 `analytics` 属性，将统计代码 **压缩成一行** 放入。

**社交分享按钮**
> 添加 `socialshare` 属性，将 JiaThis 等社交分享按钮的代码 **压缩成一行** 放入。

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
- 2013-07-14 发觉正文和标签之间太靠近了，有点怪，秉承“感觉怪就赶紧改改”的精神（病），于是在 post.html 中两者之间加了个 `</br>` 。
- 2013-07-14 经@taresky 提醒，发现在列表页中，“下一页”没和“上一页”、“存档”水平对齐，修改 paginator.html 代码后修复成功。
- 2013-07-14 添加 FontAwesome 字体，个别地方会显示类似图片其实是字符的图案，比如“上一页”“下一页”旁边的箭头。
- 2013-07-15 发现相册整个样式排版有问题，都堆在左边了，修改了 file.html 和 file-list.html 两个文件，让相册也显示在中间了，不过样式还没调整，所以依然很难看，而且感觉探测文件和显示的逻辑上有点不对，另外找时间调整看看。目前的显示效果可以在这里查看：[模板折腾处-相册](http://if404template.farbox.com/folder/ "模板折腾处-相册")
- 2013-07-16 今天翻旧文时发现刚搬进 FarBox 时写的文章《[正式把博客搬到 Farbox](http://blog.if404.com/post/life/2013-05-22-zheng-shi-ba-bo-ke-ban-daofarbox)》中，提到要把以前以状态形式发布的内容放到一个文件中，在新主题里调用显示。加上话痨症又犯了，于是利用午休时间做了一个，期间多次犯二，在 FarBox 团队的帮助下搞清楚了。通过在根目录创建 `isaid.md` 并设定相关参数即可在左侧导航中出现相关链接。既可以隔三差五更新内容，也可以放入微博秀代码。
- 2013-07-20 修复在*分类(category.html)*和*归档(archive.html)*页面中，跳转外链的文章链接没有指向外链的 bug 。
- 2013-07-21 修复在*分类(category.html)*和*标签(tags.html)*页面中，网页标题显示有误的 bug ，感谢 @taresky 童鞋的反馈。同时将*标签(tags.html)*和*文章(post.html)*页面中的“Tags:”汉化为中文。
- 2013-07-23 修复因 *feed.html* 文件引起的在 Feedly 等订阅工具中，文章访问链接显示不全和图片无法显示的问题。
- 2013-07-26 修改 *post.html* 文件，方便用户通过在 *site.md* 中加入 `socialshare` 属性，添加 JiaThis 等社交分享按钮。
- 2013-07-28 个别用户和基友反馈需要QQ在线状态、邮箱和微信社交链接，于是有了，顺手多了个QQ群，虽然我想应该没几个FarBox用户会用到这个。折腾一晚上，最后让微信二维码显示在顶部作者头像的地方。涉及文件：*base.html*、*screen.css*。显示效果可以参考我的[主题折腾专用博客](http://if404template.farbox.com/ "IF404主题折腾专用博客")。
- 2013-07-28 修改 *post.html* ，增加通过支付宝付费支持作者的功能。
- 2013-08-01 修改存档页面(*archive.html*），使文章按照年份和月份倒序排列，之前是年份正序，月份倒序，略别扭。
- 2013-08-01 在 *base.html* 增加 *highlight.css* 样式控制代码，通过 *site.md* 可控制文章中的代码是否高亮显示。顺便修改了一下 `pre` 样式（*screen.css*）的背景色(#282722)和字体颜色(#fff)。
- 2013-08-03 增加 Fancybox 特效，点击文中图片链接和相册图片时会以灯箱模式浏览图片。文章中的图片需要带有图片链接才有效果。效果可参考：[一次有点蛋疼的Kindle PaperWhite购买经历](http://blog.if404.com/post/life/2013-04-03-yi-ci-you-dian-dan-teng-dekindlepaperwhite-gou-mai-jing-li)