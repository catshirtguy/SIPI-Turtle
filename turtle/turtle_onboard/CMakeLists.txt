cmake_minimum_required(VERSION 2.8.3)
project(turtle)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
  rospy
  std_msgs
)

## System dependencies are found with CMake's conventions
# find_package(Boost REQUIRED COMPONENTS system)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES turtle
#  CATKIN_DEPENDS geometry_msgs roscpp rospy std_msgs
#  DEPENDS system_lib
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(joy_control src/joy_control_node.cpp)
target_link_libraries(joy_control ${catkin_LIBRARIES})
add_dependencies(joy_control turtle_generate_messages_cpp)

add_executable(motor_control src/motor_control_node.cpp)
target_link_libraries(motor_control ${catkin_LIBRARIES})
add_dependencies(motor_control turtle_generate_messages_cpp)

