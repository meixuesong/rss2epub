Google Reader虽然灭亡了，但读书人的情怀却不曾消亡。[RSS2EPUB](http://rss2epub.appspot.com)将您的RSS订阅转换成EPUB电子书，并每天定时推送至您的邮箱。让您轻松在Kindle、多看等EPUB阅读器上享受阅读的乐趣。

![image](http://blog.ubone.com/myresource/images/kindle_rss2epub.png)

Kindle安装多看客户端后，也可以阅读Epub格式的电子书。
	
您可以通过[http://rss2epub.appspot.com](http://rss2epub.appspot.com)进行订阅设置。如果您无法访问此网站，请使用邮件进行订阅。

##邮件订阅方法
通过邮件订阅非常简单。您只需写一封邮件发送至邮箱：ebook@rss2epub.appspotmail.com。

订阅邮件的正文可以简单到只有数行：

```
昵称：读书人
推送邮箱：myemail@foo.com

书名：酷壳
订阅：http://coolshell.cn/feed
```

上面的信息足以为您建立一个帐户，并创建一本自己的电子书。当然，我相信你还会想要更个性化的定制：

```
#帐户信息设置
昵称：读书人
推送邮箱：myemail@foo.com

#您最多可以有三本电子书。

书名：InfoQ China
文件名：InfoQ.epub
#每天23点推送
推送时间：23
#一本书最多包括3个RSS
#每个RSS订阅您还可以为其设置标题，它会成为书的一级目录，而二级目录就是其中的每篇文章。
订阅：InfoQ新闻，http://foo2.com/rss
订阅：InfoQ文章，http://foo3.com/rss

书名：我的第二本电子书
文件名：我的第二本电子书.epub
推送时间：7
订阅：http://foo4.com/rss
订阅：http://foo5.com/rss
订阅：http://foo6.com/rss

#如果书名与已有书名相同，系统会进行修改操作。

#您可以删除已有的电子书，只需在删除后面加上书名。
删除：我的第三本电子书

#对于书名和文件名，加上日期(%yyyy-MM-dd%，最终会被解释为年-月-日)也许更容易区别，例如：
书名：我的第一本电子书%yyyy-MM-dd%
```

系统并不要求您的邮件必须包括完整的账户和电子书信息。您可以任意组合，例如一封邮件设置帐户信息，另一封邮件建一本电子书，第三封邮件删除一本书。

您的电子书将通过邮件服务器发送，如果某个时间点的电子书订阅用户太多，邮件可能需要多飞一会。超过10M的电子书将无法起飞。如果您发现电子书的排版不理想，请发送邮件至：format@rss2epub.appspotmail.com。如果您在使用过程中有任何意见或建议，请随时告诉我们：ubone.com@gmail.com
