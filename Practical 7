// Q7-Write a program to calculate GCD of two numbers (i) with recursion (ii) without
//recursion.


#include <iostream>
using namespace std;

// Recursive function to find GCD
int gcdRecursive(int a, int b) {
    if (b == 0)
        return a;
    return gcdRecursive(b, a % b);
}

// Iterative function to find GCD
int gcdIterative(int a, int b) {
    while (b != 0) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int main() {
    int num1, num2;
    
    cout << "Enter two numbers: ";
    cin >> num1 >> num2;
    
    cout << "GCD (Recursive): " << gcdRecursive(num1, num2) << endl;
    cout << "GCD (Iterative): " << gcdIterative(num1, num2) << endl;
    
    return 0;
}
