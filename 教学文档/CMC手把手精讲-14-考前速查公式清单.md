# CMC 手把手精讲
## ——《14 考前速查单》：上考场前必须背下来的公式与套路

> 🐱 喵～这是整套资料的最后一篇，也是唯一一篇**不讲原理/推导、只列要背**的篇目。它的用法只有一个：**考前最后 1–2 天，反复扫、反复默写**，把该在脑子里的东西固定住。
>
> **覆盖范围**：初赛高数 8 大板块全覆盖（极限、一元微分、一元积分、ODE、解析几何、多元微分、多元积分（重积分 + 曲线曲面）、级数）。每条 = 公式 + 一行"什么时候用 / 最容易错在哪"；需要动作记忆的套路给 2–3 步。
>
> **优先级标记**：🔴 = S 级必背，考前一天必须能默写；🟡 = 保底，混个眼熟、考到能想起来；⚪ = 冷门，扫一眼即可。节级标记给整节定调；节内行内 🔴 表示该条是 S 级核心。**时间不够时，从下往上砍。**
>
> **配套**：本单是"索引"，不是"教材"。哪条背不下来、想不起它从哪来，回对应篇目（每章标题后标了篇号）看 10 分钟。

---

# 〇、如果只剩 30 分钟：只看这 12 条

| # | 必背内容 | 在哪 |
|---|---|---|
| 1 | 等价无穷小 8 个主力（$\sin x,\tan x,\arcsin x,\arctan x,1-\cos x,\ln(1+x),e^x-1,(1+x)^\alpha-1$） | §1.1 |
| 2 | 泰勒 5 式（$e^x,\sin x,\cos x,\ln(1+x),(1+x)^\alpha$） | §1.2 |
| 3 | $1^\infty$ 公式：$\lim f^g=e^{\lim g(f-1)}$ | §1.4 |
| 4 | 基本求导表 + 复合/隐函数/参数方程法则 | §2.1–2.2 |
| 5 | 拉格朗日与柯西中值定理的**条件 + 结论** | §2.5 |
| 6 | 基本积分表 + 分部积分 + 区间再现 | §3.1–3.4 |
| 7 | 一阶线性通解公式 + 二阶常系数特征根三情形 | §4.2、4.4 |
| 8 | 二重/三重积分坐标变换的雅可比（$r$、$\rho^2\sin\varphi$） | §7.1–7.2 |
| 9 | Green / Gauss / Stokes 三个公式的**条件与方向** | §8.3、8.6、8.7 |
| 10 | $p$ 级数、几何级数、比值/根值判别法 | §9.1–9.2 |
| 11 | 收敛半径公式 + 常用展开式 | §10.1–10.2 |
| 12 | 傅里叶系数 + Dirichlet 收敛值 $\dfrac{f(x^-)+f(x^+)}{2}$ | §10.4 |


> ⚠️ 这 12 条是"底裤级"。下面每一节还有更细的表，但**这 12 条必须先做到提笔就写**。

---

# 一、极限与连续（01、02 篇）

## 1.1 🔴 等价无穷小替换表（x→0）

| 原式 | 等价于 | 提示 |
|---|---|---|
| $\sin x$ | $x$ | 最常用；注意只对**乘除因子**整体替换 |
| $\tan x$ | $x$ | 与 $\sin x$ 同阶 |
| $\arcsin x$ | $x$ | 反三角三兄弟一起记 |
| $\arctan x$ | $x$ | 同上 |
| $1-\cos x$ | $\dfrac{x^2}{2}$ | 二阶；别写成 $x^2$ |
| $\sec x-1$ | $\dfrac{x^2}{2}$ | 由 $1-\cos x$ 推 |
| $\ln(1+x)$ | $x$ | 一阶 |
| $e^x-1$ | $x$ | 一阶 |
| $a^x-1$ | $x\ln a$ | 别漏 $\ln a$ |
| $(1+x)^\alpha-1$ | $\alpha x$ | $\alpha$ 任意实数 |
| $\sqrt{1+x}-1$ | $\dfrac{x}{2}$ | $\alpha=\frac12$ 的特例 |
| $\sqrt[3]{1+x}-1$ | $\dfrac{x}{3}$ | $\alpha=\frac13$ 的特例 |
| $\sqrt[3]{1-\cos x}$ | $\dfrac{x^{2/3}}{\sqrt[3]{2}}$ | 先算框内再开三次方 |
| $\log_a(1+x)$ | $\dfrac{x}{\ln a}$ | 别把 $\ln a$ 放分子 |
| $x-\sin x$ | $\dfrac{x^3}{6}$ | 三阶，泰勒的直接结论 |
| $\tan x-x$ | $\dfrac{x^3}{3}$ | 三阶 |
| $\arcsin x-x$ | $\dfrac{x^3}{6}$ | 三阶 |
| $x-\arctan x$ | $\dfrac{x^3}{3}$ | 三阶 |
| $\tan x-\sin x$ | $\dfrac{x^3}{2}$ | 三阶；等价于 $x^3/2$ |
| $x-\ln(1+x)$ | $\dfrac{x^2}{2}$ | 二阶 |
| $e^x-1-x$ | $\dfrac{x^2}{2}$ | 二阶 |

⚠️ **替换三原则**：① 只对**乘除**整体替换，加减项不能单独换（除非用泰勒算到同阶）；② 替换后**阶数要匹配**——分母是 $x^3$ 就必须展到 $x^3$；③ 复合时要整体看：$\sin(x^2)\sim x^2$，不是 $\sim x$。

## 1.2 🔴 泰勒（麦克劳林）基本公式（x→0）

| 函数 | 展开（写到常用阶） |
|---|---|
| $e^x$ | $1+x+\dfrac{x^2}{2!}+\dfrac{x^3}{3!}+\cdots+\dfrac{x^n}{n!}+o(x^n)$ |
| $\sin x$ | $x-\dfrac{x^3}{3!}+\dfrac{x^5}{5!}-\cdots+(-1)^{n-1}\dfrac{x^{2n-1}}{(2n-1)!}+o(x^{2n-1})$ |
| $\cos x$ | $1-\dfrac{x^2}{2!}+\dfrac{x^4}{4!}-\cdots+(-1)^n\dfrac{x^{2n}}{(2n)!}+o(x^{2n})$ |
| $\ln(1+x)$ | $x-\dfrac{x^2}{2}+\dfrac{x^3}{3}-\cdots+(-1)^{n-1}\dfrac{x^n}{n}+o(x^n)$ |
| $(1+x)^\alpha$ | $1+\alpha x+\dfrac{\alpha(\alpha-1)}{2!}x^2+\cdots+\dfrac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}x^n+o(x^n)$ |
| $\dfrac{1}{1-x}$ | $1+x+x^2+\cdots+x^n+o(x^n)$ |
| $\dfrac{1}{1+x}$ | $1-x+x^2-\cdots+(-1)^nx^n+o(x^n)$ |
| $\arctan x$ | $x-\dfrac{x^3}{3}+\dfrac{x^5}{5}-\cdots+(-1)^n\dfrac{x^{2n+1}}{2n+1}+o(x^{2n+1})$ |
| $\arcsin x$ | $x+\dfrac{x^3}{6}+\dfrac{3x^5}{40}+o(x^5)$ |
| $\tan x$ | $x+\dfrac{x^3}{3}+\dfrac{2x^5}{15}+o(x^5)$ |
| $a^x$ | $1+x\ln a+\dfrac{(x\ln a)^2}{2!}+\cdots$ |
| $\log_a(1+x)$ | $\dfrac{x}{\ln a}-\dfrac{x^2}{2\ln a}+\cdots$ |

⚠️ **考场上怎么选阶数**：看分母的最低阶。分母 $\sim x^k$，分子就展到 $x^k$ 且**多展一阶**（防抵消后阶数不够）。加减混合时不要用等价无穷小偷懒。

## 1.3 🔴 洛必达法则：条件与规范

**适用**：$\dfrac{0}{0}$ 或 $\dfrac{\infty}{\infty}$。**三个条件**（缺一不可）：

1. $x\to a$ 时分子分母都趋于 $0$（或都趋于 $\infty$）；
2. 在 $a$ 的去心邻域内 $f',g'$ 存在，且 $g'(x)$ ≠ 0；
3. $\lim\dfrac{f'(x)}{g'(x)}$ 存在或为 $\infty$。

**结论**：$\lim\dfrac{f}{g}=\lim\dfrac{f'}{g'}$。

⚠️ 三个坑：① 不是未定式直接用 = 错；② 求导后极限不存在（如振荡）**不能反推原极限不存在**，要换方法；③ 分子分母要**分别**求导，不是商法则。

**单向门**：$\lim\dfrac{f'}{g'}$ 存在 ⇒ 原极限存在且相等；$\lim\dfrac{f'}{g'}$ 不存在 $\nRightarrow$ 原极限不存在。反例：$\lim\limits_{x\to+\infty}\dfrac{x+\sin x}{x}=1$，但 $\lim\limits_{x\to+\infty}(1+\cos x)$ 不存在。

## 1.4 🔴 七种未定式与处理路线

| 型 | 处理 |
|---|---|
| $\dfrac{0}{0},\dfrac{\infty}{\infty}$ | 洛必达 / 泰勒 / 等价无穷小 |
| $0\cdot\infty$ | 改写为 $\dfrac{0}{1/\infty}$ 或 $\dfrac{\infty}{1/0}$，转 $\dfrac{0}{0}$ 或 $\dfrac{\infty}{\infty}$ |
| $\infty-\infty$ | 通分、有理化、提公因子；或令 $t=1/x$ 转 $0/0$ |
| $0^0,\infty^0,1^\infty$ | 取对数：$f^g=e^{g\ln f}$，先算 $\lim g\ln f$ |

🔴 **$1^\infty$ 专用公式**：若 $f\to 1$，$g\to\infty$，则

$$\lim f(x)^{g(x)}=\exp\!\left[\lim g(x)\bigl(f(x)-1\bigr)\right].$$

⚠️ 用之前先确认"底确实趋于 1、指数确实趋于 $\infty$"，否则退回 $e^{g\ln f}$。

## 1.5 🟡 夹逼与单调有界

- **夹逼**：$g(x)\le f(x)\le h(x)$，且 $\lim g=\lim h=A$，则 $\lim f=A$。数列版同理。看到"$n$ 项和""最大/最小项"先想夹逼。
- **单调有界**：单调递增且有上界（或递减且有下界）→ 极限存在。证明递推数列收敛的标准流程：**先证有界（归纳）→ 再证单调（作差/作商）→ 设极限 $A$ 解方程**。
- **压缩映射**：$\lvert a_{n+1}-A\rvert\le k\lvert a_n-A\rvert$（$0<k<1$）→ $a_n\to A$。适合递推式能直接减出 $A$ 的题。
- **数列变形四把扳手**：取倒数、换元配 $y+\dfrac{a}{y}$、裂项/望远镜、取对数（连乘先证 $x_n>0$）。

## 1.6 🟡 数列极限常用结论

| 结论 | 提示 |
|---|---|
| $\lim\limits_{n\to\infty}\left(1+\dfrac{1}{n}\right)^n=e$ | 单调递增趋 $e$ |
| $\lim\limits_{n\to\infty}\left(1+\dfrac{1}{n}\right)^{n+1}=e$ | 单调递减趋 $e$ |
| $\lim\limits_{n\to\infty}\sqrt[n]{n}=1$ | 取对数或用 $n^{1/n}=e^{\ln n/n}$ |
| $\lim\limits_{n\to\infty}\sqrt[n]{a}=1\ (a>0)$ | 常数开 $n$ 次方 |
| $\lim\limits_{n\to\infty}\dfrac{n!}{n^n}=0$ | 阶的比较：$n!\ll n^n$ |
| $\lim\limits_{n\to\infty}\sqrt[n]{n!}=+\infty$ | Stirling 的粗糙版 |

**增长阶（从小到大）**：$\ln n \ll n^\alpha\ (\alpha>0)\ll a^n\ (a>1)\ll n!\ll n^n$。

## 1.7 🔴 变限积分型极限/求导模板

$$\frac{\mathrm{d}}{\mathrm{d}x}\int_{u(x)}^{v(x)}f(t)\,\mathrm{d}t=f\bigl(v(x)\bigr)v'(x)-f\bigl(u(x)\bigr)u'(x).$$

