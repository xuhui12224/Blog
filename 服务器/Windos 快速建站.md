

---


@[TOC](Windos 快速建站)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808144912637.jpg)
大家打开浏览器直接输入118.25.63.144就可以直接访问我的个人网站了。

自从转行做软件，一直想拥有一个属于自己的博客，记录自己生活和工作。这个想法由于各种原因，被拖了一年多始终没有实现。突然觉得不要再拖延下去了了，我要来实现这个想法，以后督促自己每天写博客。

经过多方探索，最后决定使用CSDN。于是在这里一步一步搭建自己的博客平台，购买云服务器、搭建网页环境、挑选网页模板、修改然后把我在CSDN的博客贴过来。经过一番挣扎我的博客和个人网站也算初步完成。虽然没有网址只有一个公网ip（备案实在太麻烦了），虽然没有访问量,但是看着一点一点完善心里也比较欣慰。

## 1. 购买服务器
我买的腾讯云学生版服务器https://cloud.tencent.com/，不是学生的话你就想办法完成学生认证（找朋友什么的）。
之所以选择这个，当然是因为便宜了！我把腾讯云、百度云、华为云等几个大的云都免费体验了下，感觉腾讯云最傻瓜，比较适合新手，再加上学生版一年只要120就够了。
1核2gb内存1m宽带反正是够我用了，我就是建个小网站，基本上没有访问量那种，让后自己搭两个个人使用的小型的数据库。
或者你买个虚拟机，那更便宜。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808145135996.png)

买完之后就可以查看自己的公网ip，比如我的118.25.63.144。我就不打码了，我还巴不得有人可以访问我的网站呢，哈哈。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808145639599.png)
如何访问自己服务器
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808150030846.png)
当然了，我这么随意的的人  直接按下键盘win+R
输入mstsc
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808150151921.png)

输入118.25.63.144   （这是我的欢迎访问），这里需要输入上边大家看到的公网ip，让后点   显示选项  本地资源    详细信息

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808150159680.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808150334554.png)
挑一个自己的盘符，负责跟服务器共享数据

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808150344758.png)
连接完成后就登录自己的远程服务器了。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808150506985.png)


## 2. 搭建php环境
怎么搭建，最傻瓜办法  https://www.xp.cn/  phpstudy，一键安装一键使用。
这个是最新版本的，我是去年搭建的网站（就尝试了一下让后再也没管过了），用这个新版本的我看了下更傻瓜。我下边演示还是用原来的版本，我就不更新了。
自己电脑把安装包下载好，放到刚才远程操控的共享盘符，这样在服务器上就可以直接安装了。（或者你可以直接去服务器下载，就是网速很慢，谁叫没钱买的1m的宽带哈）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808150842103.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808151014107.png)
安装完就是这样了

## 3. 绑定ip
mysql选项  站点域名管理器按照下边设置   118.25.63.144  换成自己的公网ip
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808151049465.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808151056626.png)
在host文件里填入服务器ip和域名
其他选项 打开host  或者去c盘里找。


## 4. 上传网页
在网上找一个个人博客模板下载来，修改成自己介绍和文章
复制在服务器phpstudy安装目录下的PHPTutorial文件夹里www文件夹里
C:\phpStudy\PHPTutorial\WWW
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808151809856.png)
然后在其他电脑  手机  ipad  打开浏览器输入自己公网ip地址就可以访问到自己的博客了
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808152107217.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808151953512.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808152012751.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190808152033795.png)


我这里提供自己这个博客的静态html文件和几个博客模板网址
https://github.com/chinayaoxin
https://www.yangqq.com/
http://www.templatesy.com/Search/category/2
http://www.cssmoban.com/tags.asp?n=%E5%8D%9A%E5%AE%A2


## 5. 解析ip  有自己网址
需要买一个网址  几块就可以，让后自己给网址备案。差不多要一个月完成，我去年申请让后工作太忙后来就忽略了
https://console.cloud.tencent.com/beian