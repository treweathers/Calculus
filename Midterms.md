This is a comprehensive set of Calculus II problems covering limits, integration techniques (trigonometric substitution, partial fractions), improper integrals, and parametric/polar calculus.

Below are the step-by-step solutions for your original problems, followed by a set of parallel practice problems with their own detailed answer key.

---

## Part 1: Solutions to Original Problems

### Problem 1: Limits

**(a)** \lim_{x \to 0} \frac{x - \sin x}{x - \tan x}

1. Plug in x=0: \frac{0-0}{0-0} = \frac{0}{0}. Apply **L'Hôpital's Rule**.
2. Differentiate: \lim_{x \to 0} \frac{1 - \cos x}{1 - \sec^2 x}.
3. Still \frac{0}{0}. Apply L'Hôpital again: \lim_{x \to 0} \frac{\sin x}{-2\sec^2 x \tan x}.
4. Simplify using \tan x = \frac{\sin x}{\cos x}: \lim_{x \to 0} \frac{\sin x}{-2 \cdot \frac{1}{\cos^2 x} \cdot \frac{\sin x}{\cos x}} = \lim_{x \to 0} -\frac{\cos^3 x}{2}.
5. Plug in x=0: -\frac{1^3}{2} = \mathbf{-\frac{1}{2}}.

**(b)** \lim_{x \to 1^+} \ln x \tan\left(\frac{\pi x}{2}\right)

1. Form: 0 \cdot (-\infty). Rewrite as \frac{\ln x}{\cot(\pi x / 2)} to get \frac{0}{0}.
2. Apply L'Hôpital: \lim_{x \to 1^+} \frac{1/x}{-\frac{\pi}{2} \csc^2(\frac{\pi x}{2})}.
3. As x \to 1, \csc(\frac{\pi}{2}) = 1.
4. Result: \frac{1}{-\pi/2} = \mathbf{-\frac{2}{\pi}}.

**(c)** \lim_{x \to 0} \frac{\sin(x)\cos(2x)e^{3x}}{x^2 + x}

1. Factor the denominator: \lim_{x \to 0} \frac{\sin x}{x} \cdot \frac{\cos(2x)e^{3x}}{x + 1}.
2. Recall the fundamental limit: \lim_{x \to 0} \frac{\sin x}{x} = 1.
3. Evaluate the rest by direct substitution: \frac{\cos(0)e^0}{0+1} = \frac{1 \cdot 1}{1} = 1.
4. Final Answer: 1 \cdot 1 = \mathbf{1}.

### Problem 2: Trig Substitution

\int \frac{dx}{x^2\sqrt{9 - x^2}}

1. Let x = 3\sin\theta, so dx = 3\cos\theta d\theta. The radical becomes \sqrt{9-9\sin^2\theta} = 3\cos\theta.
2. Substitute: \int \frac{3\cos\theta d\theta}{(3\sin\theta)^2 (3\cos\theta)} = \int \frac{d\theta}{9\sin^2\theta} = \frac{1}{9} \int \csc^2\theta d\theta.
3. Integrate: -\frac{1}{9}\cot\theta + C.
4. Back-substitute: Since \sin\theta = \frac{x}{3}, then \cot\theta = \frac{\sqrt{9-x^2}}{x}.
5. Final Answer: \mathbf{-\frac{\sqrt{9-x^2}}{9x} + C}.

### Problem 3: Trig Integral

\int \sin^2 x \cos^3 x dx

1. Save one \cos x: \int \sin^2 x \cos^2 x (\cos x dx).
2. Convert \cos^2 x to 1 - \sin^2 x: \int \sin^2 x (1 - \sin^2 x) \cos x dx.
3. Let u = \sin x, du = \cos x dx: \int u^2(1 - u^2) du = \int (u^2 - u^4) du.
4. Integrate: \frac{u^3}{3} - \frac{u^5}{5} + C.
5. Final Answer: \mathbf{\frac{\sin^3 x}{3} - \frac{\sin^5 x}{5} + C}.

### Problem 4: Trig Substitution

\int \frac{x^3}{\sqrt{x^2 + 4}} dx

1. Let x = 2\tan\theta, dx = 2\sec^2\theta d\theta, \sqrt{x^2+4} = 2\sec\theta.
2. Substitute: \int \frac{8\tan^3\theta}{2\sec\theta} 2\sec^2\theta d\theta = 8 \int \tan^3\theta \sec\theta d\theta.
3. Rewrite: 8 \int (\sec^2\theta - 1) \sec\theta \tan\theta d\theta.
4. Let u = \sec\theta, du = \sec\theta \tan\theta d\theta: 8 \int (u^2 - 1) du = 8(\frac{u^3}{3} - u) + C.
5. Back-substitute u = \frac{\sqrt{x^2+4}}{2}: \mathbf{\frac{(x^2+4)^{3/2}}{3} - 4\sqrt{x^2+4} + C}.

