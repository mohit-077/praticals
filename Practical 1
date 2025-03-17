// Q1-Write a program to compute the sum of the first n terms of the following series:
//□ = 1 − 1/2^2 + 1/3^3 - 1/4^4 + 1/5^5 - .......
//The number of terms n is to be taken from the user through the command line. If the
//command line argument is not found then prompt the user to enter the value of n.


#include <iostream>
#include <cmath>
#include <cstdlib> // For atoi

using namespace std;

// Function to compute the sum of the series
double computeSeriesSum(int n) {
    double sum = 0.0;
    for (int i = 1; i <= n; i++) {
        double term = 1.0 / pow(i, i);
        if (i % 2 == 0) {
            sum -= term;
        } else {
            sum += term;
        }
    }
    return sum;
}

int main(int argc, char *argv[]) {
    int n;
    
    // Check if command-line argument is provided
    if (argc > 1) {
        n = atoi(argv[1]); // Convert argument to integer
    } else {
        // Prompt the user for input
        cout << "Enter the number of terms (n): ";
        cin >> n;
    }
    
    if (n <= 0) {
        cout << "Please enter a positive integer." << endl;
        return 1;
    }
    
    // Compute and display the sum
    double result = computeSeriesSum(n);
    cout << "The sum of the first " << n << " terms is: " << result << endl;
    
    return 0;
}
