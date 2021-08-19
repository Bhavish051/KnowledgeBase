Sping MVC

Java framework for web applications 

Model: Controls the data flow and manipulation
View: Controls how the content is displayed
Controller: Controls what needs to be displayed


@GetMapping(REQ) => Maps GET requests to /REQ to the specified method under it
@RequestParam is used to take parameters for the request

main static html is the home page
@RequestMapping used to display a particular mapping file like a targeted HTML File
When that function is tagged you return the name of the html file you want to return as a String

Default Home page is static html file in the resources folder
the default / mapping goes to the index.html file in the static resources folder

DispatcherServlet basically wires everything in the application together 
example maps the request to the speciifed mapping, handles which view to be displayed at what request
HandlerAdapter used to route the request to the specified method.


@Autowired: Used for getter and setter methods/ Constructors
@Bean: Used to instantiate a Spring Bean Factory Method
Spring Bean Factory: Outside Objects reach out to Bean Factory which creates a new Bean of a the other object which is required.
Spring Beans are basically objects that form a part of the core funcationality.
@Qualifier is used when an object requires multiple properties and some of them are just created for sake of just creating that object so we pass that object as a parameter to the Qualifier Annotation.
@Required used on setter methods to mark compulsary properties
@Value is used to inject property values eg in setters or constructors
@DependsOn to intialize another bean before the annotated one
@Primary to annotate the most frequently used @Component to indicate that the class is a component
@GenerateValue to automatically generate values for example IDs

@Configuration used to indicate that the class has more than one @Bean
@PreDestroy and @PostDestroy used for beaninit and destroy methods
@ComponentScan specify the base packages to check for components
@Repository specifies that the class is responsible for CRUD operations

(mvnw clean package) to build an executable JAR file 
(java -jar target/{JAR_FILE_NAME}) to execute the JAR file

Model Contains the data of the application, can be anything strings, int etc

DB Initialization
JPA: Java Persistence API


Do we use some libraries for CRUD cause the example is a hard coded sql example  : https://spring.io/guides/gs/crud-with-vaadin/
import org.springframework.data.repository.CrudRepository;
Accessing data using JPA
Create an entity class with the attributes specified and getter and setter methods. 
set the appropriate annotations such as @ID, etc

Create an interface extending the CrudRepository for the methods extract data
https://spring.io/guides/gs/accessing-data-jpa/

LEARN ABOUT DEPENDENCY INJECTIONS
Dependency injections allow for loosely coupled programming. Its a way of injecting objects into another as dependencies

Extend Crud Repository on an interface to allow for methods like get, save, delete etc
JPA: Java Persistence API

Dependency Injections:
Design patten to make code loosely coupled
For objects or methods that depend on one another instead of writing code to couple them specify the dependencies in the xml file example the bean employeeDAOImpl depends on jdbcTemplate
dependency is defined in the property attributes of the bean iteself 
So instead of goinf new object you go for getBean


Inversion of Controller 
Used to manage Java Objects which are dependencies of another object
For example, if A is depenedent on B, before creating A we would have B as a dependency so it was pass the control to B to instantiate it and then create A.

Dependency injections are done with the help of inversion of control

Aspect Oriented Programming
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-aop</artifactId>
    <version>5.2.7.RELEASE</version>
</dependency>
@EnableAspectJAutoProxy

Tag with @Aspect and then accordingly @Before(execution) / @After
Types of advice/action before, after, around
@AfterReturing: Used after a certain return value is returned
@AfterThrowing: After an exception is thrown
@Aroung: Both before and after 


Aspect: The class where AOP is to be used
Join Point:  In Spring AOP a join point is always the execution of a method.
Advice: Advices are actions taken for a particular join point. In terms of programming, they are methods that get executed when a certain join point with matching pointcut is reached in the application. @Before, @After, @Around
Pointcut: Pointcut is expressions that are matched with join points to determine whether advice needs to be executed or not. Pointcut uses different kinds of expressions that are matched with the join points and Spring framework uses the AspectJ pointcut expression language.
Target Object: They are the object on which advices are applied. 
AOP proxy: Spring AOP implementation uses JDK dynamic proxy to create the Proxy classes with target classes and advice invocations, these are called AOP proxy classes. 
Weaving: It is the process of linking aspects with other objects to create the advised proxy objects. This can be done at compile time, load time or at runtime. Spring AOP performs weaving at the runtime.




For adding CSS
<link href="<c:url value="Path to file" />" rel="stylesheet">
