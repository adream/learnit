## 安装docker并运行swarm模式

### 概念

_swarm_

docker swarm是一个容器编排管理工具，docker-engine在1.12版本之后集成了docker swarm。

常用的编排工具有Google开源的kubernetes、apache的mesos、docker公司的swarm。

### 安装docker

以centos7为例

*   1、更新yum源，yum update
*   2、添加docker的yum仓库
> sudo tee /etc/yum.repos.d/docker.repo &lt;&lt;-'EOF'
> [dockerrepo]
> name=Docker Repository
> baseurl=[https://yum.dockerproject.org/repo/main/centos/7/](https://yum.dockerproject.org/repo/main/centos/7/)
> enabled=1
> gpgcheck=1
> gpgkey=[https://yum.dockerproject.org/gpg](https://yum.dockerproject.org/gpg)
> EOF

*   3、安装docker-engine，sudo yum install docker-engine
*   4、启动docker守护进程，sudo systemctl start docker