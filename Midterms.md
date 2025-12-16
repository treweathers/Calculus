# Calculus II Solutions and Practice

## Part 1: Solutions to Original Problems

---

### Problem 1: Limits
**(a)** $\lim_{x \to 0} \frac{x - \sin x}{x - \tan x}$
1. Plug in $x=0$: This results in the indeterminate form $\frac{0}{0}$. Apply **L'Hôpital's Rule**.
2. Differentiate the numerator and denominator: $\lim_{x \to 0} \frac{1 - \cos x}{1 - \sec^2 x}$.
3. Still $\frac{0}{0}$. Apply L'Hôpital again: $\lim_{x \to 0} \frac{\sin x}{-2\sec^2 x \tan x}$.
4. Simplify the expression using $\tan x = \frac{\sin x}{\cos x}$: 
   $\lim_{x \to 0} \frac{\sin x}{-2 \cdot \frac{1}{\cos^2 x} \cdot \frac{\sin x}{\cos x}} = \lim_{x \to 0} -\frac{\cos^3 x}{2}$.
5. Substitute $x=0$: $-\frac{1^3}{2} = \mathbf{-\frac{1}{2}}$.

**(b)** $\lim_{x \to 1^+} \ln x \tan\left(\frac{\pi x}{2}\right)$
1. This is form $0 \cdot (-\infty)$. Rewrite as $\frac{\ln x}{\cot(\pi x / 2)}$ to obtain $\frac{0}{0}$.
2. Apply L'Hôpital's Rule: $\lim_{x \to 1^+} \frac{1/x}{-\frac{\pi}{2} \csc^2(\frac{\pi x}{2})}$.
3. As $x \to 1$, $\csc(\frac{\pi}{2}) = 1$.
4. Result: $\frac{1}{-\pi/2} = \mathbf{-\frac{2}{\pi}}$.

**(c)** $\lim_{x \to 0} \frac{\sin(x)\cos(2x)e^{3x}}{x^2 + x}$
1. Factor the denominator: $\lim_{x \to 0} \left( \frac{\sin x}{x} \cdot \frac{\cos(2x)e^{3x}}{x + 1} \right)$.
2. Recall the fundamental limit: $\lim_{x \to 0} \frac{\sin x}{x} = 1$.
3. Evaluate the remaining part by direct substitution: $\frac{\cos(0)e^0}{0+1} = \frac{1 \cdot 1}{1} = 1$.
4. Final Answer: $1 \cdot 1 = \mathbf{1}$.

---

### Problem 2: Trig Substitution
**Evaluate:** $\int \frac{dx}{x^2\sqrt{9 - x^2}}$
1. Let $x = 3\sin\theta$, which means $dx = 3\cos\theta d\theta$.
2. The radical becomes $\sqrt{9 - 9\sin^2\theta} = \sqrt{9\cos^2\theta} = 3\cos\theta$.
3. Substitute into the integral: $\int \frac{3\cos\theta d\theta}{(3\sin\theta)^2 (3\cos\theta)} = \int \frac{d\theta}{9\sin^2\theta} = \frac{1}{9} \int \csc^2\theta d\theta$.
4. Integrate: $-\frac{1}{9}\cot\theta + C$.
5. Back-substitute using a right triangle: Since $\sin\theta = \frac{x}{3}$, then $\cot\theta = \frac{\sqrt{9-x^2}}{x}$.
6. Final Answer: $\mathbf{-\frac{\sqrt{9-x^2}}{9x} + C}$.

---

### Problem 3: Trig Integral
**Evaluate:** $\int \sin^2 x \cos^3 x dx$
1. Separate one $\cos x$: $\int \sin^2 x \cos^2 x (\cos x dx)$.
2. Use the identity $\cos^2 x = 1 - \sin^2 x$: $\int \sin^2 x (1 - \sin^2 x) \cos x dx$.
3. Use $u$-substitution: Let $u = \sin x$, so $du = \cos x dx$.
4. The integral becomes: $\int u^2(1 - u^2) du = \int (u^2 - u^4) du$.
5. Integrate: $\frac{u^3}{3} - \frac{u^5}{5} + C$.
6. Final Answer: $\mathbf{\frac{\sin^3 x}{3} - \frac{\sin^5 x}{5} + C}$.

