
#include <stdio.h>
#include <stdlib.h> // For the exit() function
#include <conio.h> // For getch()

#define MAX 10

// Function prototypes
void create();
void insert();
void deletion();
void search();
void display();

int b[MAX], n = 0, pos, p, e;

void main() {
    // clrscr(); // Uncomment if you are using Turbo C/C++ or similar
    int ch;
    char g = 'y';

    do {
        printf("\nMain Menu");
        printf("\n1. Create\n2. Delete\n3. Search\n4. Insert\n5. Display\n6. Exit\n");
        printf("\nEnter your Choice: ");
        scanf("%d", &ch);

        switch (ch) {
            case 1:
                create();
                break;
            case 2:
                deletion();
                break;
            case 3:
                search();
                break;
            case 4:
                insert();
                break;
            case 5:
                display();
                break;
            case 6:
                exit(0);
                break;
            default:
                printf("\nEnter the correct choice:");
        }

        printf("\nDo you want to continue (y/n): ");
        scanf(" %c", &g); // Added space before %c to consume the newline character
    } while (g == 'y' || g == 'Y');

    getch();
}

void create() {
    printf("\nEnter the number of elements (max %d): ", MAX);
    scanf("%d", &n);

    if (n > MAX) {
        printf("\nNumber exceeds maximum limit of %d", MAX);
        n = 0; // Reset n to 0 if it exceeds the limit
        return;
    }

    for (int i = 0; i < n; i++) {
        printf("\nEnter element %d: ", i + 1);
        scanf("%d", &b[i]);
    }
}

void deletion() {
    printf("\nEnter the position to delete (0 to %d): ", n - 1);
    scanf("%d", &pos);

    if (pos >= n || pos < 0) {
        printf("\nInvalid position");
        return;
    }

    for (int i = pos; i < n - 1; i++) {
        b[i] = b[i + 1];
    }
    n--;

    printf("\nThe elements after deletion:");
    display();
}

void search() {
    printf("\nEnter the element to be searched: ");
    scanf("%d", &e);

    for (int i = 0; i < n; i++) {
        if (b[i] == e) {
            printf("Value is at position %d\n", i);
            return;
        }
    }
    printf("Value %d is not in the list\n", e);
}

void insert() {
    if (n == MAX) {
        printf("\nList is full. Cannot insert new element.");
        return;
    }

    printf("\nEnter the position to insert (0 to %d): ", n);
    scanf("%d", &pos);

    if (pos > n || pos < 0) {
        printf("\nInvalid position");
        return;
    }

    for (int i = n; i > pos; i--) {
        b[i] = b[i - 1];
    }

    printf("\nEnter the element to insert: ");
    scanf("%d", &p);

    b[pos] = p;
    n++;

    printf("\nThe list after insertion:");
    display();
}

void display() {
    printf("\nThe elements of the list are:");
    for (int i = 0; i < n; i++) {
        printf("\n%d", b[i]);
    }
}
