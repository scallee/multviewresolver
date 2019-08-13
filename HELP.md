# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Apache Maven documentation](https://maven.apache.org/guides/index.html)
* [Spring Boot DevTools](https://docs.spring.io/spring-boot/docs/{bootVersion}/reference/htmlsingle/#using-boot-devtools)
* [Thymeleaf](https://docs.spring.io/spring-boot/docs/{bootVersion}/reference/htmlsingle/#boot-features-spring-mvc-template-engines)
* [Apache Freemarker](https://docs.spring.io/spring-boot/docs/{bootVersion}/reference/htmlsingle/#boot-features-spring-mvc-template-engines)
* [Spring Data JPA](https://docs.spring.io/spring-boot/docs/{bootVersion}/reference/htmlsingle/#boot-features-jpa-and-spring-data)
* [MyBatis Framework](http://www.mybatis.org/spring-boot-starter/mybatis-spring-boot-autoconfigure/)
* [Spring Web Starter](https://docs.spring.io/spring-boot/docs/{bootVersion}/reference/htmlsingle/#boot-features-developing-web-applications)

### Guides
The following guides illustrate how to use some features concretely:

* [Handling Form Submission](https://spring.io/guides/gs/handling-form-submission/)
* [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
* [Accessing data with MySQL](https://spring.io/guides/gs/accessing-data-mysql/)
* [MyBatis Quick Start](https://github.com/mybatis/spring-boot-starter/wiki/Quick-Start)
* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/bookmarks/)

### freemarker配置

## 如果变量为null,转化为空字符串，比如做比较的时候按照空字符串做比较
classic_compatible=true
##去掉多余的空格，非常有用
whitespace_stripping=true
##模板更新事件，设置为1秒，正式环境设置为3600秒
#template_update_delay=3600
##模板更新时间，这里配置是1秒更新一次，正式环境，模板不会改变，可以降这个值很大，提高效率，就是被这个参数害死了，老是不更新
template_update_delay=1
##中国
locale=zh_CN
##编码utf8
default_encoding=utf_8
##url编码utf8
url_escaping_charset=utf_8
##显示日期格式
date_format=yyyy-MM-dd
##显示时间格式
time_format=HH:mm:ss
##显示日期格式
datetime_format=yyyy-MM-dd HH:mm:ss
##数字显示格式
number_format=0.######    
output_encoding=UTF-8


#template_update_delay=1
boolean_format=true,false
#auto_import="/common/index.ftl" as ui
tag_syntax=auto_detect


FreeMarker 配置详解：
spring.freemarker.allow-request-override=false
英语： Set whether HttpServletRequest attributes are allowed to override (hide) controller generated model attributes of the same name.
翻译：设置是否允许HttpServletRequest属性覆盖（隐藏）控制器生成的具有相同名称的模型属性。
spring.freemarker.allow-session-override=false#
英语： Set whether HttpSession attributes are allowed to override (hide) controller generated model attributes of the same name.
翻译：设置是否允许HttpSession属性覆盖（隐藏）同名控制器生成的模型属性。
spring.freemarker.cache=false
英语： Enable template caching.
翻译：启用模板缓存。
spring.freemarker.charset=UTF-8
英语： Template encoding.
翻译：模板编码。
spring.freemarker.check-template-location=true
英语： Check that the templates location exists.
翻译：检查模板位置是否存在。
spring.freemarker.content-type=text/html
英语： Content-Type value.
翻译：内容类型值。
spring.freemarker.enabled=true
英语： Enable MVC view resolution for this technology.
翻译：为此技术启用MVC视图分辨率。
spring.freemarker.expose-request-attributes=false
英语： Set whether all request attributes should be added to the model prior to merging with the template.
翻译：设置在与模板合并之前是否应将所有请求属性添加到模型中。
spring.freemarker.expose-session-attributes=false
英语： Set whether all HttpSession attributes should be added to the model prior to merging with the template.
翻译：设置是否应该在与模板合并之前将所有HttpSession属性添加到模型中。
spring.freemarker.expose-spring-macro-helpers=true
英语： Set whether to expose a RequestContext for use by Spring's macro library, under the name "springMacroRequestContext".
翻译：设置是否公开一个由Spring的宏库使用的名为“springMacroRequestContext”的RequestContext。
spring.freemarker.prefer-file-system-access=true
英语： Prefer file system access for template loading. File system access enables hot detection of template changes.
翻译：首选文件系统访问模板加载。 文件系统访问启用模板更改的热检测。
spring.freemarker.prefix=
英语： Prefix that gets prepended to view names when building a URL.
翻译：在构建URL时，前缀会被视为查看名称。
spring.freemarker.request-context-attribute=
英语： Name of the RequestContext attribute for all views.
翻译：所有视图的RequestContext属性的名称。
spring.freemarker.settings.*=
英语： Well-known FreeMarker keys which will be passed to FreeMarker's Configuration.
翻译：将已知的FreeMarker键将被传递给FreeMarker的配置。
spring.freemarker.suffix=
英语： Suffix that gets appended to view names when building a URL.
翻译：在构建URL时被附加到查看名称的后缀。
spring.freemarker.template-loader-path=classpath:/templates/
英语： Comma-separated list of template paths.
翻译：模板路径列表。
spring.freemarker.view-names=
英语： White list of view names that can be resolved.
翻译：可以解决的视图名称的白名单。
--------------------- 
版权声明：本文为CSDN博主「shicetu」的原创文章，遵循CC 4.0 by-sa版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/shicetu/article/details/79353534


```$xslt
freemarker:
    request-context-attribute: rc
    allow-request-override: false
    cache: true
    enabled: true
    check-template-location: true
    charset: UTF-8
    content-type: text/html
    expose-request-attributes: true
    expose-session-attributes: true
    expose-spring-macro-helpers: false
    template-loader-path: classpath:/templates/   
    suffix: .ftl
    settings:
      classic_compatible: true
      template_exception_handler: ignore
      number_format: #
      prefer-file-system-access: false
--------------------- 
版权声明：本文为CSDN博主「JessyLucky」的原创文章，遵循CC 4.0 by-sa版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/luliuliu1234/article/details/80851259
```