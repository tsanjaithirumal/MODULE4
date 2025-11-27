# Ex.No:5
# Ex.Name: Write a CPP program using the concept of virtual functions and multiple inheritance to implement the population of Asia.
## Date:28/08/25

## Aim:
To write a C++ program using the concept of virtual functions and multiple inheritance to implement the population of Asia.

## Algorithm:
1. Start the program.
2. Create a base class India with a virtual function population() that prints “Population of India is 150 crore”.
3. Create another base class China with a virtual function population() that prints “Population of China is 200 crore”.
4. Create a derived class Asia that inherits from both India and China.
5. Override the population() function to print “Population of India and China amounts to 75% of Asia's population”.
6. In main(), create base class pointers (India*, China*) and point them to objects of their respective classes.
7. Create a base class pointer pointing to an Asia object to demonstrate runtime polymorphism.
8. Display results.
9. End the program.


## Program:
```cpp
#include <iostream>
using namespace std;
class Asia
{
   public:
   virtual void population(){
       cout << "Population of india and china amounts to 75% of the asia's population" << endl;
   }
};
class India: public Asia
{
    public:
    void population(){
       cout << "Population of india and china amounts to 75% of the asia's population" << endl;
   }
};
class China: public Asia
{
    public:
    void population(){
       cout << "Population of india and china amounts to 75% of the asia's population" << endl;
   }
    
};
int main()
{
  Asia *m;
  India Ind;
  China chna;
  m = &Ind;
  m -> population();
  m = &chna;
  m -> population();
  
}
```

## Output:
<img width="956" height="182" alt="image" src="https://github.com/user-attachments/assets/5dfbf1d7-17e9-4792-a6c6-9960f8c2dce2" />



## Result:
The program successfully demonstrates the use of virtual functions and multiple inheritance by implementing population details of India, China, and Asia with polymorphic behavior.
