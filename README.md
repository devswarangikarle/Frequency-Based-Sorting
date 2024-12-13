# Frequency-Based-Sorting

Mia is organizing a list of items represented by an array of numbers. She wants to sort the list by arranging items that appear most frequently first, in ascending order of frequency. If two items appear the same number of times, she places the larger item first. Can you help Mia organize her list according to these rules?

from collections import Counter

def frequency_sort(nums):
    # Count frequencies
    freq = Counter(nums)
    
    # Sort based on frequency (ascending) and value (descending)
    sorted_nums = sorted(nums, key=lambda x: (freq[x], -x))
    
    return sorted_nums

# Input
N = int(input())
nums = list(map(int, input().split()))

# Get the sorted result
result = frequency_sort(nums)

# Print the result
print(" ".join(map(str, result)))
