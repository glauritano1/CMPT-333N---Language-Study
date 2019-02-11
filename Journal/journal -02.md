Gary Lauritano
CMPT 333N Sec 111

<h1>Journal Entry 02</h1>

<h2>Solving the Aaah! Kattis Problem</h2>

In this problem, Jon Marius is trying to determine which doctor he should go to. Jon doesn't like to say "aah" for too long when the doctors ask him to. He is trying to compare how long he can say "aah" to how long each doctor is going to ask hime to say "aah".

<h3>Input</h3> 

For this problem you are given two lines of input. The first line is how long Jon can say "aah" that day. The second line is the length of the "aah" that the doctor would like to hear. 

<h3>Output</h3>

We need to be able to inform Jon which doctor(s) he would be able to go to, and which doctor(s) he wouln't. In order to do this, we will simply output a String saying go or a String saying no. 

<h3>Solution</h3> 

<h4>Parsing Input</h4>

This problem is pretty simple to solve. The input is two lines, but they are not in any format. First, we need to parse the input into two seperate lines. This is done within our parseInput function. The parseInput function uses the commands show, which will convert our input into one String. This function takes an input of any type and converts it into a String. Next, we will need to seperate this singular String into seperate lines. This is because later on in solution code, we are going to have to compare these lines to one another.

So, to do this, we use the lines function. The lines function takes a String, and seperates it into a list of Strings, where each line of input ends. 

In total our parseInput function takes an parameter of any type and converts it into a list of Strings. 

<h4>Doing the Work</4>

The work portion of this solution, involves making a comparison between the two lines of input. We need to compare the length of Jon's "aah" to the length of the candidate doctor's "aah", to see if Jon would be able to go to that doctor. Since our input has been converted into a list of Strings, that consist of the two now seperate lines of input, we can compare them. First, we must take the first item of the list to isolate the first line of input. Luckily, their is already a Haskell function, that was taught to us by Professor Johnson, that does just that. This is the head function. The head function take a parameter of any type of list and returns the first element or item in that list.

Next we need to find out how long Jon's "aah" is. Since the input of this function is strictly an amount of lowercase a's between 0 and 999 followed by a single h, there are no conversions that need to be done formatting wise. Therefore, since the formats between the two lines of input will be the same except for the number of lowercase a's in each line of input, we can simply find the length of each line of input in order to compare them. Once again, their is already a Haskell function that can do just that. This is the length function. I discovered this function using Hoogle in our previous lab. This function takes a parameter of a list of any type, and outputs an integer that specifies how many items are in that list. This works perfectly, because a String is just a list of characters.

Using the head and length function we are able to find the length of the first line. The next step is finding the length of the second line of input.

We already know that we can use the length function on a String to determine the amount of characters it contains, but now we have to isolate the last line of input in order to do so. It is important to remember that our two input lines are currently a list of Strings thanks to the lines function. So, if we just use the length function it will only return the length of our list of Strings, not the length of the second line itself. We used the head function previously to isolate just the first line, so can we do something similar here? 

Thinking back to Professor Johnson's lecture on lists, their was a similar type of function taught to us that does the oposite of the head function. This is the last function. This function returns the last element/item in a list. Would this work? We know that their are only two lines, so their should be only two elements/items in our list of Strings created by the lines function. If this is the case then the last element/item of our list would be be the second line we are trying to isolate. So, the last function is perfect for this situation. Now that we can isolate the last line of input, we can use the length function on it. 

If we are able to get the length of both strings then we simply need to compare them to determine if Jon's "aah" is smaller than the "aah" that the candidate doctor requires.

So, our doTheWork function will take the length of the head of the list and check whether it is less than the length of the last element of the list. If it is it will return false, else it will return true.

The doTheWork function takes a parameter of a list of Strings, and outputs a Bool (Boolean). 

<h4>Showing the Results</h4> 

This is the easy part of the solution. We will already know whether Jon's aah is smaller than the candidate doctor's required "aah" so 
if it is we simply output "no", else we output "go". To do this we use an if-then statement. If doTheWork then "go" else "no". The doTheWork function will only retrun true if Jon's "aah" is greater than the candidate doctor's required "aah", in which case we will tell him to "go". Otherwise it will return false, and we will tell him "no"

The showResults function takes a parameter of a Bool (Boolean) and outputs a String.

