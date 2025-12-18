# Midterm Recitation 1
## Solutions for Problem 1: Limits

### (i) $\lim_{x \to \infty} \frac{(\ln x)^2}{x}$
**1. Identify the form:** As $x \to \infty$, $(\ln x)^2 \to \infty$ and $x \to \infty$. This is an indeterminate form of type $\frac{\infty}{\infty}$.  
**2. First L'Hôpital's Rule application:**
$$\lim_{x \to \infty} \frac{\frac{d}{dx}(\ln x)^2}{\frac{d}{dx}x} = \lim_{x \to \infty} \frac{2(\ln x) \cdot \frac{1}{x}}{1} = \lim_{x \to \infty} \frac{2\ln x}{x}$$
**3. Second L'Hôpital's Rule application:** This is still $\frac{\infty}{\infty}$.
$$\lim_{x \to \infty} \frac{\frac{d}{dx}(2\ln x)}{\frac{d}{dx}x} = \lim_{x \to \infty} \frac{\frac{2}{x}}{1} = 0$$
**Final Answer:** $0$

---

### (ii) $\lim_{x \to 0} \frac{\sin^{-1} x}{x}$
**1. Identify the form:** At $x = 0$, $\sin^{-1}(0) = 0$, so we have $\frac{0}{0}$.  
**2. Apply L'Hôpital's Rule:**
$$\lim_{x \to 0} \frac{\frac{d}{dx}(\sin^{-1} x)}{\frac{d}{dx}x} = \lim_{x \to 0} \frac{\frac{1}{\sqrt{1-x^2}}}{1}$$
**3. Evaluate:** Plug in $x = 0$: $\frac{1}{\sqrt{1-0}} = 1$.  
**Final Answer:** $1$

---

### (iii) $\lim_{x \to \infty} x^{1/x}$
**1. Identify the form:** This is an indeterminate power $\infty^0$. Let $L = \lim_{x \to \infty} x^{1/x}$.  
**2. Take the natural log:** $\ln L = \lim_{x \to \infty} \ln(x^{1/x}) = \lim_{x \to \infty} \frac{\ln x}{x}$.  
**3. Apply L'Hôpital's Rule:**
$$\lim_{x \to \infty} \frac{\frac{1}{x}}{1} = 0$$
**4. Solve for L:** Since $\ln L = 0$, then $L = e^0 = 1$.  
**Final Answer:** $1$

---

### (iv) $\lim_{x \to 1} \left( \frac{x}{x-1} - \frac{1}{\ln x} \right)$
**1. Identify the form:** This is $\infty - \infty$. Find a common denominator:
$$\lim_{x \to 1} \frac{x \ln x - (x - 1)}{(x - 1) \ln x} = \lim_{x \to 1} \frac{x \ln x - x + 1}{x \ln x - \ln x}$$
**2. Apply L'Hôpital's Rule ($\frac{0}{0}$):**
$$\lim_{x \to 1} \frac{\ln x + x(\frac{1}{x}) - 1}{\ln x + x(\frac{1}{x}) - \frac{1}{x}} = \lim_{x \to 1} \frac{\ln x}{\ln x + 1 - \frac{1}{x}}$$
**3. Apply L'Hôpital's Rule again ($\frac{0}{0}$):**
$$\lim_{x \to 1} \frac{\frac{1}{x}}{\frac{1}{x} + \frac{1}{x^2}} = \frac{1}{1 + 1} = \frac{1}{2}$$
**Final Answer:** $1/2$

---

### (v) $\lim_{x \to \infty} \left( 1 + \frac{4}{x} \right)^x$
**1. Use the definition of $e$:** The standard limit $\lim_{n \to \infty} (1 + \frac{a}{n})^n = e^a$.  
**2. Apply to the problem:** Here $a = 4$.  
**Final Answer:** $e^4$

---

### (vi) $\lim_{x \to \infty} \frac{1 + 2x}{1 - 2x}$
**1. Algebraic simplification:** Divide the numerator and denominator by $x$:
$$\lim_{x \to \infty} \frac{\frac{1}{x} + 2}{\frac{1}{x} - 2}$$
**2. Evaluate:** As $x \to \infty$, $\frac{1}{x} \to 0$.
$$\frac{0 + 2}{0 - 2} = -1$$
**Final Answer:** $-1$

