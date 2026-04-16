# 线性空间

给定非空集合 $V$ 和数域 $F$

若有映射 $\sigma: V \times V \rightarrow V$，$(v_1, v_2) \mapsto \sigma(v_1, v_2)$ 称为 $V$ 上的加法，并记 $\sigma(v_1, v_2) = v_1 + v_2$

及映射 $I: V \times F \rightarrow V$，$(v, k) \mapsto I(v, k)$ 称为 $V$ 和 $F$ 间的数乘法，并记 $I(v, k) = v \cdot k$

且这两运算满足线性计算法则，则称 $V$ 关于此 $+$ 和 $\cdot$ 是 $F$ 上的线性空间，简称 $V$ 是线性空间。线性空间中的元素称为向量

---

$$S_1 \times S_2 = \{(s_1, s_2) \mid s_1 \in S_1 \text{ 且 } s_2 \in S_2\} \quad \text{(卡氏积)}$$

$$F^n = F \times F \times F \times \cdots \times F$$

从集合到集合的映射：$S_1 \rightarrow S_2$  

从元素到元素的映射：$s_1 \mapsto s_2$

**域**：对加、减、乘、除四则运算封闭的集合

---

**线性运算条件**：

1.  $v_1 + v_2 = v_2 + v_1$  （交换律）
2.  $(v_1 + v_2) + v_3 = v_1 + (v_2 + v_3)$  （结合律）
3.  $\exists\ 0 \in V,\ \forall w \in V,\ 0 + w = w$  （有零元）
4.  $\forall v \in V,\ \exists w \in V,\ v + w = 0$  （有负元）
5.  $(v_1 + v_2) \cdot k = v_1 \cdot k + v_2 \cdot k$
6.  $v \cdot (k_1 + k_2) = v \cdot k_1 + v \cdot k_2$
7.  $v \cdot (k_1 k_2) = (v \cdot k_1) \cdot k_2$
8.  $v \cdot 1 = v$（数字放右边是为了和矩阵运算对齐）

---

**函数空间**:$F[I,R^n]={\{f:f是定义在I上，取值于R^n的函数\}}$

定义：$f + g \in F[I,R^n]$如下 

$f + g: t \mapsto f(t) + g(t)$；$f \cdot k \in F(I)$，则 $f \cdot k: t \mapsto f(t) \cdot k$

---

**线性相关**：抽象矩阵方程组有非零解 $A \mathbf{x} = 0, \mathbf{x} \neq 0$

记 $\beta_{1},\beta_{2},\ldots,\beta_{q}$ 可由 $\alpha_{1},\alpha_{2},\ldots,\alpha_{p}$ 线性表示为 $\{\beta_{1},\beta_{2}\} \leq{\text{lin}} \{\alpha_{1},\ldots,\alpha_{p}\}$ 且有传递性

若 $A \in F^{m \times n}, 1 \leq m < n$ 则 $Ax=0$, 必有非零解

若 $\{\alpha_{i}\},\{\beta_{i}\}$ 在 $V$ 内, $\alpha_{1},\cdots,\alpha_{p}$ 线性无关且 $\{\alpha_{i}\} \leq{\text{lin}} \{\beta_{i}\}$ 则 $p \leq q$

---

记 $\beta_{1},\beta_{2},\ldots,\beta_{s}$ 为 $\alpha_{1},\alpha_{2},\ldots,\alpha_{p}$ 的子集，且 $\{\beta_{i}\} \leq{\text{sub}} \{\alpha_{j}\}$ 

若: $\alpha_{1},\alpha_{2},\ldots,\alpha_{n}$ 线性无关且 $\forall \alpha \in V, \alpha$ 可由 $\{\alpha_{i}\}$ 线性表示，称 $V$ 是 $F$ 上的 $n$ 维线性空间, $\alpha_{1},\cdots,\alpha_{n}$ 为 $V$ 的一个基/坐标系，记 $\dim V=n$ 表示 $V$ 的维数

