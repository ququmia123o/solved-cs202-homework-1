Download Link: https://assignmentchef.com/product/solved-cs202-homework-1
<br>
<h1>Question 1</h1>

<ul>

 <li>[5 points] Show that <em>f</em>(<em>n</em>) = 100<em>n</em><sup>3 </sup>+8<em>n</em><sup>2 </sup>+4<em>n </em>is <em>O</em>(<em>n</em><sup>4</sup>) by specifying appropriate <em>c </em>and <em>n</em><sub>0 </sub>values in Big-O de nition.</li>

 <li>[5 points] Find the asymptotic running time (in O notation, tight bound) of the recurrence equation <em>T</em>(<em>n</em>) = 8<em>T</em>(<em>n/</em>2)+ <em>n</em><sup>3 </sup>where <em>T</em>(<em>n</em>) = 1 for all <em>n </em>≤ 100. Use the repeated substitution method and show your steps in detail.</li>

 <li>[5 points] Express the running time complexity (using asymptotic notation) of the following loop. Show all the steps clearly.</li>

</ul>

for (i = n; i &gt; 0; i /= 2) { for (j = 1; j &lt; n; j++) { for (k = 1; k &lt; n; k += 2) { sum += (i + j * k); } } }

<ul>

 <li>[10 points] Trace the following sorting algorithms to sort the array [16, 6, 39, 21, 10, 21, 13, 7, 28, 19] in ascending order. Use the array implementation of the algorithms as described in the textbook and show all major steps.</li>

</ul>

Selection sort

Insertion sort

<h1>           Question 2</h1>

Implement the following methods in the sorting.cpp        le:

<ul>

 <li>[40 points] Implement the radix sort, bubble sort, quick sort, and merge sort algorithms. Your functions should take an array of integers and the size of that array and then sort it in the ascending order. Add two counters to count and return the number of key comparisons and the number of data moves for all sorting algorithms except the radix sort. For the quick sort algorithm, you are supposed to take the rst element of the array as pivot. Your functions should have the following prototypes: void bubbleSort(int *arr, int size, int &amp;compCount, int &amp;moveCount); void quickSort(int *arr, int size, int &amp;compCount, int &amp;moveCount); void mergeSort(int *arr, int size, int &amp;compCount, int &amp;moveCount); void radixSort(int *arr, int size);</li>

</ul>

For key comparisons, you should count each comparison like <em>k</em><sub>1 </sub>&lt; <em>k</em><sub>2 </sub>as one comparison, where <em>k</em><sub>1 </sub>and <em>k</em><sub>2 </sub>correspond to the value of an array entry (that is, they are either an array entry like arr[i] or a local variable that temporarily keeps the value of an array entry).

For data moves, you should count each assignment as one move, where either the right-hand side of this assignment or its left-hand side or both of its sides correspond to the value of an array entry (e.g. a swap function mostly has 3 data moves).

<ul>

 <li>[5 points] Implement a function that prints the elements in an array.</li>

</ul>

void printArray(int arr, int size);

<ul>

 <li>[10 points] In this part, you will analyze the performance of the sorting algorithms that you implemented in part a. Write a function named performanceAnalysis which creates four identical arrays of 2000 random integers. Use one of the arrays for the radix sort, second for bubble sort, third for the merge sort, and the last one for the quick sort algorithm. Output the elapsed time (in milliseconds), the number of key comparisons and the number of data moves. Number of key comparisons and number of data moves are not required for the radix sort. Repeat the experiment for the following sizes: 6000, 10000, 14000, 18000, 22000, 26000, 30000.</li>

</ul>

When the performanceAnalysis function is called, it needs to produce an output similar to the following one:

Listing 2: Sample output

—————————————————–

Part c – Time analysis of Radix Sort

<table width="250">

 <tbody>

  <tr>

   <td width="144">Array Size</td>

   <td width="106">Time Elapsed</td>

  </tr>

  <tr>

   <td width="144">2000</td>

   <td width="106">x ms</td>

  </tr>

  <tr>

   <td width="144">6000</td>

   <td width="106">x ms</td>

  </tr>

 </tbody>

</table>

…

—————————————————-Part c – Time analysis of Bubble Sort

Array Size                            Time Elapsed                   compCount            moveCount

2000                                                   x ms                                      x                               x

6000                                                   x ms                                      x                               x

…

—————————————————-Part c – Time analysis of Quick Sort

Array Size                            Time Elapsed                   compCount            moveCount

2000                                                   x ms                                      x                               x

6000                                                   x ms                                      x                               x

…

—————————————————-Part c – Time analysis of Merge Sort

Array Size                            Time Elapsed                   compCount            moveCount

2000                                                   x ms                                      x                               x

6000                                                   x ms                                      x                               x

…

—————————————————–

<ul>

 <li>[5 points, mandatory] Create a main.cpp le which does the following in order:</li>

</ul>

creates an array from the following numbers: {7<em>,</em>3<em>,</em>6<em>,</em>12<em>,</em>13<em>,</em>4<em>,</em>1<em>,</em>9<em>,</em>15<em>,</em>0<em>,</em>11<em>,</em>

14<em>,</em>2<em>,</em>8<em>,</em>10<em>,</em>5}

calls the bubbleSort method and the printArray() method calls the quickSort method and the printArray() method calls the mergeSort method and the printArray() method calls the radixSort method and the printArray() method

calls the performanceAnalysis() method

At the end, write a basic Make le which compiles all of your code and creates an executable le named hw1. Check out these tutorials for writing a simple make le: <a href="http://mrbook.org/blog/tutorials/make/">tutorial</a> <a href="http://mrbook.org/blog/tutorials/make/">1</a><a href="http://mrbook.org/blog/tutorials/make/">,</a> <a href="http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/">tutorial</a> <a href="http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/">2</a><a href="http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/">.</a> <u>Please make sure that your Makefile works properly, otherwise you will not get any points from Question 2.</u>

Important note: Add the screenshot of the console output of Question 2 to the pdf submission.

<h1>           Question 3         15 points</h1>

After running your programs, you are expected to prepare a single page report about the experimental results that you obtained in Question 2 c. With the help of a spreadsheet program (Microsoft Excel, Matlab or other tools), plot elapsed time versus the size of array for each sorting algorithm implemented in question 2. Combine the outputs of each sorting algorithm in a single graph. A sample gure is given in Figure 1 (these values do not re ect real values).

In your report, you need to discuss the following points:

Interpret and compare your empirical results with the theoretical ones. Explain any di erences between the empirical and theoretical results, if any.

How would the time complexity of your program change if you applied the sorting algorithms to an array of decreasing numbers instead of randomly generated numbers?

Figure 1: Sample       gure for Sorting Performance Analysis