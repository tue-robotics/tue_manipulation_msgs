cmake_minimum_required(VERSION 2.8.3)
project(tue_manipulation_msgs)

find_package(catkin REQUIRED COMPONENTS
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
    tue_msgs
)

catkin_package(
 CATKIN_DEPENDS message_runtime tue_msgs
)
