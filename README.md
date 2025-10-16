#include <iostream>

int main() {
    setlocale(LC_ALL, "Russian");
    int userNumber;
    std::cout << "Введите число: ";
    std::cin >> userNumber;

    int multiplier = 1;
    bool success = true;

    while (multiplier <= userNumber && success) {
        // Генерация примера
        std::cout << "Решите пример: " << userNumber << " х " << multiplier << std::endl;
        std::cout << "[+] Ответ: ";
        int userAnswer;
        std::cin >> userAnswer;

        int correctAnswer = userNumber * multiplier;

        if (userAnswer == correctAnswer) {
            std::cout << "[ + ] Пример решен правильно!\n";
            multiplier++;
        }
        else {
            std::cout << "[ - І Ошибка, пример решен неверно!\n";
            success = false;
        }
    }

    if (success && multiplier > userNumber) {
        std::cout << "[ + ] Примеры решены, поздравляем!\n";
    }

    return 0;
}
