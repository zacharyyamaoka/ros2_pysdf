cmake_minimum_required(VERSION 3.5)
project(ros2_pysdf)

# Find dependencies
find_package(ament_cmake REQUIRED)
find_package(ament_cmake_python REQUIRED)
find_package(rclpy REQUIRED)


# Install Python package
ament_python_install_package(${PROJECT_NAME})

install(PROGRAMS
    scripts/sdf2urdf.py

    ros2_pysdf/conversions.py
    ros2_pysdf/naming.py
    ros2_pysdf/parse.py

    DESTINATION lib/${PROJECT_NAME}
)


# Setup the project
ament_package()
