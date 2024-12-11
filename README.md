# Algorithms Project

This repository is a journey through the key algorithms introduced in the book *Grokking Algorithms* by Aditya Bhargava. The book provides a beginner-friendly approach to learning algorithms, and this repository will follow its format, exploring each algorithm in detail.

## Algorithms Covered

### 1. Binary Search
Binary search is a fast algorithm for finding an item in a sorted list. It works by repeatedly dividing the search interval in half. If the value of the target is less than the middle element, the search continues in the lower half; otherwise, it continues in the upper half. This process continues until the target is found or the search interval becomes empty.

#### Steps:
1. Start with two pointers, `low` and `high`, representing the beginning and end of the list.
2. Calculate the `mid` index: `mid = (low + high) // 2`.
3. Compare the `mid` element with the target:
   - If equal, return the `mid` index.
   - If the target is smaller, move the `high` pointer to `mid - 1`.
   - If the target is larger, move the `low` pointer to `mid + 1`.
4. Repeat until the target is found or the search interval is empty.

#### Time Complexity:
- **Best Case:** O(1)
- **Average/Worst Case:** O(log n)

#### Implementation:
```python
def binary_search(arr, target):
    low = 0
    high = len(arr) - 1

    while low <= high:
        mid = (low + high) // 2
        guess = arr[mid]

        if guess == target:
            return mid
        elif guess > target:
            high = mid - 1
        else:
            low = mid + 1

    return -1
```

### 2. Selection Sort
Selection sort is a simple sorting algorithm that works by repeatedly finding the smallest element in the unsorted portion of the array and swapping it with the first unsorted element.

#### Steps:
1. Start from the first element of the array.
2. Find the smallest element in the remaining unsorted portion of the array.
3. Swap the smallest element with the current element.
4. Move to the next position and repeat until the entire array is sorted.

#### Time Complexity:
- **Best/Average/Worst Case:** O(n^2)

#### Implementation:
```python
def selection_sort(arr):
    for i in range(len(arr)):
        min_index = i
        for j in range(i + 1, len(arr)):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[i], arr[min_index] = arr[min_index], arr[i]
    return arr
```

## Planned Algorithms
Here is the roadmap of algorithms I plan to study and implement as part of this project:

1. **Binary Search**  
2. **Selection Sort**  
3. **Recursion Basics**  
4. **Quicksort**  
5. **Breadth-First Search (BFS)**  
6. **Depth-First Search (DFS)**  
7. **Dijkstra's Algorithm**  
8. **Greedy Algorithms**  
9. **Dynamic Programming (Knapsack Problem)**  
10. **K-Nearest Neighbors (KNN)**

## How to Use This Repository
Each algorithm will have its own directory containing:
1. A detailed explanation of the algorithm.
2. Python implementation.
3. Test cases to demonstrate the algorithm.

## Getting Started
Clone this repository to your local machine:
```bash
git clone https://github.com/your-username/algorithms-project.git
```
Navigate to the algorithm you want to learn and explore its implementation and test cases.

## Resources
- *Grokking Algorithms* by Aditya Bhargava: [Link to Book](https://www.manning.com/books/grokking-algorithms)

Feel free to fork this repository and contribute by improving the explanations or adding new algorithms!

---

