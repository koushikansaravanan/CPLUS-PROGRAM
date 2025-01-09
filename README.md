
#C++ Programs

**CLASS AND OBJECT PROGRAM**

#include<iostream.h>
#include<conio.h>
class student
{
public:
char name[20];
int roll,m1,m2,m3,tot;
float avg;
void get()
{
cout<<"enter the name:";
cin>>name;
cout<<"enter the roll number:";
cin>>roll;
cout<<"enter the marks:";
cin>>m1>>m2>>m3;
}
void sum()
{
tot=m1+m2+m3;
}
void average()
{
avg=tot/3;
}
void result()
{
if(m1>=35)
{
cout<<"m1 pass\n"<<m1;
}
else
{
cout<<"m1 fail\n"<<m1;
}
if(m2>=35)
{
cout<<"m2 pass\n"<<m2;
}
else
{
cout<<"m2 fail\n"<<m2<<"\n";
}
if(m3>=35)
{
cout<<"m3 pass\n"<<m3<<"\n";
}
else
{
cout<<"m3 fail\n"<<m3<<"\n";
}
}
void display()
{
cout<<"student mark:"<<name<<endl;
cout<<"roll number:"<<roll<<endl;
cout<<"total mark:"<<tot<<endl;
cout<<"average:"<<avg<<endl;
}
};
void main()
{
clrscr();
student s1;
cout<<"\n";
s1.get();
s1.sum();
s1.average();
s1.display();
s1.result();
getch();
}

**TYPE OF FUNCTION PROGRAM**

#include<iostream.h>
#include<conio.h>
#include<math.h>
inline int max(int x,int y)
{
if(x>y)
return(x);
else
return(y);
}
class func
{
public:
void power(int x,int y)
{
cout<<"power value is:"<<pow(x,y);
}
void swap(int a,int b)
{
b=a+b;
a=b-a;
b=b-a;
cout<<"after swap\n e="<<a<<"f="<<b;
}
};
int main()
{
int e,f,c,d,y,n,m,k,ch;
char z;
func obj;
clrscr();
do
{
cout<<"\n Do you want continue(Y\N)";
cin>>z;
if(z=='y')
{
cout<<"\n enter the choice \n 1.swap \n 2.Power \n 3.inline function \n 4.exit\n";
cin>>ch;
switch(ch)
{
case 1:
cout<<"\t swap \n";
cout<<"enter the value of e\n";
cin>>e;
cin>>f;
obj.swap(e,f);
break;
case 2:
cout<<"\t Power of x value \n";
cout<<"enter the value of c\n";
cin>>c;
cout<<"enter the value of d\n";
cin>>d;
obj.power(c,d);
break;
case3:
cout<<"\t inline function\n";
cout<<"enter the value of m\n";
cin>>m;
cout<<"enter the valueof k\n";
cin>>k;
cout<<"maximum:"<<max(m,k);
break;
default:
cout<<"no process \n";
break;
}
}
else
{
cout<<"\n Process is terminated";
break;
}
}
while(ch<=3);
getch();
return(0);
}

**TO IMPLEMENT THE CONCEPT OF FUNCTION OVERLOADING**

#include<iostream.h>
#include<stdlib.h>
#include<conio.h>
#define PI 3.14
class func
{
public:
void area(int a);
void area(int a,int b);
void area(float t,int h,int b);
};
void func:: area(int a)
{
cout<<"area of circle"<<PI*a*a;
}
void func::area(int a,int b)
{
 cout<<"area of rectangle :"<<a*b;
 }
void func:: area(float t,int a,int b)
{
cout<<"area of triangle:"<<t*a*b;
}
void main()
{
int ch;
int a,b,r;
clrscr();
func obj;
cout<<"\n\t\t function overloading";
cout<<"\n 1.area of circle \n 2.area of rectangle \n 3.area of trianglr \n4.exit";
cout<<"\n enter your choice:";
cin>>ch;
switch(ch)
{
case 1:
cout<<"enter your radius of the circle:";
cin>>r;
obj.area(r);
break;
case 2:
cout<<"enter sides of the rectangle:";
cin>>a>>b;
obj.area(a,b);
break;
case 3:
cout<<"enter sides of the triangle:";
cin>>a>>b;
obj.area(0.5,a,b);
break;
case 4:
exit(0);
}
getch();
}

**CONSTRUCTORS PROGRAM**

#include<iostream.h>
#include<conio.h>
class integer
{
private:
int empid;
double empsalary;
char empname[20];
public:
integer();
void display()
{
cout<<"the id of the employee:"<<empid<<"\n";
cout<<"the name of the employee:"<<empname<<"\n";
cout<<"the salary of the employee:"<<empsalary<<"\n";
}
};
integer::integer()
{
cout<<"enter the employee id:";
cin>>empid;
cout<<"enter the employee name:";
cin>>empname;
cout<<"enter the employee salary:";
cin>>empsalary;
}
void main()
{
clrscr();
integer int1;
int1.display();
getch();
}

**TO IMPLEMENT THE CONCEPT OF OPERATOR OVERLOADING PROGRAM**

