#include <stdio.h>

int main(void) {
    int n;
    printf("Введите трёхзначное положительное целое число: ");
    if (scanf("%d", &n) != 1) return 0;

    if (n < 100 || n > 999) {
        printf("Ошибка: число не является трёхзначным (100..999).\n");
        return 0;
    }

    int units = n % 10;
    int tens = (n / 10) % 10;
    int hundreds = n / 100;

    int result = units * 100 + hundreds * 10 + tens;

    printf("Результат: %d\n", result);
    return 0;
}
