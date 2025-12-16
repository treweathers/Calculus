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


# 🧮 Calculus II Final Formula Sheet
## Section 1: Integration, Parametric, & Polar
### **Standard Antiderivatives**
* **∫ sec(x)tan(x) dx** = sec(x) + C
* **∫ csc(x)cot(x) dx** = -csc(x) + C
* **∫ tan(x) dx** = ln|sec(x)| + C
* **∫ sec(x) dx** = ln|sec(x) + tan(x)| + C
* **∫ csc(x) dx** = -ln|csc(x) + cot(x)| + C

---

### **Parametric & Polar Operations**
| Feature | Parametric (x=f(t), y=g(t)) | Polar (r=f(\theta)) |
| --- | --- | --- |
| **Tangent Slope** | `(dy/dt) / (dx/dt)` | `[(dr/dθ)sinθ + rcosθ] / [(dr/dθ)cosθ - rsinθ]` |
|  | **Operation:** Divide 1st degree derivative of **y** by 1st degree derivative of **x**. | **Operation:** Combine 1st degree derivative of **r** and original function **r**. |
| **Arc Length** | `∫ √[(dx/dt)² + (dy/dt)²] dt` | `∫ √[r² + (dr/dθ)²] dθ` |
|  | **Operation:** Square 1st degree derivatives, sum them, and square root. | **Operation:** Sum the square of **r** and the square of its 1st degree derivative. |
| **Area (A)** | *Varies by boundary* | `∫ 1/2 [r(θ)]² dθ` |
|  |  | **Operation:** Square the function **r** before integrating. |


---

## ♾️ Section 2: Infinite Series
### **Known Maclaurin Series**

| Function $f(x)$ | Maclaurin Series $\sum_{n=0}^\infty c_n x^n$ | I.O.C. |
| :--- | :--- | :--- |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $(-\infty, \infty)$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $(-\infty, \infty)$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $(-1, 1]$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $[-1, 1]$ |
| $(1+x)^k$ (Binomial) | **$\sum_{n=0}^\infty \binom{k}{n} x^n = 1 + kx + \frac{k(k-1)}{2!}x^2 + \dots$** | **$(-1, 1)$**$^\dagger$ |

---

## 🧊 Section 3: 3D Geometry & Vectors
### **Vector Operations**
* **Angle between Vectors:** cos(θ) = (u · v) / (|u||v|)
* **Vector Projection:** proj_u(v) = [(u · v) / |u|²] * u

---
