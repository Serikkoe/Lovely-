#include <iostream>
#include <thread>  // Для функции sleep_for
#include <chrono>  // Для времени
#include <string>  // Для строк

void printWithDelay(const std::string& text, int delay = 100) {
    for (char c : text) {
        std::cout << c << std::flush;
        std::this_thread::sleep_for(std::chrono::milliseconds(delay));
    }
    std::cout << std::endl;
}

int main() {
    std::string name;

    std::cout << "Введите имя того, кому вы хотите признаться: ";
    std::getline(std::cin, name);

    std::cout << "\nПривет, " << name << "!" << std::endl;
    std::this_thread::sleep_for(std::chrono::seconds(1));

    printWithDelay("У меня есть для тебя важное сообщение...");
    std::this_thread::sleep_for(std::chrono::seconds(2));

    printWithDelay("Ты самая замечательная и прекрасная девушка, которую я знаю!", 50);
    std::this_thread::sleep_for(std::chrono::seconds(2));

    printWithDelay("Ты делаешь мой мир ярче, и каждый день с тобой - это счастье.", 50);
    std::this_thread::sleep_for(std::chrono::seconds(2));

    printWithDelay("Я люблю тебя всем сердцем!", 100);
    std::this_thread::sleep_for(std::chrono::seconds(2));

    printWithDelay("\nСпасибо, что ты есть в моей жизни. ❤️");
    return 0;
}
