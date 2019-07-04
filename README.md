# Serving Web Content with Spring MVC 学习记录
## 看官方文档
* 用时约0.5小时 [官方地址](https://spring.io/guides/gs/serving-web-content/)
## 编写代码并运行 用时约1.5小时
* 步骤与restful学习过程基本一致

## 总结
* In Spring’s approach to building web sites, HTTP requests are handled by a controller. You can easily identify these requests by the @Controller annotation.
  + 在Spring构建web站点的方法中，HTTP请求由controller处理。您可以通过@Controller注解轻松地识别这些请求。
  + 例子中GreetingController处理地址为“/greeting”的GET请求，通过@GetMapping注解确保HTTP GET请求映射到greeting()方法。、
* The implementation of the method body relies on a view technology, in this case Thymeleaf, to perform server-side rendering of the HTML. Thymeleaf parses the greeting.html template below and evaluates the th:text expression to render the value of the ${name} parameter that was set in the controller.
  + 上面所说的方法实现中依赖一项视图技术，Thymeleaf，用来执行html的服务端渲染。
  + 方法返回名称为“greeting”的view，映射到"greeting.html",Thymeleaf解析这个模板，通过th:text表达式显示controller中设置的${name}参数的值
* A common feature of developing web apps is coding a change, restarting your app, and refreshing the browser to view the change. This entire process can eat up a lot of time. To speed up the cycle of things, Spring Boot comes with a handy module known as spring-boot-devtools.
  + spring boot 提供"spring-boot-devtools" ，可以支持热部署
  
