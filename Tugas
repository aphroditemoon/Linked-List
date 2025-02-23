#include<stdio.h>
#include<stdlib.h>

struct tnode
{
    int x;
    struct tnode *next;
    struct tnode *prev;
} *head = NULL, *tail = NULL, *curr = NULL;

void push_front(int value)
{
    struct tnode *node = (struct tnode*)malloc(sizeof(struct tnode));
    node->x = value;
    node->prev = NULL;
    node->next = NULL;

    if(head == NULL)
    {
        head = tail = node;
    }
    else
    {
        node->next = head;
        head->prev = node;
        head = node;
    }
}

void push_back(int value)
{
    struct tnode *node = (struct tnode*)malloc(sizeof(struct tnode));
    node->x = value;
    node->next = NULL;
    node->prev = NULL;

    if(head == NULL)
    {
        head = tail = node;
    }
    else
    {
        node->prev = tail;
        tail->next = node;
        tail = node;
    }
}

void push_mid(int value, int searchKey)
{
    if(head == NULL)
    {
        printf("List is empty!\n");
        return;
    }
    
    struct tnode *node = (struct tnode*)malloc(sizeof(struct tnode));
    node->x = value;
    node->next = NULL;
    node->prev = NULL;
    
    curr = head;
    while(curr != NULL)
    {
        if(curr->x == searchKey)
        {
            if(curr == tail)
            {
                push_back(value);
            }
            else
            {
                node->next = curr->next;
                node->prev = curr;
                curr->next->prev = node;
                curr->next = node;
            }
            return;
        }
        curr = curr->next;
    }
    printf("Data %d not found\n", searchKey);
    free(node);
}

void delete_front()
{
    if(head == NULL)
    {
        printf("List is empty\n");
        return;
    }
    
    curr = head;
    if(head == tail) // Hanya satu node
    {
        head = tail = NULL;
    }
    else
    {
        head = head->next;
        head->prev = NULL;
    }
    free(curr);
}

void delete_back()
{
    if(tail == NULL)
    {
        printf("List is empty\n");
        return;
    }
    
    curr = tail;
    if(head == tail) // Hanya satu node
    {
        head = tail = NULL;
    }
    else
    {
        tail = tail->prev;
        tail->next = NULL;
    }
    free(curr);
}

void delete_mid(int searchKey)
{
    if(head == NULL)
    {
        printf("List is empty\n");
        return;
    }
    
    curr = head;
    while(curr != NULL)
    {
        if(curr->x == searchKey)
        {
            if(curr == head)
            {
                delete_front();
            }
            else if(curr == tail)
            {
                delete_back();
            }
            else
            {
                curr->prev->next = curr->next;
                curr->next->prev = curr->prev;
                free(curr);
            }
            return;
        }
        curr = curr->next;
    }
    printf("Data %d not found\n", searchKey);
}

void clearData()
{
    while(head != NULL)
    {
        curr = head;
        head = head->next;
        free(curr);
    }
    tail = NULL;
}

void printList()
{
    if(head == NULL)
    {
        printf("There is No Data\n");
        return;
    }

    curr = head;
    printf("List: ");
    while(curr != NULL)
    {
        printf("%d ", curr->x);
        curr = curr->next;
    }
    printf("\n");
}

int main()
{
    printf("PUSH DATA\n");
    push_front(11);  
    push_back(90);  
    push_front(78);  
    push_back(50);  
    printList(); // 78 11 90 50
    
    printf("\nInsert after 90\n");
    push_mid(22, 90);
    printList(); // 78 11 90 22 50
    
    printf("\nInsert after 78\n");
    push_mid(18, 78);
    printList(); // 78 18 11 90 22 50
    
    printf("\nDelete front\n");
    delete_front();
    printList(); // 18 11 90 22 50
    
    printf("\nDelete back\n");
    delete_back();
    printList(); // 18 11 90 22
    
    printf("\nDelete 90\n");
    delete_mid(90);
    printList(); // 18 11 22
    
    printf("\nDelete all\n");
    clearData();
    printList();
    
    return 0;
}
