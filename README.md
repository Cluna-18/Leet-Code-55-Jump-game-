# Leet-Code-55-Jump-game
For my final project for CMSC 510, I will tackling the leet code problem titled as "Jump Game". 

## Description
You are given an integer array nums. You are initially positioned at the array's first index, and each element in the array represents your maximum jump length at that position. 

Return true if you can reach the last index, or false otherwise.

Example 1:
Input: nums = [2,3,1,1,4]
Output: true
Explanation: Jump 1 step from index 0 to 1, then 3 steps to the last index.


Example 2:
Input: nums = [3,2,1,0,4]
Output: false
Explanation: You will always arrive at index 3 no matter what. Its maximum jump length is 0, which makes it impossible to reach the last index.

The problem asks whether it's possible to reach the last index of an integer array, where each element in the array represents the maximum jump length you can make from that position. A real world example that this problem could represent would be if we were planning the placement of charging infrastructure for electric vehicles. Each index represents a charging station along a highway, and the value indicates how far an electric vehicle can travel after charging at that station. The goal is to determine whether the EV can reach the final charging station (destination) with the current placement of charging points.

## My Approach
I had taken a dynamic programming approach to this problem. I created a DP table where dp[i] indicates whether index i is reachable. We start from the first index, then the algorithm iteratively marks all indices reachable from i. If the last index is marked reachable, the function returns true. One of the greatest challenges I faced for this problem was correctly setting up and understanding how the DP table would work. It was challenging trying to visual the table I needed in order to get it to work for our dynamic programming approach. Another challenge I ran into was understanding when to quit the for loop early. I wanted to make sure that once we determined the last index of the vector is reachable, we should be able to quit and return true. If this is not the case, we would continue looping through the vector till we reach the final index. This allows us to save computation time and improve efficiency as it skips unnecessary steps after determining if the final index can be reached. 

## Sources
One source I used was scalar.com. I had used this site as a reference to dynamic programming and it's idea of a 1 dimensional table for memoization. https://www.scaler.com/topics/data-structures/1-d-dynamic-programming-problem/


