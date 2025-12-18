# Midterm Recitation 1
## Solutions for Problem 1: Limits
### (i) $\lim_{x \to \infty} \frac{(\ln x)^2}{x}$
1. **Identify the form:** As $x \to \infty$, $(\ln x)^2 \to \infty$ and $x \to \infty$. This is an indeterminate form of type $\frac{\infty}{\infty}$.
2. **Apply L'Hôpital's Rule (First time):**
   $$\lim_{x \to \infty} \frac{\frac{d}{dx}(\ln x)^2}{\frac{d}{dx}x} = \lim_{x \to \infty} \frac{2(\ln x) \cdot \frac{1}{x}}{1} = \lim_{x \to \infty} \frac{2\ln x}{x}$$
3. **Apply L'Hôpital's Rule (Second time):** The form is still $\frac{\infty}{\infty}$.
   $$\lim_{x \to \infty} \frac{\frac{d}{dx}(2\ln x)}{\frac{d}{dx}x} = \lim_{x \to \infty} \frac{\frac{2}{x}}{1}$$
4. **Evaluate:** As $x \to \infty$, the fraction $\frac{2}{x}$ approaches $0$.
**Final Answer:** $0$

---

### (ii) $\lim_{x \to 0} \frac{\sin^{-1} x}{x}$
1. **Identify the form:** At $x = 0$, $\sin^{-1}(0) = 0$, so we have the indeterminate form $\frac{0}{0}$.
2. **Apply L'Hôpital's Rule:**
   $$\lim_{x \to 0} \frac{\frac{d}{dx}(\sin^{-1} x)}{\frac{d}{dx}x} = \lim_{x \to 0} \frac{\frac{1}{\sqrt{1-x^2}}}{1}$$
3. **Evaluate:** Substitute $x = 0$ into the expression:
   $$\frac{1}{\sqrt{1-0^2}} = \frac{1}{1} = 1$$
**Final Answer:** $1$

---

### (iii) $\lim_{x \to \infty} x^{1/x}$
1. **Identify the form:** This is an indeterminate power of type $\infty^0$. Let $L = \lim_{x \to \infty} x^{1/x}$.
2. **Use Natural Logarithms:** Take the log of both sides to move the exponent:
   $$\ln L = \lim_{x \to \infty} \ln(x^{1/x}) = \lim_{x \to \infty} \frac{\ln x}{x}$$
3. **Apply L'Hôpital's Rule ($\frac{\infty}{\infty}$):**
   $$\lim_{x \to \infty} \frac{\frac{d}{dx}(\ln x)}{\frac{d}{dx}x} = \lim_{x \to \infty} \frac{\frac{1}{x}}{1} = 0$$
4. **Solve for L:** Since $\ln L = 0$, then $L = e^0 = 1$.
**Final Answer:** $1$

---

### (iv) $\lim_{x \to 1} \left( \frac{x}{x-1} - \frac{1}{\ln x} \right)$
1. **Identify the form:** This is $\infty - \infty$. Combine the terms using a common denominator:
   $$\lim_{x \to 1} \frac{x \ln x - (x - 1)}{(x - 1) \ln x} = \lim_{x \to 1} \frac{x \ln x - x + 1}{x \ln x - \ln x}$$
2. **Apply L'Hôpital's Rule ($\frac{0}{0}$):** Use the product rule for $\frac{d}{dx}(x \ln x) = \ln x + 1$.
   $$\lim_{x \to 1} \frac{(\ln x + 1) - 1}{(\ln x + 1) - \frac{1}{x}} = \lim_{x \to 1} \frac{\ln x}{\ln x + 1 - \frac{1}{x}}$$
3. **Apply L'Hôpital's Rule again ($\frac{0}{0}$):**
   $$\lim_{x \to 1} \frac{\frac{1}{x}}{\frac{1}{x} + \frac{1}{x^2}}$$
4. **Evaluate:** Substitute $x = 1$:
   $$\frac{1}{1 + 1} = \frac{1}{2}$$
**Final Answer:** $1/2$

---

### (v) $\lim_{x \to \infty} \left( 1 + \frac{4}{x} \right)^x$
1. **Identify the standard form:** This matches the definition $\lim_{x \to \infty} (1 + \frac{a}{x})^x = e^a$.
2. **Apply the constant:** In this problem, $a = 4$.
3. **Conclusion:** The limit evaluates directly to $e^4$.
**Final Answer:** $e^4$

