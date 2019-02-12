Gary Lauritano
CMPT 333N 

<h1>Journal Entry 03</h1>

<h2>Creating Lists</h2>

1. Conjure the list of positive, even integers up to 10...
   * using only the (:) sigil, [], and number literals
   * using the filter spell on the list [0..]
   * using a list comprehension
  
1  a) 0:2:4:6:8:10:[]<br>
   b) (take 6 (filter even [0..]))<br>
   c) take 6 ([x | x <- [0..], even x]<br>
  
2. Conjure the list of the first 10 square numbers...
   * using only the (:) sigil, [], and number literals
   * by casting the take spell on the appropriate list comprehension
   
2  a) 0:1:4:9:16:25:36:49:64:81:[]
   b) take 10 ([x^2 | x <- [0..]])

3. Conjure the list of triangular numbers...
   * using explicit recursion and the (:) sigil
   * using a list comprehension
  
3  a) 
  
<h2>Decomposing Lists</h2> 

1. Decompose the lists below using two different methods: first using only the take and/or drop spells, and second using the (!!) sigil together with an appropriate other function (hmm... which one?).

From the String "The quick brown fox jumps over the lazy dog.", get each of the following words:
   * "The"
   * "fox"
   * "dog"

1. a) take 3 "The quick brown fox jumps over the lazy dog."
   b) (drop 16 . take 19) "The quick brown fox jumps over the lazy dog."
   c) (take 3 . drop 40) "The quick brown fox jumps over the lazy dog."

2. a) (words "The quick brown fox jumps over the lazy dog.")!!0
   b) (words "The quick brown fox jumps over the lazy dog.")!!3
   c) (words "The quick brown fox jumps over the lazy dog.")!!8
<h2>Devise Your Own List Spells</h2> 

<h3>Removing An Element</h3>

removeElement :: [a] -> int -> [a]

removeElement xs x = (. take x-1 (x)) 
  
----------------------------------------------------------

<h2>Explanation</h2>

`(:)` - This is used to add an element to the front of a list. It is right associative. It will only work by appending a value to a list which means we must use it with an empty list if we are trying to create a list.

`take n` - This function is used to return the first n elements of a list. 

`drop n` - This function takes a parameter of a list and returns a newly created list without the first n elements of the actual parameter. 

`!!n` - This is used after a list to return the element at the index of n. Indexing begins at 0, it is important to remember that. 

`words x` - This function takes a String parameter x, and returns converts x into a list of Strings, by breaking spliting the actual parameter at whitespaces. 

`even xs` - Even is a function that takes a parameter of a list of Nums and returns a list of all of the even elements in the parameter x. 

`tail xs` - This function takes a parameter of a list and returns a newly created list with all of the elements given in the xs except for the first element. In my observation, it seems that tail is quite similar to "drop 1 xs".

----------------------------------------------------------

<h2>Further Exploration</h2>

I have completed a good portion of exploration 2, but still have a section to complete. I will complete the remaining portion of exploration 2 on my free time this week, and report on it in a seperate journal entry. I also have one question left in "Creating Lists" that I was unable to complete because it is stumping me. Not to worry though, I am sure will some diligent research/exploration I will find a solution. 
