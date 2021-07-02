# Move Zeroes

Given an integer array nums, move all 0's to the end of it while maintaining the relative order of the non-zero elements.

Note that you must do this in-place without making a copy of the array.

 

_Example 1:_

Input: `nums = [0,1,0,3,12]`

Output: `[1,3,12,0,0]`

_Example 2:_

Input: `nums = [0]`

Output: `[0]`
 

_Constraints:_

`1 <= nums.length <= 10^4`

`-2^31 <= nums[i] <= 2^31 - 1`


# Solution in JavaScript
```
var moveZeroes = function(nums) {
    let index = 0;
        for(let i=0; i<nums.length; i++){
            if(nums[i] != 0){
                nums[index++] = nums[i];
            }
        }
        
        for(let i = index; i<nums.length; i++){
            nums[i] = 0;
        }
};
```
