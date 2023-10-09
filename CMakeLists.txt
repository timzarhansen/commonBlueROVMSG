cmake_minimum_required(VERSION 3.3)
set(CMAKE_CXX_STANDARD 14)
project(commonbluerovmsg)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(builtin_interfaces REQUIRED)




## System dependencies are found with CMake's conventions
# find_package(Boost REQUIRED COMPONENTS system)

## Generate messages in the 'msg' folder
#add_message_files(
#    FILES
#    LeakageDetection.msg
#    DesiredStateForRobot.msg
#    StateRobotForEvaluation.msg
#    HeightStamped.msg
#    StateOfBlueRov.msg
#    SonarEcho2.msg
##   Message1.msg
##   Message2.msg
#)
#add_message_files(DIRECTORY msg FILES Num.msg)


## Generate services in the 'srv' folder
#add_service_files(
#    FILES
#    CameraAngle.srv
#    LightDensity.srv
#    ResetEkf.srv
#    SaveGraph.srv
#    RestartSonarService.srv
#)

#add_service_files(DIRECTORY srv FILES AddTwoInts.srv)

## Generate added messages and services with any dependencies listed here
rosidl_generate_interfaces( ${PROJECT_NAME}
    "msg/LeakageDetection.msg"
    "msg/DesiredStateForRobot.msg"
    "msg/StateRobotForEvaluation.msg"
    "msg/HeightStamped.msg"
    "msg/StateOfBlueRov.msg"
    "msg/SonarEcho2.msg"

    "srv/CameraAngle.srv"
    "srv/LightDensity.srv"
    "srv/ResetEkf.srv"
    "srv/SaveGraph.srv"
    "srv/RestartSonarService.srv"
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()






















