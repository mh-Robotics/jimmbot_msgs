cmake_minimum_required(VERSION 2.8.3)
project(jimmbot_msgs)

add_compile_options(-std=c++17)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

add_message_files(
  FILES
  CanFrame.msg
  CanFrameArray.msg
  CanFrameArrayStamped.msg
  CanFrameStamped.msg
  ExtnData.msg
  ExtnDataStamped.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(CATKIN_DEPENDS std_msgs message_runtime)