---

### (vi) $\lim_{x \to \infty} \frac{1 + 2x}{1 - 2x}$
1. **Identify the form:** This is $\frac{\infty}{-\infty}$.
2. **Algebraic Simplification:** Divide every term in the numerator and denominator by the highest power of $x$, which is $x^1$:
   $$\lim_{x \to \infty} \frac{\frac{1}{x} + 2}{\frac{1}{x} - 2}$$
3. **Evaluate:** As $x \to \infty$, the terms with $\frac{1}{x}$ approach $0$:
   $$\frac{0 + 2}{0 - 2} = -1$$
**Final Answer:** $-1$

---

### (vii) $\lim_{x \to 0} \frac{e^{2x} - e^{-2x}}{\ln(1 + x)}$
1. **Identify the form:** At $x = 0$, we get $\frac{1 - 1}{\ln(1)} = \frac{0}{0}$.
2. **Apply L'Hôpital's Rule:** Differentiate the numerator (using chain rule) and the denominator:
   $$\lim_{x \to 0} \frac{2e^{2x} - (-2e^{-2x})}{\frac{1}{1+x}} = \lim_{x \to 0} \frac{2e^{2x} + 2e^{-2x}}{\frac{1}{1+x}}$$
3. **Simplify and Evaluate:** Rewrite the complex fraction and substitute $x = 0$:
   $$\lim_{x \to 0} (2e^{2x} + 2e^{-2x})(1 + x) = (2(1) + 2(1))(1 + 0) = 4$$
**Final Answer:** $4$

---

## Solutions for Problem 2: Integrals

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

### (ix) $\int \sin^2 x \cos^3 x dx$
1. **Identify the strategy:** Since the power of cosine is odd, save one cosine factor and convert the remaining $\cos^2 x$ to sines.
2. **Rewrite the integral:**
   $$\int \sin^2 x (\cos^2 x) \cos x dx = \int \sin^2 x (1 - \sin^2 x) \cos x dx$$
3. **Substitution:** Let $u = \sin x$, then $du = \cos x dx$.
4. **Integrate:**
   $$\int u^2 (1 - u^2) du = \int (u^2 - u^4) du = \frac{u^3}{3} - \frac{u^5}{5} + C$$
5. **Back-substitute:**
   $$\frac{\sin^3 x}{3} - \frac{\sin^5 x}{5} + C$$
**Final Answer:** $\frac{1}{3}\sin^3 x - \frac{1}{5}\sin^5 x + C$

---

### (x) $\int \frac{1}{1 - \cos 2\theta} d\theta$
1. **Apply Trig Identity:** Use $1 - \cos 2\theta = 2\sin^2 \theta$.
2. **Simplify:**
   $$\int \frac{1}{2\sin^2 \theta} d\theta = \frac{1}{2} \int \csc^2 \theta d\theta$$
3. **Integrate:** Recall that $\frac{d}{d\theta}(\cot \theta) = -\csc^2 \theta$.
   $$\frac{1}{2} (-\cot \theta) + C = -\frac{1}{2} \cot \theta + C$$
**Final Answer:** $-\frac{1}{2} \cot \theta + C$

---

### (xi) $\int_{0}^{2/3} \sqrt{4 - 9x^2} dx$
1. **Factor for Trig Substitution:** Rewrite the radicand as $4(1 - \frac{9}{4}x^2) = 4(1 - (\frac{3x}{2})^2)$.
2. **Substitution:** Let $\frac{3x}{2} = \sin \theta \implies x = \frac{2}{3}\sin \theta$. Then $dx = \frac{2}{3}\cos \theta d\theta$.
3. **Change limits:** - If $x = 0$, $\sin \theta = 0 \implies \theta = 0$.
   - If $x = 2/3$, $\sin \theta = 1 \implies \theta = \pi/2$.
4. **Simplify integral:** $\sqrt{4 - 9x^2} = \sqrt{4 - 4\sin^2 \theta} = 2\cos \theta$.
   $$\int_{0}^{\pi/2} (2\cos \theta) (\frac{2}{3}\cos \theta) d\theta = \frac{4}{3} \int_{0}^{\pi/2} \cos^2 \theta d\theta$$
