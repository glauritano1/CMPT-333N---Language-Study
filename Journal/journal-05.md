Gary Lauritano
CMPT 333N Sec 111

<h1>Journal Entry 05</h1>

<h2>Working On the The Easiest Problem Is This One Kattis Problem</h2>

<h3>Input</h3>
The input consists of several test cases. Each case is described by a single line containing one positive integer number N, where 
1≤N≤100000. The last test case is followed by a line containing zero to denote the end of input. 

<h3>The Problem</h3>
Each integer contains either 1 or multiple digits. We must find the sum of each integers digits. For example, the integer 14 has the sum of 5, and the integer 247 has the sum of 13.
Our job is to find a second integer denoted as p, that we can multiply our original integer N with, such that N times p will equal another postive integer whose digits have the same sum of N's digits. This integer p must 
also be the minimal integer that can be multiplied with our inputted integer N to accomplish this. 
For example, if N is 3029 its digits have the sum 14. If we multiply 3029 by 37 the result is 112073. The sum of 112073's digits is 14. Thus they are equal and p is 37. In summary, we must find p.

<h3>Output</h3> 
We must find an integer p for each of our inputted positive integers and output each p on seperate lines. So, we must output only a single positive integer on each line, and this integer will be
the integer p associated with each of the lines of inputted integers.

<h3>Parsing Input</h3>
The input is going to be seperate lines of integers such that 1<N<100000. All input is originally taken as a string since it is coming from an input file. First, we must seperate these
inputs. Since Haskell has a function that seperates strings based on a new line character I used this function. So I used the lines function on our incoming input. This results in a list of strings, where each individual 
string in this list is one of our inputted integers. I left the input as a list of strings instead of converting each input into integers because we are going to further need to break these integers down. There is no 
haskell function to perform a task of summing the digits of integers but there is a function sum, which adds all of the numbers of a list of numbers together. If I would have left them as integers I would need to create a function to break each integers into digits
in order sum up these digits. But, since I left them as strings it easier to break individual integers down into their digits. This is because strings are considered lists of characters.
Here is an example of my code for parseInput: 'parseInput :: String -> [String]<br>
parseInput xs = (lines xs)'

<h3>Doing the Work</h3>
I haven't yet completed this problem, but I will detail what I have done so far, and what problems I my thought process is. 
I will create a seperate function called digitsOfInt which will break up an individual integer into a list of a list of its digits. This function will take a string and output and output a list of strings.
I will use pattern matching to do this. The base case will be an empty string, where the function with equal zero. Next, if a string has a head its will take the head and use the (:) and call itself with the tail of the list. (digitsOfInt x:xs = x:(tail xs))
Next, I will have a function sumOfDigits which will take a list of Strings and output an integer. This function will simply map the read function to convert the individual digits which are strings into integers, and then use the sum
function on this list, which is a predefined Haskell function. It will look something like this 'sum(map read(xs):Integer)'. Next, I will create a function that combines these two functions for simplicity sake. It will be something like 
integerSum or digitsTotal, and will take a String and output an Integer. It will be look like: 'digitsTotal xs = sumOfDigits (digitsOfInt xs)'. Finally, the doTheWorkFunction will take a list of Strings and output a list of integers. It will use a nested if statement and a the digitsTotal function. 
If there is a head to our original string from parseInputs it will see if the total sum if the digitsTotal of that element is equal to the digitsTotal of that element times 11. If it is, it will take that element and call itself with the tail of the parseInput list, if it is not it will check will the next number i.e. 12. 


<h3>Output</h3> 
My showTheResults function will output each integer on a seperate line. It takes a list of integers and outputs an integer. It will use pattern matching. If a the list has a head it will output the head and call itself with the tail of the list, if it is an empty list it will output nothing. 
This is not a completed solution, but this is as far as I have gotten thus far. I will briefly comment on my final solution in my next journal entry on top of the seperate content within that entry, just to give a final updated solution. Or perhaps I will do an extra journal entry titled update with a completed solution. I have a 
pretty good concept and outline of how to complete the task. I just have a few issues that I have run into thus far.



