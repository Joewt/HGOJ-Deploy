FROM golang
MAINTAINER Joewt <joewttx@gmail.com>
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
# RUN mkdir -p $GOPATH/src/golang.org/x/
# WORKDIR $GOPATH/sr/golang.org/x/
#RUN git clone https://github.com/golang/net.git
#RUN git clone https://github.com/golang/sys.git
#RUN git clone https://github.com/golang/tools.git
#RUN go get github.com/gpmgo/gopm
#RUN go get github.com/astaxie/beego
#RUN go get github.com/beego/bee
#RUN go get github.com/go-redis/redis
#RUN mkdir -p $GOPATH/github.com/go-sql-driver/
#RUN go get github.com/go-sql-driver/mysql
#RUN go get github.com/shirou/gopsutil/mem
RUN mkdir -p /data/www/
WORKDIR /data/www/
RUN git clone https://gitee.com/yinrenxin/hgoj.git
WORKDIR /data/www/hgoj/
EXPOSE 8086
CMD [ "go","run","main.go" ]
# RUN go build -o hgoj main.go
# RUN nohup ./hgoj &
