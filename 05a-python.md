# Learn Python

Read Allen Downey's [Think Python](http://www.greenteapress.com/thinkpython/) for getting up to speed with Python 2.7 and computer science topics. It's completely available online, or you can buy a physical copy if you would like.

<a href="http://www.greenteapress.com/thinkpython/"><img src="img/think_python.png" style="width: 100px;" target="_blank"></a>

For quick and easy interactive practice with Python, many people enjoy [Codecademy's Python track](http://www.codecademy.com/en/tracks/python). There's also [Learn Python The Hard Way](http://learnpythonthehardway.org/book/) and [The Python Tutorial](https://docs.python.org/2/tutorial/).

---

### Q1. Lists &amp; Tuples

How are Python lists and tuples similar and different? Which will work as keys in dictionaries? Why?

>> REPLACE THIS TEXT WITH YOUR RESPONSE

>> (1) Similarities:  Lists and tuples are both sequence types.

>> (2) Differences:  Lists are dynamic and mutable. Tuples are fixed size in nature and mutable.  

>> (3) Tuples.  A dictionary key must be immutable.


### Q2. Lists &amp; Sets

How are Python lists and sets similar and different? Give examples of using both. How does performance compare between lists and sets for finding an element. Why?

>> REPLACE THIS TEXT WITH YOUR RESPONSE

>> (1) Similarities:  Lists and sets are both collections of elements.  

>> (2) Differences:  
(i) Sets cannot contain duplicates, are unordered and can only contain hashable items.
(ii) Sets = unordered collections of unique elements
(iii) Lists = ordered collections of elements
(iv) Sets allow you to do operations such as intersection, union, difference and symmetric difference
(v) Sets do not allow indexing and are implemented on hash tables
(vi) Lists are variable-length arrays.  List elements are accessed by indices.  

>> (3) Examples:  
list1 = [1, 2, 3, 4, 5 ];
list2 = ["a", "b", "c", "d", "e"]
set1 = {1, 2, 3, 4, 5}
set2 = {1.0, "Hello", (1, 2, 3)}

>> (4) Performance for Finding Element:
(i) Sets are faster for finding if an object is present in a set.  This is because sets use a bash function to map to a bucket. Since Python implementations resize the hash table, the speed can be constant regardless of the size of the set.  Lists, in comparison, require Python to compare every single member for equality.  
(ii) Sets are slower than lists when iterating over contents.      


### Q3. Lambda Function

Describe Python's `lambda`. What is it, and what is it used for? Give at least one example, including an example of using a `lambda` in the `key` argument to `sorted`.

>> REPLACE THIS TEXT WITH YOUR RESPONSE

>> (1) Python supports the creation of anonymous functions using a construct called "lambda" (i.e. functions not bound to a name).

>> (2) FUNCTION:  
def f(x): 
  return x^2
>> LAMBDA
g = lambda x: x^2

>> (3) The sorted() function sorts uppercase words before words that are lowercase.
>> Using the 'key' keyword, you can change each entry so it will be sorted differently.
>> Note: lambdas are limited to one expression only, the result of which is the return value.

>> sorted(['Some', 'words', 'sort', 'differently'], key=lambda word: word.lower())

>> '#' ['differently', 'Some', 'sort', 'words']

---

### Q4. List Comprehension, Map &amp; Filter

Explain list comprehensions. Give examples and show equivalents with `map` and `filter`. How do their capabilities compare? Also demonstrate set comprehensions and dictionary comprehensions.

>> REPLACE THIS TEXT WITH YOUR RESPONSE

#1.  List comprehensions are a tool for transforming one list into another list.  During this transformation, elements can be conditionally included in the new list and each element can be transformed as needed.
---

>> map() is a function with two arguments:

>> r = map(func, seq)

>> The first argument func is the name of a function and the second a sequence (e.g. a list) seq. 

>> map() applies the function func to all the elements of the sequence seq. 

>> It returns a new list with the elements changed by func.

>>    def fahrenheit(T):

>>    return ((float(9)/5)*T + 32)

>>    def celsius(T):

>>    return (float(5)/9)*(T-32)

>>    temp = (36.5, 37, 37.5,39)

>>    F = map(fahrenheit, temp)

>>    C = map(celsius, F)

>> map() can be applied to more than one list. The lists have to have the same length. map() will apply its lambda function to the elements of the argument lists, i.e. it first applies to the elements with the 0th index, then to the elements with the 1st index until the n-th index is reached:

>>> a = [1,2,3,4]
>>> b = [17,12,11,10]
>>> c = [-1,-4,5,9]
>>> map(lambda x,y:x+y, a,b)
[18, 14, 14, 14]
>>> map(lambda x,y,z:x+y+z, a,b,c)
[17, 10, 19, 23]
>>> map(lambda x,y,z:x+y-z, a,b,c)
[19, 18, 9, 5]

>> The function filter(function, list) offers an elegant way to filter out all the elements of a list, for which the function function returns True. 
The function filter(f,l) needs a function f as its first argument. f returns a Boolean value, i.e. either True or False. This function will be applied to every element of the list l. Only if f returns True will the element of the list be included in the result list.

>>> fib = [0,1,1,2,3,5,8,13,21,34,55]
>>> result = filter(lambda x: x % 2, fib)
>>> print result
[1, 1, 3, 5, 13, 21, 55]
>>> result = filter(lambda x: x % 2 == 0, fib)
>>> print result
[0, 2, 8, 34]


>> A set comprehension is similar to a list comprehension, but returns a set and not a list. Syntactically, curly brackets are used instead of square brackets to create a set.

>>> from math import sqrt
>>> n = 100
>>> sqrt_n = int(sqrt(n))
>>> no_primes = {j for i in range(2,sqrt_n) for j in range(i*2, n, i)}
>>> no_primes
{4, 6, 8, 9, 10, 12, 14, 15, 16, 18, 20, 21, 22, 24, 25, 26, 27, 28, 30, 32, 33, 34, 35, 36, 38, 39, 40, 42, 44, 45, 46, 48, 49, 50, 51, 52, 54, 55, 56, 57, 58, 60, 62, 63, 64, 65, 66, 68, 69, 70, 72, 74, 75, 76, 77, 78, 80, 81, 82, 84, 85, 86, 87, 88, 90, 91, 92, 93, 94, 95, 96, 98, 99}
>>> primes = {i for i in range(n) if i not in no_primes}
>>> print(primes)
{0, 1, 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97}

>> You can use dict comprehensions in ways very similar to list comprehensions, except that they produce Python dictionary objects instead of list objects.

>> In addition, dict comprehensions can be used to create dictionaries from arbitrary key and value expressions:

>>> {x: x**2 for x in (2, 4, 6)}
{2: 4, 4: 16, 6: 36}


### Complete the following problems by editing the files below:

### Q5. Datetime
Use Python to compute days between start and stop date.   
a.  

```
date_start = '01-02-2013'    
date_stop = '07-28-2015'
```

>> REPLACE THIS TEXT WITH YOUR RESPONSE (answer will be in number of days)

b.  
```
date_start = '12312013'  
date_stop = '05282015'  
```

>> REPLACE THIS TEXT WITH YOUR RESPONSE (answer will be in number of days)

c.  
```
date_start = '15-Jan-1994'      
date_stop = '14-Jul-2015'  
```

>> REPLACE THIS TEXT WITH YOUR RESPONSE  (answer will be in number of days)

Place code in this file: [q5_datetime.py](python/q5_datetime.py)

---

### Q6. Strings
Edit the 7 functions in [q6_strings.py](python/q6_strings.py)

---

### Q7. Lists
Edit the 5 functions in [q7_lists.py](python/q7_lists.py)

---

### Q8. Parsing
Write a script as indicated (using the football data) in [q8_parsing.py](python/q8_parsing.py)





