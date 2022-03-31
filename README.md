# **Java Essentials :smirk:**

## **Editions**
* SE - Standard Edition
* EE - Enterprise Edition
* ME - Micro Edition

## **Features**
* OOP
* Platform Independent
* Simple and Secure
* Architectural Neutral
* Portable
* Robust
* Multithreaded
* Integrated
* High Performance
* Distributed
* Dynamic

## **History**
* June 1991
* James  Gosling

## **Basic Syntax**
* Case sensitive
* Class name - uppercase
* Method name - lowercase, camel casing
* Program file name - same as the class name
* correct chars => A to Z, a to z, $, _
* can't use predefined keywords
* white space is ignored by compiler
* comments
  - _// ...single-line..._
  - _/* ...multi-line... */_

## **data types**
* primitive
  - _byte     - 8 bits_
  - _short    - 16 bits_
  - _int      - 32 bits_
  - _long     - 64 bits_
  - _float    - 32 bits_
  - _double   - 64 bits_
  - _char     - 16 bits - single quotes_
  - _boolean  - 1 bit_
* reference - created using constructors
  - _string - double quotes_
  - _arrays_
  - _classes_
* escape sequences
  - _arithmetic (+, -, *, /, ++, --, %)_
  - _relational (==, !=, >, <, >=, <=)_
  - _bitwise (&, |, ^, ~)_
  - _logical (&&, ||, !)_
  - _assignment (=, +=, -=, *=, /=, %=, <<=, >>=, &=, ^=, != )_
  - _misc_ 
    - _conditional_
    - _instanceof - check if type_of a data type_
    - _precedence of - operator priorities_

## **Conditional statements and loops**
* if
* if-else
* if...else-if
* nested if 
* switch
  - _switch expression_
  - _case_
  - _break statement_
  - _continue statement_
  - _default_
* ternary operator
  - `<condition> ? ... : ...`
* while loop
  - _takes condition_
  - _can take update e.g. increment_
* for loop
  - _takes initialization_
  - _takes condition_
  - _can take update e.g. decrement_
  - `for(int x=5; x >= 0; x--) {}`
* enhanced for loop
  - traverse collection of elements
  - `for(int number : numbers) {}` 
* do while loop
  - _takes condition in while block_
  - _can take increment_
* loop control statements
  - _break_
  - _continue_

## **Variables Types**
* local variables
  - _local to a particular method, constructor, block_
  - _not accessible to other methods_
  - _should be assigned a value before they can be used_
* instance variables
  - _declared inside a class but outside methods_
  - _can be accessed by other methods_
  - _can take a default value_
  - _can be accessed directly or through object references of the class they are declared and methods they are used in a class_
* class/static variables
  - _declared inside a class but outside methods with a static keyword_
  - _can be used to private/public/final declare constants_
  - `public static final double PI = 3.14159`
  - _can be called by static on non-static method depending on class location_
  - _can only be changed by the static members_

## **Modifier Types**
* Access
  - _**public**_
    - _if accessed by another package, there is need to import the class into the required class_
    - _all public methods or variables of a class are inherited by its subclasses_
  - _**private**_
    - _accessible only within the same class_
    - _to access them outside a class, there is need to define a public getter & setter methods_
    - _`return this.name`_
    - _`this.name = name`_
  - _**protected**_
    - _can be only be accessed by subclasses in other packages or any class within the same package_
    - _!methods and fields in an interface can't be declared protected_
  - _**no modifiers**_
    - _can't be accessed by classes in another package_
* Non-Access
  - _**static**_
    - _for creating class methods and variables_
    - _can be called with class name, no object reference needed_
    - _static variables_
      - [ ] _aka class variables_
      - [ ] _can be called by both static and non-static variables_
      - [ ] _instance variables can't be called by static methods_
      - [ ] _only a static method can change it_
    - _static methods_
      - [ ] _do not use instance variables instead take the data from parameters and compute them_
      - [ ] _does not allow non-static variables or methods_
      - [ ] _does not allow **this** and **super** keywords_
      - [ ] _execute before the main methods at time of class loading_
  - _**final**_
    - _for finalizing the implementations of classes, methods and variables_
    - _variable declared cannot be changed_
    - _a constructor can initialize an uninitialized variable in a static block only_
    - _a final class can not be inherited_
    - _a subclass can inherit the final method of the parent class but can't override it_
    - _final parameters of a method can't be changed_
  - _**abstract**_
    - _for creating abstract classes and methods_
    - _abstract class can never be instantiated. they can be subclassed_
    - _abstract class can contain both abstract and normal methods_
    - _any class that extends an abstract class must implement all the abstract methods of that class unless it is also an abstract_
    - _an abstract method is a method declared without any implementation, its body is implemented by the subclass_
    - _both abstract class and methods can never be final_
    - _`public absract methodName();`_
  - _**synchronized, transient & volatile**_
    - _used for threads to allow for concurrent task executions_
    - _synchronise_
      - [ ] _to indicate that a method can be accessed by only one thread at a time_
      - [ ] _can be applied with any of the four access level modifiers_
    - _transient_
      - [ ] _used with instance variables to exclude them from serialization - when running a number of threads, state of object stored in streams_
      - [ ] _when object is deserialized, it is reset to its default value - null for reference types, 0 for primitive types_
      - [ ] _can only be used with static keyword_
    - _volatile_
      - [ ] _related to the visibility of variables when a number of threads are running concurrently_
      - [ ] _can't be used with the static keyword_
      - [ ] _value stored in main memory no CPU cache_
