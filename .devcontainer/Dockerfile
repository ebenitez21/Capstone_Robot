FROM osrf/ros:jazzy-desktop-full-noble

# Set environment variables
ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8

# Install additional build and CLI tools
RUN apt-get update && apt-get install -y \
    python3-colcon-common-extensions \
    python3-rosdep \
    git \
    && rm -rf /var/lib/apt/lists/*

# Source ROS 2 environment automatically on bash startup
RUN echo "source /opt/ros/jazzy/setup.bash" >> ~/.bashrc
