# Gazebo121
## 更新
  此项目为作者就职于wheeltec期间（2021年期间）所作  
  详细教程请参照提供的pdf文件（gazebo使用教程.pdf）
## 实现功能：
  建图、保存地图、导航
## install:
  环境：  
  ROS1 melodic  
  Ubuntu 18.04  
  Gazebo 9.0.0  

  环境配置：  
  gmapping建图算法：  
  sudo apt-get install ros-melodic-gmapping  
  navigation：  
  sudo apt-get install ros-melodic-navigation  
  控制器相关依赖：  
  sudo apt-get install ros-melodic-ros-control  
  sudo apt-get install ros-melodic-ros-controllers  
  sudo apt-get install ros-melodic-ackermann-*  
  运动插件复制，将动态库文件libgazebo_ros_wheeltec_mec.so置于/opt/ros/melodic/lib下  
  sudo cp ./gazebo_configuration/libgazebo_ros_wheeltec_mec.so /opt/ros/melodic/lib/libgazebo_ros_wheeltec_mec.so  
  cartographyer部分：  
  将demo_revo_lds.launch替换于/opt/ros/melodic/share/cartographer_ros/launch下  
  sudo cp ./gazebo_configuration/demo_revo_lds.launch /opt/ros/melodic/share/cartographer_ros/launch/demo_revo_lds.launch  
  将revo_lds_gazebo.lua置于/opt/ros/melodic/share/cartographer_ros/configuration_files下  
  sudo cp ./gazebo_configuration/revo_lds_gazebo.lua /opt/ros/melodic/share/cartographer_ros/configuration_files/revo_lds_gazebo.lua  
## 文件描述  
  gazebo_configuration文件夹中为动态库等配置文件  
  wheeltec_description文件夹中为模型urdf以及gazebo world地图等文件，其中meshes的stl文件是使用SolidWorks导出，默认导出urdf过长，实际采用xacro进行简写复用。  
  wheeltec_gazebo_control文件夹为模型的运动控制插件部分  
  wheeltec_gazebo_function文件夹中为模型的建图导航、保存地图部分

## 运行效果图
键盘控制进行建图：  
![image](https://github.com/user-attachments/assets/8b2d4c09-98f6-4ec8-aa7d-3cc495ea0616)  
保存地图：  
![image](https://github.com/user-attachments/assets/869d1ff5-d674-49c0-b43a-2ac07faf04af)  
多点导航：  
![image](https://github.com/user-attachments/assets/2ee91fde-d2c8-4a19-867f-188af5f46dd7)  

## 功能运行
1、Gazebo 2D建图  
roslaunch wheeltec_gazebo_function mapping.launch  
2、键盘控制  
roslaunch wheeltec_gazebo_function keyboard_teleop.launch  
3、保存地图  
一键保存地图(WHEELTEC.pgm、WHEELTEC.yaml)  
roslaunch wheeltec_gazebo_function map_saver.launch  
4、Gazebo 2D导航  
roslaunch wheeltec_gazebo_function navigation.launch  