---

### (vii) $\lim_{x \to 0} \frac{e^{2x} - e^{-2x}}{\ln(1 + x)}$
**1. Identify the form:** $\frac{e^0 - e^0}{\ln(1)} = \frac{0}{0}$.  
**2. Apply L'Hôpital's Rule:**
$$\lim_{x \to 0} \frac{2e^{2x} - (-2e^{-2x})}{\frac{1}{1+x}} = \lim_{x \to 0} (2e^{2x} + 2e^{-2x})(1 + x)$$
**3. Evaluate:** Plug in $x = 0$: $(2(1) + 2(1))(1) = 4$.  
**Final Answer:** $4$

## Solutions for Problem 2: Integrals

### (i) $\int_{0}^{\sqrt{3}/4} \frac{1}{1 + 16x^2} dx$ [Corrected]
**1. Rewrite the denominator:** $1 + (4x)^2$.
**2. Substitution:** Let $u = 4x$, then $du = 4 dx \implies dx = \frac{1}{4} du$.
**3. Change limits:**
- If $x = 0$, $u = 4(0) = 0$.
- If $x = \frac{\sqrt{3}}{4}$, $u = 4(\frac{\sqrt{3}}{4}) = \sqrt{3}$.
**4. Integrate:**
$$\frac{1}{4} \int_{0}^{\sqrt{3}} \frac{1}{1 + u^2} du = \frac{1}{4} \left[ \arctan(u) \right]_{0}^{\sqrt{3}}$$
**5. Evaluate:** $\frac{1}{4} (\arctan(\sqrt{3}) - \arctan(0)) = \frac{1}{4} (\frac{\pi}{3} - 0) = \frac{\pi}{12}$.
**Final Answer:** $\frac{\pi}{12}$

---

### (ii) $\int_{0}^{\pi/2} \frac{\sin x}{1 + \cos^2 x} dx$
**1. Substitution:** Let $u = \cos x$, then $du = -\sin x dx$, so $-du = \sin x dx$.
**2. Change limits:** - If $x = 0$, $u = \cos(0) = 1$.
- If $x = \pi/2$, $u = \cos(\pi/2) = 0$.
**3. Integrate:**
$$\int_{1}^{0} \frac{-1}{1 + u^2} du = \int_{0}^{1} \frac{1}{1 + u^2} du$$
$$[\arctan u]_{0}^{1} = \arctan(1) - \arctan(0) = \frac{\pi}{4} - 0 = \frac{\pi}{4}$$
**Final Answer:** $\pi/4$

---

### (iii) $\int \frac{1 + x}{1 + x^2} dx$
**1. Split the integral:**
$$\int \frac{1}{1 + x^2} dx + \int \frac{x}{1 + x^2} dx$$
**2. Solve first part:** This is the standard $\arctan x$.
**3. Solve second part:** Use $u = 1 + x^2$, $du = 2x dx \implies \frac{1}{2}du = x dx$:
$$\frac{1}{2} \int \frac{1}{u} du = \frac{1}{2} \ln|1 + x^2|$$
**Final Answer:** $\arctan x + \frac{1}{2} \ln(1 + x^2) + C$

---

### (iv) $\int \frac{t^2}{\sqrt{1 - t^6}} dt$
**1. Rewrite the denominator:** $\sqrt{1 - (t^3)^2}$.
**2. Substitution:** Let $u = t^3$, then $du = 3t^2 dt \implies \frac{1}{3}du = t^2 dt$.
**3. Integrate:**
$$\frac{1}{3} \int \frac{1}{\sqrt{1 - u^2}} du = \frac{1}{3} \arcsin(u) + C$$
**Final Answer:** $\frac{1}{3} \arcsin(t^3) + C$

---

### (v) $\int \frac{1}{1 + \cos 2\theta} d\theta$
**1. Use Trig Identity:** $1 + \cos 2\theta = 2\cos^2 \theta$.
**2. Simplify:**
$$\int \frac{1}{2\cos^2 \theta} d\theta = \frac{1}{2} \int \sec^2 \theta d\theta$$
**3. Integrate:** $\int \sec^2 \theta d\theta = \tan \theta$.
**Final Answer:** $\frac{1}{2} \tan \theta + C$

