[编译运行过程中有问题参考文章](https://blog.csdn.net/yekong1225/article/details/81000446)

### Create File
- `mkdir catalina-home`
> catalina-home 目录下有 `logs`、`conf`、`lib`、`temp`、`webapps`、`work`

> `mv conf/ /catalina-home`

### 编辑配置
```$xslt
Main class设置为org.apache.catalina.startup.Bootstrap

-Dcatalina.home=${tomcat-path}/catalina-home
-Dcatalina.base=${tomcat-path}/catalina-home
-Djava.endorsed.dirs=${tomcat-path}/catalina-home/endorsed
-Djava.io.tmpdir=${tomcat-path}/catalina-home/temp
-Djava.util.logging.manager=org.apache.juli.ClassLoaderLogManager
-Djava.util.logging.config.file=${tomcat-path}/catalina-home/conf/logging.properties
```