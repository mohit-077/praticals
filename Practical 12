// Q12-Copy the contents of one text file to another file, after removing all whitespaces


#include <iostream>
#include <fstream>
#include <cctype>
using namespace std;

void removeWhitespaces(const string& inputFile, const string& outputFile) {
    ifstream inFile(inputFile);
    ofstream outFile(outputFile);
    
    if (!inFile || !outFile) {
        cerr << "Error opening file!" << endl;
        return;
    }
    
    char ch;
    while (inFile.get(ch)) {
        if (!isspace(ch)) {
            outFile.put(ch);
        }
    }
    
    inFile.close();
    outFile.close();
    cout << "File copied successfully without whitespaces." << endl;
}

int main() {
    string sourceFile, destFile;
    cout << "Enter source file name: ";
    cin >> sourceFile;
    cout << "Enter destination file name: ";
    cin >> destFile;
    
    removeWhitespaces(sourceFile, destFile);
    return 0;
}
