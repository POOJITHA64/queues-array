# queues-array
#include<stdio.h>
#include<stdlib.h>
int que[100],front=0,rear=0,n=10,i,x;
void enqueue()
{
    if(rear==(n-1))
    {
        printf("que is full");
    }
    else
    {
        printf("enter the element to enqueue\n");
        scanf("%d",&x);
        que[rear]=x;
        rear++;
    }
}
void dequeue()
{
    if(front==rear)
    {
        printf("que is empty");
    }
    else
    {
        printf(" the element  dequeue is: %d\n" ,que[front]);
        front++;
    }
}
void display()
{
    if(front==rear)
    {
        printf("que is empty\n");
    }
    else
    {
        printf("elements in que is:\n");
        for(i=front;i<rear;i++)
        printf("%d\t", que[i]);
        printf("\n");
    }
}
int main()
{
    int choice;
     printf("\n\n***** MENU *****\n");
     do{
     printf("1. enqueue\n2. dequeue\n3. Display\n");
     printf("\nEnter your choice: ");
     scanf("%d",&choice);
     switch(choice)
     {
case 1:
enqueue();
break;
case 2:
    dequeue();
break;
case 3:
     display();
 break;
default:
      printf("\nWrong selection!!! Try again!!!");
      break;
      }
   }while(choice<=4);
}
