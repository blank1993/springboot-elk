**1.先创建挂载日志目录并且赋予权限**
```
mkdir elasticsearch
chmod 777 elasticsearch
```
**2.修改max_map_count大小**
```
vi /etc/security/limits.conf 
最下面添加 vm.max_map_count=262144然后保存
```

**3.启动**
```
docker-compose up -d
```
**4.访问**

浏览器打开http://127.0.0.1:5601

**5.设置默认显示**

找到defaultColumns 并且修改成 host, level, logger_name, message