零维线性空间:仅含一个元素

---

$$
\begin{bmatrix}\text{抽} \\ \text{象} \\ \text{矩} \\ \text{阵}\end{bmatrix} = \begin{bmatrix} \text{基矩阵} \end{bmatrix} \begin{bmatrix} \text{坐} \\ \text{标} \\ \text{向} \\ \text{量} \end{bmatrix}
$$

抽象矩阵：线性变换 $ \mathcal{A} $ 在基 $ \{\alpha_{i}\} $ 下的矩阵表示称为 $ \mathcal{A} $ 的**抽象矩阵**。

基矩阵：由基向量 $ \alpha_{1}, \alpha_{2}, \ldots, \alpha_{n} $ 排成的矩阵 $ [\alpha_{1}, \alpha_{2}, \ldots, \alpha_{n}] $ 称为**基矩阵**。

坐标向量：向量 $ \beta $ 在基 $ \{\alpha_{i}\} $ 下的坐标 $ X $ 所成的列向量 $ [x_{1}, x_{2}, \ldots, x_{n}]^{T} $ 称为 $ \beta $ 的**坐标向量**。

三者的关系：
$$ \mathcal{A}(\alpha_{1}, \alpha_{2}, \ldots, \alpha_{n}) = (\alpha_{1}, \alpha_{2}, \ldots, \alpha_{n}) A $$
$$ \beta = (\alpha_{1}, \alpha_{2}, \ldots, \alpha_{n}) X $$
$$ \mathcal{A}(\beta) = (\alpha_{1}, \alpha_{2}, \ldots, \alpha_{n}) A X $$

坐标系实现了有限维抽象线性空间与标准线性空间的一一对应

无限维线性空间的例子：$R_n[x] = \{ f \mid f \in F(R, R) 且可写成实多项式\}$

**矩阵的像与核**：给定 $A \in F^{m \times n}$，定义 $\ker A = \{ \mathbf{x} \in F^n \mid A\mathbf{x} = 0 \}$，即 $A\mathbf{x} = 0$ 的解空间，称为 $A$ 的**核**

$\dim(\ker A) = n - \dim(\operatorname{im} A)$。

$\operatorname{im}  = \{ A\mathbf{x} \mid \mathbf{x} \in F^n \} $，称为 $A$ 的**像**。

称 $\operatorname{span}\{\alpha_1, \ldots, \alpha_t\} = \{ \alpha_1 k_1 + \alpha_2 k_2 + \cdots + \alpha_t k_t \mid k_i \in F, i=1,\ldots,t \}$ 为 $\alpha_1, \cdots, \alpha_t$ **张成的子空间** $W$

若由 $W$ 找到 $\alpha_1, \cdots, \alpha_n$，称 $\alpha_i$ 为 $W$ 的一个**生成组**。

$\operatorname{im} A = \operatorname{span}\{\alpha_1, \alpha_2, \ldots, \alpha_n\}$

---

设 $V$ 是 $F$ 上的线性空间，$W$ 为 $V$ 的一个子空间，则：
(1) $\dim W \leqslant \dim V$
(2) $W$ 的任一基可扩充为 $V$ 的一个基

将 $W$ 的基扩充到 $V$ 的基的方法：
设 $A \in F^{n \times m}$, $\operatorname{rank} A = m$。取 $B = I$ (非奇异) $\in F^{n \times n}$。将 $[A, B]$ 化为行阶梯形，则有几个位置有台阶，对应 $n-m$ 个向量

$V_1 \cap V_2$ 为子空间，但 $V_1 + V_2$ 不一定。

---

**直和**

设 $V$ 为 $F$ 上的线性空间，$V_1, V_2, W$ 为 $V$ 的子空间。若：
(1) $V_1 + V_2 = W$
(2) $V_1 \cap V_2 = \{0\}$
则称 $W$ 为 $V_1$ 与 $V_2$ 的**直和**，记作 $V_1 \oplus V_2 = W$。$V_1, V_2$ 称为 $W$ 的一个**直和分解**。

