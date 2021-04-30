
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
#define max 5
void enqueue();
void display();
void dequeue();
void peek();
void isEmpty();
void isFull();
int front=-1;
int rear=-1;
int data=0;
int queue[max];
void enqueue()
{
if(front=-1)
front=0;
if(rear==max-1)
{
printf("queue is full");
}
else
{
rear=rear+1;
printf("enter element for queue:");
scanf("%d",&data);
queue[rear]=data;
}
}
void display()
{
if(front==-1||front>rear)
printf("\nqueue is emptyy");
else{
int temp=0;
printf("\nthe elements of the queue are:\n ");
for(temp=front;temp<=rear;temp++)
{
printf("%d \t",queue[temp]);

}
}
}
void dequeue()
{
if(front==-1||front>rear)
printf("\nunderflow condition");
else
{
printf("\nthe element to be removed from queue is :%d",queue[front]);
front=front+1;
}
}
void peek()
{
if(front==-1 && rear==-1)
{
printf("queue is empty\n");
}
else
{
printf("the element at the front is :%d",queue[front]);
}
}
void isEmpty()
{
if(front==-1||front>rear)
printf("queue is empty\n");
}
void isFull()
{
if(rear==max);
printf("queue is full\n");
}
void main()
{
printf("\nqueue implementation");
int choice;

while(1)
{
printf("\n\n");
printf("1.ENQUEUE OPERATION\n");
printf("2.DEQUEUE OPERATION\n");
printf("3.DISPLAY OPERATION\n");
printf("4.PEEK OPERATION\n");
printf("5.ISFULL OPERATION\n");
printf("6.ISEMPTY OPERATION\n");
printf("enter your choice:");
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
case 4:
peek();
break;
case 5:
isEmpty();
break;
case 6:
isFull();
break;
case 7:
printf("end");
exit;
break;
}
}
getch();
}
