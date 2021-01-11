# GMM_Map_Python

该项目是多机 GMM Submap 建图的工作

## 环境配置

项目基于 ROS 和 Python2
需要安装的库主要有

```
sudo apt install ros-melodic-tf2-ros
pip install autolab_core
pip install sklearn
```

如果遇到库缺失,基本上可以通过 ```apt install ros-melodic-{缺失库}``` 进行安装.

## 数据集

目前采用自己录制的数据集 30sec.bag

## 使用方法

先启动可视化和建图节点

```
roslaunch gmm_map_python visualgmm.launch
```

再播放相关的数据记录(得cd到.bag文件所在的文件夹中)

```
rosbag play --clock --keep-alive 30sec.bag
```

2021年更新:
我们现在新建了全新 rosbag,在rosbag 中增加了命名空间.运行方法.

```
roslaunch gmm_map_python visualgmm_realsence.launch
```

注意,要先在 visualgmm_realsence.launch 中28,29 行设置rosbag的路径.

rosbag 下载链接:

[https://cloud.tsinghua.edu.cn/f/ecc82823171e4a0aa20f/?dl=1](https://cloud.tsinghua.edu.cn/f/ecc82823171e4a0aa20f/?dl=1)
