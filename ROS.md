#安装ROS
***
####一、查看虚拟机版本
鉴于我的虚拟机版本是14.04，所以使用网址
http://wiki.ros.org/jade/Installation/Ubuntu
的安装方法。

####二、开始安装
1. Setup your sources.list
<code>sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'</code>

![](http://upload-images.jianshu.io/upload_images/3239501-ec7b4ecfe6d0c879.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2.Set up your keys
<code>sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116</code>

3.Installation
<code>sudo apt-get update</code>
![](http://upload-images.jianshu.io/upload_images/3239501-7885a95de2bf36f4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

<code>sudo apt-get install ros-jade-desktop-full</code>

![](http://upload-images.jianshu.io/upload_images/3239501-3598545a8d25affc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
<code>apt-cache search ros-jade</code>

![](http://upload-images.jianshu.io/upload_images/3239501-6f5b5f9769d0f92a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

4.Initialize rosdep
<code>sudo rosdep init
rosdep update</code>

![](http://upload-images.jianshu.io/upload_images/3239501-69e269edae22e988.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

5.Environment setup
<code>echo "source /opt/ros/jade/setup.bash" >> ~/.bashrcsource ~/.bashrc</code>

![](http://upload-images.jianshu.io/upload_images/3239501-0943ed27764605c0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

6.Getting rosinstall
<code>sudo apt-get install python-rosinstall</code>

![](http://upload-images.jianshu.io/upload_images/3239501-c241f7d4358acf9d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

综上ROS安装完成！