---

### (vi) $\int \tan^{-1} x dx$
**1. Integration by Parts:** Let $u = \tan^{-1} x$ and $dv = dx$.
- $du = \frac{1}{1+x^2} dx$
- $v = x$
**2. Apply formula $\int u dv = uv - \int v du$:**
$$x \tan^{-1} x - \int \frac{x}{1+x^2} dx$$
**3. Solve remaining integral:** Use substitution $w = 1+x^2, dw = 2x dx$:
$$x \tan^{-1} x - \frac{1}{2} \ln(1+x^2) + C$$
**Final Answer:** $x \arctan x - \frac{1}{2} \ln(1 + x^2) + C$

---

### (vii) $\int x^2 e^x dx$
**1. Integration by Parts (Tabular Method):**
- Differentiate $x^2$: $x^2 \to 2x \to 2 \to 0$
- Integrate $e^x$: $e^x \to e^x \to e^x \to e^x$
**2. Combine with alternating signs:**
$$(x^2)(e^x) - (2x)(e^x) + (2)(e^x) + C$$
**3. Factor:** $e^x(x^2 - 2x + 2) + C$.
**Final Answer:** $e^x(x^2 - 2x + 2) + C$

---

### (viii) $\int (\tan^2 x + \tan^4 x) dx$
**1. Factor out $\tan^2 x$:**
$$\int \tan^2 x (1 + \tan^2 x) dx$$
**2. Use Identity:** $1 + \tan^2 x = \sec^2 x$.
$$\int \tan^2 x \sec^2 x dx$$
**3. Substitution:** Let $u = \tan x$, $du = \sec^2 x dx$.
$$\int u^2 du = \frac{1}{3} u^3 + C$$
**Final Answer:** $\frac{1}{3} \tan^3 x + C$

---

### (ix) $\int \sin^2 x \cos^3 x dx$
**1. Use Identity:** Save one $\cos x$ and convert the rest to sine: $\cos^3 x = \cos^2 x \cos x = (1 - \sin^2 x) \cos x$.
**2. Substitute:** $\int \sin^2 x (1 - \sin^2 x) \cos x dx$. Let $u = \sin x$, $du = \cos x dx$.
**3. Expand and Integrate:**
$$\int u^2(1 - u^2) du = \int (u^2 - u^4) du = \frac{u^3}{3} - \frac{u^5}{5} + C$$
**Final Answer:** $\frac{\sin^3 x}{3} - \frac{\sin^5 x}{5} + C$

---

### (x) $\int \frac{1}{1 - \cos 2\theta} d\theta$
**1. Use Trig Identity:** $1 - \cos 2\theta = 2\sin^2 \theta$.
**2. Simplify:** $\int \frac{1}{2\sin^2 \theta} d\theta = \frac{1}{2} \int \csc^2 \theta d\theta$.
**3. Integrate:** Since $\frac{d}{d\theta}(-\cot \theta) = \csc^2 \theta$.
**Final Answer:** $-\frac{1}{2} \cot \theta + C$

---

### (xi) $\int_{0}^{2/3} \sqrt{4 - 9x^2} dx$
**1. Factor out a 4:** $\int_{0}^{2/3} \sqrt{4(1 - \frac{9}{4}x^2)} dx = 2 \int_{0}^{2/3} \sqrt{1 - (\frac{3}{2}x)^2} dx$.
**2. Trig Substitution:** Let $\frac{3}{2}x = \sin \theta$, then $\frac{3}{2} dx = \cos \theta d\theta \implies dx = \frac{2}{3} \cos \theta d\theta$.
**3. Limits:** If $x=0, \theta=0$. If $x=2/3, \sin \theta = 1 \implies \theta = \pi/2$.
**4. Solve:**
$$2 \int_{0}^{\pi/2} \sqrt{1 - \sin^2 \theta} \cdot \frac{2}{3} \cos \theta d\theta = \frac{4}{3} \int_{0}^{\pi/2} \cos^2 \theta d\theta = \frac{4}{3} \int_{0}^{\pi/2} \frac{1 + \cos 2\theta}{2} d\theta$$
$$\frac{2}{3} [\theta + \frac{1}{2}\sin 2\theta]_{0}^{\pi/2} = \frac{2}{3} [(\frac{\pi}{2} + 0) - (0 + 0)] = \frac{\pi}{3}$$
**Final Answer:** $\frac{\pi}{3}$

