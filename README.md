# Oracle_OneKey_Active
为了应对甲骨文最新回收机制而作的垃圾脚本


说在前面：
由于甲骨文目前对不活跃机器实行回收，本脚本的作用就是  通过下载文件，上传，cpu跑分让甲骨文以为你是"活跃用户"
脚本仅做辅助，无法保证不被删机

================================================================

OneKeyFuck_OCPU.sh

一键吃掉CPU（可精准控制）
```
cd /root && wget -qO OneKeyFuck_OCPU.sh https://raw.githubusercontent.com/Mrmineduce21/Oracle_OneKey_Active/main/OneKeyFuck_OCPU.sh && chmod +x OneKeyFuck_OCPU.sh && bash OneKeyFuck_OCPU.sh
```
当ssh终端出现  nohup: appending output to 'nohup.out'  时按回车即可
================================================================

memory_usage.sh
使用方法： 需要root 权限 启动

bash memory_usage.sh consume 内存大小

eg : bash memory_usage.sh consume 1G 即消耗1G 的内存


一键吃内存（2G）
```
cd /root && wget -qO memory_usage.sh https://raw.githubusercontent.com/Mrmineduce21/Oracle_OneKey_Active/main/memory_usage.sh && chmod +x memory_usage.sh && bash memory_usage.sh consume 2G
```

一键吃内存（20G）[适用于24G内存]
```
cd /root && wget -qO memory_usage.sh https://raw.githubusercontent.com/Mrmineduce21/Oracle_OneKey_Active/main/memory_usage.sh && chmod +x memory_usage.sh && bash memory_usage.sh consume 20G
```

取消内存消耗
```
cd /root && wget -qO memory_usage.sh https://raw.githubusercontent.com/Mrmineduce21/Oracle_OneKey_Active/main/memory_usage.sh && chmod +x memory_usage.sh && bash memory_usage.sh release
```

================================================================

cpu_usage.sh

使用之前使用命令先查询下cpu的个数

cat /proc/cpuinfo | grep “processor”|wc -l

或 grep processor /proc/cpuinfo |wc -l


一键吃掉1核心
```
cd /root && wget -qO cpu_usage.sh https://raw.githubusercontent.com/Mrmineduce21/Oracle_OneKey_Active/main/cpu_usage.sh && chmod +x cpu_usage.sh && bash cpu_usage.sh consume 1
```

取消CPU消耗
```
cd /root && wget -qO cpu_usage.sh https://raw.githubusercontent.com/Mrmineduce21/Oracle_OneKey_Active/main/cpu_usage.sh && chmod +x cpu_usage.sh && bash cpu_usage.sh release
```

需要构造消耗2颗cpu的资源运行脚本sh cpu_usage.sh consume 2，此时运行top命令查看cpu的使用率。如果要释放cpu资源
运行sh cpu_usage.sh release即可释放cpu资源。

================================================================

Fuck_OCPU.sh

运行方法  bash Fuck_OCPU.sh <cores> 

需要自行安装CPUlimit
