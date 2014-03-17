配置指南
=======

当前环境
>1.Windows7 64位
>
>2.Intellij IDEA 13.0.2

工具环境准备
------------

###安装JDK
* [下载JDK 1.6.x](http://www.oracle.com/technetwork/java/javase/downloads/jdk6u38-downloads-1877406.html)
* 解压到某个目录，例如`D:\Program Files\Java\jdk1.6.0_38`
* 设置环境变量，可以设置为用户变量

        JAVA_HOME -> D:\Program Files\Java\jdk1.6.0_38
        CLASSPATH  ->  .;%JAVA_HOME%\lib
        PTAH中加上%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;
        
* 验证安装成功`java -version``javac`输出正常


###安装SVN
* [下载 svn 1.8.8](http://sourceforge.net/projects/win32svn/files/1.8.8/)
* [下载 TortoiseSVN-1.8.5.25224](http://tortoisesvn.net/downloads.html)
* 开始菜单->TortoiseSVN->settings，添加特殊过滤词

        *.o *.lo *.la *.al .libs *.so *.so.[0-9]* *.a *.pyc *.pyo *.rej *~ #*# .#* .*.swp .DS_Store target .settings .project .classpath maven-eclipse.xml *.log *.cache configuration META-INF

###安装Maven
* [下载 maven 2.2.1](http://apache.dataguru.cn/maven/maven-2/2.2.1/binaries/apache-maven-2.2.1-bin.zip)
* 解压到某个目录，例如`D:\Program Files\Java\maven`，进入该目录可以看到bin、boot、conf等目录
* 设置环境变量，可以设置为用户变量

        M2_HOME -> D:\Program Files\Java\maven
        M2  ->  %M2_HOME%\bin
        PTAH中加上%M2_HOME%\bin;
        MAVEN_OPTS -> -Xms256m -Xmx512m (Xms256m表示程序初始分配堆内存为256M，Xmx表示程序可使用的内存)

* 命令行测试maven是否安装成功`mvn --version`

* 添加淘宝的repo，下载[settings.xml](https://raw.github.com/tiemei/opennotes/master/maven/settings.xml)放置到目录`C:\Users\你的用户名\.m2`
* 所有的maven插件会下载到`D:\.m2\repo`，在'<localRepository>$HOME/.m2/repo</localRepository>'进行设置

###安装IntelliJ IDEA
* 当前下载版本为[13.0.2](http://download-ln.jetbrains.com/idea/ideaIC-13.0.2.exe)
