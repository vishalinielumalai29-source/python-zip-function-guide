Overview 
Most developers use python's Zip() for basic pairing.
This respsitory explores advanced and lesser-known use cases off zip() that demonstrates deeper pythonic thinking and problem- solving ability 
----
1. Matrix transpose using Zip()
''' python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
transpose = list(zip(*matrix))
print(transpose)
this converts rows into column efficiently

# 2. parallel sorting using zip()
names = ["A", "B", "C"]
marks = [70, 90, 80]
sorted_data = sorted(zip(marks, names), reverse=True)
print(sorted_data)
this sort one list based on another

# 3. pairwise comparison
nums = [10, 20, 15, 25]
comparisons = [(a, b, b - a) for a, b in zip(nums, nums[1:])]
print(comparisons)
this used in time-series & trend analysis

# 4. unzipping trick 
pairs = [(1, 'a'), (2, 'b'), (3, 'c')]
numbers, letters = zip(*pairs)
print(numbers)
print(letters)
this splits structures data 

# 5. Dictionary inversion 
data = {"a": 1, "b": 2}

inverted = dict(zip(data.values(), data.keys()))
print(inverted)
this reverse key-value mapping 

# 6. Combining More Than Two Iterables
a = [1, 2]
b = [3, 4]
c = [5, 6]

result = list(zip(a, b, c))
print(result)
this Multi-dimensional data grouping

# 7. Handling Unequal Lengths (Advanced)
from itertools import zip_longest

a = [1, 2, 3]
b = [4]

result = list(zip_longest(a, b, fillvalue=0))
print(result)

# 8. Sliding Window Technique
arr = [1, 2, 3, 4, 5]

windows = list(zip(arr, arr[1:], arr[2:]))
print(windows)


