#include <iostream>
#include <cmath>
#include <iomanip>

int main() {
    // Вхідні дані (можна замінити на cin)
    double a = 4.0;
    double b = 0.707;

    // Проміжні обчислення
    double A = 0.5 * (1.0 - std::cos(b * M_PI)) / (1.0 - std::sin(a * M_PI));
    double B = 0.3 * (1.0 + std::cos(a * M_PI)) / (1.0 + std::sin(b * M_PI));

    double t1 = std::exp(A);
    double t2 = std::exp(B);

    double y = std::pow(t1 + t2, 1.5); // 3/2 = 1.5

    std::cout << std::fixed << std::setprecision(10);
    std::cout << "A = " << A << "\n";
    std::cout << "B = " << B << "\n";
    std::cout << "t1 = e^A = " << t1 << "\n";
    std::cout << "t2 = e^B = " << t2 << "\n";
    std::cout << "y = " << y << "\n";

    return 0;
}
