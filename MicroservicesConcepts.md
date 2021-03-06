https://www.edureka.co/blog/microservices-with-spring-boot   3 wotai service clearly deko cha..

https://dzone.com/articles/microservices-with-spring-boot-part-1-getting-star   DZone ko microservices ma Forex Services and Currency 
Conversion services ko lagi cha, dynamic increase of instance ko concept cha 


## What are microservices?
		Microservices are set of services which are fine grained and light weight. In the context of SOA, the services are 
		loosely coupled. The independent services are easy to develop, test, deploy. Services are created using different 
		programming languages, databases. Using microservices, there is chance to continuous delivery and deployment. All the
		microservices communicates using REST. Communication can be HTTP or event based. Even though many other jobs are present,
		Microservices job is unique.

		Microservices architecture allows to avoid monolith application for large system.
		Microservices are the styles that structures an application as a collection of loosely coupled services. 
		Advantages: 
			1.  improves modularity and makes the application easier to understand, develop and test.
			2.  Fault isolation i.e. a process failure should not bring whole system down.
			3.  Independent deployment. 
			4.  Faster release cycle.
			5. Scaling with the cloud. 
		Dis-advantages: 
			1.  Greater need for end to end testing.
			
## Monolith: 
		Monolith applications are typically huge - more 100,000 line of code. They are characterized by:
			-Large Application Size
			-Long Release Cycles
			-Large Teams
			
## Spring Cloud: 
		Spring Cloud provides solutions to cloud-enable your microservices. It leverages and builds on top of some of the 
		Cloud solutions opensourced by Netflix (Netflix OSS).
			Important Spring Cloud Modules are as follows:
				-Dynamically scale up and down. using a combination of
					Naming Server (Eureka)
					Ribbon (Client Side Load Balancing)
					Feign (Easier REST Clients)
				-Visibility and monitoring with
					Zipkin Distributed Tracing
					Netflix API Gateway
				-Configuration Management with Spring Cloud Config Server.
				-Fault Tolerance with Hystrix.

Fault Tolerance with Hystrix.
			
## Advantages of using Spring Cloud:
		1. Ability to handle Service Discovery: This tool manage how processes and services in a cluster can find and talk to 
		one another.
		2. Solves the redundancy issues in distributed systems.
		3. Load balancing: it improves the distribution of workloads across multiple computing resources
			
## Eureka: Netflix Service Discovery Server and Client.
			Eureka Server is using Spring Cloud.
			
## Ribbon: Client-Side Load Balancing
			Based on the load, we can have multiple instances of microservices. Load will be uniformly distributed among 
			these different instances. 

## Hystrix: Fault-tolerance 
		

## How Will You Monitor Multiple Microservices For Various Indicators Like Health?
		Spring Boot provides actuator endpoints to monitor metrics of individual microservices. With the help of actuator, 
		you can check various metrics and monitor your application.
		
## What Does One Mean By Service Registration And Discovery ?
		As all services are registered to the Eureka server and hookup done by calling the Eureka Server, any change in service
		locations need not be handled and is taken care of. 
		Context:When we start a project, we usually have all the configurations in the properties file. As more and more services
		are developed and deployed, adding and modifying these properties become more complex. Some services might go down, 
		while some the location might change. This manual changing of properties may create issues. Eureka Service 
		Registration and Discovery helps in such scenarios.
		
## How Do You Setup Service Discovery?
		 Spring Cloud provide several annotation to make it use easy and hiding lots of complexity.
		 
## How Do You Access A Restful Microservice?
		 We can access a RestFul Microservices suing Load Balanced RestTemplate. RestTemplate can do:
			-If there are multiple RestTemplate you get the right one.
			-It can used to access multiple microservices.
		Microservices can be implemented with or without RESTful APIs, but it’s always easier to build 
		loosely coupled microservices using RESTful APIs.

## Ribbon: Client-Side Load Balancing 			
## How To Achieve Server Side Load Balancing Using Spring Cloud?
		Server side load balancing can be achieved using Netflix Zuul. Zuul is a JVM based router and server side load balancing
		by Netflix. It provides a single entry to our system, which allows a browser, mobile app, or other user interface to
		consume services from multiple hosts without managing cross-origin resource sharing (CORS) and authentication for each 
		one. We can integrate Zuul with other Netflix projects like Hystrix for fault tolerance and Eureka for service discovery, 
		or use it to manage routing rules, filters, and load balancing across your system.
		
##  What are Client certificates?
		A type of digital certificate that is used by client systems to make authenticated requests to a remote server is known as
		the client certificate. Client certificates play a very important role in many mutual authentication designs, providing
		strong assurances of a requester’s identity.

## Annotations used while creating Eureka Server: 
		@EnableEurekaServer - allows us to register microservices to the spring cloud.
		@EnableDiscoveryClient - allows us to query Discovery server to find miroservices.
		@SpringBootApplication - 
		@LoadBalanced - 
		
##  What is DRY in Microservices architecture?
		DRY stands for Don’t Repeat Yourself. It basically promotes the concept of reusing the code. This results in developing 
		and sharing the libraries which in turn result in tight coupling.
		
		
## What is the use of WebMvcTest annotation in Spring MVC applications?
		@WebMvcTest(value = ToTestController.class, secure = false)
		WebMvcTest annotation is used for unit testing Spring MVC Applications in cases where the test objective is to just 
		focus on Spring MVC Components. 
		
## What are different types of Tests for Microservices?
		While working with microservices, testing becomes quite complex as there are multiple microservices working together. 
		So, tests are divided into different levels:
			1. At the bottom level, we have technology-facing tests like- unit tests and performance tests. These are 
			completely automated.
			2. At the middle level, we have tests for exploratory testing like the stress tests and usability tests.
			3. At the top level, we have acceptance tests that are few in number. These acceptance tests help stakeholders 
			in understanding and verifying software features.
			
##  What is End to End Microservices Testing?
		End-to-end testing validates each and every process in the workflow is functioning properly. This ensures that the 
		system works together as a whole and satisfies all requirements.


## What do you understand by Semantic monitoring in Microservices architecture?
		Semantic monitoring, also known as synthetic monitoring combines automated tests with monitoring the application in 
		order to detect business failing factors.
			
##  What is the use of PACT in Microservices architecture?
		PACT is an open source tool to allow testing interactions between service providers and consumers in isolation against 
		the contract made so that the reliability of Microservices integration increases.
			Usage in Microservices:
				-Used to implement Consumer Driven Contract in Microservices.
				-Tests the consumer-driven contracts between consumer and provider of a Microservice.
