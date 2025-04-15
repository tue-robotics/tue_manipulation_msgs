cmake_minimum_required(VERSION 3.5)
project(tue_manipulation_msgs)

find_package(catkin REQUIRED COMPONENTS
  actionlib_msgs
  message_generation
  tue_msgs
)

add_message_files(
  FILES
    cart_pos.msg
)

add_action_files(
  FILES
    GraspPrecompute.action
    GripperCommand.action
)

generate_messages(
  DEPENDENCIES
    actionlib_msgs
    tue_msgs
)

catkin_package(
 CATKIN_DEPENDS actionlib_msgs message_runtime tue_msgs
)
