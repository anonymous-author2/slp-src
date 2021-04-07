cmake_minimum_required(VERSION 2.8.3)
project(slp_msgs)

find_package(catkin REQUIRED COMPONENTS 
        actionlib_msgs
        geometry_msgs
        std_msgs
        sensor_msgs
        robot_msgs
)

add_message_files(
    DIRECTORY msg
    FILES
    Action.msg
    Command.msg
    POI.msg
    POIArray.msg
)

add_action_files(
  DIRECTORY action
  FILES Slp.action
)

generate_messages(
    DEPENDENCIES actionlib_msgs geometry_msgs std_msgs sensor_msgs robot_msgs
)

catkin_package(
  CATKIN_DEPENDS actionlib_msgs geometry_msgs std_msgs sensor_msgs robot_msgs
)

