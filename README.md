作为一名爱阅读的码农，RSS和Kindle是我的两个最爱。我喜欢RSS的简单和便捷，不用从这个网站跳到另一个网站，不用理会广告和弹窗。而Kindle电纸书则太美妙了，不需要Pad的超高分辨率，却带给我们纸质书般的阅读享受，既保护眼睛又拥有电子书的方便。

如果能够将两者结合起来，世界将会怎样？当你安静地靠窗坐在咖啡厅、在草坪上享受温暖的阳光或者睡前静卧于床，拿起Kindle，看看自动推送过来的RSS订阅内容，我想也是醉了。

#什么是RSS2EPUB
[RSS2EPUB](http://rss2epub.appspot.com)正是为了满足这样的阅读需求，它将您的RSS订阅内容转换成EPUB电子书，并每天定时推送至您的邮箱。让您轻松在Kindle、iBooks和多看等EPUB阅读器上享受阅读的乐趣。

![image](https://raw.githubusercontent.com/meixuesong/rss2epub/master/resource/images/rss2epub-intro.jpg)
（Kindle安装多看客户端后，也可以阅读EPUB格式的电子书。）
	
每一本EPUB电子书可以包括多个RSS订阅的内容，注意是全文内容哦！系统会根据RSS的内容自动抓取全文，然后生成电子书推送到你的邮箱。

![image](https://raw.githubusercontent.com/meixuesong/rss2epub/master/resource/images/book3rss.jpg)

# 如何使用RSS2EPUB的服务
如果你能访问[http://rss2epub.appspot.com](http://rss2epub.appspot.com)，并且有一个Google帐户，那就非常简单了。可以直接登录网站去设置“我的帐户”和创建“我的电子书”。

可是RSS2EPUB服务构建于Google App Engine（GAE），如果你从国内直接访问Google的服务时，网页是打不开的！所以另一个选项是你可以通过邮件完成订阅。其实也是很简单的。
 
##邮件订阅方法
通过邮件订阅的方法就是你发邮件给ebook@rss2epub.appspotmail.com，系统收到你的邮件后，处理完成，会回复一封邮件告诉你结果。

我们现在就开始了解怎么通过邮件订阅吧。（下面所有的内容都是说邮件正文怎么写，至于邮件主题你可以随便输。）

###建立帐户
首先你得有个自己的帐户吧，让系统知道怎么称呼你，你的推送邮箱地址是哪里。为了描述方便，假设我的昵称是“读万卷书”，我接收电子书的邮箱是：12345678@iduokan.com，为什么是这个邮箱呢？因为我使用多看客户端，这个邮箱是我的多看推送邮箱。它会自动推送到我的Kindle。

**建立帐户的邮件正文就是这样的：**

```
昵称：读万卷书

推送邮箱：12345678@iduokan.com

```

这就可以了，简单吧！现在你就可以发邮件给ebook@rss2epub.appspotmail.com，它会帮你建立帐户。如果你不着急的话，还可以写好下面的订阅内容后再发邮件。

### 电子书订阅
怎么通过邮件订阅RSS的内容，并生成电子书呢？首先你得给书取个名字，例如《科技前沿》。这本电子书会每天定时通过邮件发送给你，所以你需要定个时间，是早上8点还是晚上21点发送给你？另外电子书还得有个文件名，就叫“科技前沿.epub”吧。书的基本信息已经够了，那么书的内容从哪来呢，你得有RSS的订阅地址，例如http://www.guokr.com/rss和http://coolshell.cn/feed。

这些信息汇总起来，邮件正文就是这样的：

```

书名：科技前沿
文件名：科技前沿.epub
推送时间：21
订阅：http://www.guokr.com/rss
订阅：http://coolshell.cn/feed

```

如果你要订阅多本电子书，同样按上面的格式写到正文中就可以。每个帐户可以最多有三个电子书，每本电子书最多有三个RSS源。

好了，现在就发送邮件吧，我们的邮件看起来是这样的：

![image](https://raw.githubusercontent.com/meixuesong/rss2epub/master/resource/images/emailbook.jpg)

邮件发送成功后，稍等片刻，我们就收到了回复：

![image](https://raw.githubusercontent.com/meixuesong/rss2epub/master/resource/images/emailbookreply.jpg)

这就是订阅的全过程。每天21点，RSS2EPUB将会把最新的内容推送到你的邮箱。

### 其他操作
前面的内容已经完成了电子书的订阅，但在使用过程中，下面这些内容你可能需要了解。

**我想再增加一本电子书怎么操作？**

你再发一封邮件，正文按照电子书订阅的格式就可以。

**我想删除一本电子书怎么操作？**
假设你要删除的书名为“科技前沿”，那么发一封邮件，正文为“删除：科技前沿”就可以了。如下：

```
删除：科技前沿

```

**我想修改电子书的内容和推送时间怎么操作？**

再发一封电子书订阅的邮件，同样按照上面的格式。书名必须是你要修改的那本书名，其它内容你可以任意修改。也就是说，只要书名相同系统就认为是修改，会用新邮件的内容替换老邮件数据。

**我想要修改书名怎么操作？**

你可以先删除原书，然后再建一本电子书。

**每天都收到一本电子书，但书名都相同，不好区分怎么办？**

书名和文件名都可以包括日期，这样就可以很容易区分了。但日期是每天都变化的，怎么告诉系统使用当天的日期呢？你可以加一个变量%yyyy-MM-dd%，它会代表当天的日期。例如你可以将文件名改为：

```

书名：科技前沿
文件名：科技前沿%yyyy-MM-dd%.epub
推送时间：21
订阅：http://www.guokr.com/rss
订阅：http://coolshell.cn/feed

```

它生成的文件名就会类似于：科技前沿2014-11-01.epub, 科技前沿2014-11-02.epub。


# 后记
[sample文件夹](https://github.com/meixuesong/rss2epub/tree/master/sample)中有两本系统生成的电子书样本，你可以先一睹为快。

电子书的排版与RSS源网站有很大关系，系统并没有对所有网站进行过滤优化，因此会存在内容和排版不理想的情况。遇到这种情况你只需要发邮件给ubone.com@gmail.com，一般会很快解决。

电子书将通过邮件服务器发送，如果某个时间点的电子书订阅用户太多，邮件可能需要多飞一会。超过10M的电子书将无法起飞。

如果您在使用过程中有任何意见或建议，请随时告诉我们：ubone.com@gmail.com

请记住，电子书的订阅地址是：ebook@rss2epub.appspotmail.com

# 版权声明
电子书的内容来源于您订阅的RSS网站，版权归原网站所有。

