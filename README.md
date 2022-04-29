
# Algorithms and Data Structures in Swift
Computational complexity (Big O Notation), recursion and sorting practices

# Computaitonal complexity

## Big O Notation

Mathematical model used to describe the efficiency of algorithms deppending on their input size

**Constant Time** - **O(1)**
Always executes in the same amount of times, regardless of the input size.
Are ideal, they are not affected by the input size.
*Example: A fuction that check if the first element of an array is a certein value*.

**Linear time** - **O(n)**
It’s performs growth linearly and in direct proportion to the size of the input data set.
1:1 corelation betweeen input size and excecution time
*Example: A sum of the elements in an Array*

**Quadratic Time** - **O(n2)**
Whose performance is directly proportional to the square of the size of the input data set.
Typical with algorithms that involve nested iterations over the input data set.
We should avoid nested loops.

Deeper nested iterations, result in **Cubic Time** - **O(n3)**, **Quartic Time** - **O(n4)**, and worse...

**Logatihmic time** - **O(log n)** *(Logatihmic complexity)*
Represent a highly efficient algorithms (example: binary search, quicksort, divide and conquer)
Excecution time goes up linearly while the input data size grows exponentially 
Logarithm is the inverse operation to exponention.

<image src="https://user-images.githubusercontent.com/42684822/165955139-bcff904a-b261-4336-bd62-0c596af930f2.png" height="80" /><image src="https://user-images.githubusercontent.com/42684822/165955164-166934cd-4f03-496b-ada6-10407fdc8d47.png" height="80" />

## Recursion

**Recursive function** is recursive if it calls itself (example: calculate factorial number)

It must have at least one condition to avoid infitive recursion

<img width="508" alt="Screen Shot 2022-02-07 at 4 32 44 PM" src="https://user-images.githubusercontent.com/42684822/165955522-8ad9f0fc-5795-47f8-8dcb-2921c7498dec.png">

**Recursive Data Structures** *(example linked lists)*

<img width="392" alt="Screen Shot 2022-02-07 at 4 30 31 PM" src="https://user-images.githubusercontent.com/42684822/165955542-34f5cc50-6425-4d3b-a044-dc0bec7b476c.png">


# Sorting

**Selection Sort** _(Quadratic time complexity)_
Select the smallest item and replacing it with the previous one

**Insertion Sort** _(Quadratic time complexity)_
Inserting elements into their proper placer. Largest element must move one position to the right.
It’s performance is affected by the initial order of the elements

**Bubble sort**
Repeating evaluating adjacent items and swapping their position if they are in the wrong order.
Quite innefficient

**Merge sort**
-   divide and conquer technique: splits the original array recyrsively into smaller sublists
-   use for larger sequences / user insertion sort when input is small

**Quick sort**
Most popular for its performance. Divide and conquer strategy: pick a pivot (eje), and split the array in three parts (it calls **partitioning**).
    -   the numbers that are **smaller** than the pivot
    -   the numbers that are **equals** to the pivot
    -   the numbers that are **bigger** than the pivot
    Once we are done with the partioting phase, merge the terminanting sublists.
    

**Selection sort**
-   Start by finding the smallest item and placing it at the first place, next it finds the next smallest item and exchanges it with the second item, and goes on..

<image src="https://user-images.githubusercontent.com/42684822/165955775-5779b5c5-cd74-4317-913b-d3ffd13183ee.png" height="380" />

Easy to implement, use nested loops so it’s time complexity is quadratic, is inefficient.

**Insertion Sort**
-   Large items move to the right.
-   Quadratic time complexity. The performance is largely affected by the initial order of the elements in the sequence

<image src="https://user-images.githubusercontent.com/42684822/165955909-b48b86e0-755d-4747-b353-ed828d105cf6.png" height="230" />

uses two nested loops, it’s worse time cimplexity is quadratic.

Is much more performant than the selection sort if the input array includes already sorted sequences.
-   already sorted input: performs in linear time
-   input is shuffled or reverde ordered: quadratic time

O(n2) worst-case complexity.
Works well for partiall sorted input.
O(n - 1) best-case complexity

**Bubble Sort**
Works by repeatedly evaluating adjacent items and swapping their positions if they are in the wrong order

<image src="https://user-images.githubusercontent.com/42684822/165956197-11ba219a-304d-4374-8b42-00767ae2f852.png" height="400"/>

**Merge Sort**
- Works by splitting the sequence.
- Sub arrays are sorted and merged
- Additional sorting done while merging.

-   divide and conquer technique: splits the original array recyrsively into smaller sublists
-   use for larger sequences / user insertion sort when input is small

<img width="802" alt="mergeSort1" src="https://user-images.githubusercontent.com/42684822/165956830-24ff953b-1f79-4c5d-96f8-f868560c72ca.png">
<img width="845" alt="mergeSort2" src="https://user-images.githubusercontent.com/42684822/165956846-1527d1d2-2878-46b5-91e6-7e58d24cf464.png">

**Quick Sort**
- Divide and conquer approach
- No aditional sorting while merging
- Most popular for its performance
    
-   divide and conquer strategy: pick a pivot (eje), and split the array in three parts (it calls **partitioning**)
    
    -   the numbers that are **smaller** than the pivot
    -   the numbers that are **equals** to the pivot
    -   the numbers that are **bigger** than the pivot
-   Once we are done with the partioting phase, merge the terminanting sublists

    Simple implementation
    
    <image src="https://user-images.githubusercontent.com/42684822/165956998-93e98b18-e963-4c44-b3da-6357c581417f.png" height="321"/>
    
    To improve performance: Smarter partiotining schemes and find the optimal pivot


