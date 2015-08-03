# docker build -t jbasney/mech-saml-ec-centos .
# docker run --name gss-server -it mech-saml-ec-centos bash
# docker run --name gss-client -it mech-saml-ec-centos bash
FROM centos
MAINTAINER Jim Basney <jbasney@illinois.edu>
ENV container docker
COPY shibboleth.repo /etc/yum.repos.d/shibboleth.repo
COPY .gss_saml_ec_cb_type /root/
RUN yum -y update && yum -y install \
    gcc \
    gcc-c++ \
    git \
    libcurl-devel \
    libevent \
    liblog4shib-devel \
    liblog4shib1 \
    libsaml-devel \
    libsaml7 \
    libtool \
    libxerces-c-3_1 \
    libxerces-c-devel \
    libxml-security-c-devel \
    libxml-security-c16 \
    libxml2-devel \
    libxmltooling-devel \
    libxmltooling5 \
    opensaml-schemas \
    shibboleth \
    shibboleth-devel \
    xmltooling-schemas \
    && yum clean all
RUN git clone https://github.com/jbasney/mech_saml_ec.git /opt/mech_saml_ec
RUN cd /opt/mech_saml_ec && ./autogen.sh && ./configure && make
ENV MECH_SAML_EC_DEBUG anyvalue
