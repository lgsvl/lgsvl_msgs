cmake_minimum_required(VERSION 2.8.3)
project(lgsvl_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  geometry_msgs
  sensor_msgs
  std_msgs
)

add_message_files(
  DIRECTORY msg
  FILES
  Detection3DArray.msg
  Detection3D.msg
  BoundingBox3D.msg
  Detection2DArray.msg
  Detection2D.msg
  BoundingBox2D.msg
)

generate_messages(
  DEPENDENCIES
  geometry_msgs   
  sensor_msgs   
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS 
  message_runtime 
  geometry_msgs
  sensor_msgs 
  std_msgs
)
