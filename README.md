# Springboot-reference

**Inversion of Control (IoC)**

  IoC is a principle, which states that the dependent classes should not create objects of the dependency classes. 
  Dependency objects would be created by either the IoC container or the framework and be provided to the dependent object.
  
**Dependency Injection (DI)**

  Dependency Injection is the design princial, which helps to inject dependencies in to depedent objects.
  There are basically three types of dependency injection:
   
  reference link : https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring

**Features of the Spring framework**
  - It is lightweight and open sourced.
  - It is modular and can easily connect with other frameworks.
  - It uses aspect-oriented programming (AOP).
  - It relies on IoC principles and helps in DI.
  
**Spring Container :**

   Spring provides the following two distinct types of containers:
   - Spring BeanFactory Container
   - Spring ApplicationContext Containe
   
   ![image](https://user-images.githubusercontent.com/20484835/219436047-40b9af5f-3e35-44bb-ba59-663314fb4e17.png)

**Spring Core :**

  A bean is an object of a class. You can create beans in the following three ways:

  1. XML-based configuration
  2. Java-based configuration
  3. Annotation-based configuration

 In Spring, you can perform DI in three ways:
 
 - Field or property injection
 - Setter injection
 - Constructor injection

  Field or propery injection
  
    @Component
    public class EnglishGreetingService implements GreetingService {
    
      @Autowired
      private TimeService timeService;

      @Override
      public void greet(String name) {
        //Implementation goes here
      }
    }

  Setter injection 
  
    @Component
    public class EnglishGreetingService implements GreetingService {
    
       private TimeService timeService;
       @Autowired
       public void setTimeService(TimeService timeService) {
          this.timeService = timeService;
       }
       @Override
       public void greet(String name) {
         //Implementation goes here
       }
    }
    
  Constructor injection 
  
    @Component
    public class EnglishGreetingService implements GreetingService {
    
       private TimeService timeService;
       @Autowired
       public EnglishGreetingService(TimeService timeService) {
          this.timeService = timeService;
       }
       @Override
       public void greet(String name) {
         //Implementation goes here
       }
    }

  Bean Scope :
  
  - By default, Spring creates one bean per dependency class, but you can control this feature using the @Scope annotatio
  - The default scope of a Spring bean is Singleton. You can change the scope of a bean by making use of the @Scope annotation. 
      
    The different scopes of a bean are as follows:
     
        ● Singleton 
        ● Prototype 
        ● Request 
        ● Session 
        ● Global-session

        Singletone -
        
        @Component
        @Scope(ConfigurableBeanFactory.SCOPE_SINGLETON)
            public class EnglishGreetingService implements GreetingService {
        }
        
        Prototype -
        
        @Component
        @Scope(ConfigurableBeanFactory.SCOPE_PROTOTYPE)
            public class EnglishGreetingService implements GreetingService {
        }
 
    Resolving Conflicts :
    
      If there is more than one class implementing an interface, then you would need to tell Spring whose bean it should inject out of those classes. 
      This can be done by making use of the @Qualifier annotation.
    
      ```
      public class Store {
          @Autowired
          @Qualifier("item1")
          private Item item;
      }
      ```

# Spring Boot :
  
•	Spring Boot can further simplify a developer’s job by handling the boilerplate configuration, which you need to write in the Spring framework. 
  Spring eliminates the need for writing boilerplate code. In addition to this, Spring Boot eliminates the need for writing boilerplate configurations. 

•	Spring Boot takes an opinionated view of building Spring applications, which means that Spring Boot comes with certain default configurations, and it makes some smart assumptions to auto-configure your application.

  ![image](https://user-images.githubusercontent.com/20484835/219474949-de36195f-2418-4c02-9e18-da876ddcb041.png)

•	Spring Boot projects can be created in a number of ways using the following:

  1. Spring Boot Initializr
  2. Spring Starter Project Wizard Of IntelliJ or Eclipse
  3. Spring Boot CLI
  4. Spring Maven Project
  
•	In Spring Boot, you only need to mention the starter POM using the <dependency> tag, which will download all the related dependencies into the project.
  
  Here are some of the commonly used starters: 
    ● $${\color{red}spring-boot-starter }$$ (core starter): Used to enable logging, auto-configuration and YAML 
    ● $${\color{red}spring-boot-starter-web}$$: Used for creating web and RESTful applications with Spring MVC 
    ● $${\color{red}spring-boot-starter-data-jpa}$$: Used for database access using Spring Data JPA with Hibernate 
    ● $${\color{red}spring-boot-starter-security}$$: Used for Spring Security 
    ● $${\color{red}spring-boot-starter-test}$$: Used for testing an application with libraries such as Junit and Mockito 
    ● $${\color{red}spring-boot-starter-aop}$$: Used for Aspect-Oriented Programming with Spring AOP and Aspect

  
•	Using Spring Boot, you can package your web applications as jar files containing both the code and an embedded server. To ensure that your application is running in the auto-configure mode, you can use the @SpringBootApplication annotation.
  
•	A web application is an application that is hosted on a remote server and can be accessed via the Internet.
  
•	The different layers of a web application are as follows: data access layer, service layer and presentation layer. The components responsible for interacting with the database are a part of the data access layer. The service layer consists of all the components that are responsible for processing the client request, based on the business logic, and preparing the response. The presentation layer consists of components that expose the end points to the front-end section of a web application. 
  
•	The components of the data access layer are injected into the components of the service layer. Similarly, the components of the service layer are injected into the components of the controller layer. 
  
•	You can configure the project using the following:
  
  1. Application.properties file
  2. Command-line arguments
  3. Java system properties
  4. Environment variables
  5. YAML files
  
•	By using the @Profile annotation, you can control the bean creation process. You can specify the profiles for which you want the bean to be created, and the bean will be created only when the active profile is set to that profile.


  