* Default Access - No Keyword
  - _available to any other class methods in same package_

## **Methods**
* allow grouped collection of statements to be executed together.
* can return or not return values
  - _`return` or `void` keywords_
* can be invoked with or without parameters
* void
  - _do not return a value_
* return
  - _return a value_
* Passing parameter by value
  - name, type and number of arguments in parameter

## **Arrays**
* Has a fixed size of stored sequential collections
* Stored values are indexed
* Store values of the same type
* Declaration
  - _`dataType[] arrayRefVar = new dataType[arraySize];`_
  - _`dataType[] arrayRefVar = {val1, val2, val3};`_
* Some uses of array methods
  - _sorting_
  - _searching_
  - _comparing_
  - _filtering_
  - _assignment_
* can use a _for_ or _foreach_ loop to iterate/transverse an array
* Array as method argument
  - _pass array parameter: `methodName(new int[]{1,2,3,4});`_
  - _receive array parameters: `public static void methodName(int[] arrayName);`_
* Array as return value
  - _`return arrayName;`_

## **Constructors**
* Initializes an object of the class when it is created
* A method defines the behaviour of a class
* Constructor has the same name as its class and syntactically similar to a method.
* To give initial values to instance variables defined by a class, or perform any other startup procedures required
* A default constructor is by default provided by Java for a class that initializes all member variables to zero.
* `ConstructorName` - same as class name
  - `ConstructorName objName = new ConstructorName();` - _using constructor to create an object_
  - _object will now allow access of values in constructor_
  - _can pass parameters into constructor to update initialized variables  in constructor._
* NB: Constructor is **_invoked_** when it is initialized/instantiated
* Parameterized constructors
  - Constructor will accept a parameter variable with type defined.
* this keyword
  - _used to reference to the object of the current class, within an instance method or constructor._
  - _allows referring to the members of a class such a constructors, variables and methods._
  - _differentiates the instance variable from the local variables if they have the same names, within a constructor or method._
  - _`this.name = name;`_
  - _`this()`_ - invokes the default constructor without arguments
  - _`this.name`_ - refer to the instance variable
  - _`this.methidName()`_ - to call a method of the class

## **finalize() method**
* a method that will be called before an object's final destruction by the garbage collector.
* to ensure an object terminates cleanly
* program threads
  - main - during initialization
  - thread scheduler
  - garbage collector - release resources

## **Nested Classes**
* inner and outer class logic
* a nested class can help create the nested class as private
* the inner class can access methods or members of its outer class
* types
  - _non-static_
    - inner classes
    - method local inner class
    - anonymous inner class
  - _static_
    - static member of outside class 
* **Inner classes**
  - _to provide a sense of security, private class_
  - _inner classes_ type
    - _initiated in the method of the outer class_
    - `InnerClass classOjc = new InnerClass()` - instantiation
    - _can then use the method to access inner class methods_
  - _method local inner class_ type
    - _defining an inner class within a method_
    - _scope of the class is restricted to that method_
    - _instantiated only within the method it is defined_
  - _anonymous inner_ class
    - _inner class declared without a class name, outside a class_
    - _`abstract class AnonymousClass{}`_
    - _can be declared and instantiated at the same time_
    - _used whenever a need to override a method of a class or interface_
* **Static classes**
  - _a static member of the outer class_
  - _can be accessed without instantiating the outer class, using other static members_
  - _`static class NestedClass{}`_ - defining
  - _`MainClass.NestedClass nestedObj = new MainClass.NestedClass()`_ - to access inner class methods...

## **Number Class**
* _Instead of using primitive data types, a wrapper class can be used to deal with Numbers as objects_
* boxing - primitive data type into an object, done by the compiler
* unboxing - inverse of boxing
* Number methods
  - _equals(), round(), random(), tan(), max(), compareTo() e.t.c.,_
* `Integer x = 5;`

## **Character Class**
* `Character ch = new Character('a')`
* `Character.isLowerCase('a')`
* auto boxing and unboxing
* Methods
  - _isLetter(), toLowerCase(), toString() e.t.c._

## **String Class**
* `String message = 'Hello World'`
* format() method returns a String object rather than a PrintStream object
  - _create a formatted strings that can be reused_
  - _String.format()_
  - _takes in two parameters, the value to be printed and arguments to be placed in result_
  - _%f - float, %d - int, %s - string_
* printf(), println()
* String class is immutable once created.
* String Buffer and Builder classes used to modify the Strings.
* Methods
  - _charAt()_
  - _compareTo()_
  - _concat()_

## **Date and Time**
* Methods
  - _after(Date date)_
  - _long getTime()_
  - _`Date date = new Date()`_
  - _`date.toString()`_ - display current date and time
* Formatted Date and Time
  - using _`printf()`_ method starting with _`t`_
  - _`String str = String.format("Current date/time: %tc", new Date())`_
  - %indexNumber$
  - **SimpleDateFormat class**