# HttpRouter
基于zuul实现的rest服务网关，可以动态的增加和修改路由信息

# 新增一个路由（如果已经存在则会覆盖）
http://127.0.0.1:8080/api/changeroute?serviceId=ddd&desUrl=http://github.com <br />
如同配置静态路由：
```xml
zuul:
  routes:
    ddd:
      url: http://github.com
      path: /ddd/**
```
# 查询路由
http://127.0.0.1:8080/api/getroute

# 需要注意的问题：
通过服务动态修改的路由只保存在内存中，可考虑把动态修改的路由信息持久化到redis等存储中


