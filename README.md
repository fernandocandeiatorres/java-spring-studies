# java-spring-studies
This is a quick overview to keep me sharp of the Spring Framework topics that i'm currently studying or already studied.
## Spring Fundamentals

### Inversion Of Control ( IoC )

Spring Framework relies heavily on IoC and DI, the general idea is: The application will talk to the Spring Container ( which is ApplicationContext or a variation of it ) and it'll "ask" to instantiate, configure or assemble the objects, also known as beans. This gives a good understanding of the inversion of control, in traditional programming we would instantiate objects from libraries, etc. In the IoC workflow, we ask the framework to instantiate and manage this objects ( beans ) for us, all behind the scenes.

Quick example on a web app: let's say we have a Customer bean with a name field and we don't want this field to be Null, with a simple "@NotNull" annotation on the field we can make this happen, this showcases how Spring facilitates the development process.

The ApplicationContext (IoC container) also manages the Beans Life Cycles, 


### Dependency Injection ( DI )

Let's start with a pratical example so it's easier to understand: let's say we have a BaseballCoach that implements a helper class (workoutOfTheDayService for example), this helper class is a dependency of the BaseballCoach, in traditional programming we would have to: instantiate the helper class and then instantiate the BaseballCoach class with the helper class. With Spring, we can use dependency injection (setter injection and constructor injection are the most used) to do this work behind the scenes, in the Spring Container. So the Spring object factory do all this behind the scenes for us.

### Annotations

Annotations are a modern way on Spring to delegate what the Spring Container will work on. In the beginning we would create XML config files to define what objects are Beans, etc. With annotations you can let Spring do this configuration work for you behind the scenes, so you can be more productive and less verbose. (@Autowired annotation for DI)