直和中的元素有唯一分解性：设 $W = V_1 \oplus V_2$，若 $w \in W$, $w = v_1 + v_2 = v_1' + v_2'$，其中 $v_1, v_1' \in V_1$ 及 $v_2, v_2' \in V_2$，则 $v_1 = v_1'$, $v_2 = v_2'$。

**补子空间**：设 $V$ 为 $F$ 的线性空间，$V_1, V_2$ 为 $V$ 的子空间。若 $V_1 \oplus V_2 = V$，则称 $V_1$ 和 $V_2$ **互补**

任一子空间必有补子空间

---

**线性映射**

设$V_1,V_2$为F上的两个线性空间,映射: $\mathcal{A}:V_1\rightarrow V_2$ 称为从$V_1$到$V_2$的线性映射若满足下面条件
$$
\begin{array}{l}
 \forall \alpha _ { 1 } , \alpha _ { 2 } \in V _ { 1 } , s . t . \mathcal{A}  ( \alpha _ { 1 } + \alpha _ { 2 } ) = \mathcal{A} ( \alpha _ { 1 } ) + \mathcal{A} ( \alpha _ { 2 } ) \\
 \mathcal{A} ( \alpha _ { 1 } \cdot k ) = \mathcal{A} ( \alpha ) \cdot k \\
\end{array}
$$
若$\mathcal{A}$可逆则称 $\mathcal{A}: V_1\rightarrow V_2$ 为从$V_1$到$V_2$的线性同构

---

设 $\dim V_1=n, \dim V_2=m$. 设 $\varepsilon_1,\cdots,\varepsilon_n$ 为$V_1$的一个基,记为入口基
$\eta_1, \eta_2\cdots\eta_m$ 为 $V_2$ 的一组基,即出口基
若 $\mathcal{A}(\varepsilon_j)=[\eta_1,\eta_2\cdots\eta_m]A$,称$A$为$\mathcal{A}$在相应出入口基下的矩阵表示

即 $A[\varepsilon_1, \varepsilon_2\ldots \varepsilon_n]=[\eta_1,\eta_2\ldots \eta_m] A$ 
$$
\left[ \begin{array}{l} \text{线性} \\ \text{映射} \end{array} \right] \left[ \begin{array}{l} \text{入口} \\ \text{矩阵} \end{array} \right] = \left[ \begin{array}{l} \text{出口} \\ \text{矩阵} \end{array} \right] \left[ \begin{array}{l} \text{表示} \\ \text{矩阵} \end{array} \right]
$$
表示矩阵的第j列是第j个入口基向量的像在出口基下的坐标

若 $\alpha\in V_1$ 在入口基的坐标为 $x$ 则在出口基下的坐标为 $Ax$

微分算子可表示为矩阵

---

$A, B\in F^{m\times n}$, 若 $\exists P\in F^{n\times n}, Q\in F^{m\times m}$, $\operatorname{rank} P=n,\operatorname{rank} Q=m$ 且 $QAP=B$ 则$A,$$B$等价(或 $AP=QB$ )

 $AP=QB$ 可视为$A$为映射$ P$为入口基, $Q$为出口基,则$B$为$ A$在这对基下的矩阵表示

设 $A\in F^{m\times n}$, $W\oplus ker A= F^n$ 记 $\mathcal{A}(W)=\{Ax\mid x\in W\}$ 则$\mathcal{A}(W)=\operatorname{im}A$, $\dim W=\operatorname{rank} A=\dim(\mathcal{A}(W))$

给定 $A\in F^{m\times n}$, $\operatorname{rank} A=r$, $W\oplus\operatorname{ker} A=F^n$, $U\oplus\operatorname{im} A= F^m$
$p_1, p_2,... p_r$为$W$的基, $q_{r+1},..., q_m$为 $U$ 的基, $\operatorname{ker} A$ 的基为 $p_{r+1},\cdots, p_n$
$p_1,\cdots p_n$ 为 $F^n$ 的基, $A(p_1)\cdots A(p_r), q_{r+1}\cdots q_m$ 为 $F^m$ 的基过渡表示矩阵为 $\begin{bmatrix} I_r & 0 \\ 0 & 0_{m-r,n-r} \end{bmatrix}$