5. **Use power-reduction:** $\cos^2 \theta = \frac{1 + \cos 2\theta}{2}$.
   $$\frac{4}{3} \int_{0}^{\pi/2} \frac{1 + \cos 2\theta}{2} d\theta = \frac{2}{3} \left[ \theta + \frac{1}{2}\sin 2\theta \right]_{0}^{\pi/2}$$
6. **Evaluate:** $\frac{2}{3} [(\frac{\pi}{2} + 0) - (0 + 0)] = \frac{\pi}{3}$.
**Final Answer:** $\frac{\pi}{3}$

---

### (xii) $\int \frac{x^3}{\sqrt{9 + x^2}} dx$
1. **Trig Substitution:** Let $x = 3\tan \theta$, so $dx = 3\sec^2 \theta d\theta$ and $\sqrt{9+x^2} = 3\sec \theta$.
2. **Rewrite integral:**
   $$\int \frac{(27\tan^3 \theta)(3\sec^2 \theta)}{3\sec \theta} d\theta = 27 \int \tan^3 \theta \sec \theta d\theta$$
3. **Integrate Powers of Tangent/Secant:** Separate $\sec \theta \tan \theta$.
   $$27 \int \tan^2 \theta (\sec \theta \tan \theta) d\theta = 27 \int (\sec^2 \theta - 1) \sec \theta \tan \theta d\theta$$
4. **Substitution:** Let $u = \sec \theta$, $du = \sec \theta \tan \theta d\theta$.
   $$27 \int (u^2 - 1) du = 27 (\frac{u^3}{3} - u) = 9u^3 - 27u + C$$
5. **Back-substitute:** $u = \sec \theta = \frac{\sqrt{9+x^2}}{3}$.
   $$9(\frac{\sqrt{9+x^2}}{3})^3 - 27(\frac{\sqrt{9+x^2}}{3}) = \frac{1}{3}(9+x^2)^{3/2} - 9\sqrt{9+x^2} + C$$
**Final Answer:** $\frac{1}{3}(9+x^2)^{3/2} - 9\sqrt{9+x^2} + C$

---

### (xiii) $\int x\sqrt{1 - x^4} dx$
1. **Substitution:** Let $u = x^2$, so $du = 2x dx$ or $\frac{1}{2}du = x dx$.
2. **Rewrite:** $\frac{1}{2} \int \sqrt{1 - u^2} du$.
3. **Use Formula/Trig Sub:** The integral $\int \sqrt{a^2 - u^2} du = \frac{u}{2}\sqrt{a^2-u^2} + \frac{a^2}{2}\arcsin(\frac{u}{a})$.
4. **Apply to $u$:**
   $$\frac{1}{2} \left[ \frac{u}{2}\sqrt{1-u^2} + \frac{1}{2}\arcsin(u) \right] + C$$
5. **Back-substitute:** $u = x^2$.
   $$\frac{1}{4} x^2\sqrt{1-x^4} + \frac{1}{4}\arcsin(x^2) + C$$
**Final Answer:** $\frac{1}{4}(x^2\sqrt{1-x^4} + \arcsin(x^2)) + C$

---

### (xiv) $\int_{0}^{1} \frac{1}{(x - 1)^2} dx$
1. **Identify as Improper Integral:** The function is undefined at the upper bound $x = 1$.
2. **Set up limit:** $\lim_{t \to 1^-} \int_{0}^{t} (x - 1)^{-2} dx$.
3. **Integrate:**
   $$\lim_{t \to 1^-} \left[ \frac{(x-1)^{-1}}{-1} \right]_{0}^{t} = \lim_{t \to 1^-} \left[ -\frac{1}{x-1} \right]_{0}^{t}$$
4. **Evaluate limit:**
   $$\lim_{t \to 1^-} \left( -\frac{1}{t-1} - (-\frac{1}{0-1}) \right) = \lim_{t \to 1^-} \left( -\frac{1}{t-1} - 1 \right)$$
5. **Conclusion:** As $t \to 1^-$, $(t-1)$ is a small negative number, so $-\frac{1}{t-1} \to \infty$.
**Final Answer:** Diverges

---

### (xv) $\int \frac{1}{x^2 + 2x - 3} dx$
1. **Factor the denominator:** $x^2 + 2x - 3 = (x + 3)(x - 1)$.
2. **Partial Fraction Decomposition:**
   $$\frac{1}{(x+3)(x-1)} = \frac{A}{x+3} + \frac{B}{x-1}$$
