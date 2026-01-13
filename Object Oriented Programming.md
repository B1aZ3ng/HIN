
[[Inheritance]]
[[Polymorphism]]
[[Abstraction]]
[[Composition and Aggregation]]


### Functions vs Methods



Definitions

An object is an abstract entity - a representation of a real world entity 

Each object has its own data and operations or actions it can perform on that data ( methods)


Class
 a class is a template/blueprint for creating objects
 This class identifies what needs to be stored for objects
 and the methods available to access ts data

a name that identifies an entity


# Constructor method:
- A special method that is called(executed) when an object is instantiated so that it initialises its data with specific values
- When the program executes, the constructor produces a resulting object which is an instance of the class
- Constructors are run only once, when an object is created
- In Python the constructor is identified by the name _init_(). It does not have a return type.

  

```python

class Student: #a class is a template/blueprint for creating objects
	def __init__(self, studentID, studentName):
		self.__studentID = studentID #private attribute
		self.__studentName = studentName
		self.__booksBorrowed = []
		self.__numBooks = 0
	
	def getStudentName(self):
		return self.__studentName

```


# Instantiation:
- Creates an object for that class
- An instance of a class is allocated memory to hold the object - meaning the object only exists during runtime
- Classes do not occupy memory space in a program
- Each time we create a new object, a section of RAM is ‘zoned off’ for all the states that may be recorded in that objects, whether they have data in them or not
- 
```python
newStudent = Student(93003, "Smith") #an object created from Student class
print(newStudent.getStudentName())
```
# Instance variables (non Static)

- Each instantiated object has separate instance variables that are properties that the object knows about itself.
- Every instance of an object has its own instance variables, even if the value of some of those variables is identical between some objects.
- Every instance can alter its own instance variables without affecting other instances.

# Static Variables

- A variable or method belonging to the class rather than the instance of the class
- In Python, they are declared to prior to the _init_() function as a class variable.
- There is only one copy of the static variable and this static variable is shared between all instances of the class.
- The static variable is initialised once (at the start of the execution) and retains their values throughout the program’s run.
- The static variable is accessed through the class name and not the instance name.
- Static methods in python are included by passing in the name of the class as a parameter rather than “self”.
- Static methods can only access static variables. They cannot access instance variables directly without an object interference.

```python

class Stu:
	nextStuID = 1000 # Static variable
	def __init__(self, studentName):
		self.__studentName = studentName
		# Use the class name as a prefix to access the static variables
		self.__studentID = Stu.nextStuID
		Stu.nextStuID += 1
		self.__booksBorrowed = []
		self.__numBooks = 0
	
	  
	
	def getStudentID(self):
		return self.__studentID
```
### Accessor Method:
- A special kind of method that is called to read a specific data value of an object
- For example, to access the age of a Person object, the accessor method getAge() may be used to get the value of the age property
### Mutator method:
- A special kind of method that is called to modify a specific data value of an object
- For example, to modify the age of a Person object the mutator method setAge(self, age) may be used to set the value of the age property to be equal to the provided age integer.

### Object access modifiers:
- Private - variables are only accessible within the same class as it is declared (in Python the double underscore indicates that it is private, but does not make it private) (self.__)
- Protected - Allows access to the variable from within the package (project) in which they are created/subclasse
- Public - Allows access to variables from outside of the class/unlimited access (methods are public)
- Static - Refers to variables that act on the class as a whole (and not on individual objects)

# Unified modelling language (UML) diagrams

- The structure of the UML class diagram is
- The ClassName
- The variables (State) and their type
- The methods, their return type and parameters


![[Screenshot 2025-10-23 at 11.09.22 AM.png]]

# Polymorphism
Polymorphism is another term that computer science has taken from biology and refers to something that can take many forms (poly...many; morph...change form). ​

There are two ways of getting polymorphic behaviour when programming with objects: Overriding and overloading. ​

- Overriding occurs when a child class creates a property or method of the same name as the parent class, thereby overriding it.​
    
- Overloading occurs when the one method can take multiple forms. This is generally when the combination and significance of the parameters required can vary. Overloading allows you to make the same function name available to achieve the same purpose, while accepting different inputs. ​

# Advantages of OOP
- Increased modularity: Designing programming code around data and the functions that manipulate it can make it easier to manage large code bases. Objects can be created and modified independently of each other.​
    
- Code reusability: A class, once written, can be imported into other projects and reused many times.​
    
- Encapsulation: helps to build secure programs, as the data is hidden within the objects and prevents interference from external systems. This helps prevent unintended consequences resulting from managing data directly.​
    
- Scale: By allowing increased modularity and reusability, OOP allows projects to scale in size yet remain maintainable.​
    
- Collaboration: Increased modularity also increases the ease for delegating ditferent parts of the project


# Disadvantage of OOP
- Overhead: The overhead of creating an object-oriented solution is often excessive for simpler programs. Object-oriented programs are large in size, which can slow execution in some instances.​
    
- Steep learning curve: The modular nature of the code can make programs complex to understand, especially for novice programmers.​
    
- Increased complexity: Small problems where a procedural approach would suffice can become unnecessarily complex to implement in a purely OOP approach. This complexity can also make projects more challenging to debug and maintain.​
    
- Lack of optimization: The focus of OOP is on providing abstractions to improve modularity. That comes at a cost in terms of organizing code into constructs that are more efficient for the CPU. In performance-critical applications, lower-level paradigms may be more suitable.



# Design Patterns
 - Provide proven and  a 'standard' solution to common problems, improving code structure, maintainability, and scalability
 - They address recurring challenges like resource management (Singleton), object creation and event handling, ensuring a robust and flexible design
 - By using these patterns, developers can leverage collective wisdom and best practices, avoiding reinvention of solutions for well-understood problems
## Singleton:
- When you only have one instance and provides a global point of access to it
- Useful for managing shared resources, such as a database connection or configuration manager where it is only be created once and every other creation links back to the original.
- This avoids potential conflicts or redundant resource usage
- Restricts instantiation to 1 object, ensuring centralised access and consistency.

- ### Characteristics:
	- Private constructor to prevent instantiation
	- Static method to access the single instance
	- Static variable to hold the instance 
	- \_\_new\__ function creates the instance while \_\_init\_\_ initialises the instance
	
	```python
	class Logger():
		_instance = None
		def __new__(cls):
			if cls._instance is None:
				print ("Creating Object")
				cls._instance = super (Logger,cls).__new__(cls)
			else:
				print ("Logger already exists")
			return cls._instance
	L1 = Logger()
	L2 = Logger()
	print (L1 == L2)
	```
	
## Factory Pattern:
- Defines an interface or abstract class for creating objects, allowing subclasses to decide which class to instantiate
- Promotes loose coupling by delegating object creation to a factory, making it easier to extend or modify object types without changing client code
```python
class Cat():
	def __init__():
		self.type = "Cat"
class Dog():
	def __init__():
		self.type = "Dog"

class Factory():
	
```

### Observer Pattern:
- Coordinates Updates across multiple objects which one object's state changes, without tight coupling
- Allows observers to subscribe to a subject, receiving notifications when the subject's state changes.
- 