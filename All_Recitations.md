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
# Solutions for Problem 2: Integrals

### (i) $\int_{0}^{\sqrt{3}/4} \frac{1}{1 + 16x^2} dx$
1. **Identify the form:** The denominator $1 + (4x)^2$ suggests the $\arctan$ form $\int \frac{1}{1+u^2} du = \arctan(u) + C$.
2. **Substitution:** Let $u = 4x$, then $du = 4 dx$, which means $dx = \frac{1}{4} du$.
3. **Change the limits of integration:**
   - When $x = 0$, $u = 4(0) = 0$.
   - When $x = \frac{\sqrt{3}}{4}$, $u = 4(\frac{\sqrt{3}}{4}) = \sqrt{3}$.
4. **Integrate:**
   $$\frac{1}{4} \int_{0}^{\sqrt{3}} \frac{1}{1 + u^2} du = \frac{1}{4} \left[ \arctan(u) \right]_{0}^{\sqrt{3}}$$
5. **Evaluate:**
   $$\frac{1}{4} (\arctan(\sqrt{3}) - \arctan(0)) = \frac{1}{4} \left( \frac{\pi}{3} - 0 \right) = \frac{\pi}{12}$$
**Final Answer:** $\frac{\pi}{12}$

---

### (ii) $\int_{0}^{\pi/2} \frac{\sin x}{1 + \cos^2 x} dx$
1. **Substitution:** Let $u = \cos x$. Then $du = -\sin x dx$, or $-du = \sin x dx$.
2. **Change the limits:**
   - When $x = 0$, $u = \cos(0) = 1$.
   - When $x = \pi/2$, $u = \cos(\pi/2) = 0$.
3. **Rewrite the integral:** Swap the limits to remove the negative sign:
   $$\int_{1}^{0} \frac{-du}{1 + u^2} = \int_{0}^{1} \frac{du}{1 + u^2}$$
4. **Evaluate:**
   $$\left[ \arctan(u) \right]_{0}^{1} = \arctan(1) - \arctan(0) = \frac{\pi}{4} - 0 = \frac{\pi}{4}$$
**Final Answer:** $\frac{\pi}{4}$

---

### (iii) $\int \frac{1 + x}{1 + x^2} dx$
1. **Split the fraction:** Rewrite as two separate integrals:
   $$\int \frac{1}{1 + x^2} dx + \int \frac{x}{1 + x^2} dx$$
2. **Solve the first part:** This is the standard derivative of $\arctan x$.
3. **Solve the second part:** Use substitution $u = 1 + x^2$, so $du = 2x dx$ and $\frac{1}{2}du = x dx$:
   $$\frac{1}{2} \int \frac{1}{u} du = \frac{1}{2} \ln|u| = \frac{1}{2} \ln(1 + x^2)$$
4. **Combine:**
   $$\arctan x + \frac{1}{2} \ln(1 + x^2) + C$$
**Final Answer:** $\frac{1}{2} \ln(1 + x^2) + \arctan x + C$

---

### (iv) $\int \frac{t^2}{\sqrt{1 - t^6}} dt$
1. **Rewrite for substitution:** Express the denominator as $\sqrt{1 - (t^3)^2}$.
2. **Substitution:** Let $u = t^3$, then $du = 3t^2 dt$, so $\frac{1}{3} du = t^2 dt$.
3. **Integrate:**
   $$\frac{1}{3} \int \frac{1}{\sqrt{1 - u^2}} du = \frac{1}{3} \arcsin(u) + C$$
4. **Back-substitute:**
   $$\frac{1}{3} \arcsin(t^3) + C$$
**Final Answer:** $\frac{1}{3} \arcsin(t^3) + C$

---

### (v) $\int \frac{1}{1 + \cos 2\theta} d\theta$
1. **Apply Trig Identity:** Use $1 + \cos 2\theta = 2\cos^2 \theta$.
2. **Simplify:**
   $$\int \frac{1}{2\cos^2 \theta} d\theta = \frac{1}{2} \int \sec^2 \theta d\theta$$
3. **Integrate:** Since $\frac{d}{d\theta}(\tan \theta) = \sec^2 \theta$:
   $$\frac{1}{2} \tan \theta + C$$
**Final Answer:** $\frac{1}{2} \tan \theta + C$

---

### (vi) $\int \tan^{-1} x dx$
1. **Integration by Parts:** Let $u = \arctan x$ and $dv = dx$.
   - $du = \frac{1}{1+x^2} dx$
   - $v = x$
2. **Apply formula $\int u dv = uv - \int v du$:**
   $$x \arctan x - \int \frac{x}{1+x^2} dx$$
3. **Solve the remaining integral:** Use $w = 1+x^2$, $dw = 2x dx$:
   $$x \arctan x - \frac{1}{2} \ln(1+x^2) + C$$
**Final Answer:** $x \arctan x - \frac{1}{2} \ln(1 + x^2) + C$

---

### (vii) $\int x^2 e^x dx$
1. **Integration by Parts:** Let $u = x^2$ and $dv = e^x dx$.
   - $du = 2x dx$, $v = e^x$.
   - Result: $x^2 e^x - \int 2x e^x dx$.
2. **Repeat Parts for the integral $\int 2x e^x dx$:** Let $u = 2x$ and $dv = e^x dx$.
   - $du = 2 dx$, $v = e^x$.
   - Result: $2x e^x - \int 2 e^x dx = 2x e^x - 2e^x$.
3. **Combine and simplify:**
   $$x^2 e^x - (2x e^x - 2e^x) + C = e^x(x^2 - 2x + 2) + C$$
**Final Answer:** $e^x(x^2 - 2x + 2) + C$

---

### (viii) $\int (\tan^2 x + \tan^4 x) dx$
1. **Factor:** $\int \tan^2 x (1 + \tan^2 x) dx$.
2. **Apply Identity:** Use $1 + \tan^2 x = \sec^2 x$:
   $$\int \tan^2 x \sec^2 x dx$$
3. **Substitution:** Let $u = \tan x$, then $du = \sec^2 x dx$.
4. **Integrate:**
   $$\int u^2 du = \frac{1}{3} u^3 + C = \frac{1}{3} \tan^3 x + C$$
**Final Answer:** $\frac{1}{3} \tan^3 x + C$
