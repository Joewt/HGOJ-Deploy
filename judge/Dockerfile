FROM woodenfish42/hustoj-judge as build-env
LABEL maintainer="joe <joewttx@gmail.com>"
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
CMD sed -i 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list
RUN set -ex \
    && apt update \
    && apt install \
               default-jdk \
               golang-go -y

CMD judged && tail -f /dev/null
