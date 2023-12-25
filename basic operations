#include <stdio.h>
#include <stdio.h>
#include<stdlib.h>
struct node{
    int cf;
    int expo;
    struct node *next;
};

struct node * creat()
{
    struct node *head=0,*last=0,*newnode=0;
        printf("Enter cofficiant & exponent in the list :");
    while(1)
    {
     newnode=(struct node*)malloc(sizeof(struct node));
     scanf("%d",&newnode->cf);
      scanf("%d",&newnode->expo);
       if(newnode->expo==0 || newnode->cf==0)
     break;
    if(head==0)
    {
    head=newnode;
    last=newnode;
    }
    else
    {
        last->next=newnode;
        last=newnode;
    }
    last->next=0;
  }
  return head;
}
struct node *add(struct node *p1,struct node *p2)
{
    struct node *new,*head=0,*last=0;
    
    while(p1!=0 && p2!=0)
    { 
        new=(struct node*)malloc(sizeof(struct node));
    if(p1->expo>p2->expo)
    { 
        new->cf=p1->cf;
       new->expo=p1->expo;
        p1=p1->next;
    }
      else if(p1->expo<p2->expo)
    {
        new->cf=p2->cf;
        new->expo=p2->expo;
        p2=p2->next;
    }
    else if(p1->expo==p2->expo)
    {
         new->expo=p2->expo;
    new->cf=p1->cf+p2->cf;
    p1=p1->next;
    p2=p2->next;
    }
   if(head==0)
   {
       head=last=new;
       last->next=0;
   }
   else
   {
       last->next=new;
       last=new;
       last->next=0;
   }
  }
  while(p1!=0 || p2!=0)
  {
   new=(struct node*)malloc(sizeof(struct node));   
  if(p1==0)
  { 
       new->cf=p2->cf;
        new->expo=p2->expo;
          last->next=new;
       last=new;
       last->next=0;
     p2=p2->next;
  }
  else
  {
      new->cf=p1->cf;
       new->expo=p1->expo;
         last->next=new;
       last=new;
       last->next=0;
     p1=p1->next;
  }
 }
 return head;
}


struct node* sub(struct node *p1,struct node *p2)
{
     struct node *new,*head=0,*last=0;
    
    while(p1!=0 && p2!=0)
    { 
        new=(struct node*)malloc(sizeof(struct node));
    if(p1->expo>p2->expo)
    { 
        new->cf=p1->cf;
       new->expo=p1->expo;
        p1=p1->next;
    }
      else if(p1->expo<p2->expo)
    {
        new->cf= (-p2->cf);
        new->expo=p2->expo;
        p2=p2->next;
    }
    else if(p1->expo==p2->expo)
    {
         new->expo=p2->expo;
    new->cf=p1->cf-p2->cf;
    p1=p1->next;
    p2=p2->next;
    if(new->cf==0)
    continue;
    }
   if(head==0)
   {
       head=last=new;
       last->next=0;
   }
   else
   {  
       last->next=new;
       last=new;
       last->next=0;
   }
  }
  while(p1!=0 || p2!=0)
  {
   new=(struct node*)malloc(sizeof(struct node));   
  if(p1==0)
  { 
       new->cf=-(p2->cf);
        new->expo=p2->expo;
          last->next=new;
       last=new;
       last->next=0;
     p2=p2->next;
  }
  else
  {
      new->cf=p1->cf;
       new->expo=p1->expo;
         last->next=new;
       last=new;
       last->next=0;
     p1=p1->next;
  }
 }
 return head;
}
    struct node *multi(struct node *p1,struct node *p2)
    {
         struct node *new,*head=0,*last=0,*k,*t,*p,*s;
         k=p2;
   
        while(p1!=0)
        {
            for(p2=k;p2!=0;p2=p2->next)
            {
                 new=(struct node*)malloc(sizeof(struct node));   
                if(p1->expo==p2->expo || p1->expo<p2->expo ||p1->expo>p2->expo)
                {
                    new->cf=p1->cf*p2->cf;
                    new->expo=p1->expo+p2->expo;
                }
                 if(head==0)
                {
                  head=last=new;
                  last->next=0;
                }
               else
                {
                 last->next=new;
                 last=new;
                 last->next=0;
                }
            }
            p1=p1->next;
        }
        p=head;
        while(p->next!=0)
        {     
            t=p;
            s=p->next;
            while(s!=0)
            {
                if(p->expo==s->expo)
              {
               p->cf=p->cf+s->cf;
               t->next=s->next;
               free(s);
              s=t->next;
              }
              else
              {
                  t=s;
                  s=s->next;
              }
                
            }
            p=p->next;
        }
        return head;
    }
void travers(struct node *head)
{
        while(head!=0)
        {
            printf("%dx^%d",head->cf,head->expo);
            head=head->next;
            if(head!=0)
            printf("+");
        }
}

void manu()
{
      
    printf("\n\n   ***************************************************************************\n");
    printf("   *****************WELCOME TO POLYNOMIAL LINKED LIST WORLD ******************\n");
    printf("   ***************************************************************************\n\n");
    printf("     Enter 1 for creat first polynomial :   \n");
    printf("     Enter 2 for creat second polynomial :   \n");
    printf("     Enter 3 for addition of both polynomial :   \n");
    printf("     Enter 4 for subtraction of both polynomial :   \n");
    printf("     Enter 5 for multiplication of both polynomial :   \n");
     printf("     Enter 6 for travers first polynomial :   \n");
     printf("     Enter 7 for travers second polynomial :   \n");
      printf("     Enter 8 for travers added polynomial :   \n");
       printf("     Enter 9 for travers subtracted polynomial :   \n");
        printf("     Enter 10 for travers multiplcative polynomial :   \n");
         printf("     Enter 11 for exit from polynomial world :   \n");
          printf("                                                         **** MADE BY PRITI ****\n");
}
int main()
{
    struct node *p1,*p2,*p3,*p4,*p5;
    int n;
    while(1)
    {
        manu();
    scanf("%d",&n);
    switch(n)
    {
        case 1:p1=creat();
        break;
        case 2:p2=creat();
        break;
          case 3: p3=add(p1,p2);
        break;
          case 4: p4=sub(p1,p2);
        break;
          case 5: p5=multi(p1,p2);
        break;
          case 6: travers(p1);
        break;
          case 7: travers(p2);
        break;
          case 8:  travers(p3);
        break;
          case 9: travers(p4);
        break;
          case 10:  travers(p5);
        break;
        case 11:return 0;
    }
   }
}




