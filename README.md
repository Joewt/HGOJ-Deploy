# 湖南工学院在线判题系统部署脚本
## 环境准备

### Ubuntu 系统

1. 安装必要的依赖

    ```bash
    sudo apt-get update && sudo apt-get install -y vim  curl git
    ```

2. 安装 Docker && Docker-Compose

    一键安装: `sudo curl -sSL https://get.daocloud.io/docker | sh`  

    详细步骤参照： [https://docs.docker.com/install/](https://docs.docker.com/install/)  

   ```
   sudo curl -L "https://github.com/docker/compose/releases/download/1.24.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
   sudo chmod +x /usr/local/bin/docker-compose
   sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
   ```

### Mac 系统

Mac系统安装Docker更加简单，只需要到Docker官网下载Docker安装即可，Docker-Compose也会同时安装上

### Windows 环境


Windows 下的安装仅供体验，勿在生产环境使用。如有必要，请使用虚拟机安装 Linux 并将 OJ 安装在其中。

以下教程仅适用于 Win10 x64 下的 `PowerShell`

1. 安装 Windows 的 Docker 工具
2. 右击右下角 Docker 图标，选择 Settings 进行设置
3. 选择 `Shared Drives` 菜单，之后勾选你想安装 OJ 的盘符位置（例如勾选D盘），点击 `Apply`
4. 输入 Windows 的账号密码进行文件共享
5. 安装 `docker-compose`，安装方法自行搜索。

## 开始安装

1. 请选择磁盘空间富余的位置，运行下面的命令

    ```bash
    git clone -b master https://github.com/yinrenxin/HGOJ-Deploy.git && cd HGOJ-Deploy
    ```

2. 启动服务

    ```bash
    docker-compose up -d
    ```
3. 创建数据库

安装完需要手动创建库才能运行，可打开8080端口进入phpmyadmin数据库管理程序, 服务器为mysql,账号密码都是root, 默认数据库名为hgoj，数据库创建完再重启hgoj容器即可使用

## 使用

通过浏览器访问服务器的 HTTP 80 端口或者 HTTPS 443 端口，就可以开始使用了



## 问题

发现某个服务没有启动成功,可通过查看日志看具体的问题
```
docker-compose logs xxx 
```