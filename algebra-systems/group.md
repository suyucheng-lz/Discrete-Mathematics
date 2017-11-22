## 群

设 G 是定义了二元运算（用并置表示）的非空集合，如果G满足下列的公理：

  - **结合律** 对任何元素 a，b，c \in G，有 (ab)c = a(bc)
  - **单位元** 存在元素 e \in G，使得对于G中任一个元素a，有 ae = ea = a
  - **逆元**  对每个元素 a \in G，存在一个元素 a^-1 \in G（a的逆元），使得 aa^-1 = a^-1 a = e

则称 G 为群。

若群 G 满足交换律，即对任意的 a，b \in G，有 ab = ba，则称 G 为阿贝尔群（或 交换群）。

当二元运算如上并置定义时，称 G 为乘法群；当 G 是阿贝尔群时，运算记为 +，称 G 为加法群。
此时单位元记为0，称为零元素，逆元记为-a，称为负元素。

群 G 中元素的个数记为 |G|，称为 G 的阶。若其阶是有限的，称G为有限群。

如果 A 和 B 是 G 的子集，则记：
$$
AB = {ab: a\in A, b\in B} 或 A + B = {a + b: a\in A, b\in B}
$$

### 对称群 S_n

从集合 {1, 2, 3, ..., n} 到自身的 1-1映射 称为置换，记为：
$$
\sigma = \begin{pmatrix}
1   &  2  & 3   & \cdots & n \\
j_1 & j_2 & j_3 & \cdots & j_n
\end{pmatrix}
$$
其中，j_i = \sigma(i)。

所有置换的集合记为 S_n，共有 n! 个元素（P(n, n) = \frac{n!}{(n - n)!} = n!）。
S_n 中置换的 复合** 和 **逆** 均在 S_n 中，并且单位函数 \epsilon 也在 S_n 中，这样 S_n 在函数复合运算下构成群，我们称之为 **n阶对称群**。

## MAP(A), PERM(A) 和 AUT(A)

设 A 是一非空集合，所有的函数（映射）f: A \to 组成的集合 MAP(A) 在函数的复合下是半群，但它是不是群，因为有些函数没有逆元。
但是，所有的 A 到自身的 1-1 映射（称为“置换”）组成的 MAP(A) 的子半群 PERM(A) 在函数的复合下构成群。

设 A 含有某些几何和代数结构，那么所有 A 到自身的同构映射（称为 A 的自同态）所组成的集合 **AUT(A)** 在函数的复合下也构成群。
