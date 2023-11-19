## bondsapi

* 改用django实现，fastapi部署好麻烦，还是改django，以后这种项目都要成熟的方案。

## 使用django来创建工程

django-admin startproject your_project_name
python manage.py startapp your_app_name

## 安装宝塔面板安装以及部署

* 进入宝塔面板-》网站-》python项目--》安装nginx--》安装python3.8.12
* 上传django代码bondsapi到www/wwwroot目录里面
  
  ``
  上传代码之前
  sudo chmod -R 777 www/`
  ```
* 上传之后需要调整bondsapi文件权限 
```
 sudo chmod -R 777 bondsapi 
```
* 宝塔面板里面配置python项目
   选择bondsapi目录
   端口选择不放行，通过nigix来转发
   接下来就要配置nginx了

* 在服务器端，不需要开启8000的端口，通过内部调用就可以了


## 数据库迁移和超级管理员设置

还要更新 sqlite数据库

https://www.ikxin.com/710.html

* 先数据库迁移
```
python manage.py makemigrations
python manage.py migrate
```

* 再设置超级管理员
```
python manage.py createsuperuser
```
  

## 在宝塔中配置nginx
先安装python3.8
源文件上传到www/wwwroots下面
修改settings里面的allowhosts文件
放行127.0.0.1:8000

## 设置nginx反向代理
