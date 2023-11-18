## bondsapi

* 改用django实现，fastapi部署好麻烦，还是改django，以后这种项目都要成熟的方案。

## 安装宝塔面板安装以及部署

* 进入宝塔面板-》网站-》python项目--》安装nginx--》安装python3.8.12
* 上传django代码bondsapi到www/wwwroot目录里面
* 宝塔面板里面配置python项目

## 在宝塔中配置django
先安装python3.8
源文件上传到www/wwwroots下面
修改settings里面的allowhosts文件
放行127.0.0.1:8000

## 设置nginx反向代理
