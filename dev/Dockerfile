FROM maven:3.5.2-jdk-8-alpine
RUN apk update && apk add git
WORKDIR /usr/share/app-src
RUN git clone https://github.com/sk0ld/clone-app42-test.git ./
RUN mvn clean && mvn install
WORKDIR /usr/share/app-conf
RUN cp /usr/share/app-src/WebContent/Config.properties /usr/share/app-conf
WORKDIR /usr/share/app-content
RUN cp -R /usr/share/app-src/src/com/shephertz/app42/paas/sample/* .