3. **Solve for constants:** $1 = A(x-1) + B(x+3)$.
   - If $x = 1$, $1 = 4B \implies B = 1/4$.
   - If $x = -3$, $1 = -4A \implies A = -1/4$.
4. **Integrate:**
   $$\int \left( \frac{-1/4}{x+3} + \frac{1/4}{x-1} \right) dx = -\frac{1}{4}\ln|x+3| + \frac{1}{4}\ln|x-1| + C$$
5. **Simplify using log rules:** $\frac{1}{4}\ln\left|\frac{x-1}{x+3}\right| + C$.
**Final Answer:** $\frac{1}{4}\ln\left|\frac{x-1}{x+3}\right| + C$

---

### (xvi) $\int \frac{3x + 2}{x^3 + 4x} dx$
1. **Factor denominator:** $x(x^2 + 4)$.
2. **Partial Fraction Decomposition:**
   $$\frac{3x + 2}{x(x^2 + 4)} = \frac{A}{x} + \frac{Bx + C}{x^2 + 4}$$
3. **Solve for constants:** $3x + 2 = A(x^2 + 4) + (Bx + C)x$.
   - If $x = 0$, $2 = 4A \implies A = 1/2$.
   - Compare $x^2$ terms: $0 = A + B \implies B = -1/2$.
   - Compare $x$ terms: $3 = C \implies C = 3$.
4. **Split and Integrate:**
   $$\int \frac{1/2}{x} dx + \int \frac{-1/2x}{x^2+4} dx + \int \frac{3}{x^2+4} dx$$
5. **Evaluate each:**
   - $\frac{1}{2}\ln|x|$
   - $-\frac{1}{4}\ln(x^2+4)$ (using $u$-sub $u = x^2+4$)
   - $\frac{3}{2}\arctan(\frac{x}{2})$ (using standard $\arctan$ form)
**Final Answer:** $\frac{1}{2}\ln|x| - \frac{1}{4}\ln(x^2+4) + \frac{3}{2}\arctan(\frac{x}{2}) + C$

## Solutions: Additional Definite Integrals

### (i) $\int_{0}^{1} \frac{x}{1 + x^2} dx$
1. **Substitution:** Let $u = 1 + x^2$. Then $du = 2x dx$, which means $\frac{1}{2}du = x dx$.
2. **Change limits:** - When $x = 0$, $u = 1 + 0^2 = 1$.
   - When $x = 1$, $u = 1 + 1^2 = 2$.
3. **Integrate:**
   $$\frac{1}{2} \int_{1}^{2} \frac{1}{u} du = \frac{1}{2} \left[ \ln|u| \right]_{1}^{2}$$
4. **Evaluate:**
   $$\frac{1}{2} (\ln 2 - \ln 1) = \frac{1}{2} (\ln 2 - 0) = \frac{1}{2} \ln 2$$
**Final Answer:** $\frac{1}{2} \ln 2$

---

### (ii) $\int_{0}^{\pi/2} \sin^3 x dx$
1. **Identify the strategy:** Use the identity $\sin^2 x = 1 - \cos^2 x$ to rewrite the integral.
   $$\int_{0}^{\pi/2} \sin^2 x \cdot \sin x dx = \int_{0}^{\pi/2} (1 - \cos^2 x) \sin x dx$$
2. **Substitution:** Let $u = \cos x$, then $du = -\sin x dx$, or $-du = \sin x dx$.
3. **Change limits:** - When $x = 0$, $u = \cos(0) = 1$.
   - When $x = \pi/2$, $u = \cos(\pi/2) = 0$.
4. **Integrate:** (Reverse limits to remove the negative sign)
   $$\int_{1}^{0} -(1 - u^2) du = \int_{0}^{1} (1 - u^2) du = \left[ u - \frac{1}{3}u^3 \right]_{0}^{1}$$
5. **Evaluate:**
   $$(1 - \frac{1}{3}) - (0 - 0) = \frac{2}{3}$$
**Final Answer:** $\frac{2}{3}$

---

### (iii) $\int_{0}^{1} \frac{1}{\sqrt{1 - x^2}} dx$
1. **Identify the form:** This is the standard derivative of $\arcsin x$.
2. **Note on improper integration:** The function is undefined at $x = 1$, so we treat it as a limit:
   $$\lim_{t \to 1^-} \int_{0}^{t} \frac{1}{\sqrt{1 - x^2}} dx$$
