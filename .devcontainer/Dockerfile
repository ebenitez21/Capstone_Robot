FROM osrf/ros:jazzy-desktop-full-noble

ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8
ENV DEBIAN_FRONTEND=noninteractive

# Install build tools, vision bridges, Foxglove, and Joystick/URDF tools
RUN apt-get update && apt-get install -y \
    python3-colcon-common-extensions \
    python3-rosdep \
    python3-pip \
    python3-opencv \
    git \
    ros-jazzy-cv-bridge \
    ros-jazzy-vision-msgs \
    ros-jazzy-foxglove-bridge \
    ros-jazzy-joy \
    ros-jazzy-teleop-twist-joy \
    ros-jazzy-joint-state-publisher-gui \
    ros-jazzy-robot-state-publisher \
    ros-jazzy-xacro \
    && rm -rf /var/lib/apt/lists/*

# Source ROS 2 environment automatically on bash startup
RUN echo "source /opt/ros/jazzy/setup.bash" >> ~/.bashrc