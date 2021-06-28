# Gazebo仿真环境中的全向轮小车及地图

## 背景

- 整个仿真是从2021全国大学生智能汽车竞赛创意组讯飞赛道线上赛环境修改而来
- 带有2个launch文件`gazebo.launch`和`nowall.launch` 前者生成的世界有迷宫围墙和车，后者只有车

## 安装

- Step1:
  - `sudo gedit /usr/lib/python2.7/site.py`找到 `setencoding()` 函数
  - 修改第一个 `encoding="utf-8"`
- Step2:
  - 将`models`文件夹复制到`~/.gazebo`目录下
  - 如果不存在以上目录就创建

## 运行

将整个项目作为package放入一个workspace中

```sh
catkin_make
source devel/setup.bash
roslaunch gazebo_pkg gazebo.launch
```