$AP=PB$, $A$,$B$相似, $P$非奇异

若 $A W\subseteq W$, 则$W$为$A$的不变子空间
$\operatorname{ker} A, \operatorname{im} A, \{0\}, F^n$ 均是

$\begin{bmatrix} B_{11}& B_{12}\\ B_{21}& B_{22} \end{bmatrix}$
设 $P^{-1} A P=B, P=[P_1\quad P_2], B=$
$B_{21}=0$, 当且仅当 $\operatorname{im} P_1$ 为$A$的不变子空间
$B_{12}=0$,$\operatorname{im} P_2$同理

基于 $\operatorname{ker} A,\operatorname{im} A$ 可将 $A$ 三角化

$\dim(\operatorname{ker} A)=n-r$,  $\operatorname{rank} A=r$. 取$kerA$的基 $p_1\cdots p_{n-r}$
扩充为 $[P_1, P_2]$ 则 $A[P_1, P_2]=[P_1, P_2]\begin{bmatrix} 0 & B_{12} \\ 0 & B_{22} \end{bmatrix}$

同理对 $\operatorname{im} A$ 有 $A[Q_1,Q_2]=[Q_1,Q_2]\begin{bmatrix} B_{11}& B_{12}\\ 0& 0 \end{bmatrix}$

特征向量子空间即为一个不变空间
$AP=P\Lambda$: n阶矩阵可相似对角化等价于存在n个互补的一维空间

$\forall n, A\in C^{n\times n}, \exists\lambda\in C$, $p\in C^n$, $p\neq 0$, $A p=p\cdot\lambda$

Schur定理:复矩阵恒能相似上三角化

$F[\lambda]$表示系数在F中的多项式的全体
$F(\lambda)$表示数在F中的$\lambda$的有理分式的全体
$+,-,\times$ 在$F[\lambda]$中总能进行,但除不一定,称其为环
$+,-,\times,\div$ 在$F[\lambda]$中均可,称为域

若 $U(\lambda) V(\lambda)=I_n, U(\lambda),V(\lambda)\in F^{n\times n}[\lambda]$ 称$U(\lambda)$为单位模阵
$U(\lambda)\in F^{n\times n}[\lambda]$为单位模阵 $\Leftrightarrow \det(U(\lambda))\in F$ 为零次多项式(非零多项式)

# 书签（少了一页）

$A(\lambda)$ 可经有限个初等行列化成 $B(\lambda)$ 称其等价，记为 $A(\lambda) \sim B(\lambda)$

设 $A$ 中 $a_{11} \neq 0$, 且 $A$ 中至少有一个元素不能被 $a_{11}(\lambda)$ 整除

则 $A(\lambda) \sim B(\lambda)$, $b_{11} \neq 0$, $012(b_{11}a_1) < \partial(a_{11}a_1)$

$A(\lambda) \in F^{m \times n}$, $A(\lambda) \sim [d_1(\lambda) d_2(\lambda) \cdots d_r(\lambda)] 0 0$

其中：$d_i(\lambda)$ 内非0多项式，满足 $d_1(\lambda)$ 整除 $d_{i+1}(\lambda)$，记为 $d_i(\lambda) \mid d_{i+1}(\lambda)$

Smith型具有唯一性

$A(\lambda)$ 的 $k$ 阶行列式因子是指 $A(\lambda)$ 的所有 $k$ 阶子式有 $C_m^k$, $C_n^k$ 个

若 $A(\lambda) \sim B(\lambda)$ 则其各阶行列式因子分别相同

