### 2098.Subsequence-of-Size-K-With-the-Largest-Even-Sum

本题的解法有很多。但想写得简洁不容易。比较优秀的切入角度是将nums分成奇数组和偶数组，各自从大到小排序。显然，如果奇数取0个，那么偶数就取前k个；如果奇数取前1个，那么偶数就取前k-1个...于是只要两个指针(i,j)，i在奇数组从前往后移动，j在偶数组从后往前移动，用k次找出最大的presum1+presum2.

需要注意的有两点。首先，不是每一种(i,j)组合得到的presum1+presum2都是偶数，我们肯定会舍弃掉不合条件的组合。其次，偶数组不见得有k个元素，指针移动的过程中需要时刻检查i+j是否等于k。