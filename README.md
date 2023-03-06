# Grade 11 Java Review Part 2 + Testing

### Step 1: Form Group and Assign Problems
* Form a group of two or three members.
* Create a team repository by clicking on the assignment repository generator.
* There are four sections of problems  - Strings, FileIO, Arrays - Part A, Arrays - Part B. The first member will do the first problem in each section i.e String 1, FileIO 1, etc.  Likewise, the second member will do the second problem in each section, and so on with the third member.

### Step 2: String Problems - TDD
For the first section - Strings - you will do this in the style of TDD (Test-Driven Development).  First, be sure to have a sense of what you want to test (i.e consider general and unusual cases). Next, you will **record a video** as you work through the problem using TDD, that is, repeatedly writing a test and then coding to pass that test.  

<BR>Be sure to:
* write your tests in UtilityTest.java and your solutions in Utility.java.
* commit after each *passing* test
* upload your video to the assignment
  
### Step 3: The Other sections
In the remain problem sections (FileIO, Array - Part A, Array - Part B), you can choose to do it using TDD or code your solutions and write your tests after.  You do not need to record videos for these sections.  There should be at least a commit per method (including test methods).
  
### Program Style & Project Management
* Be sure to use proper style conventions for variable names and comments.
* All methods, including test methods, should be preceded with javadoc comment.
* Name your test methods using the name of the solution method + "Test" + test case #.  For example, if your solution method in `Utility.java` is called `abc()`, there should be corresponding test methods in `UtilityTest.java` called `abcTest1(), abcTest2(), abcTest3() ...` etc.
* all work (testing and solutions) must be done on your development branch and then merged into the main branch upon completing your work.  
  
-------------------

## Problem Sets

### Strings

#### Strings 1 - isInOrder

Create a method that takes a string and returns true or false, depending on whether the characters are in order or not. 
<br>**Signature** `public static boolean isInOrder(String str) `

##### Examples
```
isInOrder("abc") ➞ true
isInOrder("edabit") ➞ false
isInOrder("123") ➞ true
isInOrder("xyzz") ➞ true
isInOrder("d") ➞ true
```

#### Strings 2 - balanced
We can assign a value to each character in a word, based on their position in the alphabet (a = 1, b = 2, ... , z = 26). A balanced word is one where the sum of values on the left-hand side of the word equals the sum of values on the right-hand side. For odd length words, the middle character (balance point) is ignored.
<br>**Signature** `public static boolean balanced(String word)`

#### Examples
```
balanced("zips") ➞ true
// "zips" = "zi|ps" = 26+9|16+19 = 35|35 = true

balanced("brake") ➞ false
// "brake" = "br|ke" = 2+18|11+5 = 20|16 = false
```

#### Strings 3 - swapPair
Write a function that swaps the first pair (1st and 2nd characters) with the second pair (3rd and 4th characters) for every quadruplet substring.
<br>**Signature** `public static String swapPair(String str) `

#### Examples
```
swapPair("ABCDEFGH") ➞ "CDABGHEF"
swapPair("AABBCCDDEEFF") ➞ "BBAADDCCFFEE"
swapPair("munchkins") ➞ "ncmuinhks"
swapPair("FFGGHHI") ➞ "GGFFHHI"
```

### File IO

