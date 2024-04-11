# Select image
# 指定镜像
FROM ubuntu:20.04
# Support Chinese
# 支持中文
ENV LANG="C.UTF-8"
# Select timezone, which some software requires
# 设置时区, 以防某些软件需要确定时区
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && \
    echo "$TZ" > /etc/timezone
    
# Install SSH and set up an auto-start python script
# 安装ssh并设置自动启动脚本
COPY install_ssh write_ssh /root/
RUN cat /root/install_ssh | bash && \
    rm -rf /root/install_ssh