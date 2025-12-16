# 🧮 Calculus II Final Formula Sheet

## Section 1: Integration, Parametric, & Polar

### **Standard Antiderivatives**
* $\int \sec(x)\tan(x) \, dx = \sec(x) + C$
* $\int \csc(x)\cot(x) \, dx = -\csc(x) + C$
* $\int \tan(x) \, dx = \ln|\sec(x)| + C$
* $\int \sec(x) \, dx = \ln|\sec(x) + \tan(x)| + C$
* $\int \csc(x) \, dx = -\ln|\csc(x) + \cot(x)| + C$

---

### **Parametric & Polar Operations**

| Feature | Parametric ($x=f(t), y=g(t)$) | Polar ($r=f(\theta)$) |
| :--- | :--- | :--- |
| **Tangent Slope** | $\frac{dy/dt}{dx/dt}$ | $\frac{\frac{dr}{d\theta}\sin\theta + r\cos\theta}{\frac{dr}{d\theta}\cos\theta - r\sin\theta}$ |
| | **Operation:** Divide $y'$ by $x'$. | **Operation:** Use product rule on $x=r\cos\theta, y=r\sin\theta$. |
| **Arc Length** | $\int \sqrt{(\frac{dx}{dt})^2 + (\frac{dy}{dt})^2} \, dt$ | $\int \sqrt{r^2 + (\frac{dr}{d\theta})^2} \, d\theta$ |
| | **Operation:** Square 1st derivatives, sum, and root. | **Operation:** Sum $r^2$ and $(r')^2$, then root. |
| **Area ($A$)** | *Varies by boundary* | $\int \frac{1}{2} [r(\theta)]^2 \, d\theta$ |
| | | **Operation:** Square the function $r$ before integrating. |

---

## ♾️ Section 2: Infinite Series

### **Known Maclaurin Series**
# 🧮 Calculus II Final Formula Sheet

## ♾️ Section 2: Infinite Series

### **Known Maclaurin Series**

| Function $f(x)$ | Maclaurin Series $\sum_{n=0}^\infty c_n x^n$ | ROC ($R$) | I.O.C. |
| :--- | :--- | :--- | :--- |
| $\frac{1}{1-x}$ | $\sum_{n=0}^\infty x^n = 1 + x + x^2 + \dots$ | $R = 1$ | $(-1, 1)$ |
| $e^x$ | $\sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \dots$ | $R = \infty$ | $(-\infty, \infty)$ |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $R = \infty$ | $(-\infty, \infty)$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $R = \infty$ | $(-\infty, \infty)$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $R = 1$ | $(-1, 1]$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $R = 1$ | $[-1, 1]$ |
| $(1+x)^k$ | $\sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \dots$ | $R = 1$ | $(-1, 1)$ |

---

### **Convergence Testing Strategy**
1. **$n$-th Term Test:** If $\lim_{n \to \infty} a_n \neq 0$, the series **diverges**.
2. **Ratio Test:** Used for factorials and powers. $L = \lim_{n \to \infty} |\frac{a_{n+1}}{a_n}|$.
   * $L < 1$: Absolute Convergence
   * $L > 1$: Divergence
   * $L = 1$: Inconclusive (Try Integral or Comparison Test).
3. **Alternating Series Test (AST):** If $b_n$ is decreasing and $\lim_{n \to \infty} b_n = 0$, the alternating series converges.



---

## 🧊 Section 3: 3D Geometry & Vectors

### **Vector Operations**

* **Dot Product:** $\vec{u} \cdot \vec{v} = |\vec{u}||\vec{v}|\cos(\theta)$
* **Cross Product Magnitude:** $|\vec{u} \times \vec{v}| = |\vec{u}||\vec{v}|\sin(\theta)$
* **Work:** $W = \vec{F} \cdot \vec{D} = |\vec{F}||\vec{D}|\cos(\theta)$
| Function $f(x)$ | Maclaurin Series $\sum_{n=0}^\infty c_n x^n$ | I.O.C. |
| :--- | :--- | :--- |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $(-\infty, \infty)$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $(-\infty, \infty)$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $(-1, 1]$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $[-1, 1]$ |
| $(1+x)^k$ | $\sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \dots$ | $(-1, 1)$ |

---

## 🧊 Section 3: 3D Geometry & Vectors

### **Vector Operations**

* **Angle between Vectors:** $$\cos(\theta) = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}||\vec{v}|}$$

* **Vector Projection:** $$\text{proj}_{\vec{u}}(\vec{v}) = \left( \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|^2} \right) \vec{u}$$

* **Dot Product:** $$\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + u_3v_3$$

* **Cross Product Magnitude:** $$|\vec{u} \times \vec{v}| = |\vec{u}||\vec{v}|\sin(\theta)$$
