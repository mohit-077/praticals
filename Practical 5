// Q5-Write a program to merge two ordered arrays to get a single ordered array.


#include <iostream>
using namespace std;

void mergeArrays(int arr1[], int size1, int arr2[], int size2, int merged[]) {
    int i = 0, j = 0, k = 0;
    
    // Merge both arrays in sorted order
    while (i < size1 && j < size2) {
        if (arr1[i] < arr2[j]) {
            merged[k++] = arr1[i++];
        } else {
            merged[k++] = arr2[j++];
        }
    }
    
    // Copy remaining elements of arr1, if any
    while (i < size1) {
        merged[k++] = arr1[i++];
    }
    
    // Copy remaining elements of arr2, if any
    while (j < size2) {
        merged[k++] = arr2[j++];
    }
}

int main() {
    int arr1[100], arr2[100], merged[200], size1, size2;
    
    cout << "Enter size of first sorted array: ";
    cin >> size1;
    cout << "Enter elements of first sorted array: ";
    for (int i = 0; i < size1; i++) {
        cin >> arr1[i];
    }
    
    cout << "Enter size of second sorted array: ";
    cin >> size2;
    cout << "Enter elements of second sorted array: ";
    for (int i = 0; i < size2; i++) {
        cin >> arr2[i];
    }
    
    mergeArrays(arr1, size1, arr2, size2, merged);
    
    cout << "Merged sorted array: ";
    for (int i = 0; i < size1 + size2; i++) {
        cout << merged[i] << " ";
    }
    cout << endl;
    
    return 0;
}
