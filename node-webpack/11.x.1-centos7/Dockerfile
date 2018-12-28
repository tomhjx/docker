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
    && yum install -y nodejs

COPY vendor /app/vendor

RUN cd /app/vendor/; \
    npm install; \
    npm audit fix

CMD ["npm", "-v"]