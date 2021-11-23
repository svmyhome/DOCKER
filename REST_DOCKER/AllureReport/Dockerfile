FROM node:14-alpine
LABEL author="Vladimir Sarychev"
LABEL email="svmyhome@mail.ru"
RUN apk update && apk add openjdk8
WORKDIR /opt
RUN wget -c https://repo.maven.apache.org/maven2/io/qameta/allure/allure-commandline/2.15.0/allure-commandline-2.15.0.tgz
RUN tar -xvf allure-commandline-2.15.0.tgz && chmod +x /opt/allure-2.15.0/bin/allure
RUN rm allure-commandline-2.15.0.tgz
RUN export PATH=$PATH:/opt/allure-2.15.0/bin
RUN env
VOLUME ["/allurenewman"]
WORKDIR /allurenewman
CMD ["/opt/allure-2.15.0/bin/allure", "generate"]
