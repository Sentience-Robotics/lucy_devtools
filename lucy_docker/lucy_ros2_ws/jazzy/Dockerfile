FROM ubuntu:24.04

LABEL org.opencontainers.image.title="lucy_ros2_base"
LABEL org.opencontainers.image.description="Lucy ROS2 base"
LABEL org.opencontainers.image.vendor="Sentience Robotics"
LABEL org.opencontainers.image.authors="Sentience Robotics"

#Setup ARG
ARG DEBIAN_FRONTEND=noninteractive
ARG ROS_DISTRO=jazzy

ARG USERNAME=rosdev

# Set the locale
ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8

# Install mandatory packages packages
RUN apt update -q && \
    apt upgrade -q -y && \
    apt install -y --no-install-recommends \
        software-properties-common \
        python3-pip \
        make ninja-build clang gcc-arm-none-eabi \
        git vim screen curl lsb-release gnupg sudo clangd \
        libboost-all-dev \
        xorg dbus-x11 tigervnc-common tigervnc-xorg-extension tigervnc-standalone-server tigervnc-tools && \
    add-apt-repository universe && \
    curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg && \
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | tee /etc/apt/sources.list.d/ros2.list > /dev/null && \
    apt update -q && \
    apt install -y --no-install-recommends \
        ros-$ROS_DISTRO-desktop \
        ros-$ROS_DISTRO-ros-gz \
        ros-dev-tools && \
    apt clean -y && \
    rm -rf /var/lib/apt/lists/* /var/cache/apt/*

# Setup user
RUN useradd -m -s /bin/bash -G sudo $USERNAME && \
    echo "$USERNAME ALL=(ALL:ALL) NOPASSWD:ALL" >> /etc/sudoers && \
    mkdir -p /home/$USERNAME && \
    chown -R $USERNAME:$USERNAME /home/$USERNAME
USER $USERNAME
RUN bash -c "echo -e '$USERNAME\n$USERNAME\n' | vncpasswd"

# Copy configuration files
RUN echo 'source /opt/ros/'$ROS_DISTRO'/setup.bash' >> /home/$USERNAME/.bashrc
