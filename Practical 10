// Q10-Create a Triangle class. Add exception handling statements to ensure the following
///conditions: all sides are greater than 0 and sum of any two sides are greater than the
//third side. The class should also have overloaded functions for calculating the area
//of a right angled triangle as well as using Heron's formula to calculate the area of any
//type of triangle.


#include <iostream>
#include <cmath>
#include <stdexcept>
using namespace std;

class Triangle {
private:
    double a, b, c;

    void validate() {
        if (a <= 0 || b <= 0 || c <= 0) {
            throw invalid_argument("Sides must be greater than zero.");
        }
        if (a + b <= c || a + c <= b || b + c <= a) {
            throw invalid_argument("Sum of any two sides must be greater than the third side.");
        }
    }

public:
    Triangle(double x, double y, double z) : a(x), b(y), c(z) {
        validate();
    }

    // Area for right-angled triangle (overloaded function)
    static double area(double base, double height) {
        if (base <= 0 || height <= 0) {
            throw invalid_argument("Base and height must be greater than zero.");
        }
        return 0.5 * base * height;
    }

    // Area using Heron's formula
    double area() {
        double s = (a + b + c) / 2;
        return sqrt(s * (s - a) * (s - b) * (s - c));
    }
};

int main() {
    try {
        double x, y, z;
        cout << "Enter the sides of the triangle: ";
        cin >> x >> y >> z;
        Triangle t(x, y, z);
        cout << "Area of the triangle (Heron's formula): " << t.area() << endl;

        double base, height;
        cout << "\nEnter base and height of right-angled triangle: ";
        cin >> base >> height;
        cout << "Area of right-angled triangle: " << Triangle::area(base, height) << endl;
    } catch (const exception& e) {
        cout << "Error: " << e.what() << endl;
    }
    return 0;
}
