weibo_python
============

毕业设计中基于给定微博数据的垃圾微博识别，用python开发。

进度：
    只对MICRO_BLOG.txt进行了解析

程序运行：
    python main.py

目录结构：

    conf: 项目配置

    data: 数据文件,由于数据太大上传到github太慢，所以放了个空文件，使用时请替换掉这个空文件.

    export: 输出文件，目前有两个，分别为垃圾用户黑名单和垃圾微博黑名单

    main.py: 主程序

策略1：
    若用户发的微博内容包含黑名单关键词，则命中策略

策略2：
    若同一个用户在短时间内发布同样内容的微博，则命中策略

最后，若某用户或某条微博命中策略的次数超过conf里配置的上限,则认定为垃圾用户或垃圾微博，并输出到文件

============
