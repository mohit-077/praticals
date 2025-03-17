// Q9-Define a class Person having name as a data member. Inherit two classes Student and
//Employee from Person. Student has additional attributes as course, marks and year
//and Employee has department and salary. Write display() method in all the three
//classes to display the corresponding attributes. Provide the necessary methods to show
//runtime polymorphism.


#include <iostream>
using namespace std;

class Person {
protected:
    string name;
public:
    Person(string n) : name(n) {}
    virtual void display() {
        cout << "Name: " << name << endl;
    }
    virtual ~Person() {}
};

class Student : public Person {
private:
    string course;
    int marks, year;
public:
    Student(string n, string c, int m, int y) : Person(n), course(c), marks(m), year(y) {}
    void display() override {
        cout << "Student Details:" << endl;
        Person::display();
        cout << "Course: " << course << "\nMarks: " << marks << "\nYear: " << year << endl;
    }
};

class Employee : public Person {
private:
    string department;
    double salary;
public:
    Employee(string n, string d, double s) : Person(n), department(d), salary(s) {}
    void display() override {
        cout << "Employee Details:" << endl;
        Person::display();
        cout << "Department: " << department << "\nSalary: " << salary << endl;
    }
};

int main() {
    Person* p1 = new Student("Alice", "Computer Science", 85, 2023);
    Person* p2 = new Employee("Bob", "HR", 50000);
    
    cout << "Displaying Student Info:\n";
    p1->display();
    
    cout << "\nDisplaying Employee Info:\n";
    p2->display();
    
    delete p1;
    delete p2;
    return 0;
}
