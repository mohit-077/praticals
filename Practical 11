// Q11-Create a class Student containing fields for Roll No., Name, Class, Year and Total
//Marks. Write a program to store 5 objects of Student class in a file. Retrieve these
//records from the file and display them.


#include <iostream>
#include <fstream>
using namespace std;

class Student {
public:
    int rollNo;
    string name;
    string studentClass;
    int year;
    float totalMarks;

    void input() {
        cout << "Enter Roll No: ";
        cin >> rollNo;
        cin.ignore(); // Ignore newline character
        cout << "Enter Name: ";
        getline(cin, name);
        cout << "Enter Class: ";
        getline(cin, studentClass);
        cout << "Enter Year: ";
        cin >> year;
        cout << "Enter Total Marks: ";
        cin >> totalMarks;
    }

    void display() {
        cout << "Roll No: " << rollNo << "\nName: " << name << "\nClass: " << studentClass << "\nYear: " << year << "\nTotal Marks: " << totalMarks << "\n\n";
    }
};

int main() {
    Student students[5];
    fstream file;

    // Writing to file
    file.open("students.dat", ios::out | ios::binary);
    if (!file) {
        cout << "Error opening file!" << endl;
        return 1;
    }
    cout << "Enter details for 5 students:\n";
    for (int i = 0; i < 5; i++) {
        students[i].input();
        file.write(reinterpret_cast<char*>(&students[i]), sizeof(Student));
    }
    file.close();

    // Reading from file
    file.open("students.dat", ios::in | ios::binary);
    if (!file) {
        cout << "Error opening file!" << endl;
        return 1;
    }
    cout << "\nStudent Records:\n";
    Student temp;
    while (file.read(reinterpret_cast<char*>(&temp), sizeof(Student))) {
        temp.display();
    }
    file.close();

    return 0;
}
