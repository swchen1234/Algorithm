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

166. [Fraction to Recurring Decimal](https://leetcode.com/problems/fraction-to-recurring-decimal/description/)
  * 给定分子，分母，将两者相除结果用字符串返回， 如  1 / 3 = 0.(3)
    - 长除法, 分别处理小数点前与小数点之后，每次 res += '0', numerator *= 10, numerator %= denominator, 直至numerator == 0,
    - 哈希 numerator及所对应的index， 若numerator第二次出现，则找到循环

592. [Fraction Addition and Subtraction](https://leetcode.com/problems/fraction-addition-and-subtraction/description/)
   * 返回分数算式的结果，如 1/2+1/3-1/4
     - 逐个处理每个分数，返回 sign * numerator, denominator
     - 从num = 1, den =1 开始，从左到右逐个添加分数(num1, den1)， 更新分母为den *= den1, 分子为 num = num * den1 + num1 * den, 更新后的分子分母同时除以 gcd(num, den)

1344. [Angle Between Hands of a Clock](https://leetcode.com/problems/angle-between-hands-of-a-clock/description/)
   * 返回时针分针之间的较小夹角


     

     
