# Codveda_Basic_Calculator
Codveda_Level1 Basic_Calculator
#include <stdio.h>

int main() {
    int choice;
    double num1, num2, result;
    char again;

    do {
        printf("\n=================================\n");
        printf("        BASIC CALCULATOR\n");
        printf("=================================\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exit\n");
        printf("=================================\n");

        printf("Enter your choice: ");
        scanf("%d", &choice);

        if (choice == 5) {
            printf("\nThank you for using the Basic Calculator!\n");
            break;
        }

        if (choice < 1 || choice > 5) {
            printf("\nInvalid choice. Please select an option from 1 to 5.\n");
            continue;
        }

        printf("Enter first number: ");
        scanf("%lf", &num1);

        printf("Enter second number: ");
        scanf("%lf", &num2);

        switch (choice) {
            case 1:
                result = num1 + num2;
                printf("\nResult: %.2f + %.2f = %.2f\n",
                       num1, num2, result);
                break;

            case 2:
                result = num1 - num2;
                printf("\nResult: %.2f - %.2f = %.2f\n",
                       num1, num2, result);
                break;

            case 3:
                result = num1 * num2;
                printf("\nResult: %.2f * %.2f = %.2f\n",
                       num1, num2, result);
                break;

            case 4:
                if (num2 == 0) {
                    printf("\nError: Division by zero is not allowed.\n");
                } else {
                    result = num1 / num2;
                    printf("\nResult: %.2f / %.2f = %.2f\n",
                           num1, num2, result);
                }
                break;
        }

        printf("\nWould you like to perform another calculation? (y/n): ");
        scanf(" %c", &again);

    } while (again == 'y' || again == 'Y');

    printf("\nProgram ended. Goodbye!\n");

    return 0;
}
