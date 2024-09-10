# Experiment_10

## Aim:
To study and implement Pointer Operations (call by value and call by reference)

## Theory:
There are two ways to call a variable to a function for various operations.

| *Feature*             | *Call by Value*                                    | *Call by Reference*                                    |
|-------------------------|-----------------------------------------------------|----------------------------------------------------------|
| *Definition*          | Passes a copy of the argument's value to the function. | Passes the actual memory address of the argument to the function. |
| *Effect on Arguments* | Changes made to the parameter inside the function do not affect the original argument. | Changes made to the parameter inside the function directly affect the original argument. |
| *Memory Usage*        | Requires more memory as a copy of the argument is created. | Requires less memory as no copy is created; only the reference is passed. |
| *Performance*         | Can be slower due to copying large data structures.  | Faster, especially for large data structures, since no copying is involved. |
| *Syntax*              | Uses the argument directly (e.g., func(x)).        | Uses & to denote a reference parameter (e.g., func(int &x)). |
| *Safety*              | Safer, as original data cannot be accidentally modified. | Riskier, as the original data can be modified, potentially leading to unintended side effects.

## Code:
~~~
a.

#include <iostream>
using namespace std;

//call by value
int a,b;
void swap (int a, int b)
{
    int sw;
    sw = a;
    a = b;
    b = sw;
    cout<<"Swapped Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
}

int main()
{
    int a,b;
    cout<<"Using call by value: "<<endl;
    cout<<"Enter a number: ";
    cin>>a;
    cout<<"Enter another number: ";
    cin>>b;
    cout<<"User Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
    swap(a,b);
    
}
    

b.

#include <iostream>
using namespace std;

//call by value
int a,b;
int *pa, *pb;
void swapr (int *pa, int *pb)
{
    int *psw;
    int sw;
    psw = &sw;
    *psw = *pa;
    *pa = *pb;
    *pb = *psw;
    cout<<"Swapped Values: "<<endl;
    cout<<"a: "<<*pa<<endl;
    cout<<"b: "<<*pb<<endl;
}

int main()
{
    int a,b;
    int *pa, *pb;
    cout<<"Using call by value: "<<endl;
    cout<<"Enter a number: ";
    cin>>a;
    pa = &a;
    cout<<"Enter another number: ";
    cin>>b;
    pb = &b;
    cout<<"User Values: "<<endl;
    cout<<"a: "<<a<<endl;
    cout<<"b: "<<b<<endl;
    swapr(pa,pb);
    
}
~~~


## Outputs:
![image](https://github.com/user-attachments/assets/14670060-4fce-421a-b3ce-b05e3bf2ffc0)


## Conclusion:
→ We learnt about call by value and call by reference in C++.
→ We learnt the use case of each in C++.