---

### Problem 4: Trig Substitution
**Evaluate:** $\int \frac{x^3}{\sqrt{x^2 + 4}} dx$
1. Let $x = 2\tan\theta$, so $dx = 2\sec^2\theta d\theta$ and $\sqrt{x^2+4} = 2\sec\theta$.
2. Substitute: $\int \frac{(2\tan\theta)^3}{2\sec\theta} (2\sec^2\theta d\theta) = 8 \int \tan^3\theta \sec\theta d\theta$.
3. Rewrite $\tan^3\theta$ as $(\sec^2\theta - 1)\tan\theta$: $8 \int (\sec^2\theta - 1) \sec\theta \tan\theta d\theta$.
4. Let $u = \sec\theta, du = \sec\theta \tan\theta d\theta$: $8 \int (u^2 - 1) du = 8(\frac{u^3}{3} - u) + C$.
5. Back-substitute $u = \frac{\sqrt{x^2+4}}{2}$: $\mathbf{\frac{(x^2+4)^{3/2}}{3} - 4\sqrt{x^2+4} + C}$.

---

### Problem 5: Partial Fractions
**Evaluate:** $\int \frac{5x + 1}{2x^2 - x - 1} dx$
1. Factor the denominator: $(2x+1)(x-1)$.
2. Setup partial fractions: $\frac{5x+1}{(2x+1)(x-1)} = \frac{A}{2x+1} + \frac{B}{x-1}$.
3. Solve for $A$ and $B$: $5x+1 = A(x-1) + B(2x+1)$.
   - Let $x=1$: $6 = 3B \implies B=2$.
   - Let $x=-1/2$: $-3/2 = A(-3/2) \implies A=1$.
4. Integrate: $\int (\frac{1}{2x+1} + \frac{2}{x-1}) dx = \mathbf{\frac{1}{2}\ln|2x+1| + 2\ln|x-1| + C}$.

---

### Problem 6: Improper Integral
**Evaluate:** $\int_0^4 \frac{\ln x}{\sqrt{x}} dx$
1. Improper at $x=0$: $\lim_{t \to 0^+} \int_t^4 x^{-1/2} \ln x dx$.
2. Use Integration by Parts: $u = \ln x, dv = x^{-1/2}dx \implies du = \frac{1}{x}dx, v = 2\sqrt{x}$.
3. Antiderivative: $2\sqrt{x}\ln x - \int 2\sqrt{x} \frac{1}{x} dx = 2\sqrt{x}\ln x - 4\sqrt{x}$.
4. Apply limits: $(2\sqrt{4}\ln 4 - 4\sqrt{4}) - \lim_{t \to 0^+} (2\sqrt{t}\ln t - 4\sqrt{t})$.
5. The limit $\lim_{t \to 0^+} 2\sqrt{t}\ln t$ is $0$ (via L'Hôpital's Rule).
6. Final Answer: $4\ln 4 - 8 = \mathbf{8\ln 2 - 8}$.

---