#include<iostream.h>
#include<conio.h>
class OVERLOAD
{
int a;
int b;
public:
OVERLOAD()
{
a=0;
b=0;
}
void in()
{
cout<<"enter the first number:";
cin>>a;
cout<<"enter the second number:";
cin>>b;
}
void operator--()
{
a=--a;
b=--b;
}
void out()
{
cout<<"The decremented elements are:"<<a<<"and"<<b<<endl;
}
};
void main()
{
clrscr();
OVERLOAD obj;
obj.in();
--obj;
obj.out();
getch();
}

**INHERITANCE PROGRAM**
#include<iostream.h>
#include<conio.h>
class student
{
public:
char name[20],dep[20],clg[20],add[20];
int rollno;
void get()
{
cout<<"enter your name :";
cin>>name;
cout<<"enter your rollno:";
cin>>rollno;
cout<<"enter your department :";
cin>>dep;
cout<<"enter your college name :";
cin>>clg;
cout<<"enter your address :";
cin>>add;
}
};
class display:public student
{
public:
void disp()
{
cout<<"**********************************************";
cout<<"\n**********detail of the student*********";
cout<<"\n******************************************";
cout<<"\nname:"<<name;
cout<<"\nrollno:"<<rollno;
cout<<"\ndepartment:"<<dep;
cout<<"\ncollege:"<<clg;
cout<<"\naddress:"<<add;
}
};
void main()
{
clrscr();
display s;
s.get();
s.disp();
getch();
}

**POLYMORPHISM USING VIRTUAL FUNCTION PROGRAM**

#include<iostream.h>
#include<conio.h>
#include<math.h>
class bank
{
public:
char accname[10],bname[10],city[10],typac[10];
double accno;
virtual void account()
{
}
virtual void display()
{
}
};
class savings:public bank
{
public:
void account()
{
cout<<"\n\t\t\t enter the account name:";
cin>>accname;
cout<<"\n\t\t\t enter the account number:";
cin>>accno;
cout<<"\n\t\t\t enter the bank name:";
cin>>bname;
cout<<"\n\t\t\t enter the city:";
cin>>city;
cout<<"\n\t\t\t enter the type of account:";
cin>>typac;
}
void display()
{
cout<<"\n________________";
cout<<"this is saving account";
cout<<"\n___________________";
}
};
class current:public bank
{
public:
void account()
{
cout<<"\n\t\t\t enter the account name:";
cin>>accname;
cout<<"\n\t\t\t enter the account number:";
cin>>accno;
cout<<"\n\t\t\t enter the bank name:";
cin>>bname;
cout<<"\n\t\t\t enter the city:";
cin>>city;
cout<<"\n\t\t\t enter the type of account:";
cin>>typac;
}
void display()
{
cout<<"\n_________________________________";
cout<<"this is current account";
cout<<"\n____________________________________";
}
};
void main()
{
bank*s[2];
clrscr();
savings a;
current b;
int opt;
s[0]=&a;
s[1]=&b;
clrscr();
cout<<"\n\t\t display the customer details";
cout<<"\n\t\t\t1.savings account \n\t\t\t 2.current account \n\t\n\t\t\t";
cout<<"\n savings account:\n";
s[0]->account();
s[0]->display();
cout<<"\n current account:\n";
s[1]->account();
s[1]->display();
getch();
}

**SWAPPING TWO NUMBERS USING FUNCTION TEMPLATES PROGRAM**

#include<iostream.h>
#include<conio.h>
template<class T>
T add(T&a,T&b)
{
T result=a+b;
return result;
}
void main()
{
clrscr();
int i=10;
int j=20;
float m=2.3;
float n=1.2;
double a=200.05;
double b=295.05;
cout<<"addition of i and j is:"<<add(i,j);
cout<<"\n";
cout<<"addition of m and n is:"<<add(m,n);
cout<<"\n";
cout<<"addition of a and b is:"<<add(a,b);
cout<<"\n";
getch();
}

**WHITESPACE SUPPRESSION PROGRAM**

#include<iostream.h>
#include<fstream.h>
{
ifstream fs;
ofstream ft;
char ch,fname1[20],fname2[20];
cout<<"Enter source file name with extension";
cin>>fname1;
fs.open(fname 1);
if(!fs)
{
cout<<"Error in opening source file....";
}
cout<<"Enter target file name with extension";
cin>>fname2;
ft.open(fname2);
if(!ft)
{
cout<<"Error in opening target file";
fs.close();
}
while(fs.eof()==0)
{
fs>>ch;
ft<<ch;
}
cout<<"file copied successfully";
fs.close();
ft.close();
return 0;
}

**FILE COPY USING COMMAND LINE ARGUMENTS PROGRAM**

#include<iostream.h>
#include<fstream.h>
using NAMESPACE STD;
int main(int argc,char*argv[])
{
if(argc!=3)
cout<<"usage:copy file infile_name outfile_name"<<endl;
else
{
ifstream infile(argv[1],ios::in);
if(!infile)
{
cout<<argv[1]<<"could not be opened"<<endl;
return -1;
}
ofstream outfile(argv[2],ios::out);
if(!outfile)
{
cout<<argv[2]<<"could not be opened"<<endl;
infile.close();
return -2;
}
char c=infile.get();
while(infile)
{
outfile.put(c);
c=infile.get();
}
}
return 0;
}
