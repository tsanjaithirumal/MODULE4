
# Ex.No:4
# Ex.Name: Write a CPP program to demonstrate the this pointer.
## Date:28/08/25

## Aim:
To write a C++ program that demonstrates the use of the this pointer.

## Algorithm:
1. Start the program.
2. Define a class Student with private members name and marks.
3. Use a constructor where the this pointer is used to differentiate between class members and parameters with the same name.
4. Define a method display() to print the student details using the this pointer.
5. In main(), create objects of Student and display their details.
6. End the program.


## Program:
```cpp
#include <iostream>
using namespace std;
class Test {
    int x;
public:
    void setX(int x) {
        this->x = x; 
    }
    void display() {
        cout << "x = " << x << endl;
    }
};
int main() {
    Test obj;
    int value;
    cin >> value;
    obj.setX(value);
    obj.display();
    return 0;
}
```



## Output:
<img width="350" height="212" alt="image" src="https://github.com/user-attachments/assets/86e16412-3838-4f67-8e08-d756c1361de3" />



## Result:
The program successfully demonstrates the this pointer by using it to distinguish class members from constructor parameters and by accessing object data inside member functions.
