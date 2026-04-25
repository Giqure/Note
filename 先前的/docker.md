docker run
-d 后台（退出时容器后台运行）
-i 交互
-t 终端
-p aaaa:bb   端口映射 a主机端口b容器端口
--name="12con" 名称
-m 内存占用上限
-e DISPLAY=":0.0" 环境变量的设置--下述
-v vva:vvb 卷挂载  a主机卷或目录 b容器位置
--gpus all

-e 
NVIDIA_DRIVER_CAPABILITIES=compute,utility 
-e 
NVIDIA_VISIBLE_DEVICES=all 
-e
DISPLAY=host.docker.internal:0.0



容器与主机的文件交互
- Docker cp命令
docker cp OPTIONS container:source_path destination_path|-
docker cp OPTIONS source_path|- containre:destination_path
- Docker 卷
docker volume
create 创建              OPTIONS volume                --driver --label --opt
inspect 查询            OPTIONS volume...              --filter --format --quiet
ls,list 列出                OPTIONS                             --format
prune 删除未用       OPTIONS                             --filter --force
rm,remove 删除一个或多个 OPTIONS volumes  --force


kuavo advanced版本增加了
1. display
2. biped_challenage
新建容器：
docker run -it --gpus all -v Share:/Tong --name kuavo kuavo_ad /bin/bash