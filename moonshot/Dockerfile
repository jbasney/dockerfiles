# https://wiki.moonshot.ja.net/display/Moonshot/Build+Moonshot+from+Source
# docker build -t jbasney/moonshot-deb7 .
# docker run -it jbasney/moonshot-deb7 bash
FROM debian:7
MAINTAINER Jim Basney <jbasney@illinois.edu>
ENV container docker
RUN echo "deb http://ftp.us.debian.org/debian wheezy-backports main" >> /etc/apt/sources.list
RUN apt-get update && apt-get install -y \
    apache2-threaded-dev \
    autoconf \
    automake \
    autopoint \
    autotools-dev \
    build-essential \
    desktop-file-utils \
    doxygen \
    fakeroot \
    libboost-all-dev \
    libconfuse-dev \
    libcurl4-openssl-dev \
    libdbus-glib-1-dev \
    libevent-dev \
    libgee-dev \
    libgnome-keyring-dev \
    libgtk2.0-dev \
    libkrb5-dev \
    liblog4cpp5-dev \
    liblog4shib-dev \
    libsqlite3-dev \
    libtalloc-dev \
    libtool \
    libxerces-c-dev \
    libxml-security-c-dev \
    libxmltooling-dev \
    python \
    valac \
    xmltooling-schemas
RUN apt-get install -yt wheezy-backports libsaml2-dev
RUN git clone --recursive http://www.project-moonshot.org/git/moonshot.git
RUN cd moonshot && ./builder --prefix=/opt/moonshot
