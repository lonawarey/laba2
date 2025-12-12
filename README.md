#include <stdio.h>

int main() {
    int number;      // Исходное трехзначное число
    int original;    // Сохраним исходное число для вывода
    int lastDigit;   // Последняя цифра
    int firstTwo;    // Первые две цифры
    int result;      // Результат после преобразования
    
    // Ввод трехзначного числа
    printf("Введите трехзначное число: ");
    scanf("%d", &number);
    
    // Сохраняем исходное число
    original = number;
    
    // Извлекаем последнюю цифру
    lastDigit = number % 10;
    
    // Извлекаем первые две цифры
    firstTwo = number / 10;
    
    // Формируем новое число: lastDigit * 100 + firstTwo
    result = lastDigit * 100 + firstTwo;
    
    // Вывод результата
    printf("\nИсходное число: %d\n", original);
    printf("После преобразования: %d\n", result);
    printf("(Последняя цифра '%d' перемещена в начало)\n", lastDigit);
    
    return 0;
}