**三步模板**：① 先看能不能直接求导（被积函数只含 $t$）；② 若被积函数含 $x$，先把 $x$ 提到积分号外或换元；③ 极限题优先洛必达，分母求导后出现 $f(x)$ 就收工。

⚠️ 别把 $\dfrac{\mathrm{d}}{\mathrm{d}x}\displaystyle\int_0^x f(x-t)\,\mathrm{d}t$ 直接写成 $f(0)$——先令 $u=x-t$ 换元，得 $\int_0^x f(u)\,\mathrm{d}u$，再求导得 $f(x)$。

## 1.8 🟡 连续与间断

| 类型 | 判别 |
|---|---|
| 可去间断 | 左右极限存在且相等，但不等于 $f(a)$ 或 $f(a)$ 无定义 |
| 跳跃间断 | 左右极限都存在但**不相等** |
| 无穷间断 | 至少一侧极限为 $\infty$ |
| 振荡间断 | 极限不存在且不趋于 $\infty$（如 $\sin(1/x)$） |

**闭区间连续函数三性质**：有界性、最值性、介值性（含零点定理）。证明题看到"存在 $\xi$ 使 $f(\xi)=0$"先想零点定理；看到"存在 $\xi$ 使 $f(\xi)=\eta$"先想介值定理。

**复合函数间断点**：先重写 $f[g(x)]$ 的显式分段，再看内层把哪些 $x$ 映到外层"危险值"；**不能直接抄** $f$、$g$ 的断点。

## 1.9 🟡 极限题"看到 → 动作"速查

| 看到 | 第一动作 |
|---|---|
| 根式差 | 有理化（乘共轭）；或洛必达后先约公因子 |
| $\infty-\infty$ | 通分 / 有理化 / 提主项 |
| $0\cdot\infty$ | $uv=\dfrac{u}{1/v}$ 翻到分母 |
| 幂指 $u^v$ | 取 $e$：$u^v=e^{v\ln u}$，再算指数极限 |
| $1-$ 连乘 | $1-abc=(1-a)+a(1-b)+ab(1-c)$，逐层等价 |
| 幂差 $(n+1)^\alpha-n^\alpha$ | 提 $n^\alpha$，用 $(1+\frac1n)^\alpha<1+\frac1n\ (0<\alpha<1)$ 放缩后夹逼 |
| 求参数使极限存在/等于定值 | 泰勒按分母定阶；低阶系数先消为 $0$，再做系数匹配 |
| 变限积分 | 换元去包裹 → 求导/洛必达 → 积分中值 + 夹逼 |
| 含 $x^n$ 的积分 | $x=1/t$ → 凑微分 → 分部 → 放缩（$\ln(1+u)\le u$）→ 夹逼 |
| $n\times$ 无穷小 | 取倒数看差分 → Stolz / Cesàro |
| 递推 $x_{n+1}=f(x_n)$ | 猜界（解 $A=f(A)$）→ 证有界（归纳）→ 证单调（作差/作商）→ 取极限 |
| 求和/连乘数列 | 夹逼：找主项 → 放缩尾巴 → 两侧同极限 |
| 出现 $f(x)-f(cx)$ | 按 $c,c^2,\dots,c^n$ 铺成 $n$ 项，先固定 $n$ 求和再令 $n\to\infty$ |
| $\tan x-\sin x$ | 提公因式 $\tan x(1-\cos x)$ 再替换，别拆开乱换 |

## 1.10 🟡 连续与证明书写

- **连续三查**：左极限、右极限、$f(x_0)$——三者相等才算连续；分段函数只查分段点。
- **闭区间是命门**：开区间上 $\frac1x$ 在 $(0,1)$ 无界无最值；只说"可导 ⇒ 连续"，不能说取到最值。
- **介值/零点辅助函数表**：

| 要证 | 令 $F(x)=$ | 验什么 |
|---|---|---|
| $f(\xi)=\mu$ | $f(x)-\mu$ | 两端异号 |
| $f(\xi)=\alpha\xi+\beta$ | $f(x)-\alpha x-\beta$ | 代入端点算 |
| $f(\xi)=\dfrac{1}{b-a}\int_a^bf$ | $f(x)-I$ | 用积分估计夹出符号 |
| $f(\xi)=g(\xi)$ | $f(x)-g(x)$ | 代入端点算 |

⚠️ **证明书写纪律**：工具名字就是分数（"由夹逼准则""由零点定理""由拉格朗日中值定理"）；用前验条件；开/闭区间写对；归纳法 = 初始验证 + 归纳步；取极限解出 $A$ 后排除负根/越界根；压缩迭代先固定 $n$ 再令 $n\to\infty$；"有界" ≠ "收敛"。

---

# 二、一元函数微分（03、04 篇）

## 2.1 🔴 基本求导表

| 函数 | 导数 | 提示 |
|---|---|---|
| $C$ | $0$ | — |
| $x^\alpha$ | $\alpha x^{\alpha-1}$ | $\alpha$ 任意实数 |
| $a^x$ | $a^x\ln a$ | 别漏 $\ln a$ |
| $e^x$ | $e^x$ | 唯一"不动"的函数 |
| $\log_a x$ | $\dfrac{1}{x\ln a}$ | $\ln a$ 在分母 |
| $\ln x$ | $\dfrac{1}{x}$ | — |
| $\sin x$ | $\cos x$ | — |
| $\cos x$ | $-\sin x$ | 负号别丢 |
| $\tan x$ | $\sec^2x$ | $=1+\tan^2x$ |
| $\cot x$ | $-\csc^2x$ | — |
| $\sec x$ | $\sec x\tan x$ | — |
| $\csc x$ | $-\csc x\cot x$ | — |
| $\arcsin x$ | $\dfrac{1}{\sqrt{1-x^2}}$ | 定义域内 |
| $\arccos x$ | $-\dfrac{1}{\sqrt{1-x^2}}$ | 负号 |
| $\arctan x$ | $\dfrac{1}{1+x^2}$ | — |
| $\operatorname{arccot}x$ | $-\dfrac{1}{1+x^2}$ | 负号 |
| $\sinh x$ | $\cosh x$ | 双曲函数偶尔考 |
| $\cosh x$ | $\sinh x$ | — |

## 2.2 🔴 求导法则

