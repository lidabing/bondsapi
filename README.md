## bondsapi

* 改用django实现，fastapi部署好麻烦，还是改django，以后这种项目都要成熟的方案。

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

  

## 在宝塔中配置nginx
先安装python3.8
源文件上传到www/wwwroots下面
修改settings里面的allowhosts文件
放行127.0.0.1:8000

## 设置nginx反向代理
