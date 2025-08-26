#include <stdio.h>
#include <stdlib.h>

void callNumber(const char *service, const char *number) {
    printf("\n📞 Calling %s... (Dialing %s)\n", service, number);
}

int main() {
    int choice;

    while (1) {
        printf("\n=== Emergency Dashboard ===\n");
        printf("1. Fire Station (101)\n");
        printf("2. Police (100)\n");
        printf("3. Ambulance (108)\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                callNumber("Fire Station", "101");
                break;
            case 2:
                callNumber("Police", "100");
                break;
            case 3:
                callNumber("Ambulance", "108");
                break;
            case 4:
                printf("Exiting... Stay safe!\n");
                exit(0);
            default:
                printf("Invalid choice! Try again.\n");
        }
    }

    return 0;
}
