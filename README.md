 Source Code
```c
#include <stdio.h>

int main() {
    int arr[] = {5, 2, 9, 1, 5, 6};
    int n = sizeof(arr) / sizeof(arr[0]);
    int i, j, temp;

    // Bubble Sort
    for(i = 0; i < n - 1; i++) {
        for(j = 0; j < n - i - 1; j++) {
            if(arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }

    // Print sorted array
    printf("Sorted array: ");
    for(i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}
```

---

 Explanation

- `arr[] = {5, 2, 9, 1, 5, 6}` → Array to be sorted.
- `n = sizeof(arr) / sizeof(arr[0])` → Calculates total number of elements.
- Outer loop → Controls number of passes.
- Inner loop → Compares adjacent elements.
- Swapping → Happens when left element is greater than right element.
- After each pass, the largest unsorted element moves to its correct position.

---

 Sample Output

```
Sorted array: 1 2 5 5 6 9
```

---

 Time Complexity

- Best Case: **O(n)** (If optimized and already sorted)
- Average Case: **O(n²)**
- Worst Case: **O(n²)**

---

 How to Compile and Run

 Compile:
```
gcc bubble_sort.c -o sort
```

 Run:
```
./sort
```

---

 Concepts Used
- Arrays in C
- Nested Loops
- Swapping Technique
- Sorting Algorithms
- Time Complexity

---
