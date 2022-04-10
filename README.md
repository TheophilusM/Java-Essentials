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
* Time Delay
  - _`Thread.sleep(5*60*10);` - stop execution for 3 seconds_
* Elapsed time
  - _Start and end time measure of a thread in milliseconds_
  - _`long start System.currentTimeMillis();`_ can then get the start and end difference

## **Regular Expressions**
* a special sequence of characters that helps match or find other strings or sets of strings
* can eb used to search, edit, or manipulate text or data
* use a pattern
* Regex package classes
  - _Pattern Class_
  - _Matcher Class_
  - _PatternSyntaxException Class_
* Expression
  - _^, $, \z, re*, [...], e.t.c._
  - _`Pattern p = Pattern.compile(".m")`_ - define match pattern
  - _`Matcher m = p.matcher(".am")`_ - pass string to be matched
  - _`Boolean b = m.matcher()`_ - get match result, true or false
  - _`boolean b = Pattern.matches(".m", ".am")`_ - in one line

## **Variable Arguments**
* allow passing of a variable number of arguments of the same type to a method
* dataType... parameterName
* `static void display(String... values)`
* Can pass 0 or many arguments

## **Java OOPs**
* Objects - an instance of a class, has state and behaviour
* Class - a combination of objects, a blueprint of the objects
* Paradigms - programming techniques to perform certain instructions
* Advantages
  - Inheritance - code reuse-ability in other classes
  - Security - data hiding
  - Project structuring
* Concepts
  * Inheritance
    * Child class inherits methods and variables from parent class
  * Polymorphism
    * _Allow to perform a task defined once in multiple ways_
    * _Overloading and overriding_
  * Abstraction
    * _Allows hiding internal data but show functionality of the program_
  * Encapsulation
    * _Wraps data and program together_
### **_Inheritance_**
* base and parent class
* follow hierarchical order
* Advantage - code reuse-ability
* _**extends**_ keyword
  - _`public class ChildClass extends ParentClass {}`_
  - _`ChildClass objName = new ChildClass()`_ - to use instantiated methods and variables of the parents class
* _**super**_ keyword
  - _similar to this keyword_
  - _to differentiate the members of superClass from the members of subClass, if they have same names_
  - _used to invoke the superClass constructor from subclasses_
  - _`super.varName`_ - to access a variable in parent class
  - _`super.display()`_ - to access method in superClass
  - _`super(values)`_ - to call a parameterized constructor of superClass
    - _`ChildClass objName = new ChildClass(values)`_
  - _`super()`_ - to call a default constructor of superClass
* IS-A Relationship
  - parent and child relationship
  - use the _extends_ - class and _implements_ - interface keywords
  - _`objNName instanceof ParentClass`_ check relationship
  - **_instanceof_**
    - _to determine relationships of classes and/or interfaces_
* HAS-A Relationship
  - _Based mainly on usage_
  - _determines whether a class **HAS-A** certain thing_
  - _helps to reduce duplication of code as well as bugs_
  - _use a reference to the class being checked_
  - _`ClassName c;`_ - class reference in another class, created as an object
  - _`c.varName`_ - accessing the variables in the other class
* Types of inheritance
  - **_single_**
  - **_multi level_**
  - **_hierarchical_**
  - **_multiple_**
    - _NB: Not supported by Java :x:_
### **_Polymorphism_**
* An object showing different stages of its life cycle or performing single action in dff ways
* Allows an interface to be used for general class of actions
* many forms
* Types of Polymorphism
  - _Compile time_
    - **Method overloading - static polymorphism**
    - _allows re-writing or reuse the method again_
    - _methods can be part of same class or subclass but with the same name and different parameters (**type, number and sequence**)_
    - _to call overloaded methods, it's a must to define the type and number of arguments to determine which version of overloaded method is to be called_
    - _Return type may or may not be the same_
    - _Constructors can be overloaded_
  - _Runtime_
    - **Overriding**
    - _To override the functionality of an existing method_
    - _SubClass can override a method in a SupperClass if method not marked final_
    - _Benefit: Ability to define a behavior that s specific to the subclass type_
    - _dynamic  binding_
    - _`ParentClass objName = new ChildClass();`_
