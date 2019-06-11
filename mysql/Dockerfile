ARG 5.7

FROM mysql:5.7
ENV MYSQL_ALLOW_EMPTY_PASSWORD yes
RUN echo "Asia/shanghai" > /etc/timezone;

RUN rm -rf /etc/localtime;
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

ADD ./conf.d/ /etc/mysql/conf.d
COPY ./init/setup.sql /etc/mysql/setup.sql
COPY ./init/schema.sql /etc/mysql/schema.sql

CMD ["sh","/etc/mysql/setup.sql"]
