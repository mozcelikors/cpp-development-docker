FROM library/gcc:6.4.0
MAINTAINER Mustafa Özcelikörs

RUN apt-get update

RUN apt-get install -y build-essential dpkg

RUN apt-get install -y cmake

RUN apt-get install -y python-dev \
	python-numpy 

RUN apt-get install -y doxygen curl valgrind ssh telnet git

RUN curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash

CMD ["/usr/bin/bash"] 
