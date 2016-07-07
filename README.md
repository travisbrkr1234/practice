# Java
###  Core concepts, definitions, and short examples

## General (re-organize this section)
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
-   [Exception/ErrorHandling](#exceptionhandling)
-   [Generics](#generics)
-   [Composition](#composition)
-   [Inheritance](#inheritance)
-   [Polymorphism](#polymorphism)
-   [Looping constructs](#loopingconstructs)
-   [Equality testing](#equalitytesting)
-   [Garbage collection](#garbagecollection)
-   [Lambda](#lambda)

## Data Types
-   [Primitives](#primitives)
-   [Nonprimitive](#nonprimitive)
-   [Data Type Table](#datatypetable)
-   [Enum](#enum)

## Data Structures
-   [Collections API](#collectionsapi)
-   [Queue](#queue)
-   [Stack](#stack)
-   [ArrayList](#arraylist)
-   [LinkedList](#linkedlist)
-   [SinglyLinked](#singlylinked)
-   [Set](#set)

## Design Patterns
-   [Builder](#builder)
-   [Singleton](#singleton)
-   [Facade](#facade)
-   [Proxy](#proxy)

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
-	Javascript/Angular

# Definitions/Explanations

## <a name="abstraction"></a> Abstraction
Moving the implementation away from function. Example the work in assembling/baking a pizza vs ordering a pizza at a restaurant

## <a name="abstractclass"></a> Abstract class
-   Abstract class may not be completely implemented
-   Cannot be instantiated

[tutorial](http://www.tutorialspoint.com/java/java_abstraction.htm)
The class that extends the abstract class must fully implement the methods (adhere to the contract)

## <a name="interface"></a> Interface
Description of the actions that an object can do (like buttons on a television set, or a light switch. You do not care how it happens, just that it happens)
    
    interface Bicycle {
    void changeCadence(int newValue);
    void changeGear(int newValue);
    void speedUp(int increment);
    void applyBrake(int decrement);
    }

-	Can only contain method signatures and fields
-	Cannot contain implementation of the methods
-	Classes that use the interface use the keyword **implements**
-	Generalized class meant to be a super class

[java doc](https://docs.oracle.com/javase/tutorial/java/concepts/interface.html)

## <a name="anonymousclass"></a> Anonymous class
A class defined and instantiated in a single expresstion using the **new** operator

    HelloWorld frenchGreeting = new HelloWorld() {
    	String name = "tout le monde";
    	public void greet() {
    		greetSomeone("tout le monde");
		}
		public void greetSomeone(String someone) {
			name = someone;
			System.out.println("Salut " + name);
		}
	};

[java doc](https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html)

## <a name="concreteclass"></a> Concrete class
-   Fully implemented class(fields and methods)
-   Opposite of an abstract class
-   Does not contain abstract methods
-   Can be instantiated

## <a name="superclass"></a> Super class
The parent or top level class that objects and other classes extend from
-   Other classes inherit methods/fields from this class

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
-	Provides protection to data in a particular class, method, or variable
-	Technique of making the fields in a class private and providing access to the fields via public methods
-	If a field is declared private, it cannot be accessed by anyone outside of the class, thereby hiding the fields within the class.

## <a name="visibilitymodifiers"></a> Visibility modifiers
-	**public** - anyone can access
-	**protected** - its class and its children have access
-	**private** - only this class has access
-	*Make global variables private* - Always use the most restrictive access within reason
-	If you must have a public field, *use constants*

## <a name="statickeyword"></a> Static keyword
Static Variables: Variables common to all objects, creates fields and methods that belong to the class rather than to an instance of the class. (Belong to the class instead of a specific instance, shared by all instances)
Static Method: Also do not belong to a specific instance, Access static fields

## <a name="autoboxing"></a> Autoboxing
Automatic conversion between primitive types and their corresponding object wrapper classes (int to Integer; double to Double)
[java doc](https://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)

[**reference** Data Type Table](#datatypetable)

## <a name="exceptionhandling"></a> Exception/ErrorHandling
Exception: an event that occurs during the execution of a program that disrupts the normal flow of instructions. You will want to handle exceptions to manage errors ** 

[java doc](https://docs.oracle.com/javase/tutorial/essential/TOC.html)

[quiz](https://docs.oracle.com/javase/tutorial/essential/exceptions/QandE/questions.html)

## <a name="generics"></a> Generics
    List<DataType> list = new ArrayList<>();
    list.add("hello");
    DataType d = list.get(0);

-   Stronger type checks at compile time
-   Data-type safety
-   No need to cast

## <a name="composition"></a> Composition (Has-a)
<font size="3" color="red">**REDO**</font>
-   Contains references to other classes
-   Refers to other class objects as members of the current class

## <a name="inheritance"></a> Inheritance (Is-a)
Sub classes that extend a super class and inherit all of the properties(fields and methods) of the super(parent) class

## <a name="polymorphism"></a> Polymorphism
-   r

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


# Data Types

## <a name="primitives"></a> Primitives
## <a name="nonprimitive"></a> Nonprimitive
A.K.A Objects, reference variables, object references, wrappers
## <a name="datatypetable"></a> Data Type Table

| Type    |  Contains                | Default     | Size   | Range                                               | Wrapper Class |
|:-------:|:-----------------------:|:-----------:|:-------:|:---------------------------------------------------:|:-------------:|
| boolean | true or false           | false       | 1 bit   | NA                                                  | Boolean       |
| char    | Unicode character       | u0000       | 16 bits | \u0000 to \uFFFF                                    | Character     |
| byte    | Signed integer          | 0           | 8 bits  | -128 to 127                                         | Byte          |
| short   | Signed integer          | 0           | 16 bits | -32768 to 32767                                     | Short         |
| int     | Signed integer          | 0           | 32 bits | -2147483648 to 2147483647                           | Integer       |
| long    | Signed integer          | 0           | 64 bits | -9223372036854775808 to 9223372036854775807         | Long          |
| float   | IEEE 754 floating point | 0.0         | 32 bits | &plusmn;1.4E-45 to &plusmn;3.4028235E+38            | Float         |
| double  | IEEE 754 floating point | 0.0         | 64 bits | &plusmn;4.9E-324 to &plusmn;1.7976931348623157E+308 | Double        |

## <a name="enum"></a> Enum
A special data type that enables for a variable to be a set of predefined constants. Such as weekdays or compass directions.

    public enum HealthStatus {
    GOOD_HEALTH(1),
    MEDIOCRE_HEALTH(2),
    BAD_HEALTH(3),
    PREGNANT(4); }
[java doc](https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html)

# Data Structures

## <a name="collectionsapi"></a> Collections api
A collection is an object that groups multiple elements into a single unit. Collections are used to store, retrieve, manipulate, and communicate aggregate data.

## <a name="queue"></a> Queue
    example code

-   Collection for holding elements prior to processing
-   First in First Out (FIFO)


## <a name="stack"></a> Stack
    example code
    
-   Collection for holding elements prior to processing
-   Last in First Out (LIFO)

## <a name="arraylist"></a> Array list
defn

## <a name="linkedlist"></a> Linked list
defn

## <a name="singlylinked"></a> Singly linked
defn

## <a name="set"></a> Set
defn

# <a name="designpatterns"></a> Design patterns

## <a name="builder"></a> Builder
Builds the object
When you have 4 or more optional parameters

## <a name="singleton"></a> Singleton
Just one exists, checks to see if it exists, when you only want 1

## <a name="facade"></a> Facade
Masks the complexity of an entire subsystem which could be composed of many objects

## <a name="proxy"></a> Proxy
Holds a reference to a single object and proxies access to it

# <a name="bigo"></a> Big O Notation
The runtime or efficienct of an algorithm

## <a name="defensivecoding"></a> Defensive coding

## <a name="recursion"></a> Recursion

# <a name="javascript"></a> Javascript
##  <a name="javascriptoop"></a> JavascriptOOP model

## <a name="loopingconstructs"></a> Looping constructs

## <a name="functions"></a> Functions

## <a name="equalitytesting"></a> Equality testing (== vs ===)

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
