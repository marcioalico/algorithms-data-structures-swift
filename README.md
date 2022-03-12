
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

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/cb6dff7d-7901-46e6-b729-786009e801df/Screen_Shot_2022-02-07_at_12.49.22_PM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45/20220312/us-west-2/s3/aws4_request&X-Amz-Date=20220312T165933Z&X-Amz-Expires=86400&X-Amz-Signature=df9968b496ea8a83af6e5179c5bc1559bfc0aab3f82f37cacd818202d0dd92eb&X-Amz-SignedHeaders=host&response-content-disposition=filename%20=%22Screen%2520Shot%25202022-02-07%2520at%252012.49.22%2520PM.png%22&x-id=GetObject" height="80" /> <image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/06d7c693-168e-4270-94b0-bf060e3d692f/Screen_Shot_2022-02-07_at_12.51.26_PM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45/20220312/us-west-2/s3/aws4_request&X-Amz-Date=20220312T165944Z&X-Amz-Expires=86400&X-Amz-Signature=a06bfbc787b685eab656efb33b072e7d53df74744281b68a06ed99ecbda65820&X-Amz-SignedHeaders=host&response-content-disposition=filename%20=%22Screen%2520Shot%25202022-02-07%2520at%252012.51.26%2520PM.png%22&x-id=GetObject" height="80" />

## Recursion

**Recursive function** is recursive if it calls itself (example: calculate factorial number)

It must have at least one condition to avoid infitive recursion

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/63ae308e-e0d2-4e64-837d-85eca768a21d/Screen_Shot_2022-02-07_at_4.32.44_PM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45/20220312/us-west-2/s3/aws4_request&X-Amz-Date=20220312T165827Z&X-Amz-Expires=86400&X-Amz-Signature=d0f21fe7e71cdbfbccbbb7ee636724c240227e2f2508750fdc5b2432269306fd&X-Amz-SignedHeaders=host&response-content-disposition=filename%20=%22Screen%2520Shot%25202022-02-07%2520at%25204.32.44%2520PM.png%22&x-id=GetObject" height="380" />

**Recursive Data Structures** *(example linked lists)*

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e6ea2efe-4acf-40fa-be54-18bea8f54e98/Screen_Shot_2022-02-07_at_4.30.31_PM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45/20220312/us-west-2/s3/aws4_request&X-Amz-Date=20220312T165755Z&X-Amz-Expires=86400&X-Amz-Signature=540cf1610c9cd1dfb4c7e1ee06bd8fd7bf78e55309d089f18a5571397259ed15&X-Amz-SignedHeaders=host&response-content-disposition=filename%20=%22Screen%2520Shot%25202022-02-07%2520at%25204.30.31%2520PM.png%22&x-id=GetObject" height="380"/>

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

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/e5b35a8d-a553-440e-ae8d-2557f5cd88ab/Screen_Shot_2022-02-08_at_8.30.48_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T170833Z&X-Amz-Expires=86400&X-Amz-Signature=b682525c39444a2a52f568930505eb878588a11ca855ae2a9623f6911f225084&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25208.30.48%2520AM.png%22&x-id=GetObject" height="380" />

Easy to implement, use nested loops so it’s time complexity is quadratic, is inefficient.

**Insertion Sort**
-   Large items move to the right.
-   Quadratic time complexity. The performance is largely affected by the initial order of the elements in the sequence

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/c0a8aac3-7c65-4e74-b670-d6195a273a6e/Screen_Shot_2022-02-08_at_8.40.34_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T171040Z&X-Amz-Expires=86400&X-Amz-Signature=5338b66675e99b17424ddf3c95e560a34da3218a5311578e8a2770507b9613fc&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25208.40.34%2520AM.png%22&x-id=GetObject" height="230" />

uses two nested loops, it’s worse time cimplexity is quadratic.

Is much more performant than the selection sort if the input array includes already sorted sequences.
-   already sorted input: performs in linear time
-   input is shuffled or reverde ordered: quadratic time

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/76b332bb-238f-4ca8-887d-68074561ff8d/Screen_Shot_2022-02-08_at_8.48.19_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T171238Z&X-Amz-Expires=86400&X-Amz-Signature=fc1b003f5dd36b648908b1ec2bd5a171cdec90f4c342a4b352419a5b8c3c1927&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25208.48.19%2520AM.png%22&x-id=GetObject" height="140"/>


**Bubble Sort**
Works by repeatedly evaluating adjacent items and swapping their positions if they are in the wrong order

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/93102337-7597-41b5-926c-331fc275d01b/Screen_Shot_2022-02-08_at_8.50.54_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T171338Z&X-Amz-Expires=86400&X-Amz-Signature=a42cb8014e86c902b72e6cebb8601d30bf67956126b97d190da3372e4f42ad83&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25208.50.54%2520AM.png%22&x-id=GetObject" height="400"/>

**Merge Sort**
Works by splitting the sequence. Sub arrays are sorted and merged
Additional sorting done while merging.

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/faf0fc07-8718-414d-8130-f0010dae64e5/Screen_Shot_2022-02-08_at_9.25.27_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T171503Z&X-Amz-Expires=86400&X-Amz-Signature=2e9e8ab238789b325c10e82a54ae9a4b2214201ca579fafdae9d18a2a6befade&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25209.25.27%2520AM.png%22&x-id=GetObject" height="300"/>

-   divide and conquer technique: splits the original array recyrsively into smaller sublists
-   use for larger sequences / user insertion sort when input is small
-   
<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/8cdf7129-2d0a-4b8d-9c83-91ae972a241a/Screen_Shot_2022-02-08_at_9.31.31_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T171550Z&X-Amz-Expires=86400&X-Amz-Signature=075e7a7a197680ec8999f5b20b6afbe4936af1afb71ec2df17bfc0ed2a1db3d3&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25209.31.31%2520AM.png%22&x-id=GetObject" height="235"/>

<image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a7d82528-e829-4718-816d-cf49036a5f9e/Screen_Shot_2022-02-08_at_9.31.05_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T171615Z&X-Amz-Expires=86400&X-Amz-Signature=0215272a19f91c43634cab61de538188c89581c19717267eba5c9ee5728d2ca8&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25209.31.05%2520AM.png%22&x-id=GetObject" height="521"/>

**Quick Sort**

-   Most popular for its performance
    
-   divide and conquer strategy: pick a pivot (eje), and split the array in three parts (it calls **partitioning**)
    
    -   the numbers that are **smaller** than the pivot
    -   the numbers that are **equals** to the pivot
    -   the numbers that are **bigger** than the pivot
-   Once we are done with the partioting phase, merge the terminanting sublists
    
    Simple implementation
    
    <image src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4f980325-2eb5-41ae-bd4f-03d0adc989a5/Screen_Shot_2022-02-08_at_9.56.25_AM.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220312%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220312T171814Z&X-Amz-Expires=86400&X-Amz-Signature=ab660937baf3397daff450040b48791212722f2e6d0cda243d28562ac0863317&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Screen%2520Shot%25202022-02-08%2520at%25209.56.25%2520AM.png%22&x-id=GetObject" height="321"/>
    
    To improve performance: Smarter partiotining schemes and find the optimal pivot


