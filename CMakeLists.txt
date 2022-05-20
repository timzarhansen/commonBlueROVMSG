cmake_minimum_required(VERSION 3.0.2)

project(commonbluerovmsg)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs message_generation)

## System dependencies are found with CMake's conventions
# find_package(Boost REQUIRED COMPONENTS system)

## Generate messages in the 'msg' folder
add_message_files(
    FILES
    leakageDetection.msg
    desiredStateForRobot.msg
    staterobotforevaluation.msg
    heightStamped.msg
    stateOfBlueRov.msg
    SonarEcho2.msg
#   Message1.msg
#   Message2.msg
)
#add_message_files(DIRECTORY msg FILES Num.msg)


## Generate services in the 'srv' folder
add_service_files(
    FILES
    cameraAngle.srv
    lightDensity0to10.srv
    resetekf.srv
    saveGraph.srv
    restartSonarService.srv
)

#add_service_files(DIRECTORY srv FILES AddTwoInts.srv)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs  # Or other packages containing msgs
)

catkin_package(
    INCLUDE_DIRS
    CATKIN_DEPENDS message_runtime
#  DEPENDS system_lib
)

include_directories(
include
        ${catkin_INCLUDE_DIRS}
)

























