# push-pop-traverse-on-stack
#include<stdio.h>
#include<conio.h>
#define stack_size 5
void push(void);
void pop(void);
void display(void);
int Top = -1;
int STACK[stack_size];
void main()
{
    int choice;
    while(1)
    {
        printf("\n\n\t\t\t\t\t  M A I N - M E N U");
        printf("\n\n\t\t\t\t\t 1.PUSH ");
        printf("\n\n\t\t\t\t\t 2.POP  ");
        printf("\n\n\t\t\t\t\t 3.DISPLAY");
        printf("\n\n\t\t\t\t\t 4.EXIT");
        printf("\n\n\t\t\t\t\t Enter Your Choice [1-4]");
        scanf("%d",&choice);
        switch (choice)
        {
            case 1:
                 push();
                 break;
            case 2:
                 pop();
                 break;
            case 3:
                display();
                break;
            case 4:
                exit(0);
            default:
                printf("\n\n \t\t\t\t\t Invalid choice");
                break;
                }
    }
}
void push()
{
    int num;
    if(Top == stack_size-1)
    {
      printf("\n\n \t\t\t\t\t Stack full");
    }
  else
  {
      printf("\n\n \t\t\t\t\t Enter value to push");
      scanf("%d",&num);
      STACK[++Top]=num;
  }
}
void pop()
{
    int num;
    if(Top == -1)
    {
      printf("\n\n \t\t\t\t\t stack Under flow");
    }
  else
  {
      num=STACK[Top--];
      printf("\n\n \t\t\t\t\t Deleted item=%d",num);
      scanf("%d",&num);
  }
}
void display()
{
    int i;
    system("cls");
    printf("\n Elements in stack are:");
    for(i=Top;i>=0;i--)
        printf("%d  ",STACK[i]);
    getch();
}
