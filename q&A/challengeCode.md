#### "Total ways to sum up to a number"

Your solution will be scored against multiple hidden test cases, with a sample case being provided for your reference.
The default code includes a mechanism for reading input strings. You will need to parse these strings into the appropriate variables as needed.
The output data type is not a concern, as long as the characters within the output box match the expected outcome.
Problem Description


Write a program that calculates the total number of unique ways to sum up to a given positive integer n using one or more positive integers.

For a given positive integer n, it can be summed up using one or more positive integers:

n = n

n = (n-1) + 1

n = (n-2) + 2

n = (n-2) + 1 + 1

n = (n-3) + 3

n = (n-3) + 2 + 1

n = (n-3) + 1 + 1 + 1
....

n = 1 + 1 + 1 + ... + 1

For example, there are totally 7 ways to sum up to the number "5":

5 = 5

5 = 4 + 1

5 = 3 + 2

5 = 3 + 1 + 1

5 = 2 + 2 + 1

5 = 2 + 1 + 1 + 1

5 = 1 + 1 + 1 + 1 + 1

Note: 3+2 and 2+3 are counted as single possibility. We are only looking for unique combinations which contain numbers in strictly descending order.

Input/Output Format

Input
The first line of input will contain a single integer t, the number of test cases. Each of the next t lines will contain a single integer n.
Each number n will be between 1 and 200, inclusive.

Output
For each test case, output a single line containing the total number of unique ways to sum up to the integer n.

Example
Input:
1
5

Output:
7

Explanation: The first line in input "1" tells us how many numbers will be in total. Then we calculate how many different ways we can sum up to number 5 - which is 7 (explanation given above).

Sample Input:

 7 <br>
 1 <br>
 2<br>
 3<br>
 4<br>
 5<br>
 7

Sample Output:

1<br>
2<br>
3<br>
5<br>
7<br>
15


Code Template
python# 

# Use urllib.request to send network request if needed.
import fileinput

inputData = ''

for line in fileinput.input():
    inputData += line

def code_here():
    # Use the function to return the solution.
    return inputData

print(code_here())
