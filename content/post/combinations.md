---
title: "Combinations"
date: 2019-10-23T13:42:18-05:00
draft: true
---
# deleteDigit

I like to have a playground like [codesignal](www.app.codesignal.com) to write code time to time.

The intent of this post is to show you how easy is to solve these kind of problems without getting deeper to finding the optimal solution.

I will borrow this description from *challenges* section and I extremely suggest to give it a shot before read the solution.


    Given some integer, find the maximal number you can obtain by deleting exactly one digit of the given number.

    Example

    For n = 152, the output should be
    deleteDigit(n) = 52;
    For n = 1001, the output should be
    deleteDigit(n) = 101.
    Input/Output

    [execution time limit] 4 seconds (py3)

    [input] integer n

    Guaranteed constraints:
    10 ≤ n ≤ 106.

    [output] integer

This is my intuitive, straightforward, brute force and accepted solution:

{{< highlight python "linenos=table,hl_lines=8 15-17,linenostart=1" >}}
import itertools
def deleteDigit(n):
    str_n=str(n)
    current_max_value=-1
    for selected_elements in itertools.combinations(str_n,len(str_n)-1):
        value=int(''.join(selected_elements))
        if value > current_max_value:
            current_max_value=value
    return current_max_value
{{< / highlight >}}

## Explanation

### Pseudocode

1. Take all possible combinations of `(# of digits) - 1` digits
2. Compare the result of each combination with the current maximum value and update it
3. Return the maximum value

### What you need to know to implement it in Python?

#### How to to use `itertools.combinations`

`itertools` is not a built-in module so you need to explicit import it

The `combinations` function receives 2 parameters:
    - a list of elements
    - number of elements that you need to take

*Examples*

{{< highlight python "linenos=table,hl_lines=8 15-17,linenostart=1" >}}
import itertools
elements = [1,2,3]
itertools.combinations(elements,1) #[(1,), (2,), (3,)]
itertools.combinations(elements,2) #[(1, 2), (1, 3), (2, 3)]
{{< / highlight >}}

#### Convert a list of digits to integer
    
An easy way to do this is concatenate all digits and then convert it to an integer. We are using a comprehension list to convert each digit to string.

{{< highlight python "linenos=table,hl_lines=8 15-17,linenostart=1" >}}
list_of_digits = [1,2,3]
str_list_of_digits = [str(d) for d in list_of_digits] #['1','2','3']
str_number = ''.join(str_list_of_digits) # '123'
int_number = int(str_number) # 123
{{< / highlight >}}

#### Calculate the max value in a list

Assume that you have a list of positive numbers you can initialize your `max_current_value` with a negative number right because all of the elements in your list are greater than.

{{< highlight python "linenos=table,hl_lines=8 15-17,linenostart=1" >}}
max_current_value = -1
elements = [71,12,31,141,23,32]
for element in elements:
    if value > current_max_value:
            current_max_value=value
print(current_max_value) #141
{{< / highlight >}}


