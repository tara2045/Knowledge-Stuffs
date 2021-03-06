Spring Boot tutorial that I am following:
                http://www.java2novice.com/spring-boot/
                

## Q.  To run spring boot through command line- 
        You will need to build the jar file first. Here is the syntax to run the main class from a jar file.
              1st step:  java -jar path/to/your/jarfile.jar fully.qualified.package.Application
              2nd step:  mvn package && java -jar target/gs-spring-boot-0.1.0.jar
              3rd step:  curl localhost:8080/readiness 
        Also you can pass configuration related properties through command line as shown below. One of the property in the command line 
        is changing server port to 9090.
              java -jar command-line.jar \
                    --server.port=9090 \
                    --site.name=java2novice.com


       
## Q.  What will spring boot make: Jar file or War File?   
        Jar

## Q.  If we are using Spring Boot application, then You will see a new set of RESTful end points added to the application. 
    These are management services provided by Spring Boot. For eg:
        /error
        /actuator/health
        /actuator/info
        /actuator
        /actuator/shutdown
  
## Q. How to run spring boot as a standalsone application(non-web)?
        In spring boot, we need to implement CommandLineRunner interface and override run() method to create standalone application.
        Since we are creating standalone application, include only "spring-boot-starter" in the pom.xml file. Since it implements 
        CommandLineRunner interface, So run() method would be the entry point for the code.
        
## Q.  application.properties in spring boot?
        Spring boot introduced its default application properties named as "application.properties" file and it is auto detected without
        any spring based configurations. We need to place application.properties file inside "src/main/resources" directory.
        
        So, by using this default file, we don’t have to explicitly register a PropertySource, or even provide a path to a property file.
        
        
## Q.  How to configure logback (SLF4J) logging to spring boot applications?
        The Spring Boot is using Logback as a default logger. By default, the SLF4j Logging is included in the Spring Boot starter 
        package. So no additional dependencies are required. You can handle all your logging related configurations with in 
        "application.properties" file itself. Spring boot also allows you to create standard logback.xml file in the resources directory.
        This will override the Spring Boot logging template. All you need to do is, specify your logback configuration file in 
        application.properties as shown below: logging.config=logback.xml
        
        Spring boot also provides profile based loggings. As we discussed in the previous pages, we can maintain multiple properties for each
        profile, so that spring boot will pick the right profile on demand. We can also handle our standard way of xml configurations with 
        logback.xml file. Spring boot supports these configurations. Create a logback-spring.xml in the root of the classpath, to take 
        advantage of the templating features provided by Spring Boot with multiple profiles in it.
        
## Q.  How to update application context path in spring boot?
        By default, spring boot will provide application context path as '/'. We can update the context path in application.properties file. 
        All you need to do is, specify "server.contextPath" property and its value as shown below:
         Open /src/main/resources/application.properties and just add server.contextPath=/shivaSpringBoot
         
         We can also change application context path using command line too. Below example shows how to update the context path by passing 
         it as a system properties: Open Terminal:
                java -jar -Dserver.contextPath=/java2novice myApplicationBundle.jar
                
## Q.  How to disable spring logo banner in spring boot?
        There are various ways to do so. One of the way is to do through application.properties: 
        You can update banner mode in application.properties file as shown below: spring.main.banner-mode=off
        Also you can update it through command line arguments: Open Terminal: 
                         $ java -Dspring.main.banner-mode=off -jar myAppBundle.jar
  
##.  
              
        
        
  
        
