<!--=============================================================================
#     FileName: README.md
#         Desc: 
#       Author: lizherui
#        Email: lzrak47m4a1@gmail.com
#     HomePage: https://github.com/lizherui
#      Version: 0.0.1
#   LastChange: 2013-04-07 13:53:50
#      History:
=============================================================================-->
weibo_python
============

毕业设计中基于给定微博数据的垃圾微博识别，用python开发。

进度：
    对MICRO_BLOG.txt进行了解析

程序运行：
    python main.py

目录结构：

    conf: 项目配置

    data: 数据文件,未上传到github.

    export: 输出文件

    main.py: 主程序

策略：

    某个用户在30秒内连续发布15条微博，则命中垃圾微博策略。

    命中后，垃圾行为映射表中该用户对应次数+1，垃圾微博映射表中这15条微博去重后对应次数+1。

    每次命中策略结束时清空该用户对应的15条微博信息，重新记录。

============