### **_Abstraction_**
* The process of hiding the implementation details from the useer
* Only the functionality will be provided to the user
* Achieved using Abstract classes and interfaces
* **Abstract class**
  - _a class containing **`abstract`** keyword in its declaration_
  - _may or may not contain abstract methods i.e., methods without body (`public void get();`)_
  - _if a class have at least one abstract method, the class **must** be declared abstract_
  - _Class used through inheritance, and provided implementations tqo its abstract methods_
  - _if a class is declared abstract, it can't be instantiated_
  - _abstract class can be determined the actual implementations by a child class_
  - _abstract method contains a method signature, but no method body and end with `;`_
  - **Interfaces**
    - A reference type similar to a class.
    - _A class implements an interface, thereby inheriting the abstract methods of the interface_
    - _may contain abstract methods, static methods, and nested types_
    - _A **class** defines attributes and behaviors of an object, an **interface** contains behaviors that a class implements_
    - _Unless the class that implements the interface is abstract, **all** the methods of the interface need to be **defined** in/by the class_
    - _Methods are abstract by default and no need to use the abstract keyword_
    - _Can not be instantiated_
    - _Can not have constructors_
    - _Can implement more than one interface_
    - _Can extend from other interfaces_
      > `interface People {
         public void department();
         void jobRole();
       }`
  - **Extending Interfaces**
    - _An interface can extend another interface or more interfaces_
    - _Child interface inherits the methods of the parent interface_
    - _`public interface MathsTeacher extends Teacher, Person {}`_
### **_Encapsulation_**
* A mechanism of wrapping the data (variables) and code acting on the data (methods) together as single unit
* The variables of a class will be hidden from other class, therefore it is aka data hiding
* To achieve data encapsulation
  - _Declare the variable of a class as private_
  - _Provide public setter and getter methods to modify and view the variables values_
* Benefits
  - _The fields of a class can be read-only or write-only_
  - _Class can have total control over what is stored in its fields_
  - _Users of the class do not know how the class stores its data, class can change the datatype of the field and users of the class do not need to change any of their code_
* **`getVar()`** and **`setName()`**

## **Packages**
* Grouping of classes, interfaces, enumerations, annotations, etc., providing access protection and name space management
* Prevent naming conflict, to control access, to make sure searching/location and usage of classes
* Types
  - _User-defined_
  - _Built-in_
* creating a package > `package Human`
* import keyword
  - _To make the classes and interfaces of another package accessible to the current package_
  - Access ways
    * `...*` - all
    * `...className` - specific class
    * `...fullyQualifiedName` - creating an object reference
      - _`packageName.ClassName objName = new packageName.ClassName()`_
### **Directory structure of the packages**
* Name of package becomes part of the name of the class
* Name of package must match the directory structure where the corresponding bytecode resides

## **Exceptions**
* Is a problem that arises during the execution of a program.
* Some reasons
  - User error
  - Programmer error
  - Network error
  - Physical resource error
* Categories 
  - Checked exception
    - _occur at the compilation time_
  - Unchecked exceptions / Runtime exception
    - _Occur at the execution_
* Exception hierarchy
  - Throwable class
    - Errors
      - _eg. memory exhaustion, can't be handled_
    - Exceptions
      - Can be handled 
      - :1: Runtime exceptions
      - :2: Other 
* Exception methods
  - _`getMessage()`_
  - _`Throwable getCause()`_
  - _`toString()`_
  - _`printStackTrace()`_
  - _`StackTraceElement [] getStackTrace()`_
  - _`Throwable fillinStackTrace()`_
* Multiple Catch blocks
  - _try/catch block_
  - _to catch more than one error type_
  - _takes note of the ExceptionType_
  - _`public void methodName() throws ArithmeticException, IOException`_ keyword
  - _`throw new ArithmeticException("Sorry")`_ keyword
* Finally block
  - _Block of code always executes. irrespective of occurrence of Exception_
  - _Clean-type statements_
  - _Try/Catch/Finally_
* User defined exceptions
  - _Must be a child of Throwable class and also the type_
  - _`class MyExceptionClassName extends Throwable`_
  - _`throw`_ - keyword

