// operator overloading using friend fuction

#include <iostream>
 
using namespace std;
 
class complex{
    int real, img;
    public:
   
    complex(){
    
        real = 0;
        img = 0;
    }
 
    
    complex(int x, int y){
    
        real = x;
        img = y;
    }

    void display(){
    cout << "The real part: " << real <<"and img part: "<<img << endl<< endl;
    }
 
    friend complex operator+(complex&,complex&);


    friend complex operator+(complex& ob1,complex& ob2)

    {
    complex temp;
 
    
    temp.real = ob1.real + ob2.real;
    temp.img = ob1.img + ob2.img;
 
    }
};
 
int main()
{
    
    complex c1(1,1),c2(5,5);
    c1.display();
    c2.display();
    complex c3;
return 0;
}
