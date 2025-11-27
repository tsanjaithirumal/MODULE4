
# Ex.No:3
# Ex.Name: Write a CPP program to demonstrate on the object composition (use string data) 
## Date:28/08/25

## Aim:
To write a C++ program to demonstrate object composition where one class is used inside another class, making use of string data.

## Algorithm:
1. Start the program.
2. Define a class Person with a string member name.
3. Create a constructor to initialize the name.
4. Provide a display function.
5. Define another class Employee that contains a Person object as a data member (composition).
6. Initialize the Person object inside Employee using the member initializer list.
7. Add employee-specific details (like designation).
8. Provide a display function to show details.
9. In main(), create an object of Employee and display the details.
10. End the program.


## Program:
```cpp
#include <iostream>
using namespace std;
class A 
{
    public:
    string x;
	A(){
	    x="";
	}
	A(string a){
	    cout<<"Constructor A(string a) is invoked"<<endl;
	    x=a;
	}
};
class B 
{
    string b;
    A objA;
    public:
    B(string a) : objA(a){
        b=a;
    }
    void display(){
        cout << "Data in object of class B = " << b<< endl; 
        cout << "Data in member object of class A in class B = " << objA.x; 
    }
};
int main()
{
    string a;
    cin>>a;
	B objb(a);
	objb.display();
	return 0;
}
```


## Output:
<img width="817" height="259" alt="image" src="https://github.com/user-attachments/assets/14755615-4432-4ab3-9983-fc84da4d9ec2" />



## Result:
The program successfully demonstrates object composition by including a Person object inside the Employee class and initializing it using the member initializer list.
