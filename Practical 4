// Q4-Write a menu driven program to perform string manipulation (without using inbuilt
//string functions):
//a. Show address of each character in string
//b. Concatenate two strings.
//c. Compare two strings
//d. Calculate length of the string (use pointers)
//e. Convert all lowercase characters to uppercase
//f. Reverse the string
//g. Insert a string in another string at a user specified position


#include <iostream>
using namespace std;

void showAddress(char* str) {
    while (*str) {
        cout << "Character: " << *str << " Address: " << (void*)str << endl;
        str++;
    }
}

void concatenate(char* str1, char* str2, char* result) {
    while (*str1) {
        *result++ = *str1++;
    }
    while (*str2) {
        *result++ = *str2++;
    }
    *result = '\0';
}

int compare(char* str1, char* str2) {
    while (*str1 && *str2) {
        if (*str1 != *str2)
            return *str1 - *str2;
        str1++;
        str2++;
    }
    return *str1 - *str2;
}

int length(char* str) {
    int len = 0;
    while (*str++) {
        len++;
    }
    return len;
}

void toUpperCase(char* str) {
    while (*str) {
        if (*str >= 'a' && *str <= 'z') {
            *str -= 32;
        }
        str++;
    }
}

void reverseString(char* str) {
    int len = length(str);
    for (int i = 0; i < len / 2; i++) {
        char temp = str[i];
        str[i] = str[len - i - 1];
        str[len - i - 1] = temp;
    }
}

void insertString(char* str1, char* str2, int pos, char* result) {
    int i = 0;
    while (i < pos && *str1) {
        *result++ = *str1++;
        i++;
    }
    while (*str2) {
        *result++ = *str2++;
    }
    while (*str1) {
        *result++ = *str1++;
    }
    *result = '\0';
}

int main() {
    char str1[100], str2[100], result[200];
    int choice, pos;
    
    do {
        cout << "\nMenu:\n";
        cout << "1. Show address of each character in string\n";
        cout << "2. Concatenate two strings\n";
        cout << "3. Compare two strings\n";
        cout << "4. Calculate length of the string\n";
        cout << "5. Convert to uppercase\n";
        cout << "6. Reverse string\n";
        cout << "7. Insert string at position\n";
        cout << "8. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;
        cin.ignore();
        
        switch (choice) {
            case 1:
                cout << "Enter string: ";
                cin.getline(str1, 100);
                showAddress(str1);
                break;
            case 2:
                cout << "Enter first string: ";
                cin.getline(str1, 100);
                cout << "Enter second string: ";
                cin.getline(str2, 100);
                concatenate(str1, str2, result);
                cout << "Concatenated string: " << result << endl;
                break;
            case 3:
                cout << "Enter first string: ";
                cin.getline(str1, 100);
                cout << "Enter second string: ";
                cin.getline(str2, 100);
                cout << "Comparison result: " << compare(str1, str2) << endl;
                break;
            case 4:
                cout << "Enter string: ";
                cin.getline(str1, 100);
                cout << "Length: " << length(str1) << endl;
                break;
            case 5:
                cout << "Enter string: ";
                cin.getline(str1, 100);
                toUpperCase(str1);
                cout << "Uppercase string: " << str1 << endl;
                break;
            case 6:
                cout << "Enter string: ";
                cin.getline(str1, 100);
                reverseString(str1);
                cout << "Reversed string: " << str1 << endl;
                break;
            case 7:
                cout << "Enter main string: ";
                cin.getline(str1, 100);
                cout << "Enter string to insert: ";
                cin.getline(str2, 100);
                cout << "Enter position: ";
                cin >> pos;
                cin.ignore();
                insertString(str1, str2, pos, result);
                cout << "Modified string: " << result << endl;
                break;
            case 8:
                cout << "Exiting...\n";
                break;
            default:
                cout << "Invalid choice. Try again.\n";
        }
    } while (choice != 8);
    
    return 0;
}
