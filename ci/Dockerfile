FROM library/gcc:6.4.0
MAINTAINER Mustafa Özcelikörs

RUN apt-get update

RUN apt-get install -y build-essential dpkg apt-utils

RUN apt-get install -y cmake

RUN apt-get install -y python-dev \
	python-numpy 

RUN apt-get install -y doxygen curl valgrind ssh telnet git

# Git LFS
RUN curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | bash

# Your SDK - In my case it's the rover
RUN wget -c 'https://owncloud.idial.institute/s/7fh4gbQjS7wfN4B/download?path=%2Fagl-kuksa-rover%2F0.0.0%2Fsdk&files=rover-glibc-x86_64-agl-demo-platform-crosssdk-armv7vehf-neon-vfpv4-toolchain-0.0.0.sh' -O rover_sdk.sh

# Copy/Install your SDK - for rover in my case
RUN mkdir -p /opt/rover/0.0.0

RUN mv rover_sdk.sh /opt/rover/0.0.0/install_rover_sdk.sh

RUN chmod u+x /opt/rover/0.0.0/install_rover_sdk.sh

RUN echo /opt/rover/0.0.0 | ./opt/rover/0.0.0/install_rover_sdk.sh
