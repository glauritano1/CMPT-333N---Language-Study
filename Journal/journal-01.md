Gary Lauritano – Journal Entry 01

<h1>Arithmetic Operations</h1>

I will be using 5 different operators, 5 times each and recording any notable observations.

**+** -> I used this operators 5 times and each time the result shown by the GHCi was the mathematical sum of the two numbers being compared by it. 

**-** -> Using this operator 5 times in the same manner that I used the plus operator yeilds the mathematical difference of the two numbers being compared by it. Something to note, is that spacing does not matter when using this operator. As long as there is a number entered, and the next entry besides white space is the operator followed by an entry of another number it will execute.

***** -> This operator with compute the mathematical sum of the numbers entered of each side of it. 

**/** -> This operator compares two integers and will compute the difference of these integers. Something to note about the result of this operation is that it is automatically converted into a floating point number. Even if the result would be a perfect integer it is converted to a floating point number. Also, when dividing by a negative number, you must enclose the negative number in parenthesis. 

**++** -> This operator is appends. It will take a list of any data type and append it to another list of the SAME data type. They also must be lists. They cannot be singular data types like a character and another character. Also, any white spaces are considered characters, so they are left within the lists.

<h1>Named Arithmetic Functions</h1>

  I will be using 4 different named arithmetic operators, 5 times each and recording any notable observations.

mod or `mod` -> Mod can be put before its inputs. The first input following mod would be the dividend, and the second input would be the divisor. This function only takes inputs and provides outputs of integers. Mod can also be used as an infix operator. This means it can be put in the middle of its inputs similar to a “+” operator or a “-“ operator. To do this the operator must be encased in backquotes. 

Example: 5 `mod` 1.

  The output of this operator is the mathematical remainder of the two integers being compared. So the output of this example would be 0 because 5 divided by 1 would be 5 with a remainder of 0.


rem -> This function will take two inputs. The first input will be the dividend and the second input will be the divisor. The output of this function will be the mathematical remainder after the comparison of the two inputs is made. This function only takes inputs and provides outputs of integers. This is similar to the mod named arithmetic function. It can also be an infixed function, or put in the middle of its inputs encased in backquotes.

The main difference between rem and mod, is noted when the divisor is a negative number. You will receive different outputs because the mod function is based off of a premise (x `div` y)*y + (x `mod` y) == x. The div function is truncated toward negative infinity. As opposed to the rem function, which is based off of the premise (x `quot` y)*y + (x `rem` y) == x. The quot function is truncated toward zero.  

Example Output: 
 

div -> The div function also takes two inputs and can be used as an infix function. Its first input would be the dividend, while the second input would be the divisor. This function only takes inputs and provides outputs of integers. The output of the function would be the mathematical quotient of the two compared inputs. The div function is truncated toward negative infinity. This means that if the actual mathematical quotient would be a decimal in between negative integers, the result would be rounded to an integer closer to negative infinity.


quot -> The quot function takes two inputs and can be used as an infix function. Its first input would be the dividend, while the second input would be the divisor. This function only takes inputs and provides outputs of integers. The output of the function would be the mathematical quotient of the two compared inputs. The quot function is truncated toward zero. This means that if the actual mathematical quotient would be a decimal in between negative integers, the result would be rounded to an integer closer to negative infinity.

Difference Between div and quot Functions Example: 
5 divided by (-3) equals -1.6666666666666666666666666666667
 

							                                     **Mapping**

  Mapping allows a function that would be applied to only one element of a list, to be applied to every element in that list. It is a general purpose function, and can be applied in accordance with many other function. 

map (*2) -> This function multiplies the elements of a list by two, or doubles all elements of a list as long as they are of the number type class.
 
map abs -> This function will find the absolute values or the distance from zero, of all elements of a list as long as they are of the number type class. 
 
map (>10) -> This function will check all elements of a list to determine whether they are greater than 10. The output of this function will be a list of Boolean values equal in size to that of the list of numbers. Each Boolean value will have a position in its list that correlates to the number of the originally compared list. In the following example the first value of the Boolean list is False, which correlates to the comparison of (>10) with 1. The second value of the Boolean list is False, which correlates to the comparison of (>10) with 2. Etc..

Example: 
 

map null -> The null function originally takes an input of a list. It checks whether a list of any type is empty or not and then returns a Boolean value. 

Example:
 

  If you do not supply it with a list of items, and supply it will a singular item it will cause an error. 

Example: 
 

  Therefore, using the map function in conjunction with the null function means we must provide an input of a list of lists of any type. Otherwise, this will cause an error. When we provide a valid input of a list of lists, the mapping of the null function, applies the null function to all lists within the list of lists, and returns a list of Boolean values. Each Boolean values position in the output list correlates to the position of the list being compared, within the inputted list of lists.

Examples: 
 
 



**Arithmetic Expressions**

  Supposing that f is a function such that f x = x * x – 1, I will give what I think is the solution to the following questions, without entering the into the GHCi first.

f(2) + 1 : 4 
f (3 + 2) : 24 
f 1 + 5 : 5 
f 0 + f 2 : 2 
5 - f 2 : 2
f f 1 : -1 

  The key to solving these questions lies with knowing the highest order of binding in Haskell as well as the order of operations within the function itself. 

**Mapping**

[1,2,3,4] to [-1,-2,-3,-4] -> For this problem I used map function in conjunction with negate and supplied the input list. Negate takes an input of a number and makes that number a negative. Using map with this function applied the negate function to every element of this list.

"Even the very Wise cannot see all Ends." to "even the very wise cannot see all ends." -> For this problem I used the map function in conjunction with the toLower function. The toLower function takes an individual character and outputs that character in lowercase form. The map function allowed me to apply the toLower function to a list of characters. This gave me the desired output.

[1,2,3] to [3,6,9] -> For this problem I used the map function in conjunction with the (*3) function. The (*3) function takes the input of a number and outputs that number value tripled. Using the map function allowed me to apply the (*3) function to all values of my number list, resulting in the desired output.  

"Go back to the Shadow!" to "GO BACK TO THE SHADOW!" -> For this problem I used the map function in conjunction with the toUpper function. The toUpper function takes an individual character and outputs that character in uppercase form. The map function allowed me to apply the toUpper function to a list of characters. This gave me the desired output.

[1,2,3] to [0,1,2] -> For this problem I used the map function in conjunction with the function (subtract 1). The function (subtract 1) takes the input of a number and subtracts 1 from that value. Using the map function allowed me to apply the function (subtract 1) to a list of numbers. This achieved the desired output. 

["Olorin","Curumo","Aiwendil"] to [6,6,8] -> 

[0,1,1,2,3,5,8] to [True,False,False,True,False,False,True] -> For this problem I used the map function in conjunction with the even function. The even function takes the input of a number and outputs a Boolean value of True if that number is even and False if the number is not even. Using the map function allowed me to apply the even function to a list of numbers giving me the desired output.