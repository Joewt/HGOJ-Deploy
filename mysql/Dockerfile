ARG 5.7

FROM mysql:5.7

RUN echo "Asia/shanghai" > /etc/timezone;

RUN rm -rf /etc/localtime;
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ADD ./conf.d/ /etc/mysql/conf.d
