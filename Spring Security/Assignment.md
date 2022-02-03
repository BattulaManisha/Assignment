# Q1
Design and develop a Spring MVC web application as follows: Create index.jsp page having one hyperlink. When user dicks on that hyperlink, it should call HelloWorldController. Design HelloWorldController class that returns a view helloWorld.jsp Design a hello World jsp page that displays "Hello World" message.
       
       
HELLOCONTROLLER.JAVA
```

          package hellocontroller;
          import org.springframework.stereotype.Controller;
          import org.springframework.ui.Model;
          import org.springframework.web.bind.annotation.RequestMapping;
          import org.springframework.web.bind.annotation.RequestParam;
           public class HelloController {
	  @Controller
	  public class HelloWorldController {
 
	  @RequestMapping("/hello")
	  public String hello(
	        @RequestParam(value = "name", required = false, defaultValue = "World") String name,
	        Model model) {
	    model.addAttribute("name", name);
	    return "helloworld";
	   }
	   }
	   }
```
HELLOPAGE.JSP
```
<html>
 <body> <h1>First Spring MVC Application Demo</h1>
<h2>${welcomeMessage}</h2>   
</body>
</html>
```
