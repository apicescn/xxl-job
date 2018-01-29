# 1 xxl-job-admin
xxl-job-admin Spring Boot版本，为xxl-job-admin-1.8.1为蓝本建立。

# 2 docker镜像


## 2.1 运行容器
通过命令行执行：
```bash
docker run -d -p 8902:8080 -it \
--name xxl-job \
registry.cn-hangzhou.aliyuncs.com/szss-sls/xxl-job:v1.8.1
```

通过docker-compose执行：
```bash
docker-compose up -d
```


# 3 启动镜像
```bash
docker run -d -p 8902:8080 --name xxl-job registry.cn-hangzhou.aliyuncs.com/szss/xxl-job:v1.8.1
```

xxl-job访问路径：http://127.0.0.1:8902/

默认用户名密码为admin/password

# 4 配置数据库链接
```bash
docker run -d -p 8761:8761 \
--name xxl-job \
-e xxl.job.db.driver-class=com.mysql.jdbc.Driver
-e xxl.job.db.jdbc-url=jdbc:mysql://192.168.10.24:3306/odin?useUnicode=true&characterEncoding=UTF-8&useSSL=true
-e xxl.job.db.user=user
-e xxl.job.db.password=password
-e xxl.job.db.driverClass=com.mysql.jdbc.Driver
-e xxl.job.db.url=jdbc:mysql://192.168.10.24:3306/odin?useUnicode=true&characterEncoding=UTF-8
registry.cn-hangzhou.aliyuncs.com/szss-sls/xxl-job:v1.8.1
```


