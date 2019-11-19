//# BUBBLE-SORT
//C programming for bubble sort with algorithm
 
 
 /* Algorithm for bubble sorting*/
 /*Bubble Sort in C is a sorting algorithm where we repeatedly iterate through the array and swap adjacent elements that are unordered.*/ 
 /*We repeat this until the array is sorted. As an example, for the array mentioned above - [5, 1, 4, 2, 3] we can see that 5 should not be on the left of 1 and so, we swap them to get: [1, 5, 4, 2, 3]. */
 /*Next, we see that 5 should again not be on the left of 4. We swap 5 and 4 to get [1, 4, 5, 2, 3]. We repeat this for 5 and 2 and subsequently for 5 and 3 to get [1, 4, 2, 3, 5]. As can be seen - after one “pass” over the array, the largest element (5 in this case) has reached its correct position - extreme right.*/
 /*Let us try to repeat this process. (1, 4) is correct. However, (4, 2) is an incorrect order. Therefore, we swap 4 and 2 to get [1, 2, 4, 3, 5]. */
 /*Now again, (4, 3) is incorrect so we do another swap and get [1, 2, 3, 4, 5]. As can be seen, the array is sorted! This exactly is how bubble sort in C works. As an example, check this graphic that pictorially depicts how bubble sort works.*/
 
 
// C program 
// C++ program for implementation of Bubble sort  
#include <bits/stdc++.h> 
#include<iostream.h>
using namespace std; 
  
void swap(int *xp, int *yp)  
{  
    int temp = *xp;  
    *xp = *yp;  
    *yp = temp;  
}  
  
// A function to implement bubble sort  
void bubbleSort(int arr[], int n)  
{  
    int i, j;  
    for (i = 0; i < n-1; i++)      
      
    // Last i elements are already in place  
    for (j = 0; j < n-i-1; j++)  
        if (arr[j] > arr[j+1])  
            swap(&arr[j], &arr[j+1]);  
}  
  
/* Function to print an array */
void printArray(int arr[], int size)  
{  
    int i;  
    for (i = 0; i < size; i++)  
        cout << arr[i] << " ";  
    cout << endl;  
}  
  
// Driver code  
int main()  
{  
    int arr[] = {64, 34, 25, 12, 22, 11, 90};  
    int n = sizeof(arr)/sizeof(arr[0]);  
    bubbleSort(arr, n);  
    cout<<"Sorted array: \n";  
    printArray(arr, n);  
    return 0;  
}  
  
// This code is contributed by rathbhupendra 
