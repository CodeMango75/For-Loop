
# Loops 

A loop is an instruction that repeats multiple times as long as some condition is met.
Suppose we are required to write any code or instruction mutliple time for 3000 times, we cannot individually write it, in that case we use Loops.
There are 2 ways for looping:

* For Loop
* While Loop 
* Controls (Optional)
   * break : breaks the loop once a condition is met
   * continue : skips the iteration in the loop
   * pass : tells python interpreter to not give error and we will come back and code again. 
* **Three things are important in Loops**
   * Counter
   * Logic
   * Increment/Decrement

### Zip Function
The `zip` function takes two or more iterables as input and returns an iterator that generates tuples containing elements from the input iterables, element-wise. The resulting iterator stops when the shortest input iterable is exhausted. This is often used to iterate over multiple lists in parallel.

```
list1 = [1, 2, 3]
list2 = ['a', 'b', 'c']

zipped = zip(list1, list2)

for item in zipped:
    print(item)
# Output: (1, 'a')
#         (2, 'b')
#         (3, 'c')

```
### Unzip Function
While there isn't a direct "unzip" function in Python, you can achieve the same result using the `zip` function in combination with the unpacking operator `*`. This allows you to separate the elements of zipped tuples back into separate lists.

Example:

```
zipped = [(1, 'a'), (2, 'b'), (3, 'c')]

list1, list2 = zip(*zipped)

print(list1)  # Output: (1, 2, 3)
print(list2)  # Output: ('a', 'b', 'c')

```
If you don't use the `*` operator when "unzipping" with the zip function, you would essentially end up with a single tuple that contains all the elements from the zipped tuples. Here's how it works:
```
zipped = [(1, 'a'), (2, 'b'), (3, 'c')]

result = zip(zipped)

for item in result:
    print(item)
# Output: ((1, 'a'),)
#         ((2, 'b'),)
#         ((3, 'c'),)
```
As you can see, each iteration yields a tuple containing a single zipped tuple. This happens because without the `*` operator, the `zip` function treats the entire list of tuples as a single argument, essentially zipping together the list itself, which results in a single tuple in the output.

To properly "unzip" the zipped tuples and separate the elements, you need to use the `*` operator, as shown in the previous examples. This operator unpacks the zipped tuples, allowing the `zip` function to receive individual elements as separate arguments.
### Enumurate Function
The `enumerate` function is used to iterate over an iterable while keeping track of the index of the current element. It returns pairs of (index, element) as tuples.

```
fruits = ['apple', 'banana', 'cherry']

for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")
# Output: Index 0: apple
#         Index 1: banana
#         Index 2: cherry

```
