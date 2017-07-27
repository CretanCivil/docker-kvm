# Dockerfile 

```
docker-compose up -d
```
## 配置

1. Hostname 设置为kvm的服务器ip，请开启kvm的tcp连接，端口16509
2. Interval 采集频率
3. ApiKey 后台分配的key
4. PollerIp 采集器安装的ip，方便故障查询时候去重启采集器
```json
{
  "Interval": 20,
  "Kvms": [
    {
      "Hostname": "172.29.231.80"
    }
  ],
  "Backend": {
    "ApiKey": "e7afaf986f5cc822406cbd5831328463",
    "KongHost" : "http://172.29.231.177:8000",
    "HostUrl": "/kvm/v1/host",
    "MetricUrl": "/kvm/v1/metrics",
    "PollerUrl": "/kvm/v1/poller",
    "PollerTags":
      {
        "PollerIp":"172.29.231.111"
      }
    ,
    "Type": "kong"
  }
}
```

