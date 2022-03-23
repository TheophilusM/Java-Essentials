# **Java Essentials**

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
    -- _conditional_
    -- _instanceof - check if type_of a data type_
    -- _precedence of - operator priorities_

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
do while loop
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
    - _**!**methods and fields in an interface can't be declared protected_
  - _**no modifiers**_
    - _can't be accessed by classes in another package_
* Non-Access
  - _**static**_
  - _**final**_
  - _**abstract**_
  - _**synchronized**_
  - _**volatile**_
* Default Access - No Keyword
  - _available to any other class methods in same package_