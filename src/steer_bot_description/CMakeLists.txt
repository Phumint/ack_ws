cmake_minimum_required(VERSION 3.8)
project(steer_bot_description)

# find_package(ament_cmake REQUIRED) is the ROS 2 equivalent of catkin
find_package(ament_cmake REQUIRED)

# If your URDFs depend on xacro, you might need this (optional usually)
find_package(urdf REQUIRED) 

# Install the directories (meshes, urdf, launch, rviz, etc.)
install(DIRECTORY 
  launch 
  urdf
  rviz
  DESTINATION share/${PROJECT_NAME}
)

# This macro marks the package as an ament package
ament_package()