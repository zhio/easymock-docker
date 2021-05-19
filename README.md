在文件夹easymock下,执行 docker-compose up -d  此时大概率会报错,因为数据卷映射的 production.json 和 logs 没有权限

执行 docker-compose down停止docker-compose,再执行下面授权指令

chmod 777 logs 和

chmod 777 production.json

然后再执行 docker-compose up -d 就能通过 http://ip:7300 进行访问了

