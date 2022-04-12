# Opencv-Mxnet-
# Python:

```
pip install python
```

先下载Python，pip默认下载的Python是比较新的版本，如果对没什么需求的话可以直接用

```
pip install opencv-python
```

下载python接口的opencv

```
pip install opencv-contrib-python
```

如果需要的话可以下载python的扩展包

在Opencv4.x版本sift算法以及没有专利了，可以直接在Opnecv的主模块中使用

但是如果你要使用surf算法

目前我测试过的**Python3.6.13**搭配**opencv-contrib-python==3.3.0.10**是可以使用surf算法的

目前(2022.4.12)我也是这么搭配的



# C++:

C++要使用Python的扩展模块，那只能去从源码构建一遍Opencv

可以观看下面的视频，我本人没有按下面的教材尝试过，但是我看过这个视频，应该是很OK的

[[重录\]使用Visual Studio 2022编译OpenCV_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Qq4y1Y7vc?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click)





# 换源

如果使用系统的默认源感觉慢的话可以尝试国内源

```
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

在终端输入这个就可以永久换成清华源，当然https://pypi.tuna.tsinghua.edu.cn/simple
这一串地址也可以改成其他的比如豆瓣、阿里......这里我就不详细把网址给出来，去网上搜一下很容易就找到。

如过不想永久换源

```
pip install pandas -i https://pypi.tuna.tsinghua.edu.cn/simple
```

可以这么使用，注意后面那一串清华的镜像源也可以自己修改





# MXnet深度学习环境的搭建

我自己用的Python版本为3.6.13



## CPU版本

```
pip install mxnet
```

直接下载就行



## GPU版本

安装GPU版本的需要先卸载CPU版本



首先要去下载cuda，一定要下载对应版本的cuda

[CUDA Toolkit Archive | NVIDIA Developer](https://developer.nvidia.com/cuda-toolkit-archive)

这个是英伟达官网，上面有各个版本的cuda，不过下载之前先去看自己的显卡应该对应哪个版本的cuda，再去看MXnet的版本对应哪个版本的cuda

下载玩cuda可以通过

```
nvcc -V
```

查看目前使用的cuda版本（cuda是可以安装好几个版本的，这里不做讨论）

**一定一定要看清cuda和MXnet对应的版本**





[Apache MXNet | A flexible and efficient library for deep learning.](https://mxnet.incubator.apache.org/versions/1.9.0/)

这是MXnet的官网



```
pip install mxnet-cu102==1.7.0 -f https://dist.mxnet.io/python
```

具体的也可以去下面的官方文档看看

[Installation — Dive into Deep Learning 0.17.5 documentation (d2l.ai)](https://d2l.ai/chapter_installation/index.html)



下面的地址有MXnet各种各样的版本

https://dist.mxnet.io/python