### Problem 5: Partial Fractions

\int \frac{5x + 1}{2x^2 - x - 1} dx

1. Factor denominator: (2x+1)(x-1).
2. Setup: \frac{5x+1}{(2x+1)(x-1)} = \frac{A}{2x+1} + \frac{B}{x-1}.
3. Solve: 5x+1 = A(x-1) + B(2x+1).
* If x=1: 6 = 3B \implies B=2.
* If x=-1/2: -3/2 = A(-3/2) \implies A=1.


4. Integrate: \int (\frac{1}{2x+1} + \frac{2}{x-1}) dx = \frac{1}{2}\ln|2x+1| + 2\ln|x-1| + C.

### Problem 6: Improper Integral

\int_0^4 \frac{\ln x}{\sqrt{x}} dx

1. Improper at x=0: \lim_{t \to 0^+} \int_t^4 x^{-1/2} \ln x dx.
2. Integration by parts: u = \ln x, dv = x^{-1/2}dx \implies du = \frac{1}{x}dx, v = 2\sqrt{x}.
3. \int \frac{\ln x}{\sqrt{x}} dx = 2\sqrt{x}\ln x - \int 2\sqrt{x} \frac{1}{x} dx = 2\sqrt{x}\ln x - 4\sqrt{x}.
4. Evaluate from t to 4: (2\sqrt{4}\ln 4 - 4\sqrt{4}) - (2\sqrt{t}\ln t - 4\sqrt{t}).
5. Limit as t \to 0: 2\sqrt{t}\ln t \to 0 (via L'Hôpital).
6. Result: 4\ln 4 - 8 = \mathbf{8\ln 2 - 8}.

### Problem 7: Arc Length

y = (x+4)^{3/2}, 0 \le x \le 4

1. y' = \frac{3}{2}(x+4)^{1/2}.
2. (y')^2 = \frac{9}{4}(x+4).
3. L = \int_0^4 \sqrt{1 + \frac{9}{4}x + 9} dx = \int_0^4 \sqrt{\frac{9}{4}x + 10} dx.
4. Integrate: [\frac{2}{3} \cdot \frac{4}{9} (\frac{9}{4}x + 10)^{3/2}]_0^4 = \frac{8}{27} [19^{3/2} - 10^{3/2}].

### Problem 8: Parametric Tangent

x = \sqrt{t}, y = t^2 - 2t, t=1

1. Point: x = \sqrt{1} = 1, y = 1 - 2 = -1. Point is (1, -1).
2. Slope: \frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{2t - 2}{1/(2\sqrt{t})}.
3. At t=1: \frac{2(1)-2}{1/2} = 0.
4. Equation: y - (-1) = 0(x - 1) \implies \mathbf{y = -1}.

### Problem 9: Parametric Arc Length

x = e^t - t, y = 4e^{t/2}, 0 \le t \le 2

1. x' = e^t - 1, y' = 2e^{t/2}.
2. (x')^2 + (y')^2 = (e^{2t} - 2e^t + 1) + 4e^t = e^{2t} + 2e^t + 1 = (e^t + 1)^2.
3. L = \int_0^2 \sqrt{(e^t+1)^2} dt = \int_0^2 (e^t + 1) dt.
4. Evaluate: [e^t + t]_0^2 = (e^2 + 2) - (e^0 + 0) = \mathbf{e^2 + 1}.

### Problem 10: Polar Area

r = 2\cos\theta, r = 2\sin\theta

1. Intersection: 2\cos\theta = 2\sin\theta \implies \tan\theta = 1 \implies \theta = \pi/4.
2. Region is symmetric. Total Area = 2 \times Area from 0 to \pi/4 for r = 2\sin\theta.
3. A = 2 \int_0^{\pi/4} \frac{1}{2} (2\sin\theta)^2 d\theta = \int_0^{\pi/4} 4\sin^2\theta d\theta.
4. Use 2\sin^2\theta = 1 - \cos(2\theta): \int_0^{\pi/4} (2 - 2\cos 2\theta) d\theta.
5. Evaluate: [2\theta - \sin 2\theta]_0^{\pi/4} = (\frac{\pi}{2} - 1) - (0 - 0) = \mathbf{\frac{\pi}{2} - 1}.

---

## Part 2: Practice Problems

1. Evaluate: (a) \lim_{x \to 0} \frac{\sin x - x}{x^3}, (b) \lim_{x \to 0^+} x \ln x.
2. Evaluate the integral: \int \frac{dx}{x^2\sqrt{x^2 - 16}}.
3. Evaluate the integral: \int \cos^2(x) \sin^3(x) dx.
4. Evaluate the integral: \int \frac{x^3}{\sqrt{x^2 - 9}} dx.
5. Evaluate the integral: \int \frac{x-7}{x^2 - x - 2} dx.
6. Evaluate the integral or show divergence: \int_1^{\infty} \frac{\ln x}{x^2} dx.
7. Find the length of the curve: y = \frac{2}{3}x^{3/2} from x=0 to x=3.
8. Find the tangent line to x = t^3 + 1, y = t^4 + t at t=1.
9. Find the length of the curve: x = \cos^3 t, y = \sin^3 t, 0 \le t \le \pi/2.
10. Find the area inside the circle r = 3\sin\theta and outside r = 1.5 (part of the circle).

---

## Part 3: Answer Key for Practice Problems

### Problem 1 Solution

**(a)** \lim_{x \to 0} \frac{\sin x - x}{x^3} \xrightarrow{L'H} \lim_{x \to 0} \frac{\cos x - 1}{3x^2} \xrightarrow{L'H} \lim_{x \to 0} \frac{-\sin x}{6x} = -\frac{1}{6}.
**(b)** \lim_{x \to 0^+} \frac{\ln x}{1/x} \xrightarrow{L'H} \lim_{x \to 0^+} \frac{1/x}{-1/x^2} = \lim_{x \to 0^+} -x = 0.

### Problem 2 Solution

\int \frac{dx}{x^2\sqrt{x^2 - 16}}

1. Let x = 4\sec\theta, dx = 4\sec\theta\tan\theta d\theta. Radical = 4\tan\theta.
2. \int \frac{4\sec\theta\tan\theta d\theta}{16\sec^2\theta \cdot 4\tan\theta} = \frac{1}{16} \int \cos\theta d\theta = \frac{1}{16}\sin\theta + C.
3. Since \sec\theta = x/4, \sin\theta = \frac{\sqrt{x^2-16}}{x}. Final: \mathbf{\frac{\sqrt{x^2-16}}{16x} + C}.

### Problem 3 Solution

\int \cos^2 x \sin^3 x dx

1. Save one \sin x: \int \cos^2 x (1-\cos^2 x) \sin x dx.
2. Let u = \cos x, du = -\sin x dx: -\int u^2(1-u^2) du = \int (u^4 - u^2) du.
3. \frac{\cos^5 x}{5} - \frac{\cos^3 x}{3} + C.

### Problem 4 Solution

\int \frac{x^3}{\sqrt{x^2-9}} dx

1. Let x = 3\sec\theta. Similar to original Prob 4, becomes \int 27\sec^3\theta \tan\theta \frac{3\sec\theta\tan\theta}{3\tan\theta} d\theta.
2. Result: \mathbf{\frac{(x^2-9)^{3/2}}{3} + 9\sqrt{x^2-9} + C}.

### Problem 5 Solution

\frac{x-7}{(x-2)(x+1)} = \frac{A}{x-2} + \frac{B}{x+1}.

1. Solve: x-7 = A(x+1) + B(x-2).
2. x=2 \implies -5=3A \implies A=-5/3. x=-1 \implies -8=-3B \implies B=8/3.
3. \mathbf{-\frac{5}{3}\ln|x-2| + \frac{8}{3}\ln|x+1| + C}.

### Problem 6 Solution

\int_1^{\infty} \frac{\ln x}{x^2} dx. u = \ln x, dv = x^{-2}dx.

1. [-\frac{\ln x}{x} - \frac{1}{x}]_1^{\infty}.
2. At \infty: Limit is 0. At 1: -(0 + 1) = -1.
3. 0 - (-1) = \mathbf{1}.

### Problem 7 Solution

y' = x^{1/2}. L = \int_0^3 \sqrt{1+x} dx = [\frac{2}{3}(1+x)^{3/2}]_0^3 = \frac{2}{3}(8-1) = \mathbf{\frac{14}{3}}.

### Problem 8 Solution

Point (2, 2). dy/dx = \frac{4t^3+1}{3t^2}. At t=1, m = 5/3.
y - 2 = \frac{5}{3}(x-2) \implies \mathbf{y = \frac{5}{3}x - \frac{4}{3}}.

### Problem 9 Solution

x' = -3\cos^2 t \sin t, y' = 3\sin^2 t \cos t.
\sqrt{(x')^2+(y')^2} = 3\sin t \cos t.
\int_0^{\pi/2} 3\sin t \cos t dt = [\frac{3}{2}\sin^2 t]_0^{\pi/2} = \mathbf{1.5}.

### Problem 10 Solution

3\sin\theta = 1.5 \implies \sin\theta = 1/2 \implies \theta = \pi/6, 5\pi/6.
A = \int_{\pi/6}^{5\pi/6} \frac{1}{2}(9\sin^2\theta - 2.25) d\theta = \dots = \mathbf{\frac{3\pi}{4} + \frac{9\sqrt{3}}{8}}.

