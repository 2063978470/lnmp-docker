### docker-compose web service 使用文档

##### 镜像服务器权限
1. 在镜像服务器注册账号(https://hub.tradecubic.com).

##### 本地docker环境搭建
1. 参照官方文档(https://docs.docker.com/engine/installation/), 安装ce版本.
2. 安装docker-compose,参照官方文档(https://docs.docker.com/compose/overview/).

##### docker-compose配置
1. 拉取项目(http://code.tradecubic.com/tradecubic_docker_compose_v1/docker-compose-tradecubic-phpweb.git)
2. 数据库初始化.
    1. 导出当前测试数据库至文件 name.sql
    2. 复制name.sql到./mysql文件夹
    3. 在.env文件中更改数据库root密码和数据库名称(数据库名称必须与name.sql文件中的数据库名称一致)
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
