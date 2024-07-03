# Array


2918. [Minimum Equal Sum of Two Arrays After Replacing Zeros](https://leetcode.com/problems/minimum-equal-sum-of-two-arrays-after-replacing-zeros/description/)
 - 对每个数组返回 0 和 1 的个数， 从而可知其下限，以及是否固定（zeros ?= 0), 分情况讨论
 - {greedy}

1700. [Number of Students Unable to Eat Lunch](https://leetcode.com/problems/number-of-students-unable-to-eat-lunch/description/)
  - 当学生无法吃的时候，这时一定是所有剩下的学生都不喜欢最上面的三明治。
  - 统计学生中0, 1 的个数，遍历sandwich, 相应减少student中0, 1 的个数，直至其中一个为0。 O(n)
