/********************************/
/******DOUBLY LINKED LIST INSERTION DELETION DISPLAY COUNT OPERATIONS****/
/********************************/


#include <iostream>
using namespace std;

class node{
    public:
    int data;
    node* next=NULL;
    node* prev=NULL;
    node(int value)
    {
        data=value;
    }
};

node *head=NULL;node* temp=NULL;

void insertnodeatbeg(int value)
{
    node* newnode =new node(value);
    temp=head;
    if(head==NULL)
    {
        head=newnode;
    }else{
        newnode->next=head;
        head->prev=newnode;
        head=newnode;
    }
}


void insertnodeatend(int value)
{
    temp=head;
     node* newnode =new node(value);
      if(head==NULL)
    {
        head=newnode;
    }else{
        newnode->next=head;
        head->prev=newnode;
        head=newnode;
    }
     
    
}

void insertnodeatanypos(int value,int pos)
{
    temp=head;
    node* newnode =new node(value);
    int i=1;
    while(i<pos)
    {
        temp=temp->next;
        i++;
    }
    newnode->next=temp->next;
    temp->next->prev=newnode;
    temp->next=newnode;
    newnode->prev=temp;
    
}
    


void display() {
     temp = head;
    while (temp != NULL) {
        cout << temp->data << endl;
        temp = temp->next;
    }
}

void deletenodeatbeg()
{
    temp=head;
    head=head->next;
    head->prev=0;
    temp->next=0;
    delete(temp);
}

void deletenodeatend()
{
    temp=head;
    node* current;
      while(temp->next!=NULL)
    {
         current=temp;
        temp=temp->next;
       
    }
    current->next=0;
    temp->prev=0;
    delete(temp);
    
}


void deletenodeatanypos(int pos)
{
    temp=head;int i=1;
    while(i!=pos)
    {   
      temp=temp->next;
      i++;
        
    }
      temp->next->prev=temp->prev;
        temp->prev->next=temp->next;
        temp->next=0;
        temp->prev=0;
        delete(temp);
}

void length()
{
    temp=head;
    int count=0;
    while(temp!=NULL)
    {
        
        temp=temp->next;
        count=count+1;
          
    }
    cout<<"length of linkedlist is "<<count;
}



int main()
{
   insertnodeatbeg(1);
   insertnodeatbeg(3);
  // insertnodeatbeg(5);
   //insertnodeatbeg(7);
   //insertnodeatbeg(9);
   //insertnodeatbeg(11);
   
  //insertnodeatend(11);
  ///insertnodeatend(9);
  //insertnodeatend(7);
  //insertnodeatend(5);
  insertnodeatend(3);
  insertnodeatend(1);
  
  //insertnodeatanypos(69,2);
   display();
   
   //deletenodeatbeg();
   //deletenodeatend();
   deletenodeatanypos(3);
   cout<<"elements after deletion";
    display();
    length();
   

    return 0;
}
