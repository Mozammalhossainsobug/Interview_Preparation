# Object Oriented Programming

### What is OOP?
Object-Oriented Programming or OOPs refers to languages that use objects in programming, they use objects as a primary source to implement what is to happen in the code.

### Basic Concept of OOP?
- Inheritance 
- Polymorphism
- Abstraction
- Encapsulation

### TABLE OF CONTENT:
- Class
- Objects
- Encapsulation
- Abstraction
- Polymorphism
- Inheritance
- Dynamic Binding
- Message Passing

# Define Class and Object
Definning class
```
class Geeks {
    // Access specifier
public:
    // Data  Members
    string geekname;
    // Member Functions()
    void printname() 
    { 
    cout << "Geekname is:" << geekname; 
    }
};
```
Declaring Object 
```
int main()
{
    // Declare an object of class geeks
    Geeks obj1;
    // accessing data member
    obj1.geekname = "Abhi";
    // accessing member function
    obj1.printname();
    return 0;
}
```
Declaring member function outside of the class
```
class MyClass {
public:
    void myFunction(); // function declaration inside the class
};

// function definition outside the class
void MyClass::myFunction() {
    // code for the function
}
```

Setter and Getter Code
```
class Person {
  private:
    std::string name;
    int age;
  
  public:
    void setName(std::string newName) {
      name = newName;
    }
  
    std::string getName() const {
      return name;
    }
  
    void setAge(int newAge) {
      age = newAge;
    }
  
    int getAge() const {
      return age;
    }
};
```
## Access Modifier
There are three access modifiers in C++: 
- public
- private
- protected

**Public:** Members declared as public can be accessed from anywhere in the program, including outside the class.
```
class MyClass {
public:
    int myPublicVar; // a public member variable
    void myPublicFunction() { // a public member function
        // code for the function
    }
};
```
<details><summary>EXPLANATION</summary>
<p>
In this example, the myPublicVar member variable and myPublicFunction() member function are declared as public. This means that they can be accessed from anywhere in the program, including outside the class.
</p>
</details>

**Private:** Members declared as private can only be accessed from within the class. 
```
class MyClass {
private:
    int myPrivateVar; // a private member variable
    void myPrivateFunction() { // a private member function
        // code for the function
    }
public:
    void setMyPrivateVar(int value) { // a public member function that can access myPrivateVar
        myPrivateVar = value;
    }
};
```
<details><summary>EXPLANATION</summary>
<p>
In this example, the myPrivateVar member variable and myPrivateFunction() member function are declared as private. This means that they can only be accessed from within the class. However, the setMyPrivateVar() member function is declared as public, so it can be used to set the value of myPrivateVar from outside the class.
</p>
</details>

**Protected:** Members declared as protected can be accessed from within the class and its subclasses
```
class MyClass {
protected:
    int myProtectedVar; // a protected member variable
    void myProtectedFunction() { // a protected member function
        // code for the function
    }
};

class MySubclass : public MyClass {
public:
    void myPublicFunction() { // a public member function that can access myProtectedVar
        myProtectedVar = 42;
    }
};
```
<details><summary>EXPLANATION</summary>
<p>
In this example, the myProtectedVar member variable and myProtectedFunction() member function are declared as protected. This means that they can be accessed from within the class and its subclasses. The MySubclass subclass is derived from MyClass and declares a myPublicFunction() member function that can access myProtectedVar.
</p>
</details>

