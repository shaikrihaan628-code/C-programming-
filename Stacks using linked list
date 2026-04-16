#include <stdio.h>
#include <stdlib.h>

struct node {
    int data;
    struct node *next;
};

struct node *top = NULL;

void push(int value) {
    struct node *newNode;
    newNode = (struct node *)malloc(sizeof(struct node));

    if (newNode == NULL) {
        printf("Memory not available\n");
        return;
    }

    newNode->data = value;
    newNode->next = top;
    top = newNode;
}

void pop() {
    struct node *temp;

    if (top == NULL) {
        printf("Stack is empty\n");
    } else {
        temp = top;
        printf("Popped element: %d\n", top->data);
        top = top->next;
        free(temp);
    }
}

void display() {
    struct node *temp;

    if (top == NULL) {
        printf("Stack is empty\n");
    } else {
        temp = top;
        printf("Stack elements:\n");
        while (temp != NULL) {
            printf("%d ", temp->data);
            temp = temp->next;
        }
        printf("\n");
    }
}

int main() {
    int choice, value;

    while (1) {
        printf("\n1.Push  2.Pop  3.Display  4.Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value: ");
                scanf("%d", &value);
                push(value);
                break;

            case 2:
                pop();
                break;

            case 3:
                display();
                break;

            case 4:
                return 0;

            default:
                printf("Invalid choice\n");
        }
    }
}
