FROM java:8-jdk
MAINTAINER wangdongxu <wangdongxu@wondertek.com.cn>
# 默认文件编码 UTF-8
ENV LANG C.UTF-8

RUN set -x \
  && apk add --no-cache \
    tzdata \
  && cp -r -f /usr/share/zoneinfo/Asia/Shanghai /etc/localtime