#### File IO 1 - variance
Given the name of a text file that contains a list of random numbers between 1-1000, write a method that returns the [variance](https://latrobe.libguides.com/maths/measures-of-variability#s-lib-ctab-21952082-2) of the values.
<br>**Signature** `public static String variance(String filenametxt)`

##### Example
See the [example calculations here](https://latrobe.libguides.com/maths/measures-of-variability#s-lib-ctab-21952082-2).  Test variance calculations against a data set using this [variance calculator](https://www.calculatorsoup.com/calculators/statistics/variance-calculator.php). 

#### File IO 2 - stDeviation
Given the name of a text file that contains a list of random numbers between 1-1000, write a method that returns the [standard deviation](https://latrobe.libguides.com/maths/measures-of-variability#s-lib-ctab-21952082-3) of the values.
<br>**Signature** `public static String variance(String filenametxt)`

##### Example
See the [example calculations here](https://latrobe.libguides.com/maths/measures-of-variability#s-lib-ctab-21952082-3).  Test standard deviation calculations against a data set using this [standard deviation calculator](https://www.calculatorsoup.com/calculators/statistics/standard-deviation-calculator.php). 

#### File IO 3 - iqRange
Given the name of a text file that contains a list of *sorted* random numbers between 1-1000, write a method that returns the [interquartile range](https://latrobe.libguides.com/maths/measures-of-variability#s-lib-ctab-21952082-1) of the values.
<br>**Signature** `public static String iqRange(String filenametxt)`

#### Example
input.txt contains:  
```
5
6
7
8
9
```
`iqRange("intput.txt")` --> 2


### Arrays - Part A

#### Arrays A1 - secondLargest
Write a function that takes an array of integers and returns the second largest number.
<br>**Signature** `public static int secondLargest(int[] num)`

##### Example
```
secondLargest([10, 40, 30, 20, 50]) ➞ 40
secondLargest([25, 143, 89, 13, 105]) ➞ 105
secondLargest([54, 23, 11, 17, 10]) ➞ 23
```

#### Arrays A2 - toTheTop
Create a function that returns the total number of steps it takes to transform each element to the maximal element in the array. Each step consists of incrementing a digit by one.
<br>**Signature** `public static int toTheTop(int[] arr)`

##### Example
```
totheTop([3, 4, 5]) ➞ 3
// Maximal element in the array is 5.
// To transform 3 to 5 requires 2 steps: 3 -> 4, 4 -> 5.
// To transform 4 to 5 requires 1 step: 4 -> 5.
// Total steps required is 3.

totheTop([4, 3, 4]) ➞ 1
// Maximal element in the array is 4.
// To transform 3 to 4 requires 1 steps: 3 -> 4.
// Total steps required is 1.

totheTop([3, 3, 3]) ➞ 0

totheTop([3, 10, 3]) ➞ 14
```

#### Arrays A3 - nthSmallest
Given an unsorted array, create a function that returns the nth smallest integer (the smallest integer is the first smallest, the second smallest integer is the second smallest, etc).
<br>**Signature** `public static int nthSmallest(int[] arr, int n)`


##### Examples
```
nthSmallest([1, 3, 5, 7], 1) ➞ 1
nthSmallest([1, 3, 5, 7], 3) ➞ 5
nthSmallest([1, 3, 5, 7], 5) ➞ -1
nthSmallest([7, 3, 5, 1], 2) ➞ 3
```


### Arrays - Part B


#### Arrays B1 - puzzlePieces
Write a function that takes two arrays and adds the first element in the first array with the first element in the second array, the second element in the first array with the second element in the second array, etc, etc. Return true if all element combinations add up to the same number. Otherwise, return false.
<br> **Signature** public static boolean puzzlePieces(int[][] n)


**Note:**
* Each array will have at least one element.
* Return false if both arrays are of different lengths.

##### Examples
```
puzzlePieces([1, 2, 3, 4], [4, 3, 2, 1]) ➞ true
// 1 + 4 = 5;  2 + 3 = 5;  3 + 2 = 5;  4 + 1 = 5
// Both arrays sum to [5, 5, 5, 5]

puzzlePieces([1, 8, 5, 0, -1, 7], [0, -7, -4, 1, 2, -6]) ➞ true

puzzlePieces([1, 2], [-1, -1]) ➞ false

puzzlePieces([9, 8, 7], [7, 8, 9, 10]) ➞ false
```

#### Array B2 - sameUnique
Write a function that returns true if two arrays have the same number of unique elements, and false otherwise.
<br>**Signature** public static boolean sameUnique(int[] a1, int[] a2)

<br>To illustrate:
```
arr1 = [1, 3, 4, 4, 4]
arr2 = [2, 5, 7]
```
In `arr1`, the number 4 appears three times, which means it contains three unique elements: `[1, 3, 4]`. Since `arr1` and `arr2` both contain the same number of unique elements, this example would return `true`.

##### Examples
```
sameUnique([1, 3, 4, 4, 4], [2, 5, 7]) ➞ true
sameUnique([9, 8, 7, 6], [4, 4, 3, 1]) ➞ false
sameUnique([2], [3, 3, 3, 3, 3]) ➞ true
```

#### Array B3 - findFulcrum
A fulcrum of a list is an integer such that all elements to the left of it and all elements to the right of it sum to the same value. Write a function that finds the fulcrum of a list.
<br>**Signature** public static int findFulcrum(int[] arr)

<br> To illustrate:
```
findFulcrum([3, 1, 5, 2, 4, 6, -1]) ➞ 2
// Since [3, 1, 5] and [4, 6, -1] both sum to 9
```


##### Examples
```
findFulcrum([1, 2, 4, 9, 10, -10, -9, 3]) ➞ 4
findFulcrum([9, 1, 9]) ➞ 1
findFulcrum([5, 4, 4, 4, 6, 6, 6]) ➞ -1
findFulcrum([7, -1, 0, -1, 1, 1, 2, 3]) ➞ 0
findFulcrum([8, 8, 8, 8]) ➞ -1
```

<br>**Notes***
* If the fulcrum does not exist, return -1 (see example #3).
* Exclude the leftmost and rightmost elements when computing the fulcrum (it doesn't make sense to sum zero values).
* If a list has multiple fulcrums, return the one that occurs first.
