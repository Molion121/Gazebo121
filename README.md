# Gazebo121
## 更新于2025.02.19
  此项目为作者就职于wheeltec期间（2021年期间）所作  
  详细教程请参照提供的pdf文件（gazebo使用教程.pdf）
## 实现功能：
  建图、保存地图、导航
## install:
  环境：  
  ROS1 melodic  
  Ubuntu 18.04  
  Gazebo>9.0.0  

  运动插件生成
  cd 
  
## 文件描述
  wheeltec_description文件夹中

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
