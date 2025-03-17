// Q6-Write a program to search a given element in a set of N numbers using Binary search
//(i) with recursion (ii) without recursion

#include <iostream>
using namespace std;

// Recursive Binary Search
int binarySearchRecursive(int arr[], int left, int right, int key) {
    if (left > right) {
        return -1; // Element not found
    }
    int mid = left + (right - left) / 2;
    if (arr[mid] == key) {
        return mid;
    } else if (arr[mid] > key) {
        return binarySearchRecursive(arr, left, mid - 1, key);
    } else {
        return binarySearchRecursive(arr, mid + 1, right, key);
    }
}

// Iterative Binary Search
int binarySearchIterative(int arr[], int size, int key) {
    int left = 0, right = size - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] == key) {
            return mid;
        } else if (arr[mid] > key) {
            right = mid - 1;
        } else {
            left = mid + 1;
        }
    }
    return -1; // Element not found
}

int main() {
    int arr[100], size, key;
    
    cout << "Enter size of sorted array: ";
    cin >> size;
    cout << "Enter elements of sorted array: ";
    for (int i = 0; i < size; i++) {
        cin >> arr[i];
    }
    
    cout << "Enter element to search: ";
    cin >> key;
    
    int resultRec = binarySearchRecursive(arr, 0, size - 1, key);
    if (resultRec != -1) {
        cout << "Element found at index (recursive): " << resultRec << endl;
    } else {
        cout << "Element not found (recursive)." << endl;
    }
    
    int resultIter = binarySearchIterative(arr, size, key);
    if (resultIter != -1) {
        cout << "Element found at index (iterative): " << resultIter << endl;
    } else {
        cout << "Element not found (iterative)." << endl;
    }
    
    return 0;
}
