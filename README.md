### docker-compose web service 使用文档


##### docker-compose配置
1. 拉取项目
2. 数据库初始化.
   
    1. 在.env文件中更改数据库root密码和数据库名称(数据库名称必须与name.sql文件中的数据库名称一致)
3. 多项目配置
    1. 打开.env文件，更改WWW_ROOT变量为本地项目代码目录，建议是不同项目的上层目录。
    2. 修改WWW_LOGS变量为本地log目录。
    3. 进入./nginx/vhosts目录，创建并配置响应项目vhost文件，文件名必须以.conf结尾，内容参照默认文件即可。
    4. 保证本地80端口未被占用。
    
##### 本地hosts文件配置
1. 不必多说，相信大家都会了，如不会，可请教同事。

##### 启动
1. 进入docker-compose-tradecubic-phpweb目录
2. 执行命令docker-compose up -d 
3. 如果查看日志 docker logs -t 容器id或者名称
