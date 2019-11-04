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
