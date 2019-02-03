FROM centos:7
MAINTAINER "Tom" <tom_hejiaxi@163.com>
RUN yum install -y git \
        gcc \
        gcc-c++ \
        gd-devel \
        gettext \
        GeoIP-devel \
        libxslt-devel \
        make \
        perl \
        perl-ExtUtils-Embed \
        readline-devel \
        unzip \
        zlib-devel \
        patch

RUN curl -sL https://rpm.nodesource.com/setup_11.x | bash - \
    && yum install -y nodejs \
    && npm install pm2 -g

COPY mybin /mybin

RUN chmod +x -R /mybin

CMD /mybin/start.sh

# CMD echo "this is 1"
# CMD echo "this is 2"
# CMD echo "this is 3"