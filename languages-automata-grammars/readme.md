# 形式语言、形式语法和自动机

## 字母表，字符串，自由半群

字母表：非空符号集合（通常记作A）
字符串：字母表元素中的有限序列（通常记作 w, u, v）
空串：没有字符的序列（通常使用希腊字母 lambda 或 epsilon表示）

A 中所有字符串的集合记为 A*（读作 A 星）

字符串长度：记作 |u| 或 l(u)，表示字符串u中字符的个数。l(\lambda) = 0.

### 连接

对于字母表A中的两个字符串 u 和 v，连接 u 和 v 记作 uv，表示字符串 v 紧接着写在字符串 u 之后。

定理13.1 字母表A中的字符串的连接运算满足结合律，空串是运算中的单位元。
（一般地，运算的交换律不成立）

### 子串，前缀

子串：对于任意字符串 u = a1 a2 ... an,任何序列 w = a_ {j} a_ {j+1} ... a_k 称作u的子串。
前缀：子串 w = a1 a2 ... ak，以u的字符开头，称作 u 的前缀。

### 自由半群，自由幺半群

自由半群：用F表示字母表A中所有非空字符串的集合，并且含有连接运算。由于连接运算满足结合律二，因此F是一个**半群**。
称作A的自由半群 或 由A 生成的自由半群。
当需要标明集合A时，A的自由半群记作 F_A。

自由幺半群：设 M = A* 是包括空串lambda在内的A中所有字符串的集合。由于lambda是连接运算的单位元，M是含幺半群，我们称M为A上的自由幺半群。

$$
F_A = A^* - \{\lambda\}
$$

## 形式语言

形式语言：字母表A上的形式语言 L 是 A 中的字符串的集合。因此，形式语言 L 是A* 的一个子集。

### 形式语言的运算

假设 L 和 M 是 A 的形式语言，那么 L 和 M 的连接，记为 LM，是 A 上的一种形式语言，定义如下：

$$
LM = {uv: u \in L, v \in M}
$$

形式语言的幂：形式语言 L 的幂定义如下：

$$
L^0 = \{\lambda\}, L^1 = L, L^2 = LL, L^{m + 1} = L^mL(m > 1)
$$

一元运算 L* （读作 “L星”），称作 L 的 Kleene 闭包，
$$
L^* = L^0 \cup L^1 \cup L^2 \cup \cdots = \cup_{k = 0}^{\infty} L^k
$$

定理13.2 L* 的定义与 A* 一致。

此外，记号 L+ 表示：
$$
L^+ = L^* - L^0
$$