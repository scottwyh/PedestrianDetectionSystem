![](https://img.shields.io/badge/License-Apache%202-yellow.svg)
# 基于深度学习的自动化行人检测和监控系统
[README](https://github.com/zhangpengpengpeng/PedestrianDetectionSystem/blob/master/README.md)

监控在安保和巡查中发挥着重要作用，但也是一项非常乏味的任务，深度学习的出现在一定程度上将人类从这一任务中解放出来。本项目基于深度学习的目标检测去搭建了一个简单有效的监控系统，能够自动化进行人流统计和行人检测。

**本系统基于Apache2.0协议开源，请严格遵守开源协议。**
# 0x00 简介
本系统由以下三个子项目组成：<br>
- 1.基于TensorFlow平台的行人检测系统
- 2.基于Android平台的推流系统
- 3.基于JavaWeb的展示系统

# 0x01 服务器部署
## 1.服务器的配置要求
| 配置        | 基本要求 |
| ---------- | ------- |
| 操作系统 | Ubuntu 16.04 x64 |
| CPU  | 主频2.0GHz 以上   |
| 内存 | 8G以上 |
| GPU | NVIDIA GTX1080以上 |
| 网络 | 服务器IP地址需是公网IP |

## 2.基于TensorFlow平台的行人检测系统
本系统依赖如下：

| 依赖项 | 安装方式 |
| ---------- | ------ |
| Python3.5 | 略 |
| pip | 略 |
| TensorFlow-1.11.0-GPU | 略 |
| Python版本OpenCV | 略 |
| requests | pip3 install requests |
| frozen_inference_graph.pb | [下载地址](https://download.csdn.net/download/huplion/10825557) |
| Nginx with RTMP | [安装流程](https://www.jianshu.com/p/b4ee6956d1ea) |

运行系统：
- 把训练模型后得到的`.pb`模型文件复制在`python`目录下；
- 修改`main.py`文件`RTMP_HOST`变量，运行`main.py`；

## 3.基于Android平台的推流系统

运行系统：

- 在Idea或者AndroidStudio中导入`android`目录下的工程，并修改`MainActivity.java`中的静态变量；


## 4.基于SSM(SpringMVC+Spring+Mybatis)互联网轻量级框架的展示系统
本系统依赖如下：

| 依赖项 | 安装方式 |
| ---------- | ------ |
| JDK-1.8.0 | 略 |
| Apache-Tomcat-9.0.12 | 略 |
| Maven | 略|
| Mysql | 需配置远程访问权限 |

运行系统：
- 展示系统基于Idea集成开发环境进行开发，SSM框架中的依赖均基于Maven进行配置，在Idea中导入`web`目录下的工程，导出`war`包，将`war`包放在服务器`tomcat/webapps`目录下，运行`./startup.sh`,启动`tomcat`容器；

# 0x02 项目展示

<img src="https://github.com/zhangpengpengpeng/PedestrianDetectionSystem/raw/master/img/example2.jpg" width="600" height="300">

<img src="https://github.com/zhangpengpengpeng/PedestrianDetectionSystem/raw/master/img/example1.png" width="700" height="400">

<img src="https://github.com/zhangpengpengpeng/PedestrianDetectionSystem/raw/master/img/example3.jpg" width="700" height="400">

- 新增了针对大数据量的人流统计的可视化视图；

<img src="https://github.com/zhangpengpengpeng/PedestrianDetectionSystem/raw/master/img/example4.png" width="700" height="600">

- 展示行人检测项目完整效果，[点击此链接](https://pan.baidu.com/s/1X7BX5QSbqZFx2Y6XElW4ZA)；

# 0x03 关于

- 如何支持作者：点击右上角的"star" 的按钮，是对作者的最大支持；
- 如有问题或者讨论行人检测算法模型，请[提交issue](https://github.com/zhangpengpengpeng/PedestrianDetectionSystem/issues/new);



