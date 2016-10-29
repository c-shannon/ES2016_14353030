###DOL实例分析及编程
***
####一、修改结果
1. 修改example2
![](http://upload-images.jianshu.io/upload_images/3239501-cdac28c7d5ba578c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](http://upload-images.jianshu.io/upload_images/3239501-71c3b495d01ae866.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 修改example1
![](http://upload-images.jianshu.io/upload_images/3239501-d25bbbd109ae5a60.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](http://upload-images.jianshu.io/upload_images/3239501-32c2d5e4bd72f16b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

####二、修改方法
1. 修改example2
进入dol/examples/example2文件夹中，用gedit打开example2.xml，修改value为2让3个square模块变成2个：
![](http://upload-images.jianshu.io/upload_images/3239501-5189db0fc9edca56.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 修改example1
进入dol/examples/example1/src文件夹中，用gedit打开square.c，修改i输出3次方数：
![](http://upload-images.jianshu.io/upload_images/3239501-03561be79a84b041.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

####三、实验感想
本次实验比较简单，任务也不难实现，主要是让我们对dol实例有更深层的了解和学习，由于上次实验已经编译运行过example1，所以需要删除dol/build/bin/main文件夹下的example文件夹，但是文件夹显示加锁需要修改权限：
![](http://upload-images.jianshu.io/upload_images/3239501-49a094f792604843.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
之后才能对文件夹进行删除，再重新编译运行就可以看到结果。
