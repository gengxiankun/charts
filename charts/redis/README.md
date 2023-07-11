# Redis packaged by gengxiankun-charts

## TL;DR
```bash
helm repo add gengxiankun-charts https://gengxiankun.github.io/charts/package/
helm install redis gengxiankun-charts/redis --version 0.2.0
```

## 先决条件
- Kubernetes 1.19+
- Helm 3.2.0+
- PV provisioner support in the underlying infrastructure

## 参数

| 名称 | 简介 | 默认值 |
| -- | -- | -- |
| replicaCount | 副本数 | 1 |
| image.repository | 镜像地址 | redis |
| image.tag | 镜像版本 | "8.0" |
| persistence.size | 持久化存储大小 | 1Gi |
| persistence.storageClass | 持久化的 StorageClass | hostpath |
| service.type | Service type | LoadBalancer |
| service.port | Service 端口 | 6379 |
| service.targetPort | Service 应用访问端口 | 6379 |
