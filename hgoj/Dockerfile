FROM golang
LABEL maintainer="joe <joewttx@gmail.com>"
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN go env -w GOPROXY=https://goproxy.cn,direct
RUN mkdir -p /data/www/
WORKDIR /data/www/
RUN git clone -b v2 https://gitee.com/acm_foreign_branch/hgoj.git
WORKDIR /data/www/hgoj/
RUN go build -o hgoj
EXPOSE 8086
CMD [ "./hgoj" ]
