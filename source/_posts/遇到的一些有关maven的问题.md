---
title: 遇到的一些有关maven的问题
toc: true
categories: 
date: 2021-09-24 20:30:09
tags:
---

# 1.xml错误

右键文件夹➡️添加框架的支持➡️maven

不行？ pom.xml添加一个groupID

不行？偏好设置➡️构建，执行，部署➡️Compiler➡️Java Compiler➡️

![image-20201201151904235](.遇到的一些有关maven的问题/image-20201201151904235.png)

如上图，project bytecode version修改成5试试，应该就好了，不行的话改成别的数字（反正要满足等于自己的JDK）



第二天搞javax.mail时又出错了，改成这样倒是可以了⬇️

![image-20201201201634418](.遇到的一些有关maven的问题/image-20201201201634418.png)

# 2.javax.mail错误

需要去oracle下载包

然后我把pom.xml的javax.mail版本号改为与新下载的一样，但是构建后还是无法找到

然后才发现右边弹出一个蓝色正方形M,点击后就可以了。![image-20201201205050052](.遇到的一些有关maven的问题/image-20201201205050052.png)

不过出现了这个![image-20201201201739631](.遇到的一些有关maven的问题/image-20201201201739631.png)

第二天，我下载完jdk-7u80(即jdk7的某一具体版本)，打开文件-项目结构，添加下载好的1.7![image-20201202180610843](.遇到的一些有关maven的问题/image-20201202180610843.png)



然后在这里改成这样（第一行11改成1.7）![image-20201202180441501](.遇到的一些有关maven的问题/image-20201202180441501.png)



这里也改成7

![image-20201202180425456](.遇到的一些有关maven的问题/image-20201202180425456.png)

最后再是这里![image-20201202181612059](.遇到的一些有关maven的问题/image-20201202181612059.png)

和这里![image-20201202181642839](.遇到的一些有关maven的问题/image-20201202181642839.png)

然后按下![image-20201201205050052](.遇到的一些有关maven的问题/image-20201201205050052.png)



> 顺带一提，如何在hexo中加图：
>
> 见[HEXO插入图片（详细版）](https://www.jianshu.com/p/f72aaad7b852)
>
> (主要是hexo new post 博客)
