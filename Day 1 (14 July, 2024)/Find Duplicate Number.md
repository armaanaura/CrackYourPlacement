## Find Duplicate Numbers 
This problem is solved with Slow and Fast Approach.
- Time Complexity: O(N)
- Space Complexity: O(1)
```java
//solution using slow and fast approach
class Solution {
    public int findDuplicate(int[] nums) {
        int hare=0;
        int turtle=0;
        do{
            hare=nums[nums[hare]];
            turtle=nums[turtle];
        }while(turtle!=hare);
        turtle=0;
        while(hare!=turtle){
            hare=nums[hare];
            turtle=nums[turtle];
        }
        return hare;
    }
}
```
