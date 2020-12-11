FROM adoptopenjdk/openjdk8-openj9

ENV TZ="Asia/Shanghai"
ENV JVM_XMS="256m"
ENV JVM_XMX="256m"

COPY halo.jar halo.jar

EXPOSE 8090

ENTRYPOINT java -Xms${JVM_XMS} -Xmx${JVM_XMX} -Djava.security.egd=file:/dev/urandom -server -jar halo.jar
