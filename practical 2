// Q2-Write a program to remove the duplicates from an array.

#include <iostream>
#include <vector>
#include <unordered_set>

using namespace std;

// Function to remove duplicates from an array
vector<int> removeDuplicates(const vector<int>& arr) {
    unordered_set<int> seen;
    vector<int> uniqueArr;
    
    for (int num : arr) {
        if (seen.find(num) == seen.end()) { // If number not seen before
            uniqueArr.push_back(num);
            seen.insert(num);
        }
    }
    return uniqueArr;
}

int main() {
    int n;
    cout << "Enter the number of elements: ";
    cin >> n;
    
    vector<int> arr(n);
    cout << "Enter " << n << " elements: ";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }
    
    vector<int> result = removeDuplicates(arr);
    
    cout << "Array after removing duplicates: ";
    for (int num : result) {
        cout << num << " ";
    }
    cout << endl;
    
    return 0;
}
