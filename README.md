diamond
=======

#####配合 https://github.com/2767131402/Config_From_DB.git 项目使用
#####使用方法： 将diamond-server 打成war包放到Tomcat下运行
#####WEB地址：http://ip:port/tomcat项目路径  port配置在com.taobao.diamond.common.Constants.DEFAULT_PORT下

diamond设计上的一些问题？
==
1. com.taobao.diamond.common.Constants.CONFIG_HTTP_URI_FILE，获取ServerAddress的值，当前没实现他们的，所以必须自己配置
1. 目前必须在：~/diamond/ServerAddress文件中配置diamond的服务器地址
1. 原来很多都写在Constants中是final的，所以提供了：-D > env > diamond.properties方式来配置一些值

###注： 配置的diamond的服务器地址以修改到——>System.getProperty("user.home") + CONFIG_HTTP_URI_FILE 目录下

client使用
==
* classpath:diamond.properties
 1. HTTP_URI_FILE=http://10.200.51.105:9900/diamond-server/config.co 配置获取dataId数据的url
