# Questions

1. Quantised Number

**Problem statement**
A number is said to be a Quantised Number, if it is divisible by ‘3’ and consists entirely of identical digits. For example: ‘666’ is a Quantised number.
You are given ‘2’ integers ‘L’ and ‘R’. You have to count all the Quantised numbers from ‘L’ to ‘R’. Here, ‘L’ and ‘R’ are both included in the range.
Your task is to count the Qunatised numbers from ‘L’ to ‘R’ and return it.
```
Example:
‘L’ = 5
‘R’ = 125
The Quantised numbers from ‘L’ to ‘R’ are: ‘6’, ‘9’, ‘33, ‘66’, ‘99’, and ‘111’.
So, the count is equal to ‘6’.
```
Constraints:
1 <= 'T' <= 10
1 <= 'L' <= ‘R’ <= 10^15

Time Limit: 1 sec
``` c++
Sample Input 1:
2
1 390
90 580
Sample Output 1:
9
6
Explanation of sample input 1:
For test case 1:

The Quantised numbers from ‘1’ to ‘390’ are: ‘3’, ‘6’, ‘9’, ‘33’, ‘66’, ‘99’, ‘111’, ‘222’, and ‘333’.

So, the count is equal to ‘9’.

For test case 2:

The Quantised numbers from ‘90’ to ‘580’ are: ‘99’, ‘111’. ‘222’, ‘333’, ‘444’, and ‘555’.

So, the count is equal to ‘6’.
Sample Input 2:
2
100 900
50 60
Sample Output 2:
8
0
```
