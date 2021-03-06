# Object Oriented Programming

Structuring a Program by Bundling related **Properties** | **Attributes** and **Behaviors** into Individual **Objects**.

### Procedural Programming
- Structures a Program like a Recipe in that it provides a Set of Steps, in the form of **Functions** and **Code Blocks**, that flow Sequentially in order to complete task.

### Object
- A **Collection** of **Data** (**Variables**) and **Methods** (**Functions**) that act on that **Data**.

An Object has two **Characteristics**
1. Attributes | Properties
2. Behaviour | Action


An object can be a person with **Attributes** like a **Name**, **Age** and **Address** and **Behaviours** such as **Walking**, **Talking** and **Running**.

The Concept of **OOP** in Python focuses on Creating **Reusable** Code | **DRY** (Don't Repeat Yourself)


### Class
- A **Blueprint** for **Creating** an **Object**.
- Contains **Attributes** and **Behaviour** of an Object.
- Create **User Defined** Data Structures.
- **class** is a **Keyword** used to **Define Class**.
- **Class Names** are written in **Capitalized Words**.
- Defines **Functions** called as **Methods** (Identifies the Behaviors and Actions than an **Object** created from  the Class can perform with its Data.

**Define** a **Class** 
``` Python
class Student:
    pass
```

### Object
- An Object (**Instance**) is an Instantiation of a Class.
- When Class is Defined, only the **Description** for an Object is **Defined**.
- No **Memory** or **Storage* is allocated.

### Type of Objects 
1. Class Object : Instance of Class
2. Instance Object
3. Function Object : 
4. Method Object

### Constructor 
- Class Functions that begins with double Underscore (\__init\__) are **Special Functions**

### \_\_init\_\_()

- Like a Constructor Method (**Initialize** an **Object**)
- Evertime a New Object is Created, __init__() Sets the **Initial State** of the Object.
- Method is called when any new **Instance** of an **Object**  is Created.
- Initialize the **Attributes** of the Class.
- You can give any number of **Parameters**
- First Parameter will always be a variable **Self**

### self
- Instance Methods can **Access** Attributes and other Methods on the Same Objects.

``` Python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

``` Python
class Student:

    # Class Attribute (Common Attribute for all Class Instances)
    school_name = "IES GNV"
    
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

Class Attributes are Defined Directly beneath the First Line of the Class Name.
- Must always Assigned an **Initial Value**

### Instantiate an Object
- Process of **Creating** an **Object** is called **Instantiation**.
- Creating a **New Object Instance** from a Class is called **Instantiating** an Object.
- Every New Object Instance is located at a different Memory Address.
- The Process to **Create** an **Object** is similar to a **Function Call**. (**ObjectName** = **ClassName()**)

### Methods
- **Functions** defined inside body of a **Class**
- Defines **Behavior** | **Action** of an Object.

### Inheritance
- A Way of Creating a New Class for using Details of an Existing Class without Modifying it.
- The Newly Formed Class is known as a **Derived** Class (**Child Class**)
- The Pre Existing Class is Known as a **Base** Class (**Parent Class**)
- To use the \_\_init\_\_() method of the **Parent Class**, use **super()** Function inside \_\_init\_\_() method of **Child Class**.
- **Inheritance** enables us to **Define** a **Class** that takes all the functionality from a **Parent Class** and allows us to **Add** more.

### Multiple Inheritance
- A **Class** can be **Derived** from more than one **Base Class** 

``` Python
class Base1:
    pass

class Base2:
    pass

class MultiDerived(Base1, Base2):
    pass
```

### Multi Level Inheritance
- Inherit from **Derived Class**
- Features of **Base Class** and **Derived Class** are inherited into a **New Derived Class**.

``` Python
class Base:
    pass

class Derived1(Base):
    pass

class Derived2(Derived1):
    pass
```

### Method Overriding
- When the \_\_init\_\_() method is Defined in both Classes (Parent | Base and Child | Derived) Class, the method in **Derived Class** overrides the **Base Class**.

``` Python
class Base:
    pass
  
class Derived(Base):
    pass

```

### Encapsulation
- **Restrict Access** to Methods and Variables of Class.
- Prevents Data from **Direct Modification**.
- We Denote **Private Attribute** using single underscore(\_) or double underscore (\_\_)

### Polymorphism
- Ability to use a common **Interface** for Multiple forms (**Data Type**)
- Create a Common Function | Method that can be used by two different Classes.

### Important Concepts in Class
1. Define a **Class**.
2. Instantiate an **Object** a **Class**.
3. Use **Attributes** and **Methods** to define the **Properties** and **Behaviors** of an Object.
4. Use **Inheritance** to Create **Child Classes** from a **Parent Class**.
5. Reference a Method in a **Parent Class** using **super()**
6. Check if an **Object** inherits from another Class using **isinstance()** 

### Benefits of Object Oriented Programming
- Makes Program **Easy** to understand
- Class is **Sharable**, Code can be **Reused**.
- Data is **Safe** and **Secure** with **Data Abstraction**.

### Operator Overloading in Python
- Same Operator behaves differently with different **Data Types** according to **context**.
- (**+**) Operator will perform **Arithmetic Addition** on Two Numbers, **Merge** two Lists and **Concatenate** two Strings.
- But it does not Performs Same Operations on **User Defined Class**
- we need to implement **\_\_add\_\_()** Function in the Class.

### Overloading Arithmetic and Logical Operators 

| Operator            | Expression	| Special Function        |
| :---                | :---:       | :---:                   |
| Addition            | p1 + p2	    | p1.\_\_add\_\_(p2)      |
| Subtraction         |	p1 - p2	    | p1.\_\_sub\_\_(p2)      | 
| Multiplication      |	p1 * p2	    | p1.\_\_mul\_\_(p2)      | 
| Power               |	p1 ** p2	| p1.\_\_pow\_\_(p2)      |
| Division            |	p1 / p2	    | p1.\_\_truediv\_\_(p2)  |
| Floor Division      |	p1 // p2	| p1.\_\_floordiv\_\_(p2) | 
| Remainder (modulo)  |	p1 % p2	    | p1.\_\_mod\_\_(p2)      |
| Bitwise Left Shift  |	p1 << p2	| p1.\_\_lshift\_\_(p2)   | 
| Bitwise Right Shift | p1 >> p2	| p1.\_\_rshift\_\_(p2)   |
| Bitwise AND         | p1 & p2	    | p1.\_\_and\_\_(p2)      |
| Bitwise OR          | p1 \| p2    | p1.\_\_or\_\_(p2)       |
| Bitwise XOR         |	p1 ^ p2	    | p1.\_\_xor\_\_(p2)      |
| Bitwise NOT         | ~p1	        | p1.\_\_invert\_\_()     |

### Overloading Comparison Operators 

| Operator	               | Expression | Special Functions     |
| :---                     | :---:      | :---:                 |
| Less than	               | p1 < p2	| p1.\_\_lt\_\_(p2)     |
| Less than or equal to    | p1 <= p2	| p1.\_\_le\_\_(p2)     |
| Equal to	               | p1 == p2	| p1.\_\_eq\_\_(p2)     |
| Not equal to	           | p1 != p2	| p1.\_\_ne\_\_(p2)     | 
| Greater than	           | p1 > p2	| p1.\_\_gt\_\_(p2)     |
| Greater than or equal to | p1 >= p2	| p1.\_\_ge\_\_(p2)     |
