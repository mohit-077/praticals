// Q3-Write a program that prints a table indicating the number of occurrences of each
//alphabet in the text entered as command line arguments.


#include <iostream>
#include <map>
#include <cctype>

int main(int argc, char* argv[]) {
    std::map<char, int> frequency;
    
    // Initialize map for all alphabets
    for (char c = 'a'; c <= 'z'; ++c) {
        frequency[c] = 0;
    }

    // Iterate over command-line arguments
    for (int i = 1; i < argc; ++i) {
        std::string arg = argv[i];
        for (char c : arg) {
            if (std::isalpha(c)) { // Check if it's an alphabet
                c = std::tolower(c); // Convert to lowercase
                frequency[c]++;
            }
        }
    }

    // Print the frequency table
    std::cout << "Character Frequency Table:\n";
    for (const auto& pair : frequency) {
        if (pair.second > 0) {
            std::cout << pair.first << " : " << pair.second << '\n';
        }
    }
    
    return 0;
}
