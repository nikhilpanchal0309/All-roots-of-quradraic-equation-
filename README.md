#include <iostream>
#include <cmath>
using namespace std;

int main() {
    float a, b, c, d, r1, r2;

    cout << "Enter a, b and c: ";
    cin >> a >> b >> c;

    d = b * b - 4 * a * c;

    if (a == 0) {
        cout << "Not a quadratic equation";
    }
    else if (d > 0) {
        r1 = (-b + sqrt(d)) / (2 * a);
        r2 = (-b - sqrt(d)) / (2 * a);

        cout << "Two distinct real roots: "
             << r1 << " and " << r2;
    }
    else if (d == 0) {
        r1 = -b / (2 * a);
        cout << "Two equal roots: " << r1;
    }
    else {
        cout << "Complex roots: "
             << -b / (2 * a) << " + "
             << sqrt(-d) / (2 * a) << "i and "
             << -b / (2 * a) << " - "
             << sqrt(-d) / (2 * a) << "i";
    }

    return 0;
}