3. **Integrate:**
   $$\lim_{t \to 1^-} \left[ \arcsin x \right]_{0}^{t} = \arcsin(1) - \arcsin(0)$$
4. **Evaluate:**
   $$\frac{\pi}{2} - 0 = \frac{\pi}{2}$$
**Final Answer:** $\frac{\pi}{2}$

---

### (iv) $\int_{0}^{1} \frac{1}{(x + 1)^2} dx$
1. **Rewrite for power rule:** $\int_{0}^{1} (x + 1)^{-2} dx$.
2. **Integrate:** Using $u = x + 1$ (where $du = dx$):
   $$\left[ \frac{(x + 1)^{-1}}{-1} \right]_{0}^{1} = \left[ -\frac{1}{x + 1} \right]_{0}^{1}$$
3. **Evaluate:**
   $$\left( -\frac{1}{1 + 1} \right) - \left( -\frac{1}{0 + 1} \right) = -\frac{1}{2} - (-1)$$
4. **Simplify:**
   $$-\frac{1}{2} + 1 = \frac{1}{2}$$
**Final Answer:** $\frac{1}{2}$

## Solutions for Problem 3: Improper Integrals

### (i) $\int_{1}^{\infty} \frac{dx}{(x + 2)^2}$
1. **Set up the limit:** Rewrite the improper integral using a limit:
   $$\lim_{t \to \infty} \int_{1}^{t} (x + 2)^{-2} dx$$
2. **Integrate:**
   $$\lim_{t \to \infty} \left[ \frac{(x + 2)^{-1}}{-1} \right]_{1}^{t} = \lim_{t \to \infty} \left[ -\frac{1}{x + 2} \right]_{1}^{t}$$
3. **Evaluate the limit:**
   $$\lim_{t \to \infty} \left( -\frac{1}{t + 2} - (-\frac{1}{1 + 2}) \right) = 0 + \frac{1}{3} = \frac{1}{3}$$
**Final Answer:** $1/3$

---

### (ii) $\int_{0}^{\infty} \frac{dx}{x^2 + 4}$
1. **Identify the form:** This matches $\int \frac{1}{x^2 + a^2} dx = \frac{1}{a} \arctan(\frac{x}{a})$. Here $a=2$.
2. **Set up the limit:**
   $$\lim_{t \to \infty} \int_{0}^{t} \frac{1}{x^2 + 2^2} dx = \lim_{t \to \infty} \left[ \frac{1}{2} \arctan\left(\frac{x}{2}\right) \right]_{0}^{t}$$
3. **Evaluate the limit:**
   $$\frac{1}{2} \left( \lim_{t \to \infty} \arctan\left(\frac{t}{2}\right) - \arctan(0) \right) = \frac{1}{2} \left( \frac{\pi}{2} - 0 \right) = \frac{\pi}{4}$$
**Final Answer:** $\pi/4$

---

### (iii) $\int_{-2}^{\infty} \frac{dx}{x^2 + 6x + 13}$
1. **Complete the square:** $x^2 + 6x + 13 = (x^2 + 6x + 9) + 4 = (x + 3)^2 + 2^2$.
2. **Set up the limit:**
   $$\lim_{t \to \infty} \int_{-2}^{t} \frac{1}{(x + 3)^2 + 2^2} dx$$
3. **Integrate:** Use the $\arctan$ formula with $u = x+3$:
   $$\lim_{t \to \infty} \left[ \frac{1}{2} \arctan\left(\frac{x+3}{2}\right) \right]_{-2}^{t}$$
4. **Evaluate:**
   $$\frac{1}{2} \left( \frac{\pi}{2} - \arctan\left(\frac{-2+3}{2}\right) \right) = \frac{1}{2} \left( \frac{\pi}{2} - \arctan\left(\frac{1}{2}\right) \right) = \frac{\pi}{4} - \frac{1}{2}\arctan\left(\frac{1}{2}\right)$$
**Final Answer:** $\frac{\pi}{4} - \frac{1}{2}\arctan(1/2)$

---