## **File and I/O**
* A stream is a sequence of data
* Stream types
  - _InPutStream_ - read data
    - FileInputStream - read byte inputs
      - from the files
      - `InputStream f new FileInputStream("file>?/location")` - reading a file
      - `File f new File("file>?/location")` - creating a file
      - Methods - _close(), finalize(), write()_
    - ByteArrayInputStream - read data that can be read from a number of files
    - FilterInputStream - BufferedInputStream - to improve the performance, DataInputStream - data can be read in future
    - ObjectInputStream - supports primitive types and graphs of java objects supporting serialization interface
  - _OutPutStream_ - write data
    - FileOutputStream
      - `OutputStream f new FileOutputStream("file>?/location")` - create and write data into file
      - Methods - _close(), finalize(), write()_
    - ByteArrayOutputStream
    - FilterOutputStream - BufferedOutputStream, DataOutputStream
    - ObjectOutputStream
  * ByTe Streams
    - _I & O of 8-bit bytes_
    - Example classes - _FileInputStream, FileOutputStream_
    - _try/catch/finally blocks_
* Output Streams
  - FileOutputStream or FileWriter
  - Methods - write()
* Input Streams
  - FileInputStream or FileReader
  - Methods - read()
  - While loop
  - try/catch block
* Character Streams
  - _I & O of 16-bit bytes_
  - Example classes - FileReader and FileWriter
  - Two bytes at a time
  - `FileReader f new FileReader("file>?/location")`
  - `FileWritter f new FileWritter("file>?/location")`
* Standard I/O Streams
  - Standard Input - `Systme.in`
  - Standard Output - `Systme.out`
  - Standard Error - `Systme.err`
* File Navigation & I/O
  - File Class - _creating a new file_
  - FileReader Class - _reading a file_
  - FileWriter Class - _writing to a file_
  - _Relative and absolute path_
  - Methods
    - _mkdir()_
    - _mkdirs()_
  - try/catch ...
* Directory Listing
  - list() method
  - result can be stored in array

## **Java Networking**
* Programs that execute across multiple devices, with all devices connected to each other using a network
* TCP/IP
* Socket programming or URL processing
* Socket types
  - _Data stream socket_
  - _Server socket_
* Server concurrency strategies
  - _Serial_
  - _Forking_
  - _Threaded_
* Classes
  - _ServerSocket_
  - _Socket_

## **Java Multithreading**
* Can develop a program that contains two or more parts that can run concurrently 
  and each part can handle a dff task at the same time making optimal use of available resources.
* Thread Lifecycle
  - New - create
  - Runnable - start
  - Running - run
  - Waiting - sleep/wait
  - Dead- end
* Thread priority
  - ranges 1 to 10
  - default 5
  - can set min and max
* Methods
  - start()
  - run()
  - setName()
  - setPriority()
  - setDaemon()
  - join()
  - interrupt()
  - isAlive()
  - yield()
  - sleep()
  - holdsLock
  - currentThread()
  - dumpStack()
* Creating and using Threads
  - _`extends Thread`_
  - _`implements Runnable`_

## **Serialization & Deserialization**
* Serialization is a process of converting an object into a sequence of bytes which can be persisted to a 
  disk or database or can be sent through streams.
* Deserialization is the reverse process
* The entire process is JVM independent
* Interfaces
  - Serializable
  - Externalizable
* Classes
  - ObjectInputStream
  - ObjectOutputStream

## **Generics**
* Generic methods and Classes enable programmers to specify, with a single method
  declaration, a set of related types respectively.
* Also provide compile-time types safety that allows programmers to catch invalid types at compile time.
* Can write a generic method for sorting an array of objects, then invoke the generic method with Integer arrays,
  Double arrays, String arrays and so on, to sort array elements.

## **Bounded Type Parameters**
* To restrict the kinds of types that are allowed to be passed to a type parameter.
* Declared by listing the type parameter's name. followed by the extends keyword, followed by its upper bound

## **Collection framework**
* Array size is fixed and updating them is costly in terms of performance
* Collections can hold 0 upto multiple objects
* Other operations
  - adding dynamically
  - removing
  - iterating and listing
  - retrieving
  - searching
  - deleting a particular object
* Collection interfaces
  - Lists - _guarantees order, implementations ArrayLists, LinkedLists_
  - Queue
    - Deque
  - Set - _no duplicates, implementations are: HashSet, LinkSet, PreSet_
    - SortedSet
  * *Map - key pair values
    - Sorted Map

## **Iterator Interface**
* Allows user to visit the elements in the container one by one in forward direction only
* Methods
  - boolean hasNext()
  - next()
  - remove()

## **Comparator**
* To order objects of User-Defined classes
* Methods
  - compare()
  - equal()
