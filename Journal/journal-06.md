Gary Lauritano
CMPT 333N Sec 111

<h1>Journal Entry 06</h1>

<h2>Using Folds</h2>
This lab session we implemented different versions of fold to get a better feel for how it is working.

<h3>Foldr</h3>
Initial Problem: Foldr (+) 0 [1,2,3,4]
= 1 + Foldr (+) 0 [2,3,4])
= 1 + (2 + (Foldr (+) 0 [3,4]))
= 1 + (2 + (3 + Foldr (+) 0 [4]))
= 1 + (2 + (3 +(0 + 4)))
= 10 
Summary: (1 +(2 +(3 + (4 + 0)))

<h3>Foldl</h3>
Initial Problem: Foldl (+) 0 [1,2,3,4]
= Foldl (+) (0 + 1) [2,3,4,]
= Foldl (+) (1 + 2) [3,4]
= Foldl (+) (3 + 3) [4]
= Foldl (+) (6 + 4)
= Foldl (+) (10)
Summary: ((((0 + 1) + 2) + 3) + 4)

<h2>Implementing Our Own Folds</h2>
- product'

product' = Foldl1 (*) 1

- concat'

concat' = Foldl (++) []

- maximum'

maximum' = foldl max 0 

- reverse' 

reverse' = Foldl (:) []



