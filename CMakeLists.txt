cmake_minimum_required(VERSION 3.5)
project(switch_controller2_interface)


# find dependencies
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/CtrlConfig.msg"
  "srv/GraspCmd.srv"
  DEPENDENCIES # Add packages that above messages depend on, in this case geometry_msgs for Sphere.msg
)

ament_package()
