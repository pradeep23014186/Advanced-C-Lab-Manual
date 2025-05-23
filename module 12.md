# EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display stack elements using linked list.

## Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
## Program:
```
struct Node   
{  
int data;  
struct Node *next;  
}*head;  
void display()  
{  
    if(head==NULL)
    {
        printf("No elements in the list\n");
        return ;
    }
    struct Node *temp=head;
    while(temp!=NULL)
    {
        printf("%c\n",temp->data);
        temp=temp->next;
    }
}
```
## Output:
![image](https://github.com/user-attachments/assets/06b25bb8-714b-49a3-842b-13a0934ad375)


## Result:
Thus, the program to display stack elements using linked list is verified successfully. 



# EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
## Aim:
To write a C program to pop an element from the given stack using liked list.

## Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
## Program:
```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void pop()  
{ 
    if(head==NULL)
    {
        printf("stack is empty\n");
        return;
    }
    else
    {
        struct Node*temp=head;
        head=head->next;
        free(temp);
    }
}
```
## Output:

![image](https://github.com/user-attachments/assets/515c7193-2a4e-46bd-a800-b92aac06cbe5)




## Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
# EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display queue elements using linked list.
## Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
## Program:
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    if(rear==NULL)
    {
        printf("queue is empty\n");
        return;
    }
    struct Node *temp=front;
    printf("queue elements:\n");
    while(temp!=NULL)
    {
        printf("%c\n",temp->data);
        temp=temp->next;
    }
}
```
## Output:

![image](https://github.com/user-attachments/assets/75aa481b-c3ed-4de8-9f73-0552d767dd28)


## Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
# EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

## Aim:
To write a C program to insert elements in queue using linked list

## Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
## Program:
```
struct Node
{
   int data;
   struct Node *next;
   struct Node *prev;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *newNode=(struct Node*)malloc(sizeof(struct Node));
    newNode->data=data;
    newNode->next=NULL;
    if(rear==NULL)
    {
        front=newNode;
        rear=newNode;
    }
    else
    {
        rear->next=newNode;
        newNode->prev=rear;
        rear=newNode;
    }
}
```
## Output:

![image](https://github.com/user-attachments/assets/81072347-d382-4bab-a32c-138f99b469fb)


## Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



# EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


## Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

## Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

## Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    if(rear==NULL)
    {
        printf("stack is empty\n");
        return;
    }
    else
    {
        printf("%.2f",front->data);
    }
}
```
## Output:

![image](https://github.com/user-attachments/assets/941981de-ba50-4fc8-89f3-bfb89264740e)



## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


