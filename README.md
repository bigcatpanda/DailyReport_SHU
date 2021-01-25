# DailyReport_SHU

受@BlueFisher大神所启发的项目，已经自己使用3个月。如下是与@BlueFisher大神项目不同之处，希望能对大家有所帮助

* 能自行识别一报和两报
* 一报根据前一天上报的地址进行填报，无需自己手动配置地址 
* 一报根据所在地调整上报内容（上海和外地的上报选项会有所差别），所以只需要知道学生学号密码即可
* 对多人上报进行优化，短时间内多次登录服务器会报429错误，因此有代码中加入休眠机制
* 没有github action
* 没有一键自动补报



## 免责声明

本项目仅做免费的学术交流使用。请勿做商业用途！！



## 依赖

* python 

* requests
* bs4
* tqdm

版本无所谓



## 文件说明

- ` once.txt`和`twice.txt`分别为每日一报和两报的上传模板
- students文件夹中存放学上学号密码，支持多人上报



## 用法

1. 假如需要使用一报时一定要自己上报过至少一天！！！！

2. 在students文件夹中加入txt文件记录学生学号和密码，具体格式如`stu_1.txt`所示，想要多人上报的话直接在students文件夹下另外新建txt，命名无所谓。

3. 在代码中配置个人Email信息，方便挂服务器的时候（或者也可以不配置...)

4. ` python dailyreport.py `  文件夹下会出现` all_stu.json`，用于记录上报者信息，方便debug、重复使用一些信息之类的。 

5. 终端会打印以下信息，`done ` 就说明上报成功，`failed`说明出现了上报内容错误，其他的话说明...出了大问题

    ``` bash
    获取cookie
    stu_1.txt login succeed!
    张三 done
    ```



## 注意事项

* 一报一定要**自己报过至少一天**！！ 
* 仍然在测试中，测试的人群有限，可能会有bug
* **一报还未适配留宿同学**！！！假如需求较大会做相应适配



## 感谢

再次感谢@BlueFisher和其他contributors，也请大家给我一个star。