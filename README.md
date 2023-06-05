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

Problem 2

Average Salary excluding minimum and maximum.

You are given an array of unique integers salary where salary[i] is the salary of the ith employee.

Return the average salary of employees excluding the minimum and maximum salary. Answers within 10-5 of the actual answer will be accepted.

Example 1:

Input: salary = [4000,3000,1000,2000]
Output: 2500.00000
Explanation: Minimum salary and maximum salary are 1000 and 4000 respectively.
Average salary excluding minimum and maximum salary is (2000+3000) / 2 = 2500
Example 2:

Input: salary = [1000,2000,3000]
Output: 2000.00000
Explanation: Minimum salary and maximum salary are 1000 and 3000 respectively.
Average salary excluding minimum and maximum salary is (2000) / 1 = 2000

Solution:
var average = function(salary) {
    salary.sort((a, b) => a - b)
    salary.shift()
    salary.pop()
    console.log(salary)
    const average = salary.reduce((acc, curr) => acc + curr) / salary.length

    return average
};

Explanation:
---
