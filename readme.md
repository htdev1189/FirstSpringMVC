# Project spring mvc
### khởi tạo bình thường trong IntelliJ (chọn webApp)
- thêm một số dependency cần thiết
> Java Servlet API
> 
> Spring Context
> 
> Spring Web MVC
> 
> Spring Core

### Tạo ccs thư mục cần thiết trong main
> java
> 
> resources

### Chỉnh sửa file web.xml (chú ý servlet-name -- nay dung để tạo file quản lý dispatcher)
> #### <web-app>
> #### <display-name>Archetype Created Web Application</display-name>
> #### <servlet>
> #### <servlet-name>spring-mvc</servlet-name>
> #### <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>    
> #### </servlet>
> #### <servlet-mapping>
> #### <servlet-name>spring-mvc</servlet-name>
> #### <url-pattern>/</url-pattern>
> #### </servlet-mapping>
> #### </web-app>
> 
# Tạo file spring-mvc-servlet.xml trong thư mục WEB-INF (chú ý xyz.htdev là pakages mình cần tạo)

> #### <?xml version="1.0" encoding="UTF-8"?>
> #### <beans xmlns="http://www.springframework.org/schema/beans"
> #### xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
> #### xmlns:context="http://www.springframework.org/schema/context"
> #### xmlns:mvc="http://www.springframework.org/schema/mvc"
> #### xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd
> #### http://www.springframework.org/schema/context http://www.springframework.org/schema/context/spring-context-2.5.xsd
> #### http://www.springframework.org/schema/mvc http://www.springframework.org/schema/mvc/spring-mvc-3.0.xsd">
> #### <context:annotation-config></context:annotation-config>
> #### <context:component-scan base-package="xyz.htdev"></context:component-scan>
> #### </beans>

# Bước tiếp theo
> Khởi tạo class và phương thức trả về
> 
> @Controller
> 
> public class HomeController {
> 
> @RequestMapping(value = "/",method = RequestMethod.POST)
> 
> public String index(){
> 
> return "home.jsp";
> 
> }
> }
> 
> 
# ok xong

