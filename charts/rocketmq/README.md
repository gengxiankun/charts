# RocketMQ packaged by gengxiankun-charts

## TL;DR
```bash
helm repo add gengxiankun-charts https://gengxiankun.github.io/charts/package/
helm install rocketmq gengxiankun-charts/rocketmq --version 0.3.0
```

## 先决条件
- Kubernetes 1.19+
- Helm 3.2.0+
- PV provisioner support in the underlying infrastructure

## 参数

| 名称 | 简介 | 默认值 |
| -- | -- | -- |
| replicaCount | 副本数 | 1 |
| image.repository | 镜像地址 | rocketmq |
| image.tag | 镜像版本 | "5.3.0" |
| persistence.size | 持久化存储大小 | 1Gi |
| persistence.storageClass | 持久化的 StorageClass | hostpath |
| service.type | Service type | LoadBalancer |
| service.port | Service 端口 | 9876 |
| service.targetPort | Service 应用访问端口 | 9876 |
| rocketmq.namesrv.max_heap_size | | 256M |
| rocketmq.namesrv.heap_newsize | | 128M |
| rocketmq.rmqbroker.max_heap_size | | 256M |
| rocketmq.rmqbroker.heap_newsize | | 128M |

## 其他配置项
### broker.conf
```conf
brokerIP1=本机 IP
```