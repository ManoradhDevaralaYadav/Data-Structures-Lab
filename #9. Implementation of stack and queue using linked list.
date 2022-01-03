#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

#define MAX 20
struct Node* start;

void display() {
    if (start == NULL) {
        printf("no elements.\n");
        return;
    }
    printf("elements:");
    for (struct Node* temp = start; temp != NULL; temp = temp->next) {
        printf(" %d", temp->data);
    }
    printf("\n");
}

void append() {
    int item;
    printf("enter data: ");
    scanf("%d", &item);
   
    struct Node* new_node =(struct Node*) malloc(sizeof(struct Node));
    new_node->next = NULL;
    new_node->data = item;
   
    if (start == NULL) {
        start = new_node;
        return;
    }
   
    struct Node* temp = start;
    while (temp->next != NULL) {
        temp = temp->next;
    }
    temp->next = new_node;
}

void pop() {
    if (start == NULL) {
        printf("underflow.");
        return;
    }
    struct Node* temp = start;
    while (temp->next->next != NULL) {
        temp = temp->next;
    }
    free(temp->next);
    temp->next = NULL;
}

void dequeue() {
    if (start == NULL) {
        printf("underflow.");
        return;
    }
    struct Node* temp = start;
    start = start->next;
    free(temp);
}

int main() {
   
    int choice;
    do {
        printf("(1) display\n"
              "(2) append\n"
              "(3) queue delete\n"
              "(4) stack delete\n"
              "(5) exit\n"
              "-->");
        scanf("%d", &choice);
       
        switch(choice) {
            case 1:
                display();
                break;
            case 2:
                append();
                break;
            case 3:
                dequeue();
                break;
            case 4:
                pop();
                break;
            case 5:
                break;
            default:
                printf("invalid choice.\n");
        }
   
    } while (choice != 5);
   
    return 0;
}
