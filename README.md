# ChaosBlade Experiment

>ChaosBlade Operator 实验场景

![](static/ai.png)

**软件要求**

- Kubernetes v1.12 以上

## 实验准备

本实验使用 [guestbook](https://github.com/cloudnativeapp/guestbook?spm=5176.2020520152.0.0.7c5f16ddH8myx6) 应用。

### 安装

```bash
# add repo
helm repo add apphub-incubator https://apphub.aliyuncs.com/incubator/
# install 
helm install guestbook apphub-incubator/guestbook --set service.type=NodePort --namespace=chaosblade
```

默认的 Service 类型为 `LoadBalancer`，这里为了方便访问设置为了 `NodePort`，访问页面：

>![guestbook](static/guestbook.png)

## [Node](node)

- [节点 CPU 负载实验场景](node/README.md#节点-CPU-负载实验场景)
- 节点网络相关实验场景
  - [节点网络延迟场景](node/README.md#节点网络延迟场景)
  - [节点网络丢包场景](node/README.md#节点网络丢包场景)
  - [节点域名访问异常场景](node/README.md#节点域名访问异常场景)
- 节点磁盘相关场景
  - [节点磁盘填充场景](node/README.md#节点磁盘填充场景)
  - [节点磁盘IO读写负载场景](node/README.md#节点磁盘IO读写负载场景)
- 节点进程相关场景
  - [杀节点上指定进程](node/README.md#杀节点上指定进程)
  - [挂起节点上指定进程](node/README.md#挂起节点上指定进程)

## [Pod](pod)

- [Pod 资源自身场景](pod/README.md#Pod-资源自身场景)
  - [删除 POD](pod/README.md#删除-Pod)
- [Pod 网络相关场景](pod/README.md#Pod-网络相关场景)
  - [Pod 网络延迟场景](pod/README.md#Pod-网络延迟场景)
  - [Pod 网络丢包场景](pod/README.md#Pod-网络丢包场景)
  - [Pod 域名访问异常场景](pod/README.md#Pod-域名访问异常场景)
- [Pod 文件相关场景](pod/README.md#Pod-文件相关场景)
  - [Pod 文件系统I/O故障](pod/README.md#Pod-文件系统I/O故障)

## [Container](container)

- [container 内 CPU 负载场景](container/README.md#container-内CPU负载场景)
- container 内网络实验场景
  - [container 网络延迟场景](container/README.md#container-网络延迟场景)
  - [container 网络丢包场景](container/README.md#container-网络丢包场景)
  - [container 域名访问异常场景](container/README.md#container-域名访问异常场景)
- container 内进程场景
  - [杀 container 内指定进程](container/README.md#杀-container-内指定进程)
  - [挂起 container 内指定进程](container/README.md#挂起-container-内指定进程)
- container 资源自身的场景
  - [删除 container](container/README.md#删除-container)
  
## 鸣谢

ChaosBlade 社区 - [chaosblade.io](https://github.com/chaosblade-io/chaosblade)

>更多内容见 [ChaosBlade 官方文档](https://chaosblade-io.gitbook.io/chaosblade-help-zh-cn)