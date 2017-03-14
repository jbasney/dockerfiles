# docker build -t jbasney/globus .
# docker run --name globus -it jbasney/globus /bin/bash
FROM jbasney/igtf-centos
MAINTAINER Jim Basney <jbasney@illinois.edu>
ENV container docker
COPY globus-toolkit-repo-latest.noarch.rpm /root
RUN yum -y update && yum -y install \
    gsi-openssh \
    myproxy \
    && yum clean all
