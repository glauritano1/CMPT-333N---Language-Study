Gary Lauritano
CMPT 333N 

<h1>Journal Entry 03</h1>

<h2>Creating Lists</h2>

1. Conjure the list of positive, even integers up to 10...
  * using only the (:) sigil, [], and number literals
  * using the filter spell on the list [0..]
  * using a list comprehension
  
1 a) 0:2:4:6:8:10:[]<br>
  b) tail (take 6 (filter even [0..]))<br>
  c) [x | x <- [1..], even n]<br>
  
2. Conjure the list of the first 10 square numbers...
   * using only the (:) sigil, [], and number literals
   * by casting the take spell on the appropriate list comprehension
   
2 a) 0:1:4:9:16:25:36:49:64:81:100:[]
  b) take 10 [0,1,4,9,16,25,36,49,64,81,100,121,169,196,225,256,289,324,361,400]

3. Conjure the list of triangular numbers...
  * using explicit recursion and the (:) sigil
  * using a list comprehension
  
3 a) 
  
<h2>Decomposing Lists</h2> 

1. 

<h2>Devise Your Own List Spells</h2> 

<h3>Removing An Element</h3>

removeElement :: [a] -> int -> [a]

removeElement xs x = (. take x-1 (x)) 
  
  

