
## Minimum subarray

```
function minSubarraySum(arr) {
  if (arr.length === 0) {
    return 0;
  }

  let minEndingHere = arr[0];
  let minSoFar = arr[0];

  for (let i = 1; i < arr.length; i++) {
    minEndingHere = Math.min(arr[i], minEndingHere + arr[i]);
    minSoFar = Math.min(minSoFar, minEndingHere);
  }

  return minSoFar;
}

// Example usage:
const arr = [3, -4, 2, -3, -1, 7, -5];
console.log(minSubarraySum(arr));  // Output: -6 (subarray [-4, 2, -3, -1])
```

### Explanation

- **Initialization**:
    
    - `minEndingHere` is initialized to the first element of the array. It keeps track of the minimum sum of the subarray ending at the current position.
    - `minSoFar` is also initialized to the first element of the array. It keeps track of the minimum sum found so far.
- **Iteration**:
    
    - For each element in the array starting from the second element:
        - `minEndingHere` is updated to be the minimum of the current element (`arr[i]`) and the sum of `minEndingHere` and the current element. This ensures that `minEndingHere` always holds the minimum subarray sum ending at the current position.
        - `minSoFar` is updated to be the minimum of `minSoFar` and `minEndingHere`. This ensures that `minSoFar` always holds the minimum subarray sum found so far.
- **Return**:
    
    - After iterating through the array, `minSoFar` contains the minimum subarray sum.

This algorithm runs in O(n) time complexity, making it efficient for large arrays.