# C-Code-for-a-Simple-calculator

#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    // Taking operator input from the user
    printf("Enter an operator (+, -, *, /, %): ");
    scanf(" %c", &operator);
    
    // Taking two numbers as input
    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    // Performing calculation based on the operator
    switch (operator) {
        case '+':
            result = num1 + num2;
            printf("Result: %.2lf\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("Result: %.2lf\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("Result: %.2lf\n", result);
            break;
        case '/':
            if (num2 != 0)
                result = num1 / num2;
            else {
                printf("Error: Division by zero is not allowed.\n");
                return 1;
            }
            printf("Result: %.2lf\n", result);
            break;
        case '%':
            if ((int)num2 != 0)
                printf("Result: %d\n", (int)num1 % (int)num2);
            else
                printf("Error: Modulus by zero is not allowed.\n");
            break;
        default:
            printf("Error: Invalid operator.\n");
    }
    return 0;
}
