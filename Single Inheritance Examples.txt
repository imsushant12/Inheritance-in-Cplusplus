//by Sushant Gaurav

#include<bits/stdc++.h>
#include<iostream>

using namespace std;

class student
{
public:
    int id;
    char name[20];

    void getstudent()
    {
        cout<<"\nEnter name : ";cin>>name;
        cout<<"\nEnter id : ";cin>>id;
    }

    /*
    void putstudent()
    {
        cout<<"\nName is "<<name;
        cout<<"\nID is "<<id;
    }
    */

};

class physical : public student
{
    float weight,height;

public:

    void getphysical()
    {
        cout<<"\nEnter weight : ";
        cin>>weight;
        cout<<"\nEnter height : ";
        cin>>height;
    }

    void putphysical()
    {
        cout<<"\nName is "<<name;
        cout<<"\nID is "<<id;
        cout<<"\nHeight is "<<weight;
        cout<<"\nWeight is "<<height;
    }

};
    
int main()
{
    physical p;
    p.getstudent();
    p.getphysical();
    //p.putstudent();
    p.putphysical();

    return 0;
}




/*

//============================================================================
//PRIVATE MODE:
//============================================================================

#include<bits/stdc++.h>
#include<iostream>
using namespace std;

class student
{
    int id;
    char name[20];
public:
    void getstudent()
    {
        cout<<"\nEnter name : ";cin>>name;
        cout<<"\nEnter id : ";cin>>id;
    }
    void putstudent()
    {
        cout<<"\nName is "<<name;
        cout<<"\nID is "<<id;
    }

};

class physical : private student
{
    float weight,height;
public:
    void getphysical()
    {
        getstudent();
        cout<<"\nEnter weight : ";cin>>weight;
        cout<<"\nEnter height : ";cin>>height;
    }
    void putphysical()
    {
        putstudent();
        cout<<"\nHeight is "<<weight;
        cout<<"\nWeight is "<<height;
    }
};

int main()
{
    physical p;
    p.getphysical();
    p.putphysical();

    return 0;
}

*/









/*

//============================================================================
//                            NEW EXAMPLE
//============================================================================

//PRIVATE MODE
//============================================================================

#include<bits/stdc++.h>
#include<iostream>

using namespace std;

class shape
{

private:

    int w;
    int h;

public:

    int getw()
    {
        cout<<"enter the width : ";
        cin>>w;
        return w;
    }

    int geth()
    {
        cout<<"enter the height : ";
        cin>> h;
        return h;
    }
};

class rectangle: private shape
{

public:

    void display ()
    {
        int a = getw();
        int b = geth();
        cout<< "Area of the rectangle is : "<<a*b;
    }

};

int main()
{
    rectangle r;
    r.display();
    return 0;
}


*/





/*

//============================================================================

//PUBLIC  MODE:



class shape
{
public:

    int w;
    int h;
    void getw()
    {
        cout<<"enter the width : ";
        cin>>w;
    }

    void geth()
    {
        cout<<"enter the height : ";
        cin>> h;
    }
};

class rectangle: public shape
{

public:

    // int getw();              cannot access private data
    // int geth();              cannot access private data

    void display ()
    {
        getw();
        geth();
        cout<< "Area of the rectangle is : "<<w*h;
    }

};

int main()
{
    rectangle r;
    r.display();
    return 0;
}

*/

