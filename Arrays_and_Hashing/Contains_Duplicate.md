#### Question:
- Leetcode: https://leetcode.com/problems/contains-duplicate/description/
- Neetcode: https://neetcode.io/problems/duplicate-integer

#### Solution: 
Neetcode Video explanation: https://www.youtube.com/watch?v=3OamzN90kPg

1. Using HashSet with time complexity O(n) and space complexity O(n)

    Code:

    ```javascript
    /**
     * @param {number[]} nums
     * @return {boolean}
     */
    const containsDuplicate = function(nums) {
        let hashSet = new Set();
        for(let num of nums){
            if(hashSet.has(num)){
                return true
            }
            hashSet.add(num);
        }
        return false;
    };
    ```
2. Creating Set from the given array which will remove duplicates

    Code:
    
    ```javascript
    // Time complexity: O(n)
    // Space complexity: O(n)
    var containsDuplicate = function(nums) {
        const s = new Set(nums); 
        return s.size !== nums.length
    };
    ```