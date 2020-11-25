cmake_minimum_required(VERSION 2.8.3)
project(knowledge_sharing_planner_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  std_msgs
)

################################################
## Declare ROS messages, services and actions ##
################################################


## Generate messages in the 'msg' folder
 add_message_files(
  FILES
  Triplet.msg
  SymbolTable.msg
 )

## Generate services in the 'srv' folder
 add_service_files(
   FILES
   Disambiguation.srv
   Verbalization.srv
   Understand.srv
   Merge.srv
 )

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
#   Action1.action
#   Action2.action
# )

## Generate added messages and services with any dependencies listed here
 generate_messages(
   DEPENDENCIES
   std_msgs
 )

 ###################################
 ## catkin specific configuration ##
 ###################################
 catkin_package(
 )
