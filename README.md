# leetcode
#Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
int* twoSum(int* nums, int numsSize, int target, int* returnSize) {
    for (int i = 0; i < numsSize; i++) {
        for (int j = i + 1; j < numsSize; j++) {
            if (nums[j] == target - nums[i]) {
                int* result = malloc(sizeof(int) * 2);
                result[0] = i;
                result[1] = j;
                *returnSize = 2;
                return result;
            }
        }
    }
    // Return an empty array if no solution is found
    *returnSize = 0;
    return malloc(sizeof(int) * 0);
}
