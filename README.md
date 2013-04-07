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

###介绍
	毕业设计中基于给定微博数据进行垃圾微博识别
###进度
    对MICRO_BLOG.txt解析完毕
    
    总天数:370
    
    总微博数量:2056089
    
    总垃圾微博数量:300555
###程序运行的方法
    python main.py
###目录结构
    conf: 项目配置
    
    data: 原始数据文件,未上传到github
    
    export: 程序输出文件
    
    main.py: 主程序
###垃圾微博判定策略
    某个用户在30秒内连续发布15条微博，则命中垃圾微博策略
    
    命中后，垃圾行为映射表中该用户对应次数+1，垃圾微博映射表中命中的所有微博对应出现次数+1
    
    每次命中策略结束时清空该用户对应的15条微博信息，重新记录
###输出文件的格式说明
	blog_blacklist.txt:垃圾微博内容，出现总次数
	
	blog_length:微博长度，出现总次数
	
	blog_length_stats:微博长度均值，微博长度方差
	
	user_blacklist.txt:用户名，用户昵称，发布垃圾微博的行为总次数
	
	user_everyday_blogs.txt:用户名，用户昵称，每天发布的微博数量
	
    user_everyday_blogs_stats.txt:用户名，用户昵称，基于总天数的发布微博数量的均值和方差，除去未发布任何微博的日期后得到的数量的均值和方差
    
    user_everyday_trush_blogs.txt:用户名，用户昵称，每天发布的垃圾微博数量
	
    user_everyday_trush_blogs_stats.txt:用户名，用户昵称，基于总天数的发布垃圾微博数量的均值和方差，除去未发布任何垃圾微博的日期后得到的均值和方差
    
    user_total_blogs.txt：用户名，用户昵称，用户发布的微博总数量和所占比率
###微博内容分类与比例
####名人名言
    实例:真正的信仰是建立在岩石上的，而其他的一切都颠簸在时间的波浪上.
    
    总微博中所占比例:60%
    
    垃圾微博中所占比例:75%
####节日祝福
    实例:祝大家七夕节快乐

    总微博中所占比例:20%
    
    垃圾微博中所占比例:10%
####社会事件
    实例:风雨同‘舟’、威武不‘曲’，中国加油！舟曲加油！
    
    总微博中所占比例:15%
    
    垃圾微博中所占比例:10%
####励志故事
    实例:产品常不守时。这些日本公司就派人整天待在微软，督促盖茨务必准时交货。盖茨一度还很不理解。后来，盖茨认识了和他同龄的日本计算机界天才西和彦，并成为莫逆之交。微软也于1977年进军日本市场，西和彦一度当上微软的副总经理，他向盖茨讲述了很多在日本做生意的要领：（1）日本人讲究信誉；
    
    总微博中所占比例:5%
    
    垃圾微博中所占比例:5%
 
============
