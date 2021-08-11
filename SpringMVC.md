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

