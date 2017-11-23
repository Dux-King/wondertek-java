FROM alpine:3.4
MAINTAINER wangdongxu <wangdongxu@wondertek.com.cn>
# 默认文件编码 UTF-8
ENV LANG C.UTF-8

RUN { \
    echo '#!/bin/sh'; \
    echo 'set -e'; \
    echo; \
    echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; \
  } > /usr/local/bin/docker-java-home \
  && chmod +x /usr/local/bin/docker-java-home
ENV JAVA_HOME /usr/lib/jvm/java-1.8-openjdk
ENV PATH $PATH:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin

ENV JAVA_VERSION 8u111
ENV JAVA_ALPINE_VERSION 8.111.14-r0

RUN set -x \
  && apk add --no-cache \
    openjdk8="$JAVA_ALPINE_VERSION" libstdc++ curl ca-certificates bash tree tzdata \
  && [ "$JAVA_HOME" = "$(docker-java-home)" ] \
  && cp -r -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime