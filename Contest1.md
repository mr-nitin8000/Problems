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

2. Crazy Integers

**Problem statement**
An integer is defined as a crazy integer if it contains only the digits ‘1’ and ‘2’. For example: ‘1’, ‘2’, ‘121’ are some crazy integers.
You are given an integer ‘N’. Count the number of non-negative crazy integers less than or equal to ‘N’.
```
Example:
‘N’ = 21
The crazy integers less than or equal to ‘21’ are: ‘1’, ‘2’, ‘11’,  ‘12’, and ‘21’.
So, the count is equal to ‘5’.
```
Constraints:
1 <= 'T' <= 10
1 <= 'N' <= 10^9

Time Limit: 1 sec
``` c++
Sample Input 1:
2
200
101
Sample Output 1:
10
6
Explanation of sample input 1:
For test case 1:

The crazy integers less than or equal to ‘200’ are: ‘1’. ‘2’, ‘11’, ‘12’, ‘21’, ‘22’, ‘111’, ‘112’, ‘121’, and ‘122’,. So, the count is equal to ‘10’. 

For test case 2:

The crazy integers less than or equal to ‘101’ are: ‘1’. ‘2’, ‘11’, ‘12’, ‘21’,  and‘22’. So, the count is equal to ‘6’.
Sample Input 2:
2
300
113
Sample Output 2:
14
8
```

3. K-beauty Components

**Problem statement**
A ‘K-beauty’ of a connected component is defined as the sum of the products of all possible subsets of ‘K’ different nodes within that connected component. For example, if a connected component contains the nodes ‘{1, 2, 5, 3}’, the ‘3-beauty’ would be calculated as: ‘(1 * 2 * 5) + (1 * 2 * 3) + (1 * 5 * 3) + (2 * 5 * 3)’.

There are ‘N’ nodes numbered from ‘1’ to ‘N’ which are disconnected initially. You are given a ‘Queries’ array of length ‘Q’ which contains ‘2’ types of queries:

“1 U V”: Connect ‘U’ and ‘V’ through an edge if there is no edge between them.
“2 U K”: Calculate the ‘K-beauty’ of a connected component which contains a node ‘U’. Since the ‘K-beauty’ can be very large, So take its modulo with ‘10^9 + 7’.
You have to answer all the type ‘2’ queries and return an array. Note that: if a connected component does not contain ‘K’ different nodes, then its ‘K-beauty’ will be equal to ‘0’.
```
Example:
‘N’ = 5
‘Q’ = 5
‘Queries’ = ‘[[1, 2, 5], [1, 3, 4], [2, 2, 2], [1, 5, 4], [2, 5, 3]]’ 

‘Queries[0] = [1, 2, 5]’: It means connect ‘2’ and ‘5’.

‘Queries[1] = [1, 3, 4]’: It means connect ‘3’ and ‘4’.

‘Queries[2] = [2, 2, 2]’: Now we have to calculate the ‘2-beauty’ of a connected component which contains ‘2’. It will be equal to ‘(2 * 5)’ which is ‘10’.

‘Queries[3] = [1, 5, 4]’: It means connect ‘5’ and ‘4’.

‘Queries[4] = [2, 5, 3]’: Now we have to calculate the ‘3-beauty’ of a connected component which contains ‘5’. The connected component contains nodes ‘{2, 5, 4, 3}’. Its ‘3-beauty’ will be equal to ‘(2 * 5 * 4) + (2 * 5 * 3) + (2 * 4 * 3) + (5 * 4 * 3)’, which is ‘154’.

So, the answer for this test case is: ‘[10, 154]’.
```
Constraints:
1 <= 'T' <= 10
1 <= 'N', ‘Q’ <= 10^5
1 <= ‘Queries[i][0]’ <= 2
For ‘Queries[i][0] = 1’:
    1 <= ‘Queries[i][1]’, ‘Queries[i][2]’ <= ‘N’
For ‘Queries[i][0] = 2’:
    1 <= ‘Queries[i][1]’ <= ‘N’
    2 <= ‘Queries[i][2]’ <= 10

Time Limit: 1 sec 
``` c++
Sample Input 1:
2
5 4
1 3 5
2 3 2
1 3 4
2 4 2
3 2
1 1 2
2 2 3
Sample Output 1:
15 47
0
Explanation of sample input 1:
For test case 1:

‘Queries[0] = [1, 3, 5]’: Connect ‘3’ and ‘5’.

‘Queries[1] = [2, 3, 2]’: We have to calculate the ‘2-beauty’ of a connected component containing node ‘3’. It will be equal to: ‘(3 * 5)’ which is ‘15’.

‘Queries[2] = [1, 3, 4]’: connect ‘3’ and ‘4’.

‘Queries[3] = [2, 4, 2]’: We have to calculate the ‘2-beauty’ of a connected component containing node ‘4’. It will be equal to ‘(3 * 5) + (3 * 4) + (4 * 5)’ which is ‘47’.

So, the answer for this test case is ‘[15, 47]’.

For test case 2:

‘Queries[0] = [1, 1, 2]’: Connect ‘1’ and ‘2’.

‘Queries[1] = [2, 2, 3]’: We have to calculate the ‘3-beauty’ of a connected component containing node ‘2’. As the number of nodes in a connected component is less than ‘3’. So, the ‘3-beauty’ will be equal to ‘0’.

Hence, the answer for this test case is ‘[0]’.
Sample Input 2:
2
5 5
1 2 5
1 3 4
2 2 2
1 5 4
2 5 3
3 4
1 1 2
1 2 3
1 1 3
2 2 2
Sample Output 2:
10 154
11
```
