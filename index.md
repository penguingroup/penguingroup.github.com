# 企鹅社区

**企鹅社区**是一款媒体发布系统，运营人员可以发布新闻或者活动，用户可以通过前端或客户端进行查看。  
  
**企鹅社区**主要包含一下三部分：
- [白鼬（前端）](#前端)
- [北极圈（接入层代码）](#接入层)
- [运营系统](#运营管理端)
  
## 前端

**白鼬（ermine）**

**部署**
```shell
git clone https://github.com/penguingroup/ermine.git
cd ermine
npm run serve
```

## 接入层

**北极圈（polar）**

**部署**
```shell
git clone https://github.com/penguingroup/polar.git
cd polar
go run main.go
```

## 运营管理端

**部署**
```shell
git clone https://github.com/penguingroup/NewsSystem.git
cd NewsSystem
python manage.py runserver 0.0.0.0:8888
```

## 完整部署脚本

```shell
git clone https://github.com/penguingroup/ermine.git
git clone https://github.com/penguingroup/polar.git
git clone https://github.com/penguingroup/NewsSystem.git
redis-server &
https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.3.0-linux-x86_64.tar.gz
tar -zxvf elasticsearch-7.3.0-linux-x86_64.tar.gz
cd elasticsearch-7.3.0-linux-x86_64/bin
./elasticsearch &
cd -
cd NewsSystem
nohup python manage.py runserver 0.0.0.0:8888 &
cd -
cd polar
go build
nohup ./polar &
cd -
cd ermine
npm run serve
```
**此时运行成功，可以访问**http://127.0.0.1:8888/admin **访问管理后台**  
**文章发布后，可以访问**http://localhost:8080/#homecode **访问前端页面**
