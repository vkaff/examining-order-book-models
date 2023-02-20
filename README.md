# examining-order-book-models
Implement and test various algorithmic approaches for an Order Book

## Collect data
https://emi.nasdaq.com/ITCH/Nasdaq%20ITCH/
https://lobsterdata.com/info/HowToJoin.php

## What is implemented 

### Structures to use
* Use SortedContainers. This is implemented using a binary search tree (some kind of red-black tree) that uses "links" between nodes. Additionally, utilizes a hash-map for fast access of price_levels. Note: mentioned in stackoverflow that keeping a separate dict might be faster because python’s dict is currently implemented in C whereas the above module is implemented in pure python (needs check not sure if that is true) 
* Keep a sorted array (vector) and insert elements into it. For this, use bisect module. The complexity of this operation is O(log(N)) to find the insertion position, and O(N) to rotate the elements of the array.

### Programming languages
* Python
* Goland
* C/C++ the actual structures, which are binding to python calls

## Streaming Order Book
Stream data in the console to visualize depth and quantity of Order Book’s price levels. Consider the following implementation for ideas:
https://github.com/quantmind/kollector

## Performance indicators
Execute tests to compare run times for the various implementations and make some plots. We can experiment with:
Adding various number of orders
Executing various number of orders
Canceling various number of orders
