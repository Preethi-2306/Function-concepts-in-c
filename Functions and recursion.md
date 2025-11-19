//Functions is what take input and returns results[Function has its declaration and function definition and function calling in main function/any other function]. 
//In function another concept is passing arguments where parameter are the values we give and return value returns the result and it is ad arguments are the values 
//a) void printhi(); - here void means that this function will only performs its definition and it will not return any value 
//b) void printable(int n);- here the function take an table number from n and the function will print the table
//c) int sum(int a,int b);- were here the int means it will return integer value and performs sum operation on int a&b that is a+b and then return its value

#include <stdio.h>
//function declration: to tell that the compiler exists
int sum(int a,int b);
int main() {
    int a,b;
    printf("enter numbers to be added:\n");
    scanf("%d",&a);
    printf("enter numbers to be added:\n");
    scanf("%d",&b);

    //here the function is called where the real usage of function 
    //so here we calling the function and telling which values to sum so now it goes to sum function,and copies  the a value to t and copies b value to h perform t+h 
    //and returns the sum value to s 
    int s=sum(a,b);
    printf("sum:%d",s);
    return 0;
}
//function definition: Now the compiler knows that this function exists and has what work does this function have to do
int sum(int t,int h){
    return t+h;// here if we give 12 still the compiler doest consider it as a error because all the function wants is to return an int value, 
              //where 12 is an interger value so it goes to printf statments and gets executed line by line and when comes to function call it returns the 12 value that's it. But when you give some 4.55 value then an error value occurs.
}

//  TO PRINT AN TABLE:
#include <stdio.h>

void printable(int n);
int main() {
    int n;
    printf("enter number fo the table:");
    scanf("%d",&n);
    printable(n);// this is the actual parameter/argument  because in the function definition you would have any value for n it is to tell that it would be of interger type so whenever we are calling function then only the real values are present in n
    
    return 0;
}
void printable(int n)//this is just formal parament the actual value comes form calling function which gives the argument here it just for formality that there is an integer value n
{
    for(int i=1;i<=12;i++){
        printf("%d\n",i*n);
    }
}

//  TO PRINT AREA OF A CORCLE,SQUARE, RECTANGLE:-
#include <stdio.h>

float areasquare(float side);
float areacircle(float radius);
float arearectangle(float length,float breadth);

int main() {
    float side=4.4;
    
    float length=3.4;
    float breadth=6.6;
    
    float radius=9.9;
    printf("Area of a square:%.2f\n",areasquare(side));
    
    printf("Area of a circle:%.2f\n",areacircle(radius));

    printf("Area of a rectangle:%.2f\n",arearectangle(length,breadth));

    return 0;
}
float areasquare(float side){
return side*side;
}

float areacircle(float radius){
return 3.14*radius*radius;
}

float arearectangle(float length,float breadth){
return length*breadth;
}

// SCOPE [ CONCEPTS OF GLOBAL AND LOCAL VARIABLE]:-  Global = shared everywhere; Static = lives forever but seen only in limited places.
Global Variable – Key Points
->Declared outside all functions. 
-> Accessible everywhere in the program.
->All functions share one single copy->Any function can change it, and the change is visible everywhere.
->Lifetime lasts for the entire program.

Static Variable – Key Points
->Can be inside a function or outside, but needs the keyword static.
->Not accessible everywhere — scope is restricted (function or file).
->Still exists for the entire program, just not visible outside its scope.
->Keeps its value between function calls (if declared inside a function).
->Used when you want persistence but don’t want global access.

//RECURSION:- It can be defined when a function calls itself, to make the big program into smaller parts and the smaller part's result 
//will be given to the called function to process it more to get the result 
-> whatever iteraiton can do , recursion can do the same work 
->disadvantage we can say how iteration has infinite loop(when we give true in do while loop it will crete and infinite loop and memory is fully used up) 
and recursion has stack overflow(means memory is used up, when there is no given base condition given )