| 法则 | 公式 |
|---|---|
| 四则 | $(uv)'=u'v+uv'$，$\left(\dfrac{u}{v}\right)'=\dfrac{u'v-uv'}{v^2}$ |
| 复合 | $\dfrac{\mathrm{d}y}{\mathrm{d}x}=\dfrac{\mathrm{d}y}{\mathrm{d}u}\cdot\dfrac{\mathrm{d}u}{\mathrm{d}x}$ |
| 反函数 | $\left(f^{-1}\right)'(y_0)=\dfrac{1}{f'(x_0)}$，$y_0=f(x_0)$ |
| 反函数二阶 | $\left(f^{-1}\right)''(y_0)=-\dfrac{f''(x_0)}{[f'(x_0)]^3}$ |
| 参数方程 | $\dfrac{\mathrm{d}y}{\mathrm{d}x}=\dfrac{y'(t)}{x'(t)}$，$\dfrac{\mathrm{d}^2y}{\mathrm{d}x^2}=\dfrac{y''x'-y'x''}{(x')^3}$ |
| 隐函数 $F(x,y)=0$ | $y'=-\dfrac{F_x}{F_y}$（验算用；主路线是两边直接求导） |
| 一阶微分形式不变性 | $\mathrm{d}f(u)=f'(u)\,\mathrm{d}u$（$u$ 为自变量或中间变量都成立） |
| 幂指函数 $u^v$ | $y'=u^v\left(v'\ln u+\dfrac{vu'}{u}\right)$ |
| 对数求导 | 先取 $\ln$ 再求导，适合连乘/连除/根式；最后别忘乘回原函数 |
| 分段函数 | 分界点必须用**左右导数定义**验证，不能直接套某一段公式 |

⚠️ 参数方程二阶导**不是** $y''/x''$；幂指函数**不能**用幂函数或指数函数单条公式。

**函数方程求 $f'(x_0)$ 三段式**：① 先取极限/代特殊点定 $f(x_0)$；② 凑双向差商 $\dfrac{f(x_0+h)-f(x_0)}{h}$；③ 解出 $f'(x_0)$。全程**禁洛必达**。

## 2.3 🟡 常用高阶导数

| 函数 | $n$ 阶导数 |
|---|---|
| $x^m$ | $m(m-1)\cdots(m-n+1)x^{m-n}$；$n=m$ 时为 $m!$，$n>m$ 时为 $0$ |
| $e^{ax}$ | $a^ne^{ax}$ |
| $\sin ax$ | $a^n\sin\left(ax+\dfrac{n\pi}{2}\right)$ |
| $\cos ax$ | $a^n\cos\left(ax+\dfrac{n\pi}{2}\right)$ |
| $\ln(1+x)$ | $\dfrac{(-1)^{n-1}(n-1)!}{(1+x)^n}$（$n\ge1$） |
| $\ln x$ | $(-1)^{n-1}\dfrac{(n-1)!}{x^n}$ |
| $\dfrac{1}{x-a}$ | $\dfrac{(-1)^nn!}{(x-a)^{n+1}}$ |
| $\dfrac{1}{1-x}$ | $\dfrac{n!}{(1-x)^{n+1}}$ |
| $\dfrac{1}{1+x}$ | $(-1)^n\dfrac{n!}{(1+x)^{n+1}}$ |

🔴 **Leibniz 公式**：$(uv)^{(n)}=\displaystyle\sum_{k=0}^{n}\binom{n}{k}u^{(k)}v^{(n-k)}$。见"多项式 × 指数/三角"就用它，多项式求到有限阶就没了。

🔴 **两个点值捷径**：若 $u=(x-x_0)^n$，则 $(uv)^{(n)}(x_0)=n!\,v(x_0)$；若 $f$ 能展开，则 $f^{(n)}(0)=n!\,[x^n]f(x)$（泰勒系数）。

**$n$ 阶导数四条路线（看到什么想什么）**：

1. **部分分式**：有理分式先拆成 $\dfrac{A}{(x-a)^k}$，再逐项套公式；
2. **Leibniz**：$u$ 是多项式、$v$ 是 $e^{ax}/\sin ax$ 时用；
3. **递推**：先求 $y',y''$ 找规律，或对等式两边求导造递推；
4. **泰勒系数**：$a_n=\dfrac{f^{(n)}(0)}{n!}$——题目要 $f^{(n)}(0)$ 时，直接展开取系数最快。

## 2.4 🔴 微分、切线法线、曲率

- 微分：$\mathrm{d}y=f'(x)\,\mathrm{d}x$；一元函数**可微 $\Leftrightarrow$ 可导**。
- 切线：$y-f(x_0)=f'(x_0)(x-x_0)$；法线：$y-f(x_0)=-\dfrac{1}{f'(x_0)}(x-x_0)$（$f'(x_0)$ ≠ 0）。
- 曲率：$\kappa=\dfrac{\lvert y''\rvert}{(1+y'^2)^{3/2}}$；曲率半径 $R=\dfrac{1}{\kappa}$。
- 参数方程曲率：$\kappa=\dfrac{\lvert x'y''-y'x''\rvert}{(x'^2+y'^2)^{3/2}}$。
- 弧微分：$\mathrm{d}s=\sqrt{1+y'^2}\,\mathrm{d}x=\sqrt{x'^2+y'^2}\,\mathrm{d}t$。

🟡 **渐近线**：垂直 $x=a$（$f\to\infty$）；水平 $y=b$（$x\to\infty$）；斜 $y=kx+b$，其中 $k=\lim\limits_{x\to\infty}\dfrac{f(x)}{x}$，$b=\lim\limits_{x\to\infty}[f(x)-kx]$。

## 2.5 🔴 中值定理：条件与结论（逐字背）

| 定理 | 条件 | 结论 |
|---|---|---|
| 费马 | $f$ 在 $x_0$ 取极值且在 $x_0$ 可导 | $f'(x_0)=0$ |
| 罗尔 | $[a,b]$ 连续，$(a,b)$ 可导，$f(a)=f(b)$ | $\exists\xi\in(a,b)$，$f'(\xi)=0$ |
| 拉格朗日 | $[a,b]$ 连续，$(a,b)$ 可导 | $\exists\xi\in(a,b)$，$f(b)-f(a)=f'(\xi)(b-a)$ |
| 柯西 | $f,g$ 在 $[a,b]$ 连续、$(a,b)$ 可导，$g'(x)$ ≠ 0 | $\exists\xi$，$\dfrac{f(b)-f(a)}{g(b)-g(a)}=\dfrac{f'(\xi)}{g'(\xi)}$ |
| 泰勒（拉格朗日余项） | $f$ 在含 $x_0$ 的区间有 $n+1$ 阶导 | 见下方泰勒公式 |

**泰勒公式（拉格朗日余项）**：

$$f(x)=\sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k+\frac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1},\qquad \xi\text{ 介于 }x_0\text{ 与 }x\text{ 之间}.$$

**两种余项，用途不同**：

| 余项 | 长相 | 用途 |
|---|---|---|
| 拉格朗日 | $\dfrac{f^{(n+1)}(\xi)}{(n+1)!}(x-x_0)^{n+1}$ | 证明/估计；**证明题必须用** |
| 皮亚诺 | $o\bigl((x-x_0)^n\bigr)$ | 求极限；不能用于估计 |

**家族关系**：罗尔是拉格朗日的特例（$f(a)=f(b)$）；拉格朗日是柯西的特例（$g(x)=x$）；拉格朗日也是泰勒的 0 阶特例。

⚠️ 三个高频扣分：① 罗尔必须写**开区间**内存在 $\xi$；② 柯西要写 $g'(x)$ ≠ 0 且 $g(b)$ ≠ $g(a)$；③ 泰勒的 $\xi$ 在 $x$ 与 $x_0$ **之间**，不是固定点。"二阶可导" ≠ "二阶连续可导"，不能把极限搬进 $f''$。

## 2.6 🔴 构造辅助函数"四板斧"

| 板斧 | 题面信号 | 2–3 步 |
|---|---|---|
| 原函数法 | 要证 $f'(\xi)+g(\xi)f(\xi)=0$ | 乘积分因子 $e^{\int g}$ → 令 $F=e^{\int g}f$ → 对 $F$ 用罗尔 |
| 常数 $k$ 值法 | 结论里 $\xi$ 与端点常数混在一起 | 把含 $\xi$ 的项与常数分离，令其比为 $k$ → 移项造 $F'=0$ → 罗尔 |
| 双中值 | 结论含两个点 $\xi,\eta$ | 在 $[a,c]$、$[c,b]$ 分别用拉格朗日/柯西 → 或对 $\dfrac{f(b)-f(a)}{g(b)-g(a)}$ 用柯西 |
| 泰勒展开 | 结论含 $f''$、要证不等式或估计 | 在极值点/中点/端点展开 → 用 $f'(\xi)=0$ 或界 $f''$ → 合并 |

**选择顺序（30 秒）**：数点 → 看导 → 找常数。多点 → 双中值；有 $f''$ → 泰勒；有可算常数 → 常数 $k$ 值法；其余 → 原函数法。

**常用辅助函数速记（默写）**：

| 待证结论 | 令 $F(x)=$ |
|---|---|
| $f'(\xi)=\lambda$ | $f(x)-\lambda x$ |
| $f'(\xi)+\lambda f(\xi)=0$ | $e^{\lambda x}f(x)$ |
| $f'(\xi)-f(\xi)=0$ | $e^{-x}f(x)$ |
| $\xi f'(\xi)+kf(\xi)=0$ | $x^kf(x)$ |
| $\xi f'(\xi)-kf(\xi)=0$ | $\dfrac{f(x)}{x^k}$ |
| $f'(\xi)g(\xi)-f(\xi)g'(\xi)=0$ | $\dfrac{f(x)}{g(x)}$ |
| $f'(\xi)g(\xi)+f(\xi)g'(\xi)=0$ | $f(x)g(x)$ |
| $f'(\xi)=f(\xi)+1$ | $e^{-x}(f(x)+1)$ |

**双中值/三中值的分点**：令 $F=f-$（目标线），两端异号，介值定理给 $x_0$；在 $[a,x_0]$、$[x_0,b]$ 分别用拉格朗日/柯西，最后写一句"$\xi<x_0<\eta$，故互异"。

**泰勒板斧的两个模板**：① 逐点估计——在 $x$ 处展开，代入 $0,1$ 两式相减消 $f(x)$；② 误差估计——中点展开后积分，一次项对称消掉。

## 2.7 🟡 单调性、凹凸性、极值、零点

- 单调：$f'>0$ 增，$f'<0$ 减（在区间上）；反之严格增只能推出 $f'\ge0$（$x^3$ 在 $0$ 处）。
- 凹凸：$f''>0$ ⟹ **凹向上（凸函数）**；$f''<0$ ⟹ 凹向下；$f''$ 变号处为拐点。
- 极值：$f'(x_0)=0$ 且 $f''(x_0)>0$ → 极小；$f''(x_0)<0$ → 极大；$f''=0$ 时看 $f'$ 两侧符号。
- 闭区间最值：比较**驻点、不可导点、端点**的函数值——一个都不能漏。
- 零点个数：单调性 + 介值定理 + 两端极限符号；"恰有 $n$ 个根" = 存在性（零点定理）+ 唯一性（严格单调/罗尔递降）**两头都写**。

**不等式证明四招（按试错顺序）**：

1. 作差 + 单调性（首选）；
2. 中值放缩：$f(x)-f(a)=f'(\xi)(x-a)$；
3. 最值法：$\Phi\ge0\iff\min\Phi\ge0$；
4. 泰勒余项 + 一致估计（证明题禁用皮亚诺余项）。

**符号接力模板（背）**：$g''<0\Rightarrow g'\downarrow\Rightarrow g'<g'(0)=0\Rightarrow g\downarrow\Rightarrow g<g(0)=0\Rightarrow f'<0$。

**常用不等式库**：$1+t\le e^t$；$\ln(1+t)\le t\ (t>-1)$；$\ln(1+t)\ge t-\frac{t^2}{2}\ (t\ge0)$；$1+u\ge2\sqrt{u}\ (u>0)$；$\sin x\ge\frac{2}{\pi}x\ (0\le x\le\frac{\pi}{2})$。

⚠️ "对一切 $x\in(0,1)$"不能直接取 $x=1$，只能令 $x\to1^-$ 取极限——这是概念性错误。

---

# 三、一元函数积分（05、06 篇）

## 3.1 🔴 基本积分表

| 被积函数 | 原函数 |
|---|---|
| $x^n$（$n$ ≠ -1） | $\dfrac{x^{n+1}}{n+1}+C$ |
| $\dfrac{1}{x}$ | $\ln\lvert x\rvert+C$ |
| $e^x$ | $e^x+C$ |
| $a^x$ | $\dfrac{a^x}{\ln a}+C$ |
| $\sin x$ | $-\cos x+C$ |
| $\cos x$ | $\sin x+C$ |
| $\sec^2x$ | $\tan x+C$ |
| $\csc^2x$ | $-\cot x+C$ |
| $\sec x\tan x$ | $\sec x+C$ |
| $\csc x\cot x$ | $-\csc x+C$ |
| $\sec x$ | $\ln\lvert\sec x+\tan x\rvert+C$ |
| $\csc x$ | $\ln\lvert\csc x-\cot x\rvert+C$ |
| $\dfrac{1}{1+x^2}$ | $\arctan x+C$ |
| $\dfrac{1}{\sqrt{1-x^2}}$ | $\arcsin x+C$ |
| $\dfrac{1}{a^2+x^2}$ | $\dfrac{1}{a}\arctan\dfrac{x}{a}+C$ |
| $\dfrac{1}{\sqrt{x^2\pm a^2}}$ | $\ln\left\lvert x+\sqrt{x^2\pm a^2}\right\rvert+C$ |
| $\dfrac{1}{x^2-a^2}$ | $\dfrac{1}{2a}\ln\left\lvert\dfrac{x-a}{x+a}\right\rvert+C$ |
| $\tan x$ | $-\ln\lvert\cos x\rvert+C$ |
| $\cot x$ | $\ln\lvert\sin x\rvert+C$ |

## 3.2 🔴 凑微分常用式

$$\mathrm{d}(ax+b)=a\,\mathrm{d}x,\qquad x\,\mathrm{d}x=\tfrac12\mathrm{d}(x^2),\qquad \frac{\mathrm{d}x}{x}=\mathrm{d}(\ln x),\qquad \frac{\mathrm{d}x}{\sqrt{x}}=2\,\mathrm{d}(\sqrt{x})$$

$$\frac{\mathrm{d}x}{x^2}=-\mathrm{d}\!\left(\frac{1}{x}\right),\qquad e^x\mathrm{d}x=\mathrm{d}(e^x),\qquad \cos x\,\mathrm{d}x=\mathrm{d}(\sin x),\qquad \sec^2x\,\mathrm{d}x=\mathrm{d}(\tan x)$$

$$\frac{\mathrm{d}x}{1+x^2}=\mathrm{d}(\arctan x),\qquad \frac{f'(x)}{f(x)}\mathrm{d}x=\mathrm{d}\bigl(\ln\lvert f(x)\rvert\bigr)$$

⚠️ 见 $u'/u$ 配 $\ln$、$u'e^u$ 配 $e^u$、$u'/(1+u^2)$ 配 $\arctan$。凑不动就换元，别硬凑。

## 3.3 🔴 分部积分

$$\int u\,\mathrm{d}v=uv-\int v\,\mathrm{d}u.$$

**选 $u$ 口诀：反、对、幂、指、三**（反三角 > 对数 > 幂 > 指数 > 三角）。排前面的当 $u$（求导降级），排后面的进 $\mathrm{d}v$（积分升级）。

⚠️ 单个 $\ln x$、$\arctan x$ 也上分部（把 $\mathrm{d}x$ 当 $\mathrm{d}v$）；$v$ 不加常数；$e^{ax}\sin bx$ 分部两次转回原积分，移项解出。

**有理式与三角有理式（保底）**：

- 假分式先长除；真分式拆 $\dfrac{A}{x-a}+\dfrac{Bx+C}{x^2+px+q}$。
- 三角有理式优先级：分子是分母导数 → 凑 $\ln$；同除 $\cos^2x$ 造 $\sec^2x$；降幂 $\sin^2x=\frac{1-\cos2x}{2}$；万能代换保底。
- 万能代换 $t=\tan\dfrac{x}{2}$：$\sin x=\dfrac{2t}{1+t^2}$，$\cos x=\dfrac{1-t^2}{1+t^2}$，$\mathrm{d}x=\dfrac{2\,\mathrm{d}t}{1+t^2}$。
- **隐函数曲线积分**：令 $y=tx$，把 $\displaystyle\int f(x,y)\,\mathrm{d}x$ 化为 $t$ 的有理积分（11 届填2 型）。

## 3.4 🔴 定积分性质与技巧

| 技巧 | 公式 | 提示 |
|---|---|---|
| 区间再现 | $\displaystyle\int_a^bf(x)\,\mathrm{d}x=\int_a^bf(a+b-x)\,\mathrm{d}x$ | 三角/根式题的主武器 |
| 三角配对 | $\displaystyle\int_0^{\pi}xf(\sin x)\,\mathrm{d}x=\frac{\pi}{2}\int_0^{\pi}f(\sin x)\,\mathrm{d}x$ | 出现 $x f(\sin x)$ 就用 |
| 正余弦互换 | $\displaystyle\int_0^{\pi/2}f(\sin x)\,\mathrm{d}x=\int_0^{\pi/2}f(\cos x)\,\mathrm{d}x$ | 常与区间再现联用 |
| 对称奇偶 | 奇函数 $\int_{-a}^af=0$；偶函数 $=2\int_0^af$ | 先看区间是否对称 |
| 周期平移 | $\displaystyle\int_a^{a+T}f=\int_0^Tf$ | 与起点无关；$n$ 个周期乘 $n$ |
| 估值 | $m(b-a)\le\int_a^bf\le M(b-a)$ | $m,M$ 为最值 |
| 积分中值 | $\displaystyle\int_a^bf=f(\xi)(b-a)$ | 加权版要求 $g$ 不变号 |
| 配对出 $\pi/4$ | $\displaystyle\int_0^{\pi/2}\frac{f(\tan x)}{f(\tan x)+f(\cot x)}\,\mathrm{d}x=\frac{\pi}{4}$ | 特例 $\frac{\sin x}{\sin x+\cos x}$ |

⚠️ 不奇不偶时用逐点合并：$\displaystyle\int_{-a}^af(x)\,\mathrm{d}x=\int_0^a[f(x)+f(-x)]\,\mathrm{d}x$。

**两件常备恒等式**：$\arctan e^x+\arctan e^{-x}=\dfrac{\pi}{2}$；$\dfrac{1+\sin x}{1+\cos x}=\dfrac12\sec^2\dfrac{x}{2}+\tan\dfrac{x}{2}$。

## 3.5 🔴 Wallis（点火公式）

$$I_n=\int_0^{\pi/2}\sin^nx\,\mathrm{d}x=\frac{n-1}{n}I_{n-2},\qquad I_0=\frac{\pi}{2},\quad I_1=1.$$

$$I_{2k}=\frac{(2k-1)!!}{(2k)!!}\cdot\frac{\pi}{2},\qquad I_{2k+1}=\frac{(2k)!!}{(2k+1)!!}.$$

⚠️ $\cos^nx$ 同公式；先判 $n$ 奇偶再套，奇偶初值不同。

## 3.6 🔴 变限积分

$$\frac{\mathrm{d}}{\mathrm{d}x}\int_{u(x)}^{v(x)}f(t)\,\mathrm{d}t=f\bigl(v(x)\bigr)v'(x)-f\bigl(u(x)\bigr)u'(x).$$

**换元两式**：

$$\int_0^xf(x-t)\,\mathrm{d}t=\int_0^xf(u)\,\mathrm{d}u,\qquad \int_0^1f(xt)\,\mathrm{d}t=\frac{1}{x}\int_0^xf(u)\,\mathrm{d}u.$$

⚠️ 被积函数含 $x$ 时**先换元再求导**；上限是函数时链式因子不能丢。

## 3.7 🟡 定积分几何应用

| 量 | 公式 |
|---|---|
| 面积（上 $f$ 下 $g$） | $A=\displaystyle\int_a^b[f(x)-g(x)]\,\mathrm{d}x$ |
| 平行截面体积 | $V=\displaystyle\int_a^bA(x)\,\mathrm{d}x$ |
| 绕 $x$ 轴旋转体 | $V=\pi\displaystyle\int_a^bf^2(x)\,\mathrm{d}x$ |
| 绕 $y$ 轴柱壳 | $V=2\pi\displaystyle\int_a^bx\lvert f(x)\rvert\,\mathrm{d}x$ |
| 弧长（显式） | $s=\displaystyle\int_a^b\sqrt{1+f'^2(x)}\,\mathrm{d}x$ |
| 弧长（参数） | $s=\displaystyle\int_\alpha^\beta\sqrt{x'^2+y'^2}\,\mathrm{d}t$ |
| 弧长（极坐标） | $s=\displaystyle\int_{\theta_1}^{\theta_2}\sqrt{r^2+r'^2}\,\mathrm{d}\theta$ |
| 绕 $x$ 轴旋转曲面面积 | $S=2\pi\displaystyle\int_a^b\lvert f(x)\rvert\sqrt{1+f'^2(x)}\,\mathrm{d}x$ |
| 函数平均值 | $\bar f=\dfrac{1}{b-a}\displaystyle\int_a^bf(x)\,\mathrm{d}x$ |

⚠️ 面积先解全部交点、分段落"上减下"；侧面积必须带 $\lvert f\rvert$。

## 3.8 🟡 广义积分敛散（保底）

- $\displaystyle\int_1^{+\infty}\frac{\mathrm{d}x}{x^p}$：$p>1$ 收敛，$p\le1$ 发散。
- $\displaystyle\int_0^{1}\frac{\mathrm{d}x}{x^p}$：$p<1$ 收敛，$p\ge1$ 发散。
- 比较判别：非负函数，$f(x)\le\dfrac{C}{x^p}$ 且 $p>1$ → 收敛；$f(x)\ge\dfrac{C}{x^p}$ 且 $p\le1$ → 发散。
- **条件收敛陷阱**：$\displaystyle\int_0^{+\infty}\frac{\sin x}{x}\,\mathrm{d}x$ 收敛但**不绝对收敛**；题面问"敛散性"若答案是条件收敛，**必须把"收敛 + 非绝对收敛"两半都写出来**，只写一半扣一半分。

## 3.9 🟡 积分不等式四板斧

| 板斧 | 触发信号 | 2–3 步模板 |
|---|---|---|
| Cauchy–Schwarz | 两积分之积、$\int f^2$ 被控制、$(\int fg)^2$ | 配权分部把 $\int f^2$ 改写成 $\int w\cdot2ff'$ → Cauchy → 约分/平方 |
| 分部积分恒等式 | "积分套积分" $\int f(x)\bigl(\int_a^xg\bigr)\mathrm{d}x$ | 记 $F=\int_a^xf$，$G=\int_a^xg$ → 分部一次 → 用题设洗掉边界项 |
| 对称化 | 证 $\int fG>0$；核可写成 $f(x)g(s)-f(s)g(x)$ | $L=\iint_Df(x)g(s)$ → 写成 $\frac12\iint_D[f(x)g(s)-f(s)g(x)]$ → 按零点分片定号 |
| 放缩 | $\lvert\sin nx\rvert$、高次/分数幂、求最佳常数 | 定方向 → 分段各取最优 → 取等分析 |
| 变限积分辅助函数 | 结论含 $\left(\int f\right)^2$ 与 $\int f^3$ | 令 $F=\left(\int_0^xf\right)^2-\int_0^xf^3$ → 验 $F(0)=0$，证 $F'>0$；不够再对内层做两级单调 |

🔴 **Cauchy–Schwarz 积分版**：

$$\left(\int_a^bfg\right)^2\le\int_a^bf^2\int_a^bg^2,$$

取等当且仅当 $f=cg$。特例 $g\equiv1$：$\left(\int_0^1f\right)^2\le\int_0^1f^2$。

**常用放缩**：$\lvert\sin nx\rvert\le n\lvert\sin x\rvert$（$0\le x\le\pi/2$），$\sin x\ge\dfrac{2}{\pi}x$（$0\le x\le\pi/2$），$\ln(1+t)\le t$，$\dfrac{a+b}{2}\ge\sqrt{ab}$。

## 3.10 🟡 三个必背模板

1. **定积分为常数设参**：把 $\int_a^bf$ 设成 $A$ → 原式变成 $f$ 的显式 → 两边积分造方程 → 解出 $A$ 回代。**绝不两边求导**（常数求导信息全灭）。
2. **区间再现**：记 $I=\int_a^bf(x)\mathrm{d}x$ → 换 $x\to a+b-x$ 得第二副面孔 → 两式相加/相减消难点。见 $[0,\pi/2]$、$[0,\pi]$ + 三角式优先想它。
3. **换元挪 $n$**：$n$ 在幂次或积分号外 → 令 $u=x^n$ 或 $x=1/t$ → 凑微分或"剪尾估头" → 夹逼。
4. **黎曼和误差**：
   - 右端点：$\displaystyle\lim_{n\to\infty}n\left(\int_0^1g-\frac1n\sum_{k=1}^{n}g\!\left(\frac{k}{n}\right)\right)=\frac{g(0)-g(1)}{2}$；
   - 中点：$\displaystyle\lim_{n\to\infty}n^2\left[\int_a^bf-\frac{b-a}{n}\sum_{k=1}^{n}f(\xi_k)\right]=\frac{(b-a)^2}{24}[f'(b)-f'(a)]$。

---

# 四、常微分方程（07 篇）

## 4.1 🔴 一阶方程识别表（看到什么，用什么）

| 类型 | 识别信号 | 解法（2–3 步） | 坑 |
|---|---|---|---|
| 可分离 | $y'=\varphi(x)\psi(y)$ | 分离变量 → 两边积分 → 代初值定 $C$ | 除过可能为零的因子，回头查 $y\equiv0$ 类丢解 |
| 齐次 | $y'=r(y/x)$，或右边分子分母同次 | 令 $u=y/x$（$y'=u+xu'$）→ 解 $xu'=r(u)-u$ → 回代 | 解完必须回代 $u=y/x$ |
| 线性 | $y'+P(x)y=Q(x)$ | 化标准形（$y$ 前系数归一）→ 套通解公式 | 公式"一正一负"，错一处全错 |
| 伯努利 | $y'+Py=Qy^n$（$n$ 非0、1） | 令 $z=y^{1-n}$ → 化线性 → 回代 | 指数是 $1-n$，不是 $n-1$ |
| 全微分 | $M\,\mathrm{d}x+N\,\mathrm{d}y=0$ | 验 $M_y=N_x$ → 凑四大恒等式 → 通解 $u(x,y)=C$ | 先凑，不硬算积分因子 |
| 平移型 | $y'=\dfrac{a_1x+b_1y+c_1}{a_2x+b_2y+c_2}$ | 解两直线交点 → 平移 $X=x-x_0,\ Y=y-y_0$ → 再令 $u=Y/X$ | 两线平行时改用线性换元 |

## 4.2 🔴 必背公式

**一阶线性通解**：

$$y=e^{-\int P(x)\,\mathrm{d}x}\left(\int Q(x)e^{\int P(x)\,\mathrm{d}x}\,\mathrm{d}x+C\right).$$

**伯努利换元**：

$$z=y^{1-n}\ \Longrightarrow\ z'+(1-n)P(x)z=(1-n)Q(x).$$

**凑微分四式**：

$$x\,\mathrm{d}x+y\,\mathrm{d}y=\tfrac12\mathrm{d}(x^2+y^2),\qquad x\,\mathrm{d}y+y\,\mathrm{d}x=\mathrm{d}(xy),$$

$$\frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{x^2}=\mathrm{d}\!\left(\frac{y}{x}\right),\qquad \frac{x\,\mathrm{d}y-y\,\mathrm{d}x}{x^2+y^2}=\mathrm{d}\!\left(\arctan\frac{y}{x}\right).$$

⚠️ 见 $x\,\mathrm{d}y-y\,\mathrm{d}x$ 就想造 $\dfrac{y}{x}$ 或 $\arctan\dfrac{y}{x}$。

## 4.3 🟡 可降阶与欧拉方程

| 类型 | 代换 | 化归 |
|---|---|---|
| $y^{(n)}=f(x)$ | 直接积分 | 逐次积分 $n$ 次，出 $n$ 个常数 |
| $y''=f(x,y')$（缺 $y$） | $p=y'$ | $p'=f(x,p)$，一阶方程 |
| $y''=f(y,y')$（缺 $x$） | $p=y'$，看作 $p(y)$ | $p\dfrac{\mathrm{d}p}{\mathrm{d}y}=f(y,p)$ |

**欧拉方程** $x^2y''+pxy'+qy=f(x)$：令 $x=e^t$，则

$$xy'=\frac{\mathrm{d}y}{\mathrm{d}t},\qquad x^2y''=\frac{\mathrm{d}^2y}{\mathrm{d}t^2}-\frac{\mathrm{d}y}{\mathrm{d}t}.$$

## 4.4 🔴 二阶常系数齐次（默写表）

| 特征根 $r^2+pr+q=0$ | 通解 |
|---|---|
| 两实根 $r_1$ ≠ $r_2$ | $y=C_1e^{r_1x}+C_2e^{r_2x}$ |
| 二重实根 $r$ | $y=(C_1+C_2x)e^{rx}$ |
| 共轭复根 $\alpha\pm\beta i$ | $y=e^{\alpha x}(C_1\cos\beta x+C_2\sin\beta x)$ |

⚠️ 重根"撞车就乘 $x$"；复根 = 指数衰减/增长 × 振荡。

## 4.5 🔴 二阶常系数非齐次：特解设法

| 右端 $f(x)$ | 试解 $y^*$（$k$ = 撞根重数 0/1/2） |
|---|---|
| $P_m(x)$ | $x^kQ_m(x)$（$0$ 是特征根时 $k\ge1$） |
| $P_m(x)e^{\lambda x}$ | $x^kQ_m(x)e^{\lambda x}$（$\lambda$ 是特征根时 $k\ge1$） |
| $e^{\alpha x}(P_m\cos\beta x+Q_m\sin\beta x)$ | $x^ke^{\alpha x}(R_m\cos\beta x+S_m\sin\beta x)$（$\alpha+\beta i$ 是特征根时 $k\ge1$） |

⚠️ 撞根不乘 $x^k$ 是最经典失分点；右端为和 → 拆开分别求特解再相加。

**解的结构**：非齐次通解 = 齐次通解 + 非齐次任一特解；非齐次两解之差 = 齐次解。反推方程：两两作差 → 读特征根定左端 → 任一特解代入定右端。

## 4.6 🔴 竞赛高频换元

| 题面信号 | 换元 |
|---|---|
| $y\,\mathrm{d}y$ 与 $x\,\mathrm{d}x$ 可配对、出现 $y^2$ | $u=y^2$（或 $u=x^2,\ v=y^2$） |
| $\sin y\cdot y'$、$\cos y$ 整块 | $u=\cos y$（$\sin y\,y'=-(\cos y)'$） |
| $e^y$、$\ln y$、$\cos y$ 整块可当未知函数 | 令 $u=e^y$ 等，一步化线性 |
| $\dfrac{\mathrm{d}y}{\mathrm{d}x}$ 解不动 | 反解 $\dfrac{\mathrm{d}x}{\mathrm{d}y}$，把 $x$ 当未知函数 |
| 分式线性带常数项 | 先平移消常数，再作齐次换元 |

⚠️ 换元本身是评分点（约 6 分）：写不出解也要把"令 …，则方程化为 …"写满。

- **隐藏型 ODE**：未知函数锁在 $\int$ 号里时，先代特殊点抢初值，再两边求导化 ODE；顺序反了会丢初值。

---

# 五、空间解析几何（08 篇）

## 5.1 🔴 向量三积

| 积 | 坐标公式 | 几何意义 / 用途 |
|---|---|---|
| 数量积 | $\vec a\cdot\vec b=a_1b_1+a_2b_2+a_3b_3=\lvert\vec a\rvert\lvert\vec b\rvert\cos\theta$ | 求夹角；$\vec a\perp\vec b\Leftrightarrow\vec a\cdot\vec b=0$ |
| 向量积 | $\vec a\times\vec b=(a_2b_3-a_3b_2,\ a_3b_1-a_1b_3,\ a_1b_2-a_2b_1)$ | 模 = 平行四边形面积；方向右手；同时垂直两者 |
| 混合积 | $(\vec a\times\vec b)\cdot\vec c$ = 三阶行列式 | 绝对值 = 平行六面体体积；$=0\Leftrightarrow$ 三向量共面 |

$$\vec a\times\vec b=\begin{vmatrix}\vec i&\vec j&\vec k\\ a_1&a_2&a_3\\ b_1&b_2&b_3\end{vmatrix}.$$

⚠️ $\vec j$ 分量带负号；$\vec a\times\vec b=-\vec b\times\vec a$；混合积为 $0$ 是"共面"不是"平行"。

**两条"制造垂直"公式**：

$$\vec n=\overrightarrow{P_1P_2}\times\overrightarrow{P_1P_3},\qquad \vec s=\vec n_1\times\vec n_2.$$

## 5.2 🔴 平面

| 形式 | 方程 | 用法 |
|---|---|---|
| 点法式 | $A(x-x_0)+B(y-y_0)+C(z-z_0)=0$ | 有一点 + 法向量（首选） |
| 一般式 | $Ax+By+Cz+D=0$ | $D=0$ 过原点；"缺谁平行谁" |
| 截距式 | $\dfrac{x}{a}+\dfrac{y}{b}+\dfrac{z}{c}=1$ | 已知三坐标轴截距 |
| 平面束 | $\pi_1+\lambda\pi_2=0$ | 过交线 $L:\pi_1=0,\pi_2=0$ 的一切平面 |

⚠️ 定 $\lambda$：与已知平面垂直 $\Leftrightarrow\vec n(\lambda)\cdot\vec n_0=0$；过某点则代坐标。单参数版不含 $\pi_2$，完整版写 $\lambda\pi_1+\mu\pi_2=0$。

## 5.3 🔴 直线

| 形式 | 方程 | 用法 |
|---|---|---|
| 对称式 | $\dfrac{x-x_0}{l}=\dfrac{y-y_0}{m}=\dfrac{z-z_0}{n}$ | 已知一点 + 方向向量 |
| 参数式 | $x=x_0+lt,\ y=y_0+mt,\ z=z_0+nt$ | 求交点、代入联立 |
| 一般式 | 两平面方程联立 | $\vec s=\vec n_1\times\vec n_2$ |

## 5.4 🟡 位置关系（垂直点积，平行叉积）

| 关系 | 条件 |
|---|---|
| 面 $\perp$ 面 | $\vec n_1\cdot\vec n_2=0$ |
| 面 $\parallel$ 面 | $\vec n_1\times\vec n_2=\vec 0$ |
| 线 $\perp$ 面 | $\vec s\parallel\vec n$ |
| 线 $\parallel$ 面 | $\vec s\cdot\vec n=0$（且直线不在面内） |
| 线 $\perp$ 线 | $\vec s_1\cdot\vec s_2=0$ |
| 线 $\parallel$ 线 | $\vec s_1\times\vec s_2=\vec 0$ |
| 两线共面 | $(\vec s_1\times\vec s_2)\cdot\overrightarrow{P_1P_2}=0$ |

## 5.5 🔴 距离与夹角（整表默写）

| 对象 | 公式 | 备注 |
|---|---|---|
| 两向量夹角 | $\cos\theta=\dfrac{\vec a\cdot\vec b}{\lvert\vec a\rvert\lvert\vec b\rvert}$ | $[0,\pi]$ |
| 两直线夹角 | $\cos\theta=\dfrac{\lvert\vec s_1\cdot\vec s_2\rvert}{\lvert\vec s_1\rvert\lvert\vec s_2\rvert}$ | 取锐角，带绝对值 |
| 线面夹角 | $\sin\theta=\dfrac{\lvert\vec s\cdot\vec n\rvert}{\lvert\vec s\rvert\lvert\vec n\rvert}$ | **用 $\sin$ 不用 $\cos$** |
| 两平面夹角 | $\cos\theta=\dfrac{\lvert\vec n_1\cdot\vec n_2\rvert}{\lvert\vec n_1\rvert\lvert\vec n_2\rvert}$ | 带绝对值 |
| 点面距 | $d=\dfrac{\lvert Ax_0+By_0+Cz_0+D\rvert}{\sqrt{A^2+B^2+C^2}}$ | 分子绝对值、分母开方 |
| 点线距 | $d=\dfrac{\lvert\overrightarrow{AP}\times\vec s\rvert}{\lvert\vec s\rvert}$ | 分母是一次 $\lvert\vec s\rvert$ |
| 两平行平面距 | $d=\dfrac{\lvert D_1-D_2\rvert}{\sqrt{A^2+B^2+C^2}}$ | 先把系数化成相同 |
| ⚪ 异面直线距（大纲外） | $d=\dfrac{\lvert\overrightarrow{P_1P_2}\cdot(\vec s_1\times\vec s_2)\rvert}{\lvert\vec s_1\times\vec s_2\rvert}$ | 仅作混合积练习 |

⚠️ 纪律："面面线线 $\cos$，线面 $\sin$，全都带绝对值"。

**单位方向向量**：方向向量先除以模长；写 $\pm$ 均可，官方评分注"得到一个即可"。

## 5.6 🟡 投影

- **投影直线** =（过 $L$ 且垂直于 $\pi$ 的平面）$\cap\ \pi$；只需方向时用

$$\vec s'=\vec s-\frac{\vec s\cdot\vec n}{\lvert\vec n\rvert^2}\vec n.$$

- **投影柱面**：$C:\{F=0,\ G=0\}$ 消去 $z$ 得 $H(x,y)=0$；投影曲线 $=\begin{cases}H(x,y)=0\\ z=0\end{cases}$。

⚠️ 高频扣分：投影曲线必须补坐标面 $z=0$。

## 5.7 🔴 曲面

- **切平面**：$\vec n=\nabla F(P_0)=(F_x,F_y,F_z)\big|_{P_0}$，

$$F_x(x-x_0)+F_y(y-y_0)+F_z(z-z_0)=0.$$

- **法线**：$\dfrac{x-x_0}{F_x(P_0)}=\dfrac{y-y_0}{F_y(P_0)}=\dfrac{z-z_0}{F_z(P_0)}$。

⚠️ "平行已知平面"三步：$\nabla F(P_0)\parallel\vec n_\pi$ 解出 $x_0,y_0$ → **回代曲面求 $z_0$** → 写点法式。第三步漏掉 = 整题错。

- **两曲面相切**：$\nabla F=\lambda\nabla G$，再加 $F=0$、$G=0$ 解切点；"相切" = 共享法线。
- **柱面**：方程缺哪个变量，母线就平行哪根轴（$F(x,y)=0$ 母线平行 $z$ 轴）。
- **旋转曲面**：绕哪根轴哪根不动；$f(y,z)=0$ 绕 $z$ 轴 → $f(\pm\sqrt{x^2+y^2},\,z)=0$。

## 5.8 🟡 二次曲面识别表

| 名称 | 标准方程 | 特征 |
|---|---|---|
| 椭球面 | $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}+\dfrac{z^2}{c^2}=1$ | 有界闭合 |
| 单叶双曲面 | $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}-\dfrac{z^2}{c^2}=1$ | 一整张，腰口是椭圆 |
| 双叶双曲面 | $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}-\dfrac{z^2}{c^2}=-1$ | 上下两张 |
| 椭圆抛物面 | $z=\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}$ | 开口向上的碗 |
| 双曲抛物面 | $z=\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}$ | 马鞍形 |
| 圆锥面 | $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=\dfrac{z^2}{c^2}$ | 顶点在原点，两叶 |
| 柱面 | 缺一个变量（如 $x^2+y^2=R^2$） | 母线平行"缺的那个"轴 |

⚠️ 致命混淆：$z=x^2+y^2$（抛物面）vs $z^2=x^2+y^2$（锥面）——"一次是碗，二次是锥"。

---

# 六、多元函数微分学（09 篇）

## 6.1 🔴 偏导、可微与关系链

- 偏导：$f_x(x_0,y_0)=\lim\limits_{\Delta x\to0}\dfrac{f(x_0+\Delta x,y_0)-f(x_0,y_0)}{\Delta x}$；求 $f_x$ 冻结 $y$，求 $f_y$ 冻结 $x$。
- 可微：$\Delta z=f_x\Delta x+f_y\Delta y+o(\rho)$，$\rho=\sqrt{\Delta x^2+\Delta y^2}$；$\mathrm{d}z=f_x\mathrm{d}x+f_y\mathrm{d}y$。
- 关系链：**偏导连续 $\Rightarrow$ 可微 $\Rightarrow$ 偏导存在**；可微 $\Rightarrow$ 连续。箭头均不可逆。
- 混合偏导：二阶偏导连续时 $f_{xy}=f_{yx}$。

⚠️ 经典反例 $\dfrac{xy}{\sqrt{x^2+y^2}}$：连续、偏导存在、**不可微**——偏导存在不能当可微的证据。

## 6.2 🔴 复合函数链式法则

$$z_x=f_1u_x+f_2v_x,\qquad z_y=f_1u_y+f_2v_y.$$

⚠️ $f_1$ 是"对第一中间变量求导"，不是 $f_x$；$f_1$ 自身仍是 $(u,v)$ 的函数，再求导要继续链式。

**二阶五项**（画变量树，别硬背）：

$$z_{xy}=f_{11}u_xu_y+f_{12}(u_xv_y+u_yv_x)+f_{22}v_xv_y+f_1u_{xy}+f_2v_{xy}.$$

⚠️ 最后两项 $f_1u_{xy}+f_2v_{xy}$ 最易漏；$f_{12}$ 与 $f_{21}$ 要合并。

## 6.3 🔴 隐函数求导

$$F(x,y)=0:\quad y'=-\frac{F_x}{F_y};\qquad F(x,y,z)=0:\quad z_x=-\frac{F_x}{F_z},\quad z_y=-\frac{F_y}{F_z}.$$

⚠️ 需 $F_z$ ≠ 0；求 $F_x$ 时 $y,z$ 全当常数；考场首选"两边直接求导"，公式用来验算。

**求点值顺序**：先用原方程定出该点 $z_0$（或中间变量值），再求导代点；顺序反了信息就丢。

## 6.4 🔴 几何应用

| 对象 | 公式 |
|---|---|
| 曲面 $F(x,y,z)=0$ 切平面 | $F_x(x-x_0)+F_y(y-y_0)+F_z(z-z_0)=0$ |
| 曲面 $z=f(x,y)$ 切平面 | $z-z_0=f_x(x-x_0)+f_y(y-y_0)$ |
| 法线方向 | $\nabla F=(F_x,F_y,F_z)$；$z=f$ 时为 $(f_x,f_y,-1)$ |
| 曲线 $\mathbf r(t)$ 切线 | 方向 $\mathbf r'(t_0)$，$\dfrac{x-x_0}{x'}=\dfrac{y-y_0}{y'}=\dfrac{z-z_0}{z'}$ |
| 曲线法平面 | $\mathbf r'(t_0)\cdot\bigl((x,y,z)-P_0\bigr)=0$ |
| 两曲面交线切向 | $\boldsymbol\tau=\nabla F_1\times\nabla F_2$ |
| 两曲面相切 | $\nabla F_1\parallel\nabla F_2$ 且 $F_1(P_0)=F_2(P_0)=0$ |

⚠️ $z=f(x,y)$ 的法向量第三个分量是 $-1$，别丢；相切两条件缺一不可。

## 6.5 🔴 方向导数与梯度

$$\frac{\partial f}{\partial\boldsymbol l}=\nabla f\cdot\boldsymbol e_l=f_x\cos\alpha+f_y\cos\beta+f_z\cos\gamma.$$

- 最大方向导数 $=\lVert\nabla f\rVert$，方向为 $\dfrac{\nabla f}{\lVert\nabla f\rVert}$；最小为 $-\lVert\nabla f\rVert$。
- ⚠️ 方向向量先**单位化**；不可微点只能按定义算。

## 6.6 🔴 极值、最值、拉格朗日

- 驻点：$f_x=f_y=0$。判别：$A=f_{xx}$，$B=f_{xy}$，$C=f_{yy}$。
  - $AC-B^2>0$ 且 $A>0$ → 极小；$A<0$ → 极大；
  - $AC-B^2<0$ → 非极值；$AC-B^2=0$ → 失效（初赛不考）。
- **闭区域最值**：内部驻点值 → 边界化一元（或 Lagrange）→ 角点值 → 全部比大小。**漏边界是头号失分点**。
- **Lagrange 乘数法**：$L=f+\lambda\varphi$ → 解 $\nabla L=0$（$f_x=-\lambda\varphi_x$，$f_y=-\lambda\varphi_y$，$\varphi=0$）→ 候选点代回比较；两个约束再加 $\mu\psi$。

⚠️ Lagrange 只给必要条件；应用题补一句"由几何意义"，这半句是评分点。

## 6.7 🟡 二阶泰勒与线性化

$$f(x_0+h,y_0+k)=f+f_xh+f_yk+\tfrac12\left(f_{xx}h^2+2f_{xy}hk+f_{yy}k^2\right)+o(\rho^2).$$

一阶线性化：$f(P_0+\Delta)\approx f(P_0)+f_x\Delta_1+f_y\Delta_2$。

---

# 七、重积分（10 篇）

## 7.1 🔴 二重积分：直角坐标、换序、极坐标

$$\iint_Df\,\mathrm{d}x\mathrm{d}y=\int_a^b\mathrm{d}x\int_{y_1(x)}^{y_2(x)}f\,\mathrm{d}y.$$

**换序**：画域 → 写成不等式组 → 以另一变量为主序重写上下限（必要时翻方向补负号）。内层积不出（$e^{-y^2}$、$\frac{\sin y}{y}$、$\frac{1}{\ln y}$）时必换。

**极坐标**：

$$x=r\cos\theta,\quad y=r\sin\theta,\quad \mathrm{d}x\mathrm{d}y=r\,\mathrm{d}r\,\mathrm{d}\theta.$$

⚠️ 忘乘 $r$ 是最高频丢分点；$x^2+y^2\le\pi$ 的半径是 $\sqrt{\pi}$。

**一般换元**：

$$\iint_Df\,\mathrm{d}x\mathrm{d}y=\iint_{D'}f\,\lvert J\rvert\,\mathrm{d}u\mathrm{d}v,\qquad J=\frac{\partial(x,y)}{\partial(u,v)}.$$

**半径 → 0 的变域积分极限**（近年填空固定戏码）：极坐标把分子积成只含 $r$ 的 $G(r)$ → 与分母 $r^k$ 泰勒配阶 → 相除；低阶项不消说明积分算错。

## 7.2 🔴 三重积分

| 方法 | 公式 | 适用信号 |
|---|---|---|
| 先一后二 | $\displaystyle\iiint_\Omega f\,\mathrm{d}V=\iint_{D_{xy}}\left(\int_{z_1(x,y)}^{z_2(x,y)}f\,\mathrm{d}z\right)\mathrm{d}x\mathrm{d}y$ | 上下曲面有显式表达式 |
| 先二后一 | $\displaystyle\iiint_\Omega f\,\mathrm{d}V=\int_c^d\left(\iint_{D_z}f\,\mathrm{d}x\mathrm{d}y\right)\mathrm{d}z$ | 被积函数缺某变量、截面面积好算 |
| 柱坐标 | $\mathrm{d}V=r\,\mathrm{d}r\,\mathrm{d}\theta\,\mathrm{d}z$ | 柱面/旋转抛物面/锥面 + $z$ 为直线段 |
| 球坐标 | $\mathrm{d}V=\rho^2\sin\varphi\,\mathrm{d}\rho\,\mathrm{d}\varphi\,\mathrm{d}\theta$ | 球/锥/球壳 |

球坐标：$x=\rho\sin\varphi\cos\theta$，$y=\rho\sin\varphi\sin\theta$，$z=\rho\cos\varphi$；$\varphi\in[0,\pi]$，锥面 $z=k\sqrt{x^2+y^2}$ 的半顶角 $\varphi_0=\arctan\dfrac{1}{k}$。

⚠️ 球坐标漏 $\sin\varphi$ 必错；柱坐标漏 $r$ 必错。

## 7.3 🔴 对称性

- **奇偶**：$D$ 关于 $x$ 轴对称且 $f$ 对 $y$ 奇 → 积分为 $0$；偶 → 化半域乘 $2$。两个前提必须同时成立。
- **轮换**：$D$ 在 $x\leftrightarrow y$ 下不变 ⇒ $\displaystyle\iint_Dx^2=\iint_Dy^2=\frac12\iint_D(x^2+y^2)$；三重各为 $\frac13\iiint(x^2+y^2+z^2)$。
- ⚠️ 三角形 $\{0\le y\le x\le1\}$ 不轮换，不能用。

## 7.4 🟡 几何与物理应用

| 量 | 公式 |
|---|---|
| 面积 | $A=\displaystyle\iint_D\mathrm{d}x\mathrm{d}y$ |
| 体积 | $V=\displaystyle\iiint_\Omega\mathrm{d}V=\int_c^dA(z)\,\mathrm{d}z$ |
| 质量 | $m=\displaystyle\iiint_\Omega\rho\,\mathrm{d}V$ |
| 质心 | $\bar x=\dfrac{1}{m}\displaystyle\iiint_\Omega x\rho\,\mathrm{d}V$（$\bar y,\bar z$ 同） |
| 转动惯量（$z$ 轴） | $I_z=\displaystyle\iiint_\Omega(x^2+y^2)\rho\,\mathrm{d}V$ |

均匀密度时质心 = 形心；某方向对称可白送该坐标。

## 7.5 🟡 常用结论（填空直接引用）

- 圆盘 $x^2+y^2\le R^2$：$\displaystyle\iint(x^2+y^2)\,\mathrm{d}\sigma=\dfrac{\pi R^4}{2}$，$\displaystyle\iint x^2\,\mathrm{d}\sigma=\dfrac{\pi R^4}{4}$。
- 整球 $\rho\le R$：$\displaystyle\iiint\rho^2\,\mathrm{d}V=\dfrac{4\pi R^5}{5}$。
- 单位球：$\displaystyle\iiint x^2\,\mathrm{d}V=\dfrac{4\pi}{15}$，$\displaystyle\iiint(x^2+y^2)\,\mathrm{d}V=\dfrac{8\pi}{15}$。
- 椭球 $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}+\dfrac{z^2}{c^2}\le1$：$V=\dfrac{4\pi abc}{3}$，$\displaystyle\iiint x^2\,\mathrm{d}V=\dfrac{4\pi abc}{15}a^2$。
- 圆锥体积 $\frac13\pi r^2h$，球体积 $\frac43\pi R^3$。

---

# 八、曲线积分与曲面积分（11 篇）

## 8.1 🔴 第一类曲线积分（对弧长）

$$\int_L f(x,y)\,\mathrm{d}s.$$

| 曲线给法 | 化法 |
|---|---|
| $y=y(x)$ | $\displaystyle\int_a^bf(x,y(x))\sqrt{1+y'^2}\,\mathrm{d}x$ |
| 参数 $x=x(t),y=y(t)$ | $\displaystyle\int_\alpha^\beta f(x(t),y(t))\sqrt{x'^2+y'^2}\,\mathrm{d}t$ |
| 空间曲线 $x=x(t),y=y(t),z=z(t)$ | $\displaystyle\int_\alpha^\beta f\sqrt{x'^2+y'^2+z'^2}\,\mathrm{d}t$ |
| 极坐标 $r=r(\theta)$ | $\displaystyle\int_{\theta_1}^{\theta_2}f(r\cos\theta,r\sin\theta)\sqrt{r^2+r'^2}\,\mathrm{d}\theta$ |

⚠️ 参数范围取 $\alpha<\beta$（下限小于上限），保证 $\mathrm{d}s>0$；第一类积分**与方向无关**。曲线方程是恒等式，可**直接代入**被积函数。

## 8.2 🔴 第二类曲线积分（对坐标）

$$\int_L P\,\mathrm{d}x+Q\,\mathrm{d}y.$$

参数化：$\displaystyle\int_\alpha^\beta\left(Px'+Qy'+Rz'\right)\mathrm{d}t$，$t$ 从起点参数积到终点参数。

两类关系：$\displaystyle\int_L P\,\mathrm{d}x+Q\,\mathrm{d}y+R\,\mathrm{d}z=\int_L(P\cos\alpha+Q\cos\beta+R\cos\gamma)\,\mathrm{d}s$，其中 $(\cos\alpha,\cos\beta,\cos\gamma)=\dfrac{(x',y',z')}{\sqrt{x'^2+y'^2+z'^2}}$ 是**有向**切线方向余弦。

⚠️ 第二类积分**与方向有关**：反向变号；$\mathrm{d}x$ 可正可负，遇绝对值按零点分段。

## 8.3 🔴 Green 公式与路径无关

**Green**：$L$ 为分段光滑**正向**（逆时针）闭曲线，$P,Q$ 在 $D$ 上有连续一阶偏导，则

$$\oint_L P\,\mathrm{d}x+Q\,\mathrm{d}y=\iint_D\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right)\mathrm{d}x\mathrm{d}y.$$

- **非闭曲线**：先补线凑闭 → Green → **减去补线积分**。
- **挖洞三步**（旋度为 $0$ 但 $L$ 内有奇点）：① 取 $L$ 内包围奇点的**同形**小闭曲线 $L_1$，使分母在 $L_1$ 上为常数；② 环域 Green：$\oint_L+\oint_{L_1}=0$（$L$ 逆、$L_1$ 顺）⇒ $\oint_L=\oint_{-L_1}$；③ 在 $-L_1$（逆时针）上参数化算值。
- **路径无关**（单连通域内）：$Q_x=P_y$ $\Leftrightarrow$ $\oint_L P\mathrm{d}x+Q\mathrm{d}y=0$ $\Leftrightarrow$ 存在 $u$ 使 $\mathrm{d}u=P\mathrm{d}x+Q\mathrm{d}y$。
- 求原函数：**凑微分首选**，常用 $\mathrm{d}\dfrac{y}{x}=\dfrac{x\mathrm{d}y-y\mathrm{d}x}{x^2}$、$\mathrm{d}\ln\dfrac{y}{x}=\dfrac{x\mathrm{d}y-y\mathrm{d}x}{xy}$、$\mathrm{d}\arctan\dfrac{y}{x}=\dfrac{x\mathrm{d}y-y\mathrm{d}x}{x^2+y^2}$；**折线积分保底**：

$$u(x,y)=\int_{x_0}^{x}P(t,y_0)\,\mathrm{d}t+\int_{y_0}^{y}Q(x,t)\,\mathrm{d}t.$$

⚠️ Green 前先确认：闭曲线、正向、$P,Q$ 在**整个内部**有连续偏导；有奇点必须挖洞。

## 8.4 🔴 第一类曲面积分（对面积）

$$\iint_\Sigma f(x,y,z)\,\mathrm{d}S.$$

| 曲面给法 | 化法 |
|---|---|
| $z=z(x,y)$ | $\displaystyle\iint_{D_{xy}}f(x,y,z(x,y))\sqrt{1+z_x^2+z_y^2}\,\mathrm{d}x\mathrm{d}y$ |
| 球面 $x^2+y^2+z^2=R^2$ | $\mathrm{d}S=R^2\sin\varphi\,\mathrm{d}\varphi\,\mathrm{d}\theta$ |
| 柱面 $x^2+y^2=R^2$ | $\mathrm{d}S=R\,\mathrm{d}\theta\,\mathrm{d}z$ |

⚠️ 投影时"曲面在坐标面上的投影区域"要算对；球面用球坐标最省。

## 8.5 🔴 第二类曲面积分（对坐标）

$$\iint_\Sigma P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y.$$

**合一投影**（$z=z(x,y)$，取上侧）：

$$\iint_\Sigma P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iint_{D_{xy}}\left(-Pz_x-Qz_y+R\right)\mathrm{d}x\mathrm{d}y.$$

**两类关系**：$\displaystyle\iint_\Sigma P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iint_\Sigma(P\cos\alpha+Q\cos\beta+R\cos\gamma)\,\mathrm{d}S$。

**方向余弦**（$z=z(x,y)$ 取上侧）：$(\cos\alpha,\cos\beta,\cos\gamma)=\dfrac{(-z_x,-z_y,1)}{\sqrt{1+z_x^2+z_y^2}}$，$\mathbf n\,\mathrm{d}S=(-z_x,-z_y,1)\,\mathrm{d}x\mathrm{d}y$。

⚠️ 口诀"一投二代三定号"：投 $D_{xy}$ → 全代成 $x,y$ → 上侧 $+$、下侧 $-$（整体变号）。

## 8.6 🔴 Gauss 公式（补面）

$\Sigma$ 为分片光滑**外侧**闭曲面，$P,Q,R$ 有连续一阶偏导：

$$\oiint_\Sigma P\,\mathrm{d}y\mathrm{d}z+Q\,\mathrm{d}z\mathrm{d}x+R\,\mathrm{d}x\mathrm{d}y=\iiint_\Omega\left(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}\right)\mathrm{d}V.$$

**补面三步**：① 补一块简单曲面 $\Sigma_1$，使 $\Sigma+\Sigma_1$ 封闭且**整体取外侧**；② 对封闭曲面用 Gauss；③ **减去**补的那块 $\iint_{\Sigma_1}$。

⚠️ 补面方向要与原曲面**配成整个闭曲面的外侧**——二者可以相反（如上半球面取上侧，底面圆盘要取下侧）；"减去补面"是最常见漏项。含 $1/r^k$ 的奇点不能直接套，需挖小球。

## 8.7 🔴 Stokes 公式与散度旋度

$\Gamma$ 为分段光滑闭曲线，$\Sigma$ 以 $\Gamma$ 为边界，方向按**右手法则**：

$$\oint_\Gamma P\,\mathrm{d}x+Q\,\mathrm{d}y+R\,\mathrm{d}z=\iint_\Sigma\begin{vmatrix}\mathrm{d}y\mathrm{d}z&\mathrm{d}z\mathrm{d}x&\mathrm{d}x\mathrm{d}y\\ \frac{\partial}{\partial x}&\frac{\partial}{\partial y}&\frac{\partial}{\partial z}\\ P&Q&R\end{vmatrix}.$$

**散度**：$\operatorname{div}\mathbf F=\dfrac{\partial P}{\partial x}+\dfrac{\partial Q}{\partial y}+\dfrac{\partial R}{\partial z}$。

**旋度**：

$$\operatorname{curl}\mathbf F=\left(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z},\ \frac{\partial P}{\partial z}-\frac{\partial R}{\partial x},\ \frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right).$$

⚠️ Stokes 的方向按右手法则；旋度三个分量**不要背错顺序**。

**常旋度速算**：$\operatorname{curl}\mathbf F$ 为常向量、$\Sigma$ 为平面块时，$\displaystyle\iint_\Sigma\operatorname{curl}\mathbf F\cdot\mathbf n\,\mathrm{d}S=(\operatorname{curl}\mathbf F\cdot\mathbf n)\,S_\Sigma$。

## 8.8 🟡 常用 dS 与对称性

| 曲面 | $\mathrm{d}S$ | 备注 |
|---|---|---|
| $z=z(x,y)$ | $\sqrt{1+z_x^2+z_y^2}\,\mathrm{d}x\mathrm{d}y$ | 通式，投影到 $xOy$ |
| 平面 $z=ax+by+c$ | $\sqrt{1+a^2+b^2}\,\mathrm{d}x\mathrm{d}y$ | 常数因子 |
| 球面 $x^2+y^2+z^2=R^2$ | $\dfrac{R}{\lvert z\rvert}\,\mathrm{d}x\mathrm{d}y$ | 上半球取 $R/z$ |
| 柱面 $x^2+y^2=R^2$ | $\dfrac{R}{\lvert x\rvert}\,\mathrm{d}y\mathrm{d}z$ | 投到 $yOz$ |
| 锥面 $z=\sqrt{x^2+y^2}$ | $\sqrt{2}\,\mathrm{d}x\mathrm{d}y$ | 常数因子 |

- 积分区域关于 $xOy$ 面对称，被积函数对 $z$ 奇 → 三重积分为 $0$；偶 → 乘 $2$。
- 第一类曲面积分：曲面关于 $xOy$ 面对称，$f$ 对 $z$ 奇 → 积分为 $0$。
- 轮换对称：对象在 $x\to y\to z$ 下不变 ⇒ $\int x^2=\int y^2=\int z^2=\frac13\int(x^2+y^2+z^2)$。
- **代方程**：曲线/曲面方程是恒等式，可直接代入被积函数；**重积分区域内部的边界方程不可代**。
- **方向余弦技巧**（上半球面取上侧）：球面 $x^2+y^2+z^2=a^2$ 外法向 $\cos\gamma=\dfrac{z}{a}$，故 $\displaystyle\iint_\Sigma z\,\mathrm{d}S=a\iint_\Sigma\cos\gamma\,\mathrm{d}S=a\iint_{D_{xy}}\mathrm{d}x\mathrm{d}y$。
- **平面平方差**：$x+y+z=c$ 上 $xy+yz+zx=\dfrac{c^2-(x^2+y^2+z^2)}{2}$。

---

# 九、无穷级数（12 篇）

## 9.1 🔴 三把标尺（判敛的终点）

| 标尺 | 敛散性 | 和 / 提示 |
|---|---|---|
| 几何级数 $\sum\limits_{n=0}^{\infty}q^n$ | $\lvert q\rvert<1$ 收敛；$\lvert q\rvert\ge1$ 发散 | 和 $=\dfrac{1}{1-q}$ |
| $p$ 级数 $\sum\limits_{n=1}^{\infty}\dfrac{1}{n^p}$ | $p>1$ 收敛；$p\le1$ 发散 | $p=1$ 即调和级数 |
| 对数标尺 $\sum\limits_{n=2}^{\infty}\dfrac{1}{n(\ln n)^p}$ | $p>1$ 收敛；$p\le1$ 发散 | $\sum\frac{1}{n\ln n}$ 发散、$\sum\frac{1}{n\ln^2n}$ 收敛 |

**必要条件**：$\sum a_n$ 收敛 $\Rightarrow a_n\to0$；反之不成立（$a_n\to0$ 只是入场券）。

## 9.2 🔴 正项级数三大判别法

| 判别法 | 公式 | 结论 / 坑 |
|---|---|---|
| 比较（极限形式） | $\lim\dfrac{a_n}{b_n}=c$ | $0<c<\infty$ 同敛散；$c=0$ 时 $\sum b_n$ 收敛 ⇒ $\sum a_n$ 收敛 |
| 比值 | $\lim\dfrac{a_{n+1}}{a_n}=\rho$ | $\rho<1$ 收敛，$\rho>1$ 发散，$\rho=1$ **失效** |
| 根值 | $\lim\sqrt[n]{a_n}=\rho$ | 同比值；连乘积/整体幂优先 |

**增长阶（判主部）**：

$$\ln n\ll n^p\ (p>0)\ll a^n\ (a>1)\ll n!\ll n^n.$$

**常用极限**：$\lim\limits_{n\to\infty}\sqrt[n]{n}=1$，$\lim\limits_{n\to\infty}\left(1+\frac1n\right)^n=e$，$\dfrac{\sqrt[n]{n!}}{n}\to\dfrac1e$。

**等价包裹（把怪通项扒成 $\frac{c}{n^p}$）**：$\sin\dfrac{1}{n^\alpha}\sim\dfrac{1}{n^\alpha}$，$\ln\left(1+\dfrac{1}{n^\alpha}\right)\sim\dfrac{1}{n^\alpha}$，$1-\cos\dfrac{1}{n^\alpha}\sim\dfrac{1}{2n^{2\alpha}}$。

## 9.3 🟡 放缩纪律与常用不等式

- **方向**：证收敛往**大**放（放到接得上收敛标尺）；证发散往**小**缩（缩到仍发散）。方向反了全题作废。
- **积分放缩**（$f$ 单调递减）：$\displaystyle\int_n^{n+1}f(x)\,\mathrm{d}x\le f(n)\le\int_{n-1}^{n}f(x)\,\mathrm{d}x$。先声明单调性（评分点）。
- 常用：$\dfrac{x}{1+x}\le\ln(1+x)\le x\ (x>-1)$；若用二次估计，$x-\dfrac{x^2}{2}\le\ln(1+x)\le x$ **仅对 $x\ge0$ 成立**；$\sin x\le x\ (x\ge0)$；$1-\cos x\le\dfrac{x^2}{2}$。

## 9.4 🔴 交错级数与绝对/条件收敛

- **Leibniz**：$u_n$ 单调递减且 $u_n\to0$ ⇒ $\sum(-1)^{n-1}u_n$ 收敛；余项 $\lvert R_N\rvert\le u_{N+1}$。
- **绝对收敛**：$\sum\lvert a_n\rvert$ 收敛 ⇒ $\sum a_n$ 收敛。
- **条件收敛**：$\sum a_n$ 收敛但 $\sum\lvert a_n\rvert$ 发散；模板 = Leibniz 证收敛 + 去绝对值证发散（往小缩到 $\frac{C}{n}$）。
- 样板：$\sum\limits_{n=1}^{\infty}\dfrac{(-1)^{n-1}}{n}=\ln2$（条件收敛）。

⚠️ 条件收敛级数**不可随意拆项、重排**；Leibniz 的单调性要写"来路"（积分式/递推式），常占 1–2 分。

## 9.5 🟡 裂项（望远镜）求和

$$\frac{1}{n(n+1)}=\frac1n-\frac1{n+1},\qquad \frac{1}{n(n+2)}=\frac12\left(\frac1n-\frac1{n+2}\right),$$

$$\frac{k}{(k+1)!}=\frac1{k!}-\frac1{(k+1)!},\qquad \frac{1}{\sqrt n+\sqrt{n+1}}=\sqrt{n+1}-\sqrt n.$$

模板：$a_n=b_n-b_{n+1}$ ⇒ $S_N=b_1-b_{N+1}$，和 $=b_1-\lim\limits_{N\to\infty}b_{N+1}$。

**递推型级数求和**：先证 $x_n\downarrow0$，再找 $g$ 使 $x_n=g(x_n)-g(x_{n+1})$（如 $g(t)=\dfrac{t}{1-t}$ 型），折叠取极限。

$$\arctan\frac{1}{n^2+n+1}=\arctan(n+1)-\arctan n.$$

⚠️ $\frac{1}{n(n+2)}$ 型首尾各留 2 项；尾巴极限要单独交代。

## 9.6 🟡 特殊点取值卡（数项级数 → 展开值）

| 级数 | 和 |
|---|---|
| $\sum\limits_{n=0}^{\infty}\dfrac{1}{n!}$ | $e$ |
| $\sum\limits_{n=1}^{\infty}\dfrac{1}{n2^n}$ | $\ln2$ |
| $\sum\limits_{n=1}^{\infty}\dfrac{(-1)^{n-1}}{n}$ | $\ln2$ |
| $\sum\limits_{n=1}^{\infty}\dfrac{(-1)^{n-1}}{n2^n}$ | $\ln\dfrac32$ |
| $\sum\limits_{n=1}^{\infty}\dfrac{(-1)^{n-1}}{n3^n}$ | $\ln\dfrac43$ |
| $\sum\limits_{n=1}^{\infty}\dfrac{(-1)^{n-1}}{2n-1}$ | $\dfrac{\pi}{4}$ |
| $\sum\limits_{n=1}^{\infty}\dfrac{n}{2^n}$ | $2$ |
| $\sum\limits_{n=1}^{\infty}\dfrac{n^2}{2^n}$ | $6$ |

⚠️ 三个 $\ln$ 别背混：$x=-\frac12\to\ln2$，$x=\frac12\to\ln\frac32$，$x=\frac13\to\ln\frac43$。

---

# 十、幂级数与傅里叶级数（13 篇）

## 10.1 🔴 收敛半径、收敛区间、收敛域

**Abel 三段**：$\lvert x-x_0\rvert<R$ 绝对收敛；$\lvert x-x_0\rvert>R$ 发散；$\lvert x-x_0\rvert=R$ 两端**分别代入**另判。

**半径公式**：

$$R=\lim_{n\to\infty}\left\lvert\frac{a_n}{a_{n+1}}\right\rvert=\frac{1}{\lim\limits_{n\to\infty}\sqrt[n]{\lvert a_n\rvert}}.$$

- **缺项型**（只有 $x^{2n}$、$x^{3n}$）：换元 $y=(x-x_0)^k$ 化标准型，或直接对通项用根值法解 $\sqrt[n]{\lvert u_n(x)\rvert}<1$。
- 三个名字：半径 $R$ 是数；收敛区间 $(x_0-R,x_0+R)$ 是开区间；收敛域 = 收敛区间 ∪ 收敛端点。
- 逐项求导/积分：半径不变，**端点可能改变**，求完和函数回头重验。

⚠️ 问"收敛域"必须逐端点交代，两端可一敛一散；机械套比值公式会在零系数处除以零。

## 10.2 🔴 基本展开式（连区间一起背）

| 展开式 | 区间 |
|---|---|
| $\dfrac{1}{1-x}=\sum\limits_{n=0}^{\infty}x^n$ | $\lvert x\rvert<1$ |
| $e^x=\sum\limits_{n=0}^{\infty}\dfrac{x^n}{n!}$ | $(-\infty,+\infty)$ |
| $\sin x=\sum\limits_{n=0}^{\infty}\dfrac{(-1)^nx^{2n+1}}{(2n+1)!}$ | $(-\infty,+\infty)$ |
| $\cos x=\sum\limits_{n=0}^{\infty}\dfrac{(-1)^nx^{2n}}{(2n)!}$ | $(-\infty,+\infty)$ |
| $\ln(1+x)=\sum\limits_{n=1}^{\infty}\dfrac{(-1)^{n-1}x^n}{n}$ | $-1<x\le1$ |
| $(1+x)^\alpha=\sum\limits_{n=0}^{\infty}\dbinom{\alpha}{n}x^n$ | $\lvert x\rvert<1$ |
| $\arctan x=\sum\limits_{n=0}^{\infty}\dfrac{(-1)^nx^{2n+1}}{2n+1}$ | $-1\le x\le1$ |

**赠品**：$\dfrac{1}{1+x}=\sum(-1)^nx^n\ (\lvert x\rvert<1)$；$\ln(1-x)=-\sum\dfrac{x^n}{n}\ (-1\le x<1)$；$\ln\dfrac{1+x}{1-x}=2\sum\limits_{n=0}^{\infty}\dfrac{x^{2n+1}}{2n+1}\ (\lvert x\rvert<1)$。

⚠️ 区间错 = 白展开：$\ln(1+x)$ 右端闭、左端开；$\arctan x$ 两端闭。

## 10.3 🔴 求和函数三招

| 信号 | 动作 |
|---|---|
| 系数含 $n$ | **逐项求导**：先提 $x^p$ 对齐 → $S'(x)$ 套 $\frac{1}{(1-x)^2}$ → 积回 $S(x)=\int_0^xS'(t)\mathrm{d}t+S(0)$ |
| 系数含 $\frac1n$ | **逐项积分**：乘/除 $x$ 配平索引 → $\int_0^xS(t)\mathrm{d}t$ 化几何级数 → 求导还原 → 补洞 |
| 多项式 ÷ 阶乘 | **索引平移 + 拆项**：令 $m=n+1$，分子写成 $m(m-1)(m-2)+\cdots$ 的组合 → 逐块套 $e^t$ |

**和函数口诀表（$\lvert x\rvert<1$）**：

$$\sum_{n=0}^{\infty}x^n=\frac{1}{1-x},\qquad \sum_{n=1}^{\infty}nx^{n-1}=\frac{1}{(1-x)^2},\qquad \sum_{n=1}^{\infty}nx^n=\frac{x}{(1-x)^2},$$

$$\sum_{n=1}^{\infty}n^2x^n=\frac{x(1+x)}{(1-x)^3},\qquad \sum_{n=1}^{\infty}n(n+1)x^n=\frac{2x}{(1-x)^3},\qquad \sum_{n=1}^{\infty}\frac{x^n}{n}=-\ln(1-x).$$

**补洞版**：$\sum\limits_{n=0}^{\infty}\dfrac{x^n}{n+1}=\dfrac{-\ln(1-x)}{x}$（$x$ ≠ 0），$S(0)=1$。

⚠️ $S(0)$ 这个常数必须补；除过 $x$ 的要补 $x=0$ 的洞；$\sum n^2x^n$ 配 $(1-x)^3$。

## 10.4 🔴 傅里叶级数

**系数**（$[-l,l]$，周期 $2l$）：

$$a_n=\frac1l\int_{-l}^{l}f(x)\cos\frac{n\pi x}{l}\,\mathrm{d}x\ (n\ge0),\qquad b_n=\frac1l\int_{-l}^{l}f(x)\sin\frac{n\pi x}{l}\,\mathrm{d}x\ (n\ge1).$$

**级数**：

$$f(x)\sim\frac{a_0}{2}+\sum_{n=1}^{\infty}\left(a_n\cos\frac{n\pi x}{l}+b_n\sin\frac{n\pi x}{l}\right).$$

**Dirichlet 收敛定理**：$f$ 在 $[-l,l]$ 分段光滑 ⇒ 级数处处收敛，在 $x$ 处收敛于 $\dfrac{f(x^-)+f(x^+)}{2}$。

**三档报值**：连续点 $f(x_0)$；第一类间断点 $\dfrac{f(x_0^-)+f(x_0^+)}{2}$；端点 $\pm l$：$\dfrac{f(l^-)+f(-l^+)}{2}$。

**奇偶延拓**：奇延拓 → 正弦级数（只剩 $b_n$）；偶延拓 → 余弦级数（只剩 $a_n$）。

⚠️ 首项写 $\dfrac{a_0}{2}$ 不是 $a_0$；端点值是"跨周期接上"的左右平均，不是 $f(l)$；周期 $2\pi$ 时 $l=\pi$。

## 10.5 ⚪ 函数项级数（两条 + 一条放弃说明）

- **收敛域**：使 $\sum u_n(x_0)$ 收敛的一切 $x_0$；把 $x$ 当参数，逐段用数项级数判别法。
- **和函数**：$S(x)=\sum u_n(x)$，定义在收敛域上；$u_n=a_n(x-x_0)^n$ 时就是幂级数。
- 一致收敛、Abel/Dirichlet 级数判别法属数学专业内容，非数学 A 类不考——战略放弃。

---

# 十一、最后一眼：最容易错的 30 个点

> 考前 10 分钟扫这一页。每一条都是"会做但写错"的失分点，不是不会做。

1. $(\cos x)'=-\sin x$，$(\arccos x)'=-\dfrac{1}{\sqrt{1-x^2}}$，$(\operatorname{arccot}x)'=-\dfrac{1}{1+x^2}$——**三个负号**。
2. $\displaystyle\int\frac{\mathrm{d}x}{x}=\ln\lvert x\rvert+C$，不是 $\ln x$。
3. $1-\cos x\sim\dfrac{x^2}{2}$，不是 $x^2$；$(1+x)^\alpha-1\sim\alpha x$，不是 $x$。
4. $\log_a(1+x)\sim\dfrac{x}{\ln a}$，$\ln a$ 在**分母**。
5. $\ln(1+x)$ 的泰勒是**交错**的：$x-\frac{x^2}{2}+\frac{x^3}{3}-\cdots$。
6. 洛必达只对 $\frac00,\frac{\infty}{\infty}$；导数比不存在 **不能** 反推原极限不存在。
7. $1^\infty$ 的结果是 $e^{\lim g(f-1)}$，别写成 $1$，别漏外面的 $e$。
8. 变限积分上限是函数时，**链式因子**不能丢。
9. 参数方程二阶导：$\dfrac{y''x'-y'x''}{(x')^3}$，不是 $\dfrac{y''}{x''}$。
10. 隐函数公式要求 $F_z$ ≠ 0；求 $F_x$ 时 $y,z$ 全当常数。
11. 方向导数先把方向向量**单位化**。
12. 二元极值先算 $AC-B^2$，再谈 $A$ 的符号；$AC-B^2=0$ 失效。
13. 闭区域最值：驻点、不可导点、**边界**、角点，一个都不能漏。
14. 极坐标 $\mathrm{d}x\mathrm{d}y=r\,\mathrm{d}r\mathrm{d}\theta$；球坐标 $\mathrm{d}V=\rho^2\sin\varphi\,\mathrm{d}\rho\,\mathrm{d}\varphi\,\mathrm{d}\theta$。
15. 二重积分换序：内层上下限只能含外层变量。
16. 轮换对称要求区域在变量交换下**不变**；三角形 $0\le y\le x\le1$ 不轮换。
17. Green 公式：$L$ 取**正向**（逆时针），$\displaystyle\oint_L P\,\mathrm{d}x+Q\,\mathrm{d}y=\iint_D(Q_x-P_y)\,\mathrm{d}x\mathrm{d}y$。
18. Green 挖洞：内边界取**顺时针**，挖洞部分要**减**。
19. Gauss 公式：$\Sigma$ 取**外侧**；补面时"补的那块要减掉"。
20. Stokes 公式：方向按**右手法则**；$\operatorname{curl}\mathbf F=(R_y-Q_z,\ P_z-R_x,\ Q_x-P_y)$。
21. 散度：$\operatorname{div}\mathbf F=P_x+Q_y+R_z$。
22. $p$ 级数 $\sum\frac{1}{n^p}$：$p>1$ 收敛；$\int_1^\infty\frac{1}{x^p}$：$p>1$ 收敛；$\int_0^1\frac{1}{x^p}$：$p<1$ 收敛——**三段别混**。
23. 几何级数从 $n=0$ 起：$\sum q^n=\dfrac{1}{1-q}$（$\lvert q\rvert<1$）；从 $n=1$ 起要乘 $q$。
24. 收敛半径 $R$ 是数；**端点必须单独代入**判敛散。
25. 傅里叶首项写 $\dfrac{a_0}{2}$，不是 $a_0$；Dirichlet 收敛值是 $\dfrac{f(x^-)+f(x^+)}{2}$。
26. ODE 问"通解"必须带 $C$；分离变量除过的因子要回头查**丢解**。
27. 二阶非齐次特解：右端是特征根时**乘 $x^k$**，这是最经典失分点。
28. 欧拉方程令 $x=e^t$：$xy'=\dot y$，$x^2y''=\ddot y-\dot y$。
29. 线面夹角用 $\sin$，面面/线线夹角用 $\cos$，全部带绝对值。
30. 投影曲线必须补坐标面（如 $z=0$）；"缺谁平行谁"的柱面别认错。

---

# 结语：把这张单子折好，放进考场包

🐱 喵～写到这里，该背的公式、该记的套路、该防的坑，都在这一篇里了。

**最后三句嘱咐**：

1. **考前只扫单子，不碰新题**——这张单子的存在意义，是让你在考场上"提笔就有"。
2. **填空先保零失误**——每题做完回代/验算 10 秒，比多抢一道大题更值钱。
3. **大题写台阶**——换元、公式、辅助函数，写出来就是分；空题才是唯一的 0 分。

明天 9:00，带着这张单子和一年的底气上场。你已经把能准备的都准备好了，剩下的就是**稳、准、快**。加油喵！🐱📚

> 💡 **本单使用建议**：
> 1. 今天先按 §〇 的 12 条默写一遍，写不出来的回对应节补；
> 2. 明天早上进考场前，只看 §十一 的 30 条；
> 3. 考完回来告诉我哪条"背了但没用上/没背却考了"，我再帮你更新下一版。
