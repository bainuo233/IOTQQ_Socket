# IOTQQ_Socket

C# 插件  By:枫林

* 1、配置Api.cs文件 设置QQ 和 Api地址
* 2、配置App.config

*  结构
   * DataProcess 数据处理
   * Plugins     插件
   * Data        Get/Send数据类
   * HttpHelper  发送提交

*  更新日志
   * 2020-04-21
      * 1、处理了服务器断线重连导致插件无法继续使用的问题
      * PS:请确保只有一个插件在运行，不然会造成死循环连接服务器
   * 2020-04-15
      * 1、自动添加好友
      * 2、复读机功能
      *    连续发三句一样的 会复读 >=10个字符不进行检测 防止恶意刷屏 Plugins.Replay.GetGroupMsg
      * 3、准点报时（QQTask任务里面）
      * 4、随机图片（关键字 来点图 可在 Plugins.RandomPic 修改关键字）
      * PS:如果群消息是自己机器人发出的
      * PS:会过滤 OnGroupMsgs 随机图片采取队列发送，如果不采用类似复读机大规模发送获取图片信息，会导致Api炸了
