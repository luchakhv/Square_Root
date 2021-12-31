#include <stdio.h>
#include <math.h>

void vvod(float *a, float *b, float *c);

float quadrat(float a, float b, float c);

int end(void);

int main() {
    float a, b, c;
    vvod(&a, &b, &c);
    quadrat(a, b, c);
    while (end()) {
        vvod(&a, &b, &c);
        quadrat(a, b, c);
    }
    return 0;
}

void vvod(float *a, float *b, float *c) {
    puts("Enter values of coefficients:");
    printf("Enter a :");

    while (scanf("%f", a) != 1) {
        while (getchar() != '\n')
            continue;
        puts("Incorrect enter!");
        printf("Enter a :");
    }

    printf("Enter b :");
    while (getchar() != '\n')
        continue;
    while (scanf("%f", b) != 1) {
        while (getchar() != '\n')
            continue;
        puts("Incorrect enter!");
        printf("Enter b : ");
    }

    printf("Enter c :");
    while (getchar() != '\n')
        continue;
    while (scanf("%f", c) != 1) {
        while (getchar() != '\n')
            continue;
        puts("Incorrect enter!");
        printf("Enter c : ");
    }
}

float quadrat(float a, float b, float c) {
    if (a == 0) {
        puts("a coefficient is 0, this is not a 2 power function");
        if (b != 0) {
            printf("X = %.5f\n", (-c) / b);
            return 1;
        } else if (c != 0) {
            puts("There are 0 solutions for X");
            return 404;
        } else if (c == 0) {
            puts("There are infinite number of solutions for X");
        }
    } else {
        float D = b * b - 4 * a * c;
        if (D > 0) {
            printf("X1 = %.5f\nX2 = %.5f\n", (-b - sqrt(D)) / (2 * a), (-b + sqrt(D)) / (2 * a));
            return 2;
        } else if (D < 0) {
            float di;
            di = sqrt(fabs(D));
            printf("X1 = %.5f - %.5fi\n", -b / (2 * a), di / (2 * a));
            printf("X2 = %.5f + %.5fi\n", -b / (2 * a), di / (2 * a));
            return -2;
        } else if (D == 0) {
            printf("X1 = X2 = %.5f\n", (-b) / (2 * a));
            return 1;
        }
    }
}

int end(void) {
    char flag[100];
    printf("Press c or C to continue, any other key - to quit\n");
    while (getchar() != '\n')
        continue;
    scanf("%s", flag);
    if ((flag[0]=='c')||(flag[0] == 'C'))
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
