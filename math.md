# Math


43. [Multiply String](https://leetcode.com/problems/multiply-strings/description/)
  * 两个字符串表示的整数相乘， 返回字符串
    - 将两字符串逆序， 从i = 0 ... n : for j = 0 ... m
    - 对于每个s1[i]， 分别乘以s2[j]， 得到 val = s1[i] * s2[j]后置于res[i + j]的位置上，若有溢位，则carry至res[i + j + 1], 直至val == 0
    - 得倒解惑后，再将结果逆序
    
1492. [The kth Factor of n](https://leetcode.com/problems/the-kth-factor-of-n/description/)
  * 找到n的第k个因子
    - 遍历1...sqrt(n), 若 n % i == 0, k -= 1, 若 k == 0， 则返回当前因子
    - 遍历sqrt(n)。。。1, 若 n % (n / i) == 0, k -= 1, 若 k == 0， 则返回当前因子
    - 特殊情况：sqrt(n) ** 2 == n, 为了避免重复，第二次遍历时跳过sqrt(n)。
