# springboot-reference

**Inversion of Control (IoC)**

  IoC is a principle, which states that the dependent classes should not create objects of the dependency classes. 
  Dependency objects would be created by either the IoC container or the framework and be provided to the dependent object.
  
**Dependency Injection (DI)**

  Dependency Injection is the design princial, which helps to inject dependencies in to depedent objects.
  There are basically three types of dependency injection:
  
    1. Constructor injection: the dependencies are provided through a class constructor.
    2. Setter injection: the client exposes a setter method that the injector uses to inject the dependency.
    3. Field-Based Dependency Injection : We can inject the dependencies by marking them with an @Autowired annotation:
   
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
