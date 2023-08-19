cmake_minimum_required(VERSION 3.0.2)

project(kr5_description)

find_package(catkin REQUIRED)

catkin_package()

if (CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED COMPONENTS
  rospy
  std_msgs
)
endif()


install(DIRECTORY config launch meshes urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
