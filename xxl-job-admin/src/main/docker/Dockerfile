# 基于哪个镜像.
FROM openjdk:8-slim
# 将本地文件夹挂载到当前容器
VOLUME /tmp
# 拷贝文件到容器
ADD xxl-job-admin-1.8.1-SNAPSHOT.jar xxl-job.jar
# shell终端中运行程序
RUN bash -c 'touch /xxl-job.jar'
# 打开服务端口
EXPOSE 8080

#-Djava.security.egd为JAVA中的配置发生器,file:/dev/./urandom为Linux要表示urandom的路径,也就是/dev/urandom文件
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/xxl-job.jar"]
