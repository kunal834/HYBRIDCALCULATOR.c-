# HYBRIDCALCULATOR.c-
help to perform some scientific and basic calculation 
#include<iostream>
#include<cmath>
using namespace std;
// create 2 calculator
//1. simple calculator -- takes input of 2 numbers using a utility function and perform +,-,*,/ displays the result using another function

//2. scientific calculator--takes input of 2 numbers using a utility function and perform any 4 scientific operation of ypur choics  displays the result using another functio



// create another class hybrid calculator and inherit it using these 2 classes;
//Q1 what type of inheritence are you using?
// ans multiple inheritence 
//Q2 which mode of inheritence are you using?
// ans public 
//Q3 create an object of hybridcalculator and display results of simple and scientific calculator.
//below 
//Q4 how is code reusbility implemented?
// ans reusability implemented because whole member function and function are inherited into hybrid function using simple and scientific calculator
class simplecalculator{
    int a , b;
    public:
    void getdatasimple(){
        cout<< " enter the value of a "<<endl;
        cin>>a;
        cout<<"enter the value of b "<<endl;
        cin>>b;

    }
    void performancesimple(){
        cout<<"the value of a+b is :"<<a+b<<endl;
        cout<<"the value of a-b is :"<<a-b<<endl;
        cout<<"the value of a*b is :"<<a*b<<endl;
        cout<<"the value of a/b is :"<<a/b<<endl ;

    }

};
class scientificcalculator{
    int a , b;
    public:
    void getdatascientific(){
        cout<< " enter the value of a "<<endl;
        cin>>a;
        cout<<"enter the value of b "<<endl;
        cin>>b;

    }
    void performancescientific(){
        cout<<"the value of cos(a) is :"<<cos(a)<<endl;
        cout<<"the value of sin(a) is :"<<sin(a)<<endl;
        cout<<"the value of exp(a) is :"<<exp(a)<<endl;
        cout<<"the value of tan(a) is :"<<tan(a)<<endl ;

    }

};

class hybridcalculator : public simplecalculator, public scientificcalculator{
 
};

int main(){
    //simplecalculator calc;
    //calc.getdatasimple();
    //calc.performancesimple();
    //
    //scientificcalculator sc;
    //sc.getdatascientific();
    //sc.performancescientific();

    hybridcalculator hc;
    hc.getdatasimple();
    hc.performancesimple();
    hc.getdatascientific();       
    hc.performancescientific();

    return 0;
}    
