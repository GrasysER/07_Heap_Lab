07_HeapLab
==============

Implement a heap in C++

Requirements
------------

1. `add` and `remove` should be O(log n), except for `grow` which can be O(n)
2. Do not leak memory

Reading
=======
"Open Data Structures," Chapter 10, just the intro and section 1. http://opendatastructures.org/ods-cpp/10_Heaps.html

Questions
=========

#### 1. Which of the above requirements work, and which do not? For each requirement, write a brief response.

1. add and remove are both O(log n) since both methods must make use of bubbleUp and trickleDown to restore the heap condition. Grow is 0(n) due to reallocating all items in the array to a new array.
2. Delete is used to prevent memory leaks.

#### 2. Exercises 10.1 and 10.2 from http://opendatastructures.org/ods-cpp/10_3_Discussion_Exercises.html
10.1: 
Add 7 to an open spot(bottom right), bubble up to the correct spot by switching with 16.

Add 3 to an open spot(bottom right), bubble up to the correct spot by switching with 7, 6, and finally 4.

10.2:
Switch 6 with largest number(bottom right, 55) and remove it, trickle down 55 to the correct spot by switching 55 with 8 then 50.

Switch 8 with largest number(bottom right, 93) and remove it, trickle down 93 to the correct spot by switching 93 with 9, 26, and 32.

#### 3. Exercise 10.4 from http://opendatastructures.org/ods-cpp/10_3_Discussion_Exercises.html
Parent: (i-1)/2

Left child: 2*1+1

Right child: 2*i+2

#### 4. What is one question that confused you about this exercise, or one piece of advice you would share with students next semester?

Advice for students next semester would be to understand the diagrams of what happens when add and remove are called. The code is pretty easy if you understand how those 2 methods should look.