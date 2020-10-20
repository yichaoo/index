# 01.开始Docker

## 官网指引

- [docker主页](https://www.docker.com/)
- [why-docker](https://www.docker.com/why-docker/)
- [docker使用场景](https://www.docker.com/use-cases)
- [docker文档](https://docs.docker.com/)  
	- [docker概览](https://docs.docker.com/get-started/overview/)
	- [快速开始](https://docs.docker.com/get-started/)
	- [使用docker开发](https://docs.docker.com/develop/)
- [使用Docker](https://www.docker.com/get-started)  
	- [Docker Desktop-Windows](https://docs.docker.com/docker-for-windows/install/)
	- [Docker Engine - CentOS(Community)](https://docs.docker.com/engine/install/centos/#install-using-the-convenience-script)
	- [Docker Hub](https://hub.docker.com/)
- **玩转Docker**  
	- [101-tutorial(docker/getting-started)](https://www.docker.com/101-tutorial)
	- [docker实验室](https://docs.docker.com/samples/#tutorial-labs)
	- [dockersamples](https://github.com/dockersamples)
	- [第三方教程](https://docs.docker.com/get-started/resources/)
- [**docker文档**](https://docs.docker.com/)
	- [docker概览](https://docs.docker.com/get-started/overview/)
	- [快速开始](https://docs.docker.com/get-started/)
	- [使用docker开发](https://docs.docker.com/develop/)
	- [数据存储](https://docs.docker.com/storage/)
  - [容器编排](https://docs.docker.com/get-started/orchestration/)
  
- **docker手册** 
	- [Docker Engine](https://docs.docker.com/engine/) 	
	- [Docker Compose](https://docs.docker.com/compose/)
	- [Docker Machine](https://docs.docker.com/machine)
	- [Registry](https://docs.docker.com/registry/)
	  - [私有仓库](https://github.com/docker/labs/blob/master/windows/registry/README.md)

## 使用Docker给开发团队带来的好处

### 1.任何环境都可以正常运行软件

作为开发人员，您知道软件开发中最棘手的问题之一是必须处理不同机器和平台之间的环境差异,**Docker允许您在本地运行容器，消除开发环境和生产环境之间以及两者之间的差异**。不需要在本地安装软件包。开发环境所需的一切都可以作为容器在Docker引擎上运行。无论使用何种语言或工具，您都可以轻松地在本地包含您的环境。通过**Docker Desktop**和**Docker Hub**，可以方便的对软件进行移植，有了这个解决方案，容器可以轻松地跨机器部署。

**至从有了`docker`,开发的小伙伴们可以理直气壮的向运维说：“软件在我的电脑上是正常运行的!"**

![image-20200709153417967](assets/imgs/image-20200709153417967.png)


### 2.团队新成员快速设置开发环境及所需要的依赖服务

无论组织的规模大小如何，如何招募新开发人员并使其尽快入手仍然是一项艰巨的挑战，使用`Docker Desktop`和`Docker Compose`，您可以显着减少本地开发环境的设置时间，并迅速为开发人员服务，使他们可以立即提高生产力。Docker Compose是用于定义和运行多容器Docker应用程序的工具，**通过Compose，您可以使用YAML文件来配置应用程序的服务。然后，只需一个命令，您就可以轻松地从配置中创建并启动所有服务**。

![image-20200709153500021](assets/imgs/image-20200709153500021.png)

### 3.快速部署和更新基于微服务架构的应用

组织越来越多地采用微服务，因为它们不仅希望替换大型的整体应用程序，而且还希望实现更快的应用程序部署和更新。Docker允许您将微服务容器化，并简化这些微服务的交付和管理。容器化为独立的微服务提供了独立的工作负载环境，使它们能够独立地部署和扩展，`Docker Desktop`和`Docker Hub`可让您在整个组织中标准化和自动化构建，共享和运行基于微服务的应用程序的方式。

![image-20200709153908187](assets/imgs/image-20200709153908187.png)




### 4.旧版应用程序也可以迁移至容器

随着容器成为发送和运行应用程序的方式，我们看到的一种趋势是组织采取“提拔和转移”的方式将其现有的应用程序转移到容器中。迈出第一步并不意味着它们永远不会被重组和分解成微服务，但是只要将它们按原样迁移就可以立即获得好处。用Docker来封装遗留应用程序有很多好处。开发和测试效率更高，部署和灾难恢复大大简化，您可以运行应用程序的多个实例，而不会与其他应用程序发生冲突。

![image-20200709154827588](assets/imgs/image-20200709154827588.png)




### 5.在Docker上部署机器学习\深度学习模型

机器学习（ML）开发中的最大挑战之一是在生产中和大规模部署经过训练的模型。Docker利用诸如TensorFlow这样的平台来支持GPU支持，简化了ML应用程序的开发和部署。设置您的开发环境非常简单，只需对您创建的图像或从Docker Hub上的发布者作为Docker图像下载的图像使用“Docker run”命令即可。Docker还可以通过在多台机器上或在云上部署容器来简化ML应用程序的分发，并利用Kubernetes等编排技术来统一管理所有这些容器。

![image-20200709160304447](assets/imgs/image-20200709160304447.png)