### Problem 7: Arc Length
**Evaluate:** $y = (x+4)^{3/2}, 0 \le x \le 4$
1. Differentiate: $y' = \frac{3}{2}(x+4)^{1/2}$.
2. Square the derivative: $(y')^2 = \frac{9}{4}(x+4)$.
3. Use the arc length formula: $L = \int_0^4 \sqrt{1 + \frac{9}{4}(x+4)} dx = \int_0^4 \sqrt{\frac{9}{4}x + 10} dx$.
4. Integrate: $[\frac{2}{3} \cdot \frac{4}{9} (\frac{9}{4}x + 10)^{3/2}]_0^4$.
5. Evaluate: $\mathbf{\frac{8}{27} [19^{3/2} - 10^{3/2}]}$.

---

### Problem 8: Parametric Tangent
**Evaluate:** $x = \sqrt{t}, y = t^2 - 2t$, at $t=1$
1. Find the point: $x(1) = 1, y(1) = -1$. Point: $(1, -1)$.
2. Find the slope $\frac{dy}{dx}$: $\frac{dy/dt}{dx/dt} = \frac{2t - 2}{1/(2\sqrt{t})} = 2\sqrt{t}(2t-2)$.
3. At $t=1$: Slope $m = 2\sqrt{1}(2(1)-2) = 0$.
4. Equation: $y - (-1) = 0(x - 1) \implies \mathbf{y = -1}$.

---

### Problem 9: Parametric Arc Length
**Evaluate:** $x = e^t - t, y = 4e^{t/2}, 0 \le t \le 2$
1. $x' = e^t - 1$ and $y' = 2e^{t/2}$.
2. Sum of squares: $(x')^2 + (y')^2 = (e^{2t} - 2e^t + 1) + 4e^t = e^{2t} + 2e^t + 1 = (e^t + 1)^2$.
3. $L = \int_0^2 \sqrt{(e^t+1)^2} dt = \int_0^2 (e^t + 1) dt$.
4. Integrate: $[e^t + t]_0^2 = (e^2 + 2) - (e^0 + 0) = \mathbf{e^2 + 1}$.

---

### Problem 10: Polar Area
**Evaluate:** $r = 2\cos\theta$ and $r = 2\sin\theta$
1. Find intersection: $2\cos\theta = 2\sin\theta \implies \tan\theta = 1 \implies \theta = \pi/4$.
2. The area is symmetric. Total Area = $2 \times \int_0^{\pi/4} \frac{1}{2} (2\sin\theta)^2 d\theta$.
3. Simplify: $\int_0^{\pi/4} 4\sin^2\theta d\theta = \int_0^{\pi/4} 2(1 - \cos 2\theta) d\theta$.
4. Integrate: $[2\theta - \sin 2\theta]_0^{\pi/4} = (2 \cdot \frac{\pi}{4} - \sin\frac{\pi}{2}) - 0$.
5. Final Answer: $\mathbf{\frac{\pi}{2} - 1}$.

---

## Part 2: Practice Problems

1. **Limits:** (a) $\lim_{x \to 0} \frac{\sin x - x}{x^3}$, (b) $\lim_{x \to 0^+} x \ln x$.
2. **Trig Sub:** $\int \frac{dx}{x^2\sqrt{x^2 - 16}}$.
3. **Trig Integral:** $\int \cos^2(x) \sin^3(x) dx$.
4. **Trig Sub:** $\int \frac{x^3}{\sqrt{x^2 - 9}} dx$.
5. **Partial Fractions:** $\int \frac{x-7}{x^2 - x - 2} dx$.
6. **Improper Integral:** $\int_1^{\infty} \frac{\ln x}{x^2} dx$.
7. **Arc Length:** $y = \frac{2}{3}x^{3/2}$ from $x=0$ to $x=3$.
8. **Parametric Tangent:** $x = t^3 + 1, y = t^4 + t$ at $t=1$.
9. **Parametric Arc Length:** $x = \cos^3 t, y = \sin^3 t, 0 \le t \le \pi/2$.
10. **Polar Area:** Inside $r = 3\sin\theta$ and outside $r = 1.5$.

---

## Part 3: Practice Problem Answer Key

### Problem 1 Solution
**(a)** $\lim_{x \to 0} \frac{\sin x - x}{x^3} \xrightarrow{L'H} \lim_{x \to 0} \frac{\cos x - 1}{3x^2} \xrightarrow{L'H} \lim_{x \to 0} \frac{-\sin x}{6x} = \mathbf{-\frac{1}{6}}$.
**(b)** Rewrite as $\frac{\ln x}{1/x}$. Apply L'Hôpital: $\lim_{x \to 0^+} \frac{1/x}{-1/x^2} = \lim_{x \to 0^+} -x = \mathbf{0}$.

### Problem 2 Solution
1. Let $x = 4\sec\theta, dx = 4\sec\theta\tan\theta d\theta$. The radical is $4\tan\theta$.
2. $\int \frac{4\sec\theta\tan\theta d\theta}{16\sec^2\theta \cdot 4\tan\theta} = \frac{1}{16} \int \frac{1}{\sec\theta} d\theta = \frac{1}{16} \int \cos\theta d\theta$.
3. Integrate: $\frac{1}{16}\sin\theta + C$.
4. Use $\sec\theta = x/4 \implies \sin\theta = \frac{\sqrt{x^2-16}}{x}$.
5. Final: $\mathbf{\frac{\sqrt{x^2-16}}{16x} + C}$.

### Problem 3 Solution
1. $\int \cos^2 x (1-\cos^2 x) \sin x dx$. Let $u = \cos x, du = -\sin x dx$.
2. $\int -(u^2 - u^4) du = \frac{u^5}{5} - \frac{u^3}{3} + C$.
3. Final: $\mathbf{\frac{\cos^5 x}{5} - \frac{\cos^3 x}{3} + C}$.

### Problem 4 Solution
1. Let $x = 3\sec\theta, dx = 3\sec\theta\tan\theta d\theta$.
2. $\int \frac{27\sec^3\theta}{3\tan\theta} 3\sec\theta\tan\theta d\theta = 27 \int \sec^4\theta d\theta = 27 \int (1+\tan^2\theta)\sec^2\theta d\theta$.
3. Let $v = \tan\theta$: $27(v + v^3/3) = 27\tan\theta + 9\tan^3\theta + C$.
4. Substitute $\tan\theta = \frac{\sqrt{x^2-9}}{3}$: $\mathbf{9\sqrt{x^2-9} + \frac{(x^2-9)^{3/2}}{3} + C}$.

### Problem 5 Solution
1. $\frac{x-7}{(x-2)(x+1)} = \frac{A}{x-2} + \frac{B}{x+1}$.
2. Solve: $x-7 = A(x+1) + B(x-2)$.
3. $x=2 \implies A=-5/3$. $x=-1 \implies B=8/3$.
4. Final: $\mathbf{-\frac{5}{3}\ln|x-2| + \frac{8}{3}\ln|x+1| + C}$.

### Problem 6 Solution
1. $u = \ln x, dv = x^{-2}dx$.
2. $[-\frac{\ln x}{x}]_1^{\infty} + \int_1^{\infty} \frac{1}{x^2} dx = [-\frac{\ln x}{x} - \frac{1}{x}]_1^{\infty}$.
3. Evaluate limit: $(0 - 0) - (0 - 1) = \mathbf{1}$.

### Problem 7 Solution
1. $y' = x^{1/2}$. $L = \int_0^3 \sqrt{1+x} dx$.
2. $[\frac{2}{3}(1+x)^{3/2}]_0^3 = \frac{2}{3}(4^{3/2} - 1^{3/2}) = \frac{2}{3}(8-1) = \mathbf{\frac{14}{3}}$.

### Problem 8 Solution
1. Point at $t=1$: $(2, 2)$.
2. Slope $\frac{dy}{dx} = \frac{4t^3+1}{3t^2}$. At $t=1, m = 5/3$.
3. Line: $y - 2 = \frac{5}{3}(x-2) \implies \mathbf{y = \frac{5}{3}x - \frac{4}{3}}$.

### Problem 9 Solution
1. $\sqrt{(x')^2+(y')^2} = \sqrt{(-3\cos^2 t \sin t)^2 + (3\sin^2 t \cos t)^2} = 3\sin t \cos t$.
2. $\int_0^{\pi/2} 3\sin t \cos t dt = [\frac{3}{2}\sin^2 t]_0^{\pi/2} = \mathbf{1.5}$.

### Problem 10 Solution
1. Intersection: $3\sin\theta = 1.5 \implies \theta = \pi/6$ to $5\pi/6$.
2. $A = \frac{1}{2} \int_{\pi/6}^{5\pi/6} (9\sin^2\theta - 2.25) d\theta$.
3. Final Answer: $\mathbf{\frac{3\pi}{4} + \frac{9\sqrt{3}}{8}}$.