### (iv) $\int_{2}^{\infty} \frac{1}{x^2 + 2x - 3} dx$
1. **Partial Fractions:** From Problem 2(xv), we know $\frac{1}{x^2 + 2x - 3} = \frac{1}{4(x-1)} - \frac{1}{4(x+3)}$.
2. **Set up the limit:**
   $$\lim_{t \to \infty} \left[ \frac{1}{4} \ln|x - 1| - \frac{1}{4} \ln|x + 3| \right]_{2}^{t} = \lim_{t \to \infty} \left[ \frac{1}{4} \ln\left| \frac{x - 1}{x + 3} \right| \right]_{2}^{t}$$
3. **Evaluate the limit:**
   - As $t \to \infty$, $\frac{t-1}{t+3} \to 1$, and $\ln(1) = 0$.
   - At $x = 2$, $\frac{1}{4} \ln\left| \frac{2-1}{2+3} \right| = \frac{1}{4} \ln(1/5)$.
4. **Final Calculation:**
   $$0 - \frac{1}{4} \ln(1/5) = - \frac{1}{4} (-\ln 5) = \frac{1}{4} \ln 5$$
**Final Answer:** $\frac{1}{4} \ln 5$

---

### (v) $\int_{0}^{\infty} xe^{-x} dx$
1. **Integration by Parts:** Let $u = x, dv = e^{-x} dx$. Then $du = dx, v = -e^{-x}$.
2. **Evaluate limit:**
   $$\lim_{t \to \infty} \left( [-xe^{-x}]_{0}^{t} + \int_{0}^{t} e^{-x} dx \right) = \lim_{t \to \infty} \left( -te^{-t} + 0 + [-e^{-x}]_{0}^{t} \right)$$
