# 使用 Jenkins 官方 LTS 镜像作为基础镜像
FROM jenkins/jenkins:lts

# 切换到 root 用户以安装 Maven
USER root

# 安装 Maven 和 Git
RUN apt-get update && \
    apt-get install -y maven git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# 切回 Jenkins 用户
USER jenkins

# 可选：如果您有需要预先配置 Jenkins 的特定文件或插件，
# 可以在这里使用 COPY 指令将它们复制到容器中的适当位置。
# 例如：
# COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
# RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

# 暴露 Jenkins 默认端口
EXPOSE 8080 50000
