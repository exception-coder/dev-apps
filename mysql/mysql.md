# mysql安装

## docker

```bash
# mysql官方镜像pull之前需要先登录认证
$ docker login
$ docker pull store/oracle/mysql-enterprise-server:5.7
$ docker run --name=mysql5.7 -p 3306:3306 -d  store/oracle/mysql-enterprise-server:5.7
$ docker logs mysql5.7
# Once initialization is finished, the command's output is going to contain the random password generated for the root user; check the password with, for example, this comman 查看临时密码
$ docker logs mysql5.7 2>&1 | grep GENERATED
# 登录mysql客户端
$ docker exec -it mysql5.7 mysql -uroot -p
# reset the server root password by issuing this statement
$ ALTER USER 'root'@'localhost' IDENTIFIED BY 'password@123';
# 创建用户zhangkai密码password@456 以允许任何ip访问
$ CREATE USER 'zhangkai'@'%' IDENTIFIED BY 'password@456';
$ CREATE DATABASE db_dev;
$ GRANT ALL PRIVILEGES ON db_dev to 'zhangkai'@'%' ;
$ flush privileges;
```



# 参考文档

- [docker-mysql-getting-started](https://dev.mysql.com/doc/refman/5.7/en/docker-mysql-getting-started.html)

