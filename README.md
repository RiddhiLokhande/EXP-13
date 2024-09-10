# EXP-13
## Aim

- To study and implement Constructor Overloading. 


## Software required-

You need to have a C++ compiler installed on your system. Common options include:

- [Microsoft Visual C++](https://visualstudio.microsoft.com/vs/features/cplusplus/)

## Theory
 Constructor Overloading in C++ means that we have more than one constructor ina class with the same name, as long as each have a different list of arguments.
A constructor is called depending upon the number and type of arguments passed.

While creating the object, arguments must be passed to let compiler know, which constructor needs to be called.

#### Code 
(A) <br> 
```cpp
// NAME - RIDDHI LOKHANDE
// PRN - 23070123107
// EXPERIMENT - 13(A) 

# include<iostream>
using namespace std;

class Room
{
    private:
    double length;
    double breadth;

    public:
    Room()                             // Constuctor with no argument 
    {
        length=7.8;
        breadth=5.1;
    }
    Room(double l, double b)      // Constructor with two arguments 
    {
        length=l;
        breadth=b;
    }
    Room(double len)         // Constructor with one argument                 
    {
        length = len;
        breadth=6.3;
    }

    double calculateArea() 
    {
        return length*breadth;
    }
};

int main() 
{
    Room room1, room2(8.2,6.6),room3(8.2);
    cout<<"When no argument is passed: "<<"endl";
    cout<<"Area of room="<<room1.calculateArea()<<endl;
    cout<<"nWhen (8.2,6.6) is passed: "<<endl;
    cout<<"Area of room = "<<room2.calculateArea()<<endl;
    cout<<"nWhen breadth is fixed to 6.3 and (8.2) is passed."<<endl;
    cout<<"Area of room = "<<room3.calculateArea()<<endl;

    return 0;
} 
```

### Output
<img width="622" alt="EXP 13 A OUTPUT" src="https://github.com/user-attachments/assets/eef97f40-a9d2-4edf-aa13-c2bfdfc88f8c">

## CODE 2 
```cpp
// NAME -RIDDHI LOKHANDE
// PRN - 23070123107
// EXPERIMENT -13(B) 

#include<iostream>
using namespace std;

class fetch
{
    int num;
    public:
    fetch()
    {
        num = 3;
    }
    fetch(int x)
    {
        num = x;
    }
    fetch(fetch &b)
    {
        num = b.num;
    }
    void disp()
    {
        cout << num << endl;
    }
};

int main()
{
    fetch f1, f2(6), f3(f1);
    f1.disp();
    f2.disp();
    f3.disp();

    return 0;
}

```
### Output
<img width="616" alt="EXP 13 B OUTPUT" src="https://github.com/user-attachments/assets/1f2bcfee-2cda-4bee-a685-261a4ff31087">

## Conclusion
We learnt the implementation and study of Constructor Overloading. 