---

### (xii) $\int \frac{x^3}{\sqrt{9 + x^2}} dx$
**1. Substitution:** Let $u = 9 + x^2$, then $du = 2x dx$ and $x^2 = u - 9$.
**2. Rewrite Integral:** $\int \frac{x^2 \cdot x}{\sqrt{9 + x^2}} dx = \int \frac{(u - 9) \cdot \frac{1}{2} du}{\sqrt{u}}$.
**3. Expand:** $\frac{1}{2} \int (u^{1/2} - 9u^{-1/2}) du = \frac{1}{2} [\frac{2}{3}u^{3/2} - 18u^{1/2}] + C$.
**4. Simplify:** $\frac{1}{3}(9+x^2)^{3/2} - 9\sqrt{9+x^2} + C$.
**Final Answer:** $\frac{1}{3}(9+x^2)^{3/2} - 9\sqrt{9+x^2} + C$

---

### (xiii) $\int x \sqrt{1 - x^4} dx$
**1. Substitution:** Let $u = x^2$, $du = 2x dx \implies \frac{1}{2} du = x dx$.
**2. New Integral:** $\frac{1}{2} \int \sqrt{1 - u^2} du$. This is the area of a sector or requires $u = \sin \theta$.
**3. Solve:** $\frac{1}{2} [\frac{1}{2}u\sqrt{1-u^2} + \frac{1}{2}\arcsin u] + C$.
**Final Answer:** $\frac{1}{4}x^2\sqrt{1-x^4} + \frac{1}{4}\arcsin(x^2) + C$

---

### (xiv) $\int_{0}^{1} \frac{1}{(x - 1)^2} dx$
**1. Identify Improper Integral:** Vertical asymptote at $x = 1$.
**2. Limit Process:** $\lim_{t \to 1^-} \int_{0}^{t} (x - 1)^{-2} dx$.
**3. Integrate:** $[-(x - 1)^{-1}]_{0}^{t} = \frac{-1}{t-1} - (\frac{-1}{0-1}) = \frac{-1}{t-1} - 1$.
**4. Evaluate Limit:** As $t \to 1^-$, $\frac{-1}{t-1} \to \infty$.
**Final Answer:** Diverges

---

### (xv) $\int \frac{1}{x^2 + 2x - 3} dx$
**1. Factor Denominator:** $(x+3)(x-1)$.
**2. Partial Fractions:** $\frac{1}{(x+3)(x-1)} = \frac{A}{x+3} + \frac{B}{x-1}$.
- $1 = A(x-1) + B(x+3)$.
- If $x=1, B=1/4$. If $x=-3, A=-1/4$.
**3. Integrate:** $\int (\frac{-1/4}{x+3} + \frac{1/4}{x-1}) dx = \frac{1}{4} \ln|x-1| - \frac{1}{4} \ln|x+3| + C$.
**Final Answer:** $\frac{1}{4} \ln \left| \frac{x-1}{x+3} \right| + C$

---

### (xvi) $\int \frac{3x + 2}{x^3 + 4x} dx$
**1. Partial Fractions:** $\frac{3x + 2}{x(x^2 + 4)} = \frac{A}{x} + \frac{Bx + C}{x^2 + 4}$.
- $3x + 2 = A(x^2 + 4) + (Bx + C)x$.
- $x=0 \implies 2 = 4A \implies A = 1/2$.
- $x^2$ coeffs: $0 = A + B \implies B = -1/2$.
- $x$ coeffs: $3 = C$.
**2. Integrate:** $\int \frac{1/2}{x} dx + \int \frac{-1/2x + 3}{x^2 + 4} dx$.
- $\frac{1}{2} \ln|x| - \frac{1}{4} \ln(x^2 + 4) + \frac{3}{2} \arctan(\frac{x}{2}) + C$.
**Final Answer:** $\frac{1}{2} \ln|x| - \frac{1}{4} \ln(x^2 + 4) + \frac{3}{2} \arctan(\frac{x}{2}) + C$
