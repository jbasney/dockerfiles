# docker build -t jbasney/igtf-centos6 .
# docker run --name igtf-centos6 -it jbasney/igtf-centos6 /bin/bash
FROM centos:6
MAINTAINER Jim Basney <jbasney@illinois.edu>
ENV container docker
COPY igtf.repo /etc/yum.repos.d/igtf.repo
RUN yum -y update && yum -y install \
    ca_policy_igtf-classic \
    ca_policy_igtf-slcs \
    ca_policy_igtf-mics \
    ca_policy_igtf-iota \
    && yum clean all
