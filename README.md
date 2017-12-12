# linked-list
#include<iostream>
using namespace std;
struct Student
{
	char name[50];
	int num[30];
	int age;
	struct Student *next;
};
int main()
{
	struct Student *p,*q,*head;
	char s='Y';
	head=new Student;
	q=head;
	p=q;
	cin>>p->name;
	cin>>p->num;
	cin>>p->age;
	while(cout<<"YorN"<<endl,cin>>s,s=='Y')
	{
		p=new Student;
		q->next=p;
		q=p;
		cin>>p->name;
		cin>>p->num;
		cin>>p->age;
		p->next=NULL;
	}
      p=head;
    while(p!=NULL)
   {
	    cout<<"学号="<<p->num<<endl<<"年龄="<<p->age<<endl<<"姓名="<<p->name<<endl;
	    p=p->next;
   }
      p=head;
    while(p!=NULL)
   {
	    q=p->next;
	    delete p;
	    p=q;
   }
