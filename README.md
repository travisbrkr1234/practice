# Java
###  Core concepts, definitions, and short examples

## General
-   [Abstraction](#abstraction)
-   [Abstract class](#abstractclass)
-   [Interface](#interface)
-   [Anonymous class](#anonymousclass)
-   [Concrete class](#concreteclass)
-   [Super class](#superclass)
-   [Sub class](#subclass)
-   [Encapsulation](#encapsulation)
-   [Visibility modifiers](#visibilitymodifiers)
-   [Static keyword](#statickeyword)
-   [Autoboxing](#autoboxing)
-   [Enum](#enum)
-   [Exception/ErrorHandling](#exceptionhandling)
-   [Generics](#generics)
-   [Composition](#composition)
-   [Inheritance](#inheritance)
-   [Looping constructs](#loopingconstructs)
-   [Equality testing](#equalitytesting)
-   [Garbage collection](#garbagecollection)
-   [Lambda](#lambda)

## Data Structures
-   [Collections API](#collectionsapi)
-   [Data structures](#datastructuresContainers)
-   [Queue](#queue)
-   [Stack](#stack)
-   [ArrayList](#arraylist)
-   [LinkedList](#linkedlist)

## Design Patterns
-   [Builder](#builder)
-   [Singleton](#singleton)
-   [Facade/Proxy](#facade/proxy)

## Big O Notation
-   [Defensive coding](#defensivecoding)
-   [Sorting/Searching](#sorting searching)
-   [Recursion](#recursion)

## Javascript
-   [Javascript](#javascript)
-   [JavascriptOOP model](#javascriptoop)
-   [Looping constructs](#loopingconstructs)
-   [Functions (First-class, anonymous, closure)](#functions)
-   [Equalitytesting](#equalitytesting)

## SQL
-   [Primary/ForeignKeys](#primaryforeignkeys)
-   [Normalization/Denormalization](#normalizationdenormalization)
-   [1-1, 1-Many, and Many-Many Relationships](#relationships)
-   [Indexes](#indexes)
-   [SQLInjection](#sqlinjection)

## Misc
-	HTML
-	CSS
-	Angular

# Definitions/Explanations

## <a name="abstraction"></a> Abstraction
Moving the implementation away from function. Example the work in assembling/baking a pizza vs ordering a pizza at a restaurant

## <a name="abstractclass"></a> Abstract class
Abstract class may not be completely implemented
[tutorial](http://www.tutorialspoint.com/java/java_abstraction.htm)
The class that extends the abstraction must return the implemented value (fully implement the methods)

## <a name="interface"></a> Interface
Description of the actions that an object can do (like buttons on a television set, or a light switch. You do not care how it happens, just that it happens)
Can only contain method signatures and fields
Cannot contain implementation of the methods

## <a name="anonymousclass"></a> Anonymous class
A class defined and instantiated in a single expresstion using the **new** operator

## <a name="concreteclass"></a> Concrete class
Fully implemented class

## <a name="superclass"></a> Super class
the parent or top level class objects extend from

## <a name="subclass"></a> Sub class
- A child of the super class(extends super) inherits public and protected members of its parent regardless of the package it is in.
- The inherited fields can be used directly, just like any other fields. *Does NOT inherit private members.
- You can declare a field in the subclass with the same firstName as the one in the superclass, thus hiding it (not recommended).
- You can declare new fields in the subclass that are not in the superclass.
- The inherited methods can be used directly as they are.
- You can write a new instance method in the subclass that has the same signature as the one in the superclass, thus overriding it.
- You can write a new static method in the subclass that has the same signature as the one in the superclass, thus hiding it.
- You can declare new methods in the subclass that are not in the superclass.
- You can write a subclass constructor that invokes the constructor of the superclass, either implicitly or by using the keyword super. 
taken from [java doc](https://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html)

## <a name="encapsulation"></a> Encapsulation
Provides protection to data in a particular class, method, or variable

## <a name="visibilitymodifiers"></a> Visibility modifiers
-	**public** - anyone can access
-	**protected** - its class and its children have access
-	**private** - only this class has access
-	*Make global variables private*

## <a name="statickeyword"></a> Static keyword
Static Variables: Variables common to all objects, creates fields and methods that belong to the class rather than to an instance of the class. (Belong to the class instead of a specific instance, shared by all instances)
Static Method: Also do not belong to a specific instance, Access static fields

## <a name="autoboxing"></a> Autoboxing
Automatic conversion between primitive types and their corresponding object wrapper classes (int to Integer; double to Double)

## <a name="enum"></a> Enum
A special data type that enables for a variable to be a set of predefined constants. Such as weekdays or compass directions.

    public enum HealthStatus {
    GOOD_HEALTH(1),
    MEDIOCRE_HEALTH(2),
    BAD_HEALTH(3),
    PREGNANT(4); }
[java doc](https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html)

## <a name="exceptionhandling"></a> Exception/ErrorHandling
Exception: an event that occurs during the execution of a program that disrupts the normal flow of instructions. You will want to handle exceptions to manage errors ** 

[java doc](https://docs.oracle.com/javase/tutorial/essential/TOC.html)

[quiz](https://docs.oracle.com/javase/tutorial/essential/exceptions/QandE/questions.html)

## <a name="generics"></a> Generics

## <a name="composition"></a> Composition

## <a name="inheritance"></a> Inheritance
Sub classes that extend a super class and inherit all of the properties of the super(parent) class

## <a name="loopingconstructs"></a> Looping constructs
???Iteration over data??

## <a name="equalitytesting"></a> Equality testing
== vs .equals()

## <a name="garbagecollection"></a> Garbage collection

## <a name="lambda"></a> Lambda
    employees
             .stream()
             .sorted((e1, e2) -> e1.getHireDate()
				.compareTo(e2.getHireDate()))
             .forEach(e -> System.out.println(e.toString()));

## <a name="datastructures"></a> Data structures
### <a name="collectionsapi"></a> Collections api
A collection is an object that groups multiple elements into a single unit. Collections are used to store, retrieve, manipulate, and communicate aggregate data.
### Data Structures vs. Containers
### <a name="queue"></a> Queue
defn

    example code

### <a name="stack"></a> Stack
defn

    example code
### <a name="arraylist"></a> Array list
defn

    example code

### <a name="linkedlist"></a> Linked list
defn

    example code

# <a name="designpatterns"></a> Design patterns

## <a name="builder"></a> Builder
Builds the object
When you have 4 or more optional parameters

## <a name="singleton"></a> Singleton
Just one exists, checks to see if it exists, when you only want 1

# <a name="bigo"></a> Big O Notation

### <a name="defensivecoding"></a> Defensive coding

### <a name="recursion"></a> Recursion

# <a name="javascript"></a> Javascript
###  <a name="javascriptoop"></a> JavascriptOOP model

### <a name="loopingconstructs"></a> Looping constructs

### <a name="functions"></a> Functions

### <a name="equalitytesting"></a> Equality testing (== vs ===)

# <a name="sql"></a> SQL

## <a name="relationships"></a> Relationships

## <a name="indexes"></a> Indexes

## <a name="sqlinjection"></a> Sql injection




# Misc
Exceptions
https://docs.oracle.com/javase/tutorial/essential/exceptions/QandE/questions.html
1. There is no catch block, try does not require a catch block
2. General exceptions, can be to ambiguous/vague
3. No, this is not a true nested exception because the first will catch the Arithmetic exception
4. a->3 b->1 c->4 d->2
