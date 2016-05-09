#《写给技术小白的HTML初级教程》

##认识HTML

在这里先认识一下什么是HTML，HT意思超文本，“超文本”就是指页面可以包含图片、链接，甚至音乐等非文字元素。

ML意思标记语言，那什么又是标记语言？为了避免复杂，小编暂时不解释，你理解为html语法就行。

##小编对HTML的看法

对于那些程序员来说，学习HTML很容易上手。其实没有任何编程基础的人也能很快掌握HTML。HTML使用标记设置网页的显示内容，没有涉及到复杂的语法和算法，只是标记的单个使用，综合使用。总之，对自己要有信心。

##用什么编辑HTML

可以用记事本写，将扩展名改为.html就行，也可使用.htm，这是最简单的一种。

也可以用html的编辑工具

Aptana代码提示工具，下载链接地址[http://www.aptana.com/](http://www.aptana.com/)

Dreamweaver网页开发工具，下载链接地址[http://rj.baidu.com/soft/detail/24405.html?ald](http://rj.baidu.com/soft/detail/24405.html?ald)

小编目前用的Dreamweaver（你可以先在记事本里写）

##HTML标记的组成

HTML用于描述功能的符号称为“标记”，标记在使用时必须用尖括号“<>”括起来，并且是成对出现，无斜杠的标记表示该标记的作用开始，有斜杠的标记表示该标记的作用结束。

HTML的基本格式如下

	    <html>
             <head>
                  <title>无标题文档</title>
             </head>
             <body>
             <!--注解：下面是网页体的正文-->
             ...     
             </body>
	    </html>

【代码解释】 `<html></html>`表示HTML语言，在`<html></html>`里包含头部`<head></head>`和内容体`<body></body>`。主题标记`<title></title>`是在头部`<head></head>`里面的。`<!--注释-->`是注释，对程序没影响，方便别人知道你写的是什么，方便修改。

##编写HTML

大多数的书上讲解HTML都是将标记单个来讲，这样处理的缺点是没有将各标记联系起来，缺乏综合应用，并且单个讲解不容易记住。小编可能要以另外一种方式讲解了，让没有任何编程基础的人能够快速学会一些基本标记，还能综合应用。所以，你应该掌握一种学习方式，就是模仿。但也不能一直模仿下去，模仿之后还要对代码一句一句的分析，弄清楚这句到底是干什么的，可不可以用其他的方式代替。

###例一：

在网页中显示效果如下：

![图片](http://i12.tietuku.com/5d4b51e5c0b87122.png)

分析：需要完成的任务是，文章中有一个标题，标题居中；第一集，文字显示红色大体；文中有些字是大写，粗体，斜体，有下划线；有一个观看视频的链接；有图片，图片居中。

那么需要完成的任务是

* 有一个标题，标题居中
* “第一集三个字”红色大写
* 有一个段落，段落开头有缩进
* 段落中文字有大写，粗体，斜体，下划线
* 观看视频的链接
* 有一个居中的图片

*代码实现如下

        <html>
             <head>
                  <title>芈月传剧集介绍</title
             </head>
             <body>          <h1>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;芈月传</h1> 
             <p><font size="6" color="red">第1集</font><br>
             &nbsp;&nbsp;公元前338年，<b>秦孝公</b>二十四年，<i>秦惠文王</i>下令逮捕<u>商鞅</u>，施以车裂之刑。时值楚威王二年，太史令唐昧夜观星象，发现霸星，急报威王。.....</p>
             <a href="http://www.letv.com/ptv/vplay/24093058.html?ch=baidu_ald">观看视频</a>
             <p align="center"><img src="images/芈月传.jpg" width="811" height="423" /></p>
             </body>
       </html>

看到代码，你可能有些头晕，不知所云，没关系，看下面的讲解

*代码中用到的标记：

标题标记：一共有六种标题标签，如下，从数字1到数字6，标题大小排列从小到大

`<h1></h1>`

`<h2></h2>`

`<h3></h3>`

`<h4></h4>`

`<h5></h5>`

`<h6></h6>`

段落标记：设置段落，段落之后自动换行。可以设置属性align="center"使段落居中。

`<p></p>`

换行标记：`<br>`单个使用

字体标记：在属性中设置字体的大小、颜色

`<font></font>`

粗体标记：`<b></b>`

斜体标记：`<i></i>`

下划线标记：`<u></u>`

文字链接：#为链接的地址

`<a href="#">点击我</a>`

插入图片：src为图片的路径

`<img src="images/#.jpg">`

你可能会发现，代码中有大量的“`&nbsp;`”，解释一下，HTML中输入多个空格是不能显示出来的，只会显示一个空格，但需要显示多个空格怎么办，采用HTML符号，“`&nbsp;`”就代表空格。（它的用处很大，比如你想在一行中的某处显示文字，用“`&nbsp;`”进行调整，段首缩进用两个“`&nbsp;`”等）

在此提供一个标记学习的链接 [HTML标记速查学习](http://www.w3school.com.cn/tags/index.asp  "HTML") 不懂的标记去此处查看，还可以在线测试哦

注意：标记可以嵌套使用，但是不能交叉使用。

现在你再去看上面的代码，是不是明白了？你可以模仿做一些其他的例子了，一定要自己多试试，多试几遍，你就懂得其中的套路了。最开始代码一定要自己写，不要直接复制粘贴。

###例二：

做(仿)百度的首页

看到这个题目你一定是吓住了，认为自己怎么能学会那么难的任务，现在跟着我的步骤往下看，到最后会有惊喜的。

页面显示效果如下：

![图片](http://i12.tietuku.com/1baaf11cec9c5de4.png)

下面分步完成代码

第一步：页面第一行有几个靠右的链接，例一讲了文字链接，照猫画虎就行

	    <html>
             <head>
                  <title>百度一下，你就知道</title
             </head>
             <body> 
                <a href="http://www.nuomi.com/?cid=002540">糯米</a>    
                <a href="http://news.baidu.com/">新闻</a>
				<a href="https://www.hao123.com/">hao123</a>
				<a href="http://map.baidu.com/">地图</a>
				<a href="http://v.baidu.com/">视频</a>
				<a href="http://tieba.baidu.com/">贴吧</a>
				<a href="#">登录</a>
				<a href="#">设置</a>     
			 </body>
	    </html>

显示效果如图所示
![图片](http://i5.tietuku.com/be701945de835b3a.png)

仔细一看你会发现问题，链接不是靠右吗？还记得例一的段落标记吗？可以将链接放在`<p></p>`里面，设置属性靠右。代码如下

	    <body> 
             <p align="right">                  <!--设置属性靠右-->
                   <a href="http://www.nuomi.com/?cid=002540">糯米</a>    
                   <a href="http://news.baidu.com/">新闻</a>
                   <a href="https://www.hao123.com/">hao123</a>
               	   <a href="http://map.baidu.com/">地图</a>
	   			   <a href="http://v.baidu.com/">视频</a>
	   			   <a href="http://tieba.baidu.com/">贴吧</a>
	  			   <a href="#">登录</a>
	   			   <a href="#">设置</a> 
             </font>
             </p>   
        </body>

显示效果如图所示

![图片](http://i12.tietuku.com/1b1eaff8aaf5cfd9.png)

第二步：往下看就是插入百度商标图片，图片居中

        <body> 
             <p align="right">                  <!--设置属性靠右-->
                   <a href="http://www.nuomi.com/?cid=002540">糯米</a>    
                   <a href="http://news.baidu.com/">新闻</a>
                   <a href="https://www.hao123.com/">hao123</a>
               	   <a href="http://map.baidu.com/">地图</a>
	   			   <a href="http://v.baidu.com/">视频</a>
	   			   <a href="http://tieba.baidu.com/">贴吧</a>
	  			   <a href="#">登录</a>
	   			   <a href="#">设置</a> 
             </p> 
             <center>
                    <img src="images/baidu.jpg"> 
             </center>   
        </body>

注意：此处图片居中用的`<center></center>`标记，对比例一中图片居中的方式。自己用两种方式尝试一下。

显示效果如图所示

![图片](http://i12.tietuku.com/91c5a18abdacf435.png)

第三步：紧接着是输入框与按钮

        <body> 
             <p align="right">                  <!--设置属性靠右-->
                   <a href="http://www.nuomi.com/?cid=002540">糯米</a>    
                   <a href="http://news.baidu.com/">新闻</a>
                   <a href="https://www.hao123.com/">hao123</a>
               	   <a href="http://map.baidu.com/">地图</a>
	   			   <a href="http://v.baidu.com/">视频</a>
	   			   <a href="http://tieba.baidu.com/">贴吧</a>
	  			   <a href="#">登录</a>
	   			   <a href="#">设置</a> 
             </p> 
             <center>
                    <img src="images/baidu.jpg"> 
             </center>
             <form action="#">
                <p align="center">
                    <input type="text" name="shuru" size="50">
                    <input type="submit" value="百度一下">
                </p>
            </form>   
        </body>

解释：`<form></form>`标记先别管，把`<input>`标记放在它里面就行。`<input>`为表单标记，可用于文本输入，密码输入，按钮等。用type来选择想要的功能。

显示效果如图所示

![图片](http://i5.tietuku.com/56cec45113accad0.png)

第四步：完成下面的链接

        <body> 
             <p align="right">                  <!--设置属性靠右-->
                   <a href="http://www.nuomi.com/?cid=002540">糯米</a>    
                   <a href="http://news.baidu.com/">新闻</a>
                   <a href="https://www.hao123.com/">hao123</a>
               	   <a href="http://map.baidu.com/">地图</a>
	   			   <a href="http://v.baidu.com/">视频</a>
	   			   <a href="http://tieba.baidu.com/">贴吧</a>
	  			   <a href="#">登录</a>
	   			   <a href="#">设置</a> 
             </p> 
             <center>
                    <img src="images/baidu.jpg"> 
             </center>
             <form action="#">
                <p align="center">
                    <input type="text" name="shuru" size="50">
                    <input type="submit" value="百度一下">
                </p>
            </form> 
            <br><br><br><br><br><br><br><br><br>
            <font color="black" size="2">
                <p><a href="https://www.baidu.com/cache/sethelp/help.html">把百度设为首页</a>    
                <a href="http://home.baidu.com/">关于百度</a>
                <a href="http://ir.baidu.com/phoenix.zhtml?c=188488&p=irol-homeprofile">About Baidu</a></p>               	
	            <p>@2015 Baidu<a href="http://www.baidu.com/duty/">使用百度前必读</a>
	            <a href="http://jianyi.baidu.com/">意见反馈</a> 京ICP证030173号</p>
            </font>  
        </body>

经过反复练习，上面的代码你应该能看懂，这里就不作解释了。

显示效果如图所示

![图片](http://i12.tietuku.com/1baaf11cec9c5de4.png)

还觉得难吗？其实很简单。到这里，你应该掌握了一些最基本的标记。













 




















