#DOL开发环境配置
***
####一、DOL框架描述
The distributed operation layer（DOL） is  a software development framework to program parallel applications. The DOL allows to specify applications based on the Kahn process network model of computation and features a simulation engine based on SystemC. Moreover, the DOL provides an XML-based specification format to describe the implementation of a parallel applicaion on a multi-processor systems, including binding and mapping.
-DOL Application Programming Interface
-DOL Functional Simulation
-DOL Mapping Optimization 
####二、DOL安装笔记
1. 安装一些必要的环境
`$  sudo apt-get update
 $  sudo apt-get install ant
 $  sudo apt-get install openjdk-7-jdk
 $  sudo apt=get install unzip`
2. 下载文件放到虚拟机里
![](http://upload-images.jianshu.io/upload_images/3239501-72ab1d84e4156118.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)![](http://upload-images.jianshu.io/upload_images/3239501-115ea96dc86845ba.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3. 解压文件
`$  mkdir dol
 $  unzip dol_ethz.zip -d dol
 $  tar -zxvf systemc-2.3.1.tgz`
4. 编译systemc
`$  cd systemc-2.3.1
 $  mkdir objdir
 $  cd objdir
 $ ../configure CXX=g++ --disable-sync-updates`
运行结果：
![](http://upload-images.jianshu.io/upload_images/3239501-60d7b5cca83e454c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`$  sudo make install`
运行结果：
![](http://upload-images.jianshu.io/upload_images/3239501-3d7cc1865eaaed9c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`$ pwd`
运行结果：
![](http://upload-images.jianshu.io/upload_images/3239501-d26af22e508c842a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
5. 编译DOL
进入dol的文件夹，修改build_zip.xml文件
![](http://upload-images.jianshu.io/upload_images/3239501-7dc80be163a0418a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`$ ant -f build_zip.xml all`
运行结果：
![](http://upload-images.jianshu.io/upload_images/3239501-612b3abab56520ef.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
6. 运行第一个例子
`$ ant -f runexample.xml -Dnumber=1`
运行结果：
![](http://upload-images.jianshu.io/upload_images/3239501-8a3760e361baec96.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
####三、实验心得
本次实验不是太难，主要就是完成dol开发环境的配置，实验步骤ppt给的也很详细，按照ppt一步步完成就能成功，完成readme.md也不是很难，主要是熟悉markdown语句，再进行编辑。