3. **Solve:** Since $\lim_{t \to \infty} \frac{t}{e^t} = 0$ (by L'Hôpital) and $e^{-\infty} = 0$:
   $$(0) + (0 - (-e^0)) = 1$$
**Final Answer:** $1$

---

### (vi) $\int_{0}^{\infty} \frac{dx}{(2x + 1)^3}$
1. **Substitution:** Let $u = 2x + 1, du = 2 dx$.
2. **Change limits:** $x=0 \to u=1$; $x \to \infty \to u \to \infty$.
3. **Integrate:**
   $$\frac{1}{2} \int_{1}^{\infty} u^{-3} du = \frac{1}{2} \left[ \frac{u^{-2}}{-2} \right]_{1}^{\infty} = -\frac{1}{4} \left[ \frac{1}{u^2} \right]_{1}^{\infty}$$
4. **Evaluate:** $-\frac{1}{4} (0 - 1) = \frac{1}{4}$.
**Final Answer:** $1/4$

---

### (vii) $\int_{2}^{\infty} \frac{dx}{x \ln x}$
1. **Identify the form:** This is an improper integral due to the infinite upper limit.
2. **Set up the limit:**
   $$\lim_{t \to \infty} \int_{2}^{t} \frac{1}{x \ln x} dx$$
3. **Substitution:** Let $u = \ln x$. Then $du = \frac{1}{x} dx$.
4. **Change limits:**
   - When $x = 2$, $u = \ln 2$.
   - As $x \to \infty$, $u \to \infty$.
5. **Integrate:**
   $$\lim_{t \to \infty} \int_{\ln 2}^{\ln t} \frac{1}{u} du = \lim_{t \to \infty} \left[ \ln|u| \right]_{\ln 2}^{\ln t}$$
6. **Evaluate the limit:**
   $$\lim_{t \to \infty} \left( \ln(\ln t) - \ln(\ln 2) \right)$$
7. **Conclusion:** As $t \to \infty$, $\ln t \to \infty$, and $\ln(\ln t)$ also approaches $\infty$. Since the limit does not result in a finite number, the integral diverges.
**Final Answer:** Diverges


---

### (viii) $\int_{2}^{6} \frac{y}{\sqrt{y - 2}} dy$
1. **Identify as Improper:** Function is undefined at $y = 2$.
2. **Substitution:** Let $u = y - 2 \implies y = u + 2, dy = du$.
3. **Change limits:** $y=2 \to u=0$; $y=6 \to u=4$.
4. **Integrate:**
   $$\int_{0}^{4} \frac{u + 2}{\sqrt{u}} du = \int_{0}^{4} (u^{1/2} + 2u^{-1/2}) du = \left[ \frac{2}{3}u^{3/2} + 4u^{1/2} \right]_{0}^{4}$$
5. **Evaluate:**
   $$\left( \frac{2}{3}(4)^{3/2} + 4(4)^{1/2} \right) - 0 = \frac{2}{3}(8) + 4(2) = \frac{16}{3} + 8 = \frac{40}{3}$$
**Final Answer:** $40/3$

---

### (ix) $\int_{0}^{1} \frac{x - 1}{\sqrt{x}} dx$
1. **Identify as Improper:** Undefined at $x = 0$.
2. **Simplify:**
   $$\int_{0}^{1} (x^{1/2} - x^{-1/2}) dx = \left[ \frac{2}{3}x^{3/2} - 2x^{1/2} \right]_{0}^{1}$$
3. **Evaluate:**
   $$(\frac{2}{3} - 2) - (0 - 0) = -\frac{4}{3}$$
**Final Answer:** $-4/3$

### (i) $\int_{1}^{\infty} \frac{dx}{(x + 2)^2}$
1. **Set up the limit:** Rewrite the improper integral:
   $$\lim_{t \to \infty} \int_{1}^{t} (x + 2)^{-2} dx$$
2. **Integrate:**
   $$\lim_{t \to \infty} \left[ -\frac{1}{x + 2} \right]_{1}^{t}$$
3. **Evaluate the limit:**
   $$\lim_{t \to \infty} \left( -\frac{1}{t + 2} - \left( -\frac{1}{1 + 2} \right) \right) = 0 + \frac{1}{3} = \frac{1}{3}$$
**Final Answer:** $1/3$

---

### (iv) $\int_{2}^{\infty} \frac{1}{x^2 + 2x - 3} dx$
1. **Partial Fractions:** From previous steps, we know the integrand is $\frac{1}{4(x-1)} - \frac{1}{4(x+3)}$.
2. **Set up the limit:**
   $$\lim_{t \to \infty} \int_{2}^{t} \left( \frac{1}{4(x-1)} - \frac{1}{4(x+3)} \right) dx$$
3. **Integrate and combine logs:**
   $$\lim_{t \to \infty} \left[ \frac{1}{4} \ln \left| \frac{x-1}{x+3} \right| \right]_{2}^{t}$$
4. **Evaluate the limit:**
   - As $t \to \infty$, the fraction $\frac{t-1}{t+3} \to 1$, and $\ln(1) = 0$.
   - At $x = 2$, we have $\frac{1}{4} \ln \left| \frac{2-1}{2+3} \right| = \frac{1}{4} \ln(1/5)$.
5. **Final Step:**
   $$0 - \frac{1}{4} \ln(1/5) = \frac{1}{4} \ln(5)$$
**Final Answer:** $\frac{1}{4} \ln 5$

---

### (v) $\int_{0}^{\infty} xe^{-x} dx$
1. **Integration by Parts:** Let $u = x$ and $dv = e^{-x} dx$, which gives $du = dx$ and $v = -e^{-x}$.
2. **Apply the formula:**
   $$\lim_{t \to \infty} \left( \left[ -xe^{-x} \right]_{0}^{t} + \int_{0}^{t} e^{-x} dx \right)$$
3. **Integrate the second term:**
   $$\lim_{t \to \infty} \left( \left[ -xe^{-x} \right]_{0}^{t} + \left[ -e^{-x} \right]_{0}^{t} \right)$$
4. **Evaluate the limit:** - $\lim_{t \to \infty} \frac{-t}{e^t} = 0$ (by L'Hôpital's Rule).
   - $\lim_{t \to \infty} -e^{-t} = 0$.
   - Evaluation at $0$: $(0) + (-e^0) = -1$.
5. **Combine:** $(0 - 0) - (0 - 1) = 1$.
**Final Answer:** $1$

---

### (vi) $\int_{0}^{\infty} \frac{dx}{(2x + 1)^3}$
1. **Substitution:** Let $u = 2x + 1$, then $du = 2 dx$ (or $dx = \frac{1}{2} du$).
2. **Change limits:** When $x=0, u=1$. When $x \to \infty, u \to \infty$.
3. **Integrate:**
   $$\frac{1}{2} \int_{1}^{\infty} u^{-3} du = \frac{1}{2} \left[ \frac{u^{-2}}{-2} \right]_{1}^{\infty}$$
4. **Evaluate:**
   $$\lim_{t \to \infty} -\frac{1}{4} \left( \frac{1}{t^2} - \frac{1}{1^2} \right) = -\frac{1}{4} (0 - 1) = \frac{1}{4}$$
**Final Answer:** $1/4$
