# Kadane-s-Algorithm

📝 Problem
Find the maximum sum of a contiguous subarray.

🚀 Approach
- Use Kadane’s Algorithm
- Track current sum and max sum
- Reset when sum becomes negative

⏱ Complexity
Time: O(n)
Space: O(1)

code:
class Solution {
    public int maxSubArray(int[] arr) {

        int currentSum = 0;
        int maxSum = Integer.MIN_VALUE;

        for (int i = 0; i < arr.length; i++) {

            currentSum += arr[i];

            maxSum = Math.max(maxSum, currentSum);

            if (currentSum < 0) {
                currentSum = 0;
            }
        }

        return maxSum;
    }
}

🧪 Dry Run (Step-by-Step)
Input:
[2, 3, -8, 7, -1, 2, 3]
Step-by-step
i	Element	currentSum	maxSum
0	2	2	2
1	3	5	5
2	-8	-3 → reset to 0	5
3	7	7	7
4	-1	6	7
5	2	8	8
6	3	11	11 ✅
✅ Final Answer
11

👉 Subarray:

[7, -1, 2, 3]

I used Kadane’s Algorithm to track the maximum subarray sum by resetting the running sum whenever it becomes negative

If you found this helpful, give it a ⭐ and follow for more such solutions 🚀
