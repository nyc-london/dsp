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

>> List comprehensions are a tool for transforming one list into another list.  During this transformation, elements can be conditionally included in the new list and each element can be transformed as needed.
---

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





