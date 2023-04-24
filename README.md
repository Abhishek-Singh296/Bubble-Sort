# Bubble-Sort
Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in the wrong order.

## __Working__
Suppose we are trying to sort the elements in ascending order.

__1. First Iteration (Compare and Swap)__

- Starting from the first index, compare the first and the second elements.
- If the first element is greater than the second element, they are swapped.
- Now, compare the second and the third elements. Swap them if they are not in order.
- The above process goes on until the last element.

![Bubble-sort-0](https://user-images.githubusercontent.com/113619312/234092150-f827869a-fcb6-4f48-9607-241c003ed99c.png)

__2. Remaining Iteration__

The same process goes on for the remaining iterations.

After each iteration, the largest element among the unsorted elements is placed at the end.

![Bubble-sort-1](https://user-images.githubusercontent.com/113619312/234092386-a9e6c169-bec5-4791-8862-07d1de9ed671.png)

In each iteration, the comparison takes place up to the last unsorted element.

![Bubble-sort-2](https://user-images.githubusercontent.com/113619312/234092542-a5c94cfd-4986-4c12-bc08-4fca62fcfbe3.png)

The array is sorted when all the unsorted elements are placed at their correct positions.

![Bubble-sort-3](https://user-images.githubusercontent.com/113619312/234092841-4f2dd85a-2b20-44a0-b3c8-6dd105895e25.png)

---

## __Code__
```
#include<stdio.h>
#include<conio.h>

#define MAX_SIZE 5

void bubble_sort(int[]);

int main() {
    int arr_sort[MAX_SIZE], i;

    printf("Simple Bubble Sort Example - Array and Functions\n");
    printf("\nEnter %d Elements for Sorting\n", MAX_SIZE);
    for (i = 0; i < MAX_SIZE; i++)
        scanf("%d", &arr_sort[i]);

    printf("\nYour Data   :");
    for (i = 0; i < MAX_SIZE; i++) {
        printf("\t%d", arr_sort[i]);
    }

    bubble_sort(arr_sort);
    getch();
}

void bubble_sort(int fn_arr[]) {
    int i, j, a, t;

    for (i = 1; i < MAX_SIZE; i++) {
        for (j = 0; j < MAX_SIZE - 1; j++) {
            if (fn_arr[j] > fn_arr[j + 1]) {
                //Swapping Values 
                t = fn_arr[j];
                fn_arr[j] = fn_arr[j + 1];
                fn_arr[j + 1] = t;
            }
        }

        printf("\nIteration %d : ", i);
        for (a = 0; a < MAX_SIZE; a++) {
            printf("\t%d", fn_arr[a]);
        }
    }

    printf("\n\nSorted Data :");
    for (i = 0; i < MAX_SIZE; i++) {
        printf("\t%d", fn_arr[i]);
    }
}
```

---

## __Output__
![Screenshot 2023-04-24 023120](https://user-images.githubusercontent.com/113619312/234093264-d19a0ddf-a328-46d7-af8d-4b115d9a546f.png)
