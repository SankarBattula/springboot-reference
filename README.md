# springboot-reference

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
