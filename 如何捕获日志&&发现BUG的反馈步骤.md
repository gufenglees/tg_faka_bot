# 自己能重现BUG

`cd ~/tg_faka_bot/ && rm ~/tg_faka_bot/output`

`killall python3`

`nohup python3 main.py >>output 2>&1 &`

***

1、自己操作测试，重现BUG。

2、机器人运行中的日志会在机器人停止后写入文件，所以需要先使用命令killall python3停止机器人

3、加入TG群组

4、详细描述错误流程，发送完整的机器人会话截图，并将output文件私发管理员，不发日志文件不予回应

***

# 自己不能重现BUG

1、机器人运行中的日志会在机器人停止后写入文件，所以需要先停止机器人，使用命令：killall python3

2、加入TG群组

3、详细描述错误流程，发送完整的机器人会话截图，并将output文件私发管理员，不发日志文件不予回应
