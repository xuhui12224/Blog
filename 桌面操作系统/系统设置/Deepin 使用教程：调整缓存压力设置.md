# Deepin 使用教程：调整缓存压力设置

我公司配的和个人笔记本内存都16G，内存正常讲是够用的。有时候数据量比较大的时候，会遇到内存不够。这时候需要虚拟内存（交换空间来救急）

这里要说一下，如果你电脑使用会有超大内存需求的时候，需要在安装系统时候吧deepin的交换空间（磁盘代替内存）设置的大一点。下图是我的，16g内存、16g交换空间。当然如果你没有这种需求设置成2g就可以了。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20191124011153513.png#pic_center)

deepin有个参数 **swappiness**  
swappiness的值的大小对如何使用swap分区是有着很大的联系的。swappiness=0的时候表示最大限度使用物理内存，然后才是swap空间，swappiness＝100的时候表示积极的使用swap分区，并且把内存上的数据及时的搬运到swap空间里面。deepin 的基本默认设置为10


```bash
cat /proc/sys/vm/swappiness #查询swappiness
```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20191124011417486.png#pic_center)

也就是说，你的内存在使用到100-10=90%的时候，就开始出现有交换分区的使用。大家知道，内存的速度会比磁盘快很多，这样子会加大系统IO，同时造的成大量页的换进换出，严重影响系统的性能，所以我们在操作系统层面，要尽可能使用内存，对该参数进行调整。

临时调整的方法如下，我们调成60：

```bash
sysctl vm.swappiness=60
#vm.swappiness=60 cat /proc/sys/vm/swappiness
#60
```

这只是临时调整的方法，重启后会回到默认设置的.
要想永久调整的话，需要在/etc/sysctl.conf修改，加上：

```bash
sudo vim /etc/sysctl.conf
```

加上

```bash
vm.swappiness = 60
```

生效

```bash
sudo sysctl -p
```

这样便完成修改设置！

**当然，日常设置成10使用是最快的，没事别搞成60。这是让你临时救急用的。**

---
Deepin  系列教程
[Deepin 使用教程：前言](https://blog.csdn.net/a15005784320/article/details/103083242)