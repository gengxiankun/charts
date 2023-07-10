# MySQL packaged by gengxiankun-charts

## TL;DR
```bash
helm repo add gengxiankun-charts https://gengxiankun.github.io/charts/package/
helm install my-mysql gengxiankun-charts/mysql --version 0.1.0
```

## Prerequisites
- Kubernetes 1.19+
- Helm 3.2.0+
- PV provisioner support in the underlying infrastructure

## Parameters

| Name | Description | Value |
| -- | -- | -- |
| replicaCount | 副本数 | 1 |
| image.repository | 镜像地址 | mysql |
| image.tag | 镜像版本 | "8.0" |
| persistence.size | 持久化存储大小 | 1Gi |
| persistence.storageClass | 持久化的 StorageClass | hostpath |
| service.type | Service type | LoadBalancer |
| service.port | Service 端口 | 3306 |
| service.targetPort | Service 应用访问端口 | 3306 |
| mysql.rootPassword | MySQL root 密码 | "123456" |