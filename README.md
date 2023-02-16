# springboot-reference

**Inversion of Control (IoC)**

  IoC is a principle, which states that the dependent classes should not create objects of the dependency classes. 
  Dependency objects would be created by either the IoC container or the framework and be provided to the dependent object.
  
**Dependency Injection (DI)**

  Dependency Injection is the design princial, which helps to inject dependencies in to depedent objects.
  There are basically three types of dependency injection:
  
    ```
    1. constructor injection: the dependencies are provided through a class constructor.
    2. setter injection: the client exposes a setter method that the injector uses to inject the dependency.
    3. Field-Based Dependency Injection : We can inject the dependencies by marking them with an @Autowired annotation:
    ```
    reference link : https://www.baeldung.com/inversion-control-and-dependency-injection-in-spring
