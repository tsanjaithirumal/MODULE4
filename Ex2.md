# Ex.No:2
# Ex.Name: Write A CPP Program to allocate memory dynamically for long integer array. (Note: p_array = new type [size]; )
## Date:28/08/25

## Aim:
To write a C++ program to allocate memory dynamically for a long integer array using the new operator.

## Algorithm:
1. Start the program.
2. Declare a pointer variable of type long int.
3. Read the size of the array from the user.
4. Dynamically allocate memory for the array using: p_array=new long[size];
5. Read elements into the array.
6. Display the entered elements.
7. Free the allocated memory using the delete[] operator.
8. End the program.




## Program:
```cpp
#include <iostream>
using namespace std; 
class student 
{
    public:
    int n;
    long int *p;
    student()
    {
        cin>>n;
        cout<<"Array Created\n";
    }
    ~student()
    {
        delete []p;
        cout<<"\nArray Deleted";
    }
    void createArray()
    {
        p=new long int[n];
        cout<<"Array Values :\n";
        for(int i=0;i<n;i++)
        {
            cin>>p[i];
        }
        for(int i=0;i<n;i++)
        {
            cout<<p[i]<<" ";
        }
    }
};
int main()
{
    student s;
    s.createArray();
}
```


## Output:
<img width="351" height="303" alt="image" src="https://github.com/user-attachments/assets/9ab6d37a-1d08-4add-b833-7b188897ec64" />



## Result:
The program successfully allocates memory dynamically for a long integer array, stores user input, displays it, and frees the allocated memory using delete[].
