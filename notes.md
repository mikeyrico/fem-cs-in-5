## Time Complexity -- Big O
* idea is to model how much time any function will take given _n_ inputs
* only need to analyze by orders of magnitude, so just interested in the largest
term
* also assume worst case scenario when analyzing for O(n)
* [big O cheatsheet](http://bigocheatsheet.com)
google.com

#### to analyze
* look for loops, each loop is n, so a nested loop would be _n²_
* if no loops, just execute constant set of commands, it is called _constant time_
* also can have _O(log n)_ with a divide and conquer algorithm, meaning as n grows, the
increase in time diminishes

O notation | desc
---        | ---
`O(n²)`    | quadratic - single nested loops
`O(n)`     | linear
`O(1)`     | constant
`O(log n)` | log time

>  A loop inside of a loop inside of a loop would likewise be O(n³)

## Recursion
* when a function calls itself
* cons
  * potentially large call stack, so sometimes worth using a more efficient iterative approach
* pros
  * can be elegant way to express the solution
  * able to maintain its own state at each level of recursion


## Sorting

* bubble sort
  * loop through, bubbling the largest values to the top
  * swap values as you loop through
  * stop looping when there are no more changes on a run through
* insertion sort
  * loop through, inserting at the correct location as comparing
* merge sort
  * typically broken down into 2 functions (`stitch` and `mergeSort`)
  * `mergeSort` basic approach:
    * split into 2 arrays
    * recursive call to `mergeSort` for 2 arrays wrapped by a `stitch` call
    * `stitch` should order the 2 arrays, iterating at same time to produce sorted array
* quick sort
  * pick a pivot, split into 2 arrays
  * recursive call to quick sort on 2 sub arrays
  * finally, concat the arrays plus the pivot

## Data Structures

### Set
* no guarantee of order
* no duplicates
* examples - a set of user names, ids
* interface
  * `add`
  * `remove`
  * `contains`
  * `toList`

### Maps
* similar to js objects
  * they do not come with the extra methods and functions and all that jazz
* just key value pairs
* the keys are a `set`

### Stacks and Queues
* a queue is a line (at the coffee shop) - FIFO
  * variation - priority queue - as in networking
  * example would be streaming video vs dropbox sync
  * dropbox sync can happen whenever, but missing packets of video will make users 😔
* a stack - LIFO
  * stacks are good for modeling programming languages

### ArrayList
* borrowed from java, since memory management isn't really a think in JS
* takes up a specific amount of space in memory
* memory performant, but deletions and insertions will be expensive since need to shift
* interface
  * `push`
  * `pop`
  * `get`
  * `delete`
  * `_collapseTo` - suggested private utility method to help with shifting

