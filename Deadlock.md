####Deadlock
***
####一、实验截图
首先编译Deadlock.java文件，生成的文件如下：

![](http://upload-images.jianshu.io/upload_images/3239501-a2def45f8c454b31.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
然后在linux终端输入程序：

![](http://upload-images.jianshu.io/upload_images/3239501-735647eb46febfb7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
得出实验结果：

![](http://upload-images.jianshu.io/upload_images/3239501-252effc77a434201.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
可以看到大约是停在2483次，产生了死锁。

####二、产生死锁的4个必要条件
1. 互斥条件：一个资源每次只能被一个进程使用
2. 请求与保持条件：一个进程因请求资源而阻塞时，对已获得的资源保持不放
3. 不剥夺条件：进程已获得的资源，在未使用完之前，不能强行剥夺
4. 循环等待条件：若干进程之间形成一种头尾相接的循环等待资源关系

####三、产生死锁的解释
程序开始执行之后，先定义一个count实现，定义一个线程t，当执行t.start()之后，线程t被插入到调度队列里，调度到它的时候执行run里面的内容，b开始执行synchronized同步代码块，等待count之后，a也要执行synchronized，但是b在执行时其他线程的访问会被阻塞且对获得的资源保持不放，所以产生了死锁。