记 $A(\lambda)$ 的 $k$ 阶行列式因子为 $D_k(\lambda)$ 则 $D_k(\lambda) = d_1(\lambda) \cdots d_k(\lambda)$

称 $d_i(\lambda)$ 为 $A(\lambda)$ 的不变因子

（或 |）幺实或为正交矩阵

若 $A^H A = A A^H = I$ 则 $A$ 为酉矩阵，则 $\det A = 1$

$A^H$ 共轭转置，在实数域即为 $A^T$

幺矩阵的Smith标准型为 $I$，可写为有限个初等矩阵的乘积

$E \in F^{m \times n}$ 幺矩阵

若 $A^H M(\lambda)$ 则 $H V A(\lambda) \in F^{m \times m}$, $D V U \in F^{n \times n}$

$V V A(\lambda) = B V$

补页的结束

---



$A\in F^{n\times n}$, 称 $\lambda I_n-A$ 为 $A$ 的特征矩阵
$A$与$B$相似当且仅当 $\lambda I-A\sim\lambda I-B\in F[\lambda]$

零多项式矩阵次数规定为无穷
零多项式≠零次多项式

非零多项式矩阵 $A(\lambda)\in F^{m\times n}[\lambda]$, $A(\lambda)=A_0+A_1\lambda+...+A_q\lambda^q$ 若$A_q\neq 0$则称$A(\lambda)$次数为$q$,记为:$\deg(A(\lambda))$或$\partial(A(\lambda))$

设 $A(\lambda)\in F^{m\times m}[\lambda]$, $B(\lambda),C(\lambda)\in F^{m\times n}[\lambda]$ 且 $A(\lambda)B(\lambda)=C(\lambda)$ 若$A(\lambda)=A_0+A_1\lambda+...+A_q\lambda^q$ 若$A_q$非奇异,则 $\deg(C(\lambda))=q+\deg(B(\lambda))$

$A(\lambda)\in F^{m\times m}[\lambda]$, $\partial(A(\lambda))=q\geqslant 1, B(\lambda)\in F^{m\times n}[\lambda]$ 则存在唯一的 $Q(\lambda), R(\lambda)$, 使$B(\lambda)=A(\lambda)Q(\lambda)+R(\lambda)$
且 $R(\lambda)=0$ 或 $\deg(R(\lambda))<\deg(A(\lambda))$

> 一元多项式环的通用性质

$\operatorname{rank}(\lambda I-A)$ 为$n$则 $\deg(\det(\lambda I-A))=n$

#书签（待校对）

$\lambda I-A$的Smith型,可有k个不为常数的不变因子其smith型可化为k个对角形式,每个子块相应于一个非常数不变因子,并配以若干个常数不变因子,使子块的rank恰为该不变因子的次数
即smith型等价

设 $A\in F^{n\times n}$, $\lambda I-A$ 的初等因子是将 $\lambda I-A$ 的所有不变因子在$F[\lambda]$中作质因式分解时出现的质因式的方幂,若同一质因式的方幂若出现多次,则算作多个初等因子,所有初等因子的全体称为初等因子组

基于初等因子的规范型
设 $\lambda I-A$ 的初等因子组为 $(p_1(\lambda))^{r_1},(p_2(\lambda))^{r_2},\ldots,(p_q(\lambda))^{r_q}$
次数为 $m_k=r_k\cdot\deg(p_k(\lambda)), k=1,\cdots,q$ 则 $\lambda I-A$ 等价于
$\operatorname{diag}(p_1(\lambda)^{r_1},p_2(\lambda)^{r_2},\ldots,p_q(\lambda)^{r_q},1,\ldots,1)$
称为 $\lambda I-A$ 的第三等价规范型

对于$A,B\in F^{n\times n}$下列条件等价:
①A相似于B
② $\lambda I-A$ 与 $\lambda I-B$ 作为多项式矩阵等价
③A与B有相同的各阶行列式因子
④A与B有相同的各阶不变因子
⑤A与B有相同的初等因子组

任一矩阵与其转置相似