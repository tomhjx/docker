FROM centos:7
MAINTAINER "Tom" <tom_hejiaxi@163.com>

ENV GOLANG_VERSION 1.11.5
ENV GOPATH /app

RUN yum clean all && \ 
	yum update -y && \
	yum install wget git -y && \
	yum clean all && yum update -y

WORKDIR /tmp

RUN wget -O go.tgz "https://dl.google.com/go/go$GOLANG_VERSION.linux-amd64.tar.gz"; \
	tar -C /usr/local -xzf go.tgz; \
    rm -rf /tmp/*

ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH
RUN go version

RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
WORKDIR $GOPATH