cmake_minimum_required(VERSION 2.8.3)
project(monitor_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  message_generation
)

add_message_files(
    FILES
    ModuleCheck.msg
    ModuleHealth.msg
)

generate_messages(
    DEPENDENCIES
    std_msgs
)


catkin_package(
    CATKIN_DEPENDS roscpp rospy std_msgs message_runtime
)
