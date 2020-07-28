```
较旧版本的Docker被称为docker或docker-engine。如果已安装，请卸载它们以及相关的依赖项。
yum remove docker docker-client docker-client-latest docker-common docker-latest docker-latest-logrotate docker-logrotate docker-engine
安装相关工具类：
yum install -y yum-utils device-mapper-persistent-data lvm2
配置docker仓库：(阿里镜像)
(sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo)
yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo   
安装docker 社区版
yum install docker-ce
启动docker
systemctl start docker
验证docker
docker run hello-world

docker search [OPTIONS]  从Docker Hub查找镜像,--automated :只列出 automated build类型的镜像；--no-trunc :显示完整的镜像描述；-s :列出收藏数不小于指定值的镜像。
docker pull 从镜像仓库中拉取或者更新指定镜像
docker push 将本地的镜像上传到镜像仓库,要先登陆到镜像仓库
docker run 创建和启动一个新的容器，启动时通过加选项和参数在容器运行命令； # docker run -p 82:80 -d  --name=hello imagename 
docker start 启动一个或多个已经被停止的容器
docker stop 停止一个运行中的容器
docker restart 重启容器
docker kill 杀掉一个运行中的容器
docker rm 删除一个或多个容器
docker ps | grep zwl查看具体版本的容器
docker pause 容器名 暂停该容器类的所有线程
docker unpause 容器名 恢复改容器内的所有线程
docker create 创建一个新的容器但不启动它语法和docker run 一致
docker exec 在运行的容器中执行命令 docker exec -i -t hello /bin/bash
输入exit可退出
docker rmi [image]  删除镜像
docker image rm [image]  删除镜像
docker image prune  清理镜像残留


```