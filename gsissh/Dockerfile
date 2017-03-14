# docker build -t jbasney/gsissh .
# docker run --name gsissh -it jbasney/gsissh gsissh ...
FROM jbasney/igtf-fedora
MAINTAINER Jim Basney <jbasney@illinois.edu>
ENV container docker
RUN yum -y update && yum -y install \
    gsi-openssh-clients \
    myproxy \
    && yum clean all
