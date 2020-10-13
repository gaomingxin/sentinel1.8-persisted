FROM openjdk:8u201-jdk-alpine3.9

#作者
MAINTAINER gstar

#系统编码
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8 PARAMS=""

#暴露8080端口
EXPOSE 8080

#定义参数
#ARG JAR_FILE
#应用构建成功后的jar文件被复制到镜像内，名字也改成了app.jar
#ADD ${JAR_FILE} demo.jar
ADD target/sentinel-dashboard.jar sd.jar

#touch命令的作用是修改这个文件的访问时间和修改时间为当前时间，而不会修改文件的内容。
#RUN bash -c 'touch /demo.jar'

#启动容器时的进程
ENTRYPOINT ["sh","-c","java -jar $JAVA_OPTS /sd.jar $PARAMS"]
