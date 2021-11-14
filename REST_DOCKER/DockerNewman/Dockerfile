FROM node:14-alpine
MAINTAINER Vladimir Sarychev: svmyhome@mail.ru
RUN npm install -g newman newman-reporter-allure
VOLUME ["/allurenewman"]
WORKDIR /allurenewman
# RUN mkdir $(date +"%d-%m-%Y-%r")
RUN ls
ADD ./DockerNewman/SWApi.postman_collection.json .
# ADD ./SWApi.postman_collection.json .
CMD ["newman", "run", "SWApi.postman_collection.json", "-r", "allure"]
