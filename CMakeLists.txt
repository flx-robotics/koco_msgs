cmake_minimum_required(VERSION 3.0.2)
project(koco_msgs)

## Message dependencies
set(message_depends
  geometry_msgs
  moveit_msgs
  sensor_msgs
  std_msgs
  trajectory_msgs
)

find_package(catkin REQUIRED COMPONENTS
  ${message_depends}
  message_generation
)

# Generate messages in the 'msg' folder
add_message_files(
  FILES
  DigitalIO.msg
  DigitalIOArray.msg
  KocoPose.msg
  KocoTool.msg
)

## Generate actions in the 'action' folder
add_action_files(
  FILES
  MoveJ.action
  MoveL.action
  MoveSequence.action
)

# Generate services in the 'srv' folder
add_service_files(
  FILES
  PlanAndStore.srv
  SetOutputs.srv
  SetRobotSpeed.srv
  TriggerString.srv
)

# Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  ${message_depends}
)

catkin_package(
  CATKIN_DEPENDS
  ${message_depends}
  message_runtime
)
