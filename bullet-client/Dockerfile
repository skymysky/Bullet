FROM ascdc/jdk8:latest

# 工作空间
WORKDIR /opt/bullet

# 开发者
MAINTAINER docker_user admin@wuweibi.com

ARG VERSION=0.0.1
# 时区处理
ENV TZ Asia/Shanghai
# Bullet设备编码
ENV BULLET_DEVICE_NO ''

# 中文乱码处理
ENV LANG C.UTF-8


# 容器内部文件处理
ADD ../build/client/bin /opt/bullet/bin/
ADD ../build/client/conf /opt/bullet/conf/
ADD ./target/bullet-client.jar /opt/bullet/lib/bullet-client.jar
ADD ./logs/ /opt/bullet/logs/

# 启动项目命令
ENTRYPOINT ["/opt/bullet/bin/bullet"]
