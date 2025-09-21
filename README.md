# Integer-to-Roman-Numbers
Java Program to Convert Integer (Numerical Values) To Roman Number

# Intuition
The problem asks was to find two indices such that their numbers add up to a given target.The brute force way would be to check every possible pair, but that would take O(n²) time.
A better way is to use a hash map to remember numbers we’ve seen so far and their indices, so we can check complements in constant time.

# Approach
Initialize a HashMap to store each number and its index as we iterate through the array.
For each element nums[i], compute its complement: target - nums[i].
If the complement is already in the map, return the indices: [map.get(complement), i].
Otherwise, store the current number and index in the map.
If no solution is found after iterating, return an empty array.
# Complexity
- Time complexity:
Each element is visited once, and map operations are O(1) on average.
So overall complexity is O(n).

- Space complexity:
The hash map stores at most n elements (in the worst case).
So space complexity is O(n).
