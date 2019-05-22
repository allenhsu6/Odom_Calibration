# Odom_Calibration
this is a ros workspace to solve the odom Calibration problem.
### 前提

ros 环境： kinetic

需要安装 csm

---

### 编译执行步骤

其余按照正常包执行即可，这是一个ros包，不是工作空间！

需要自行建立workspace，创建src文件夹，并将该ros包放入

在工作空间目录下catkin_make编译

### 运行步骤

1. cd $<your_workspace>
2. source devel/setup.bash
3. roslaunch calib_odom odomCalib.launch
4. 新开终端 cd 到bag文件夹
5. rosbag play --clock odom.bag
6. 打开rviz  `rosrun rviz rviz`  订阅三条path话题，更换不同颜色
7. 发送指令： rostopic pub /calib_flag std_msgs/Empty "{}" 激活标定程序
8. 终端看到对应的标定后的路径   
