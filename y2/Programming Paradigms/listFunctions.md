# Haskell List Functions
##
### *`!!`* - returns element at a specific index (0-indexed)
```[1,2,3,4] !! 2```  => 3    
> *Note: Cannot use negative numbers e.g. (-1) as indexes*  
##
### *`head`* - returns first element
```head [1,2,3,4]```  => 1
##
### *`tail`* - returns everything but the head
```tail [1,2,3,4]```  => [2,3,4]
##
### *`last`* - returns last element
```last [1,2,3,4]```  => 4
##
### *`init`* - returns everything but the last element
```init [1,2,3,4]```  => [1,2,3]
##
### *`length`* - returns the length of a list
```length [1,2,3,4]```  => 4
##
### *`null`* - returns True if a list is empty, False otherwise
```null [1,2,3,4]```  => False
```null []```  => True
##
### *`reverse`* - reverses the list
```reverse [1,2,3,4]```  => [4,3,2,1]
##
### *`take`* - takes a number n and a list, returns the first n elements of the list
```take 2 [1,2,3,4]```  => [1,2] 
```take 0 [1,2,3,4]```  => []  
```take 6 [1,2,3,4]```  => [1,2,3,4]  
> *Note: Does not error if n is greater than the length of the list*  
##
### *`drop`* - takes a number n and a list, returns the list with the first n elements removed
```drop 2 [1,2,3,4]```  => [3,4]  
```drop 0 [1,2,3,4]```  => [1,2,3,4]  
```drop 67 [1,2,3,4]``` => []  
##
### *`minimum`* and *`maximum`* - returns the minimum/maximum value in the list - list MUST be of type **[Ord]**
```minimum [1,2,3,4]```  => 1  
```maximum [1,2,3,4]```  => 4  
```minimum ["a","b","c"]```  => "a"    
> *Note: these are DIFFERENT to `min` and `max` which compare two values of type Ord.*
##
### *`sum`* and *`product`* - returns the sum/product of a list of numbers - list must be of type **[Num]**
```sum [1,2,3,4]```  => 10  
```sum ["a","b","c"]```  => ❌ - not of type [Num]
##
### *`elem`* - takes an item and a list and returns True or False depending on whether the item is an element in the list
```elem 4 [1,2,3,4]```  => True  
> *Note: usually used as an infix operator, using backticks ( \` \` ), e.g.:*  

```67 `elem` [1,2,3,4]```  => False  
##
### *`sort`* - sorts the list
```sort [4,3,2,1]```  => [1,2,3,4]  
```sort "penis"```  => "einps"  
> *Note: `sort` requires an import of `Data.List` for some reason*
##
### *`zip`* - takes two lists and returns a list of pairs (2-tuples) corresponding to elements in the two lists
```zip [1,2,3,4] [4,3,2,1]```  =>  [(1,4),(2,3),(3,2),(4,1)]  
> *Note: it stops when one list runs out of elements, e.g.:*  

```zip [1,2,3,4] [6,7]```  => [(1,6),(2,7)]
