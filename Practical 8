// Q8-Create a Matrix class. Write a menu-driven program to perform following Matrix
//operations (exceptions should be thrown by the functions if matrices passed to them
//are incompatible and handled by the main() function):
//a. Sum
//b. Product
//c. Transpose


#include <iostream>
#include <vector>
#include <stdexcept>
using namespace std;

class Matrix {
private:
    vector<vector<int>> data;
    int rows, cols;

public:
    Matrix(int r, int c) : rows(r), cols(c) {
        data.resize(rows, vector<int>(cols, 0));
    }

    void input() {
        cout << "Enter matrix elements (" << rows << "x" << cols << "):\n";
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                cin >> data[i][j];
            }
        }
    }

    void display() const {
        for (const auto& row : data) {
            for (int val : row) {
                cout << val << " ";
            }
            cout << endl;
        }
    }

    Matrix operator+(const Matrix& other) {
        if (rows != other.rows || cols != other.cols) {
            throw invalid_argument("Matrix dimensions must be the same for addition.");
        }
        Matrix result(rows, cols);
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result.data[i][j] = data[i][j] + other.data[i][j];
            }
        }
        return result;
    }

    Matrix operator*(const Matrix& other) {
        if (cols != other.rows) {
            throw invalid_argument("Matrix multiplication not possible, column of first matrix must match row of second.");
        }
        Matrix result(rows, other.cols);
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < other.cols; j++) {
                for (int k = 0; k < cols; k++) {
                    result.data[i][j] += data[i][k] * other.data[k][j];
                }
            }
        }
        return result;
    }

    Matrix transpose() {
        Matrix result(cols, rows);
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result.data[j][i] = data[i][j];
            }
        }
        return result;
    }
};

int main() {
    int choice;
    do {
        cout << "\nMatrix Operations:\n";
        cout << "1. Sum of matrices\n";
        cout << "2. Product of matrices\n";
        cout << "3. Transpose of a matrix\n";
        cout << "4. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        try {
            if (choice == 1) {
                int r, c;
                cout << "Enter dimensions of matrices (rows cols): ";
                cin >> r >> c;
                Matrix A(r, c), B(r, c);
                cout << "Enter first matrix:\n";
                A.input();
                cout << "Enter second matrix:\n";
                B.input();
                Matrix C = A + B;
                cout << "Sum of matrices:\n";
                C.display();
            } else if (choice == 2) {
                int r1, c1, r2, c2;
                cout << "Enter dimensions of first matrix (rows cols): ";
                cin >> r1 >> c1;
                cout << "Enter dimensions of second matrix (rows cols): ";
                cin >> r2 >> c2;
                Matrix A(r1, c1), B(r2, c2);
                cout << "Enter first matrix:\n";
                A.input();
                cout << "Enter second matrix:\n";
                B.input();
                Matrix C = A * B;
                cout << "Product of matrices:\n";
                C.display();
            } else if (choice == 3) {
                int r, c;
                cout << "Enter dimensions of matrix (rows cols): ";
                cin >> r >> c;
                Matrix A(r, c);
                cout << "Enter matrix:\n";
                A.input();
                Matrix C = A.transpose();
                cout << "Transpose of matrix:\n";
                C.display();
            } else if (choice != 4) {
                cout << "Invalid choice, try again.\n";
            }
        } catch (const exception& e) {
            cout << "Error: " << e.what() << endl;
        }
    } while (choice != 4);
    
    return 0;
}
