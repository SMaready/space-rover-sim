# Installs Ubuntu 22.04 preloaded with ROS2 Humble Hawksbill
# and all the dev tools like Gazebo
FROM osrf/ros:humble-desktop-full

# Install handy dev tools
RUN apt-get update && apt-get install -y \
    vim \
    tmux \
    git \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

# Set up working directory
WORKDIR /workspace/ros2_ws

# Source ROS2 environment automatically on bash login
RUN echo "source /opt/ros/humble/setup.bash" >> /root/.bashrc

CMD ["bash"]