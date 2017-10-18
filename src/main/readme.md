### 此项目作为对java日志的总结项目

> 目前用到的java的日志框架有log4j，logback

<hr/>

> 实现log日志的方式有：

	a)自定义，可以通过System.out.println()的方式将信息输出到控制台（console），也可以通过写入文件的方式将信息写入到文本，
	  代码中通过文本流的方式写入到文本文件中，信息的输出格式可以自定义
	  缺点：格式自定义达不到统一的效果，自定义的实现代码对于很多方面可能考虑不周，比如性能，缓存等等。
	  
	b) 通过引用框架实现，如log4j和logback框架。
	
>logback的实现原理

	a）引入logback的jar包slf4j.jar 和logback.jar（可能会引入不同的版本）
	maven配置如下：
		
```xml
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>jcl-over-slf4j</artifactId>
    <version>1.7.5</version>
</dependency>
<dependency>
	<groupId>ch.qos.logback</groupId>
	<artifactId>logback-classic</artifactId>
	<version>1.1.0</version>
</dependency>
```
生成的jar包如下：
    slf4j-api-1.7.5.jar