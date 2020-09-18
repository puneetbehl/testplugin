# A Sample Grails 3 Plugin

This plugin reproduces the following error of using Grails External Config in Grails 3 plugin application:

Problem:

```
java.lang.NoSuchMethodError: org.grails.config.yaml.YamlPropertySourceLoader.load(Ljava/lang/String;Lorg/springframework/core/io/Resource;Ljava/util/List;)Ljava/util/List;
        at grails.plugin.externalconfig.ExternalConfigRunListener.loadYamlConfig(ExternalConfigRunListener.groovy:149)
        at grails.plugin.externalconfig.ExternalConfigRunListener.environmentPrepared(ExternalConfigRunListener.groovy:55)
        at org.springframework.boot.SpringApplicationRunListeners.environmentPrepared(SpringApplicationRunListeners.java:53)
        at org.springframework.boot.SpringApplication.prepareEnvironment(SpringApplication.java:320)
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:295)
        at grails.boot.GrailsApp.run(GrailsApp.groovy:84)
        at grails.boot.GrailsApp.run(GrailsApp.groovy:393)
        at grails.boot.GrailsApp.run(GrailsApp.groovy:380)
        at grails.boot.GrailsApp$run.call(Unknown Source)
        at org.codehaus.groovy.runtime.callsite.CallSiteArray.defaultCall(CallSiteArray.java:47)
        at org.codehaus.groovy.runtime.callsite.AbstractCallSite.call(AbstractCallSite.java:116)
        at org.codehaus.groovy.runtime.callsite.AbstractCallSite.call(AbstractCallSite.java:136)
        at com.objectcomputing.example.Application.main(Application.groovy:10)
```


Solution:
* Either downgrade the plugin version to 1.4.0 
* Update your application to Grails 4 **(recommended)**
