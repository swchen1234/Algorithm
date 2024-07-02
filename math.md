# Math


43. [Multiply String](https://leetcode.com/problems/multiply-strings/description/)
  * 两个字符串表示的整数相乘， 返回字符串
    - 将两字符串逆序， 从i = 0 ... n : for j = 0 ... m
    - 对于每个s1[i]， 分别乘以s2[j]， 得到 val = s1[i] * s2[j]后置于res[i + j]的位置上，若有溢位，则carry至res[i + j + 1], 直至val == 0
    - 得倒解惑后，再将结果逆序
    
