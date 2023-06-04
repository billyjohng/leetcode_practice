# leetcode_practice
Collections of solved leet code problems and an explanation of the solution

Problem 1

Contains Duplicates

Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.
Example 1:

Input: nums = [1,2,3,1]
Output: true
Example 2:

Input: nums = [1,2,3,4]
Output: false
Example 3:

Input: nums = [1,1,1,3,3,4,3,2,4,2]
Output: true

Solution: 
var containsDuplicate = function(nums) {
  let o = {}
  for (i = 0; i < nums.length; i++) {
    if (o[nums[i]]) {
      o[nums[i]]++
    } else {
      o[nums[i]] = 1
    }
  }

  for (const [key, value] of Object.entries(o)) {
    console.log(key, value)
    if (value > 1) {
      return true
    }
  }

  return false
};

Explanation:
---
