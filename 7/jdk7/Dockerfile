FROM java:7-jdk
MAINTAINER wangdongxu <wangdongxu@wondertek.com.cn>
# 默认文件编码 UTF-8
ENV LANG C.UTF-8
ENV  TIME_ZONE Asia/Shanghai
RUN apt-get install tzdata \
&& echo "${TIME_ZONE}" > /etc/timezone \
&& ln -sf /usr/share/zoneinfo/${TIME_ZONE} /etc/localtime \
