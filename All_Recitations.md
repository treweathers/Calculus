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
1. **Set up the limit:** Rewrite the improper integral:
   $$\lim_{t \to \infty} \int_{1}^{t} (x + 2)^{-2} dx$$
2. **Integrate:**
   $$\lim_{t \to \infty} \left[ -\frac{1}{x + 2} \right]_{1}^{t}$$
3. **Evaluate the limit:**
   $$\lim_{t \to \infty} \left( -\frac{1}{t + 2} - \left( -\frac{1}{1 + 2} \right) \right) = 0 + \frac{1}{3} = \frac{1}{3}$$
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

### (v) $\int_{0}^{\infty} xe^{-x} dx$
1. **Integration by Parts:** Let $u = x, dv = e^{-x} dx$. Then $du = dx, v = -e^{-x}$.
2. **Evaluate limit:**
   $$\lim_{t \to \infty} \left( [-xe^{-x}]_{0}^{t} + \int_{0}^{t} e^{-x} dx \right) = \lim_{t \to \infty} \left( -te^{-t} + 0 + [-e^{-x}]_{0}^{t} \right)$$
3. **Solve:** Since $\lim_{t \to \infty} \frac{t}{e^t} = 0$ (by L'Hôpital) and $e^{-\infty} = 0$:
   $$(0) + (0 - (-e^0)) = 1$$
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

## Solutions for Problem 4: Area and Volume

### (i) Find the area between the curve $y = \ln x$ and the $x$-axis over the interval $(0,1]$.
1. **Set up the integral:** Since $\ln x$ is negative on $(0,1)$, the area is given by $\int_{0}^{1} | \ln x | dx = -\int_{0}^{1} \ln x dx$. 
2. **Identify as Improper:** There is a vertical asymptote at $x = 0$.
   $$\text{Area} = \lim_{t \to 0^+} \left( -\int_{t}^{1} \ln x dx \right)$$
3. **Integrate by Parts:** Using $\int \ln x dx = x \ln x - x$:
   $$\lim_{t \to 0^+} \left[ -(x \ln x - x) \right]_{t}^{1} = \lim_{t \to 0^+} \left[ x - x \ln x \right]_{t}^{1}$$
4. **Evaluate at the upper bound:** At $x=1$, we get $1 - 1 \ln(1) = 1 - 0 = 1$.
5. **Evaluate the limit at the lower bound:** We need $\lim_{t \to 0^+} (t - t \ln t)$.
   - $\lim_{t \to 0^+} t = 0$.
   - $\lim_{t \to 0^+} t \ln t$ is a $0 \cdot (-\infty)$ form. Rewrite as $\frac{\ln t}{1/t}$ and use L'Hôpital:
     $$\lim_{t \to 0^+} \frac{1/t}{-1/t^2} = \lim_{t \to 0^+} (-t) = 0$$
6. **Final Answer:** $1 - (0 - 0) = 1$.
**Final Answer:** The area is $1$.

---

### (ii) Find the volume of Gabriel’s Horn, obtained by rotating $y = 1/x, x \geq 1$ around the $x$-axis.
1. **Use the Disk Method:** The formula for volume rotated around the $x$-axis is $V = \pi \int_{a}^{b} [f(x)]^2 dx$.
2. **Set up the improper integral:**
   $$V = \pi \int_{1}^{\infty} \left( \frac{1}{x} \right)^2 dx = \pi \int_{1}^{\infty} x^{-2} dx$$
3. **Apply the limit:**
   $$\lim_{t \to \infty} \pi \int_{1}^{t} x^{-2} dx = \lim_{t \to \infty} \pi \left[ -\frac{1}{x} \right]_{1}^{t}$$
4. **Evaluate:**
   $$\pi \left( \lim_{t \to \infty} \left( -\frac{1}{t} \right) - \left( -\frac{1}{1} \right) \right) = \pi (0 + 1) = \pi$$
**Final Answer:** The volume is $\pi$.

## Solutions for Problem 5: Length of the Curve

### (i) $y = \sqrt{4 - x^2}, 0 \le x \le 2$
1. **Identify the curve:** The equation $y^2 = 4 - x^2 \implies x^2 + y^2 = 4$ represents a circle with radius $r = 2$. For $0 \le x \le 2$, this is a quarter-circle in the first quadrant.
2. **Geometric approach:** The circumference of a full circle is $2\pi r$. A quarter circle is:
   $$L = \frac{1}{4}(2\pi r) = \frac{1}{2}\pi(2) = \pi$$
3. **Calculus approach:** Find $y' = \frac{1}{2}(4-x^2)^{-1/2}(-2x) = \frac{-x}{\sqrt{4-x^2}}$.
4. **Set up the integral:**
   $$L = \int_{0}^{2} \sqrt{1 + \left(\frac{-x}{\sqrt{4-x^2}}\right)^2} dx = \int_{0}^{2} \sqrt{1 + \frac{x^2}{4-x^2}} dx$$
5. **Simplify:** $\sqrt{\frac{4-x^2+x^2}{4-x^2}} = \sqrt{\frac{4}{4-x^2}} = \frac{2}{\sqrt{4-x^2}}$.
6. **Integrate:** $\int_{0}^{2} \frac{2}{\sqrt{4-x^2}} dx = \left[ 2\arcsin\left(\frac{x}{2}\right) \right]_{0}^{2} = 2(\frac{\pi}{2} - 0) = \pi$.
**Final Answer:** $\pi$

---

### (ii) $y = \frac{2}{3}x^{3/2}, 0 \le x \le 2$
1. **Find the derivative:** $y' = \frac{2}{3} \cdot \frac{3}{2}x^{1/2} = x^{1/2} = \sqrt{x}$.
2. **Set up the arc length integral:**
   $$L = \int_{0}^{2} \sqrt{1 + (\sqrt{x})^2} dx = \int_{0}^{2} \sqrt{1 + x} dx$$
3. **Integrate:** Use $u$-substitution $u = 1+x$:
   $$\int_{0}^{2} (1+x)^{1/2} dx = \left[ \frac{2}{3}(1+x)^{3/2} \right]_{0}^{2}$$
4. **Evaluate:**
   $$\frac{2}{3}(1+2)^{3/2} - \frac{2}{3}(1+0)^{3/2} = \frac{2}{3}(3\sqrt{3} - 1)$$
**Final Answer:** $\frac{2}{3}(3\sqrt{3} - 1)$

---

### (iii) $y = \frac{x^3}{3} + \frac{1}{4x}$
1. **Find the derivative:** $y' = x^2 - \frac{1}{4x^2}$.
2. **Simplify the term $1 + (y')^2$:**
   $$1 + (x^2 - \frac{1}{4x^2})^2 = 1 + x^4 - 2(x^2)(\frac{1}{4x^2}) + \frac{1}{16x^4} = 1 + x^4 - \frac{1}{2} + \frac{1}{16x^4}$$
   $$= x^4 + \frac{1}{2} + \frac{1}{16x^4} = (x^2 + \frac{1}{4x^2})^2$$
3. **Set up the integral:**
   $$L = \int \sqrt{(x^2 + \frac{1}{4x^2})^2} dx = \int (x^2 + \frac{1}{4x^2}) dx$$
4. **Integrate:**
   $$\frac{x^3}{3} - \frac{1}{4x} + C$$
**Final Answer:** $\frac{x^3}{3} - \frac{1}{4x} + C$ (Note: Bounds were not provided in the prompt for this sub-problem).

---

### (iv) $r = 2 + \theta$
1. **Identify the formula:** For polar curves, $L = \int \sqrt{r^2 + (\frac{dr}{d\theta})^2} d\theta$.
2. **Find the derivative:** $\frac{dr}{d\theta} = 1$.
3. **Simplify the radicand:**
   $$r^2 + (\frac{dr}{d\theta})^2 = (2 + \theta)^2 + 1^2 = \theta^2 + 4\theta + 5$$
4. **Set up the integral:**
   $$L = \int \sqrt{\theta^2 + 4\theta + 5} d\theta$$
**Final Answer:** $\int \sqrt{\theta^2 + 4\theta + 5} d\theta$ (This usually requires trigonometric substitution to solve fully).

## Solutions for Problem 6: Parametric Equations

Let the curve $C$ be given by: $x = 2\sin t$, $y = 2\cos^2 t$, where $-\pi/2 < t < \pi/2$.

### (i) Find $dy/dx$, the slope at $t = \pi/4$, and the tangent line equation.
1. **Find derivatives with respect to $t$:**
   - $\frac{dx}{dt} = 2\cos t$
   - $\frac{dy}{dt} = 4\cos t (-\sin t) = -4\sin t \cos t$
2. **Find $dy/dx$:**
   $$\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{-4\sin t \cos t}{2\cos t} = -2\sin t$$
3. **Calculate slope at $t = \pi/4$:**
   $$m = -2\sin(\pi/4) = -2\left(\frac{\sqrt{2}}{2}\right) = -\sqrt{2}$$
4. **Find the point $(x, y)$ at $t = \pi/4$:**
   - $x = 2\sin(\pi/4) = \sqrt{2}$
   - $y = 2\cos^2(\pi/4) = 2(1/2) = 1$
5. **Tangent Line Equation:** Using $y - y_1 = m(x - x_1)$:
   $$y - 1 = -\sqrt{2}(x - \sqrt{2}) \implies y = -\sqrt{2}x + 2 + 1 \implies y = -\sqrt{2}x + 3$$

---

### (ii) Find $d^2y/dx^2$ at any $t$.
1. **Use the formula for the second derivative of parametric equations:**
   $$\frac{d^2y}{dx^2} = \frac{\frac{d}{dt}\left(\frac{dy}{dx}\right)}{\frac{dx}{dt}}$$
2. **Differentiate $dy/dx$ with respect to $t$:**
   $$\frac{d}{dt}(-2\sin t) = -2\cos t$$
3. **Divide by $dx/dt$:**
   $$\frac{-2\cos t}{2\cos t} = -1$$
**Final Answer:** $-1$

---

### (iii) Find the Cartesian equation of the curve.
1. **Express trig functions in terms of $x$:**
   From $x = 2\sin t$, we get $\sin t = \frac{x}{2}$.
2. **Use the Pythagorean Identity:** $\cos^2 t = 1 - \sin^2 t$.
3. **Substitute into the $y$ equation:**
   $$y = 2(1 - \sin^2 t) = 2\left(1 - \left(\frac{x}{2}\right)^2\right)$$
   $$y = 2\left(1 - \frac{x^2}{4}\right) = 2 - \frac{x^2}{2}$$
**Final Answer:** $y = 2 - \frac{1}{2}x^2$ (This is a parabola opening downward).

---

### (iv) Find the area between the curve $C$ and the $x$-axis.
1. **Identify the limits for $x$:**
   As $t$ goes from $-\pi/2$ to $\pi/2$, $x$ goes from $2\sin(-\pi/2) = -2$ to $2\sin(\pi/2) = 2$.
2. **Set up the parametric area integral:** $A = \int_{t_1}^{t_2} y(t) \cdot x'(t) dt$.
   $$A = \int_{-\pi/2}^{\pi/2} (2\cos^2 t)(2\cos t) dt = 4 \int_{-\pi/2}^{\pi/2} \cos^3 t dt$$
3. **Integrate $\cos^3 t$:** Use $\cos^2 t = 1 - \sin^2 t$.
   $$4 \int_{-\pi/2}^{\pi/2} (1 - \sin^2 t)\cos t dt$$
4. **Use $u$-substitution:** $u = \sin t, du = \cos t dt$. Limits become $-1$ to $1$.
   $$4 \left[ u - \frac{u^3}{3} \right]_{-1}^{1} = 4 \left[ (1 - \frac{1}{3}) - (-1 + \frac{1}{3}) \right] = 4 \left[ \frac{2}{3} + \frac{2}{3} \right] = \frac{16}{3}$$
**Final Answer:** $16/3$

---

### (v) Find the length of the curve $C$.
1. **Set up the arc length integral:** $L = \int_{-\pi/2}^{\pi/2} \sqrt{(x')^2 + (y')^2} dt$.
2. **Calculate $(x')^2 + (y')^2$:**
   $$(2\cos t)^2 + (-4\sin t \cos t)^2 = 4\cos^2 t + 16\sin^2 t \cos^2 t = 4\cos^2 t(1 + 4\sin^2 t)$$
3. **Simplify the integral:**
   $$L = \int_{-\pi/2}^{\pi/2} 2\cos t \sqrt{1 + 4\sin^2 t} dt$$
4. **Substitution:** $u = 2\sin t, du = 2\cos t dt$. Limits: $t=-\pi/2 \to u=-2$, $t=\pi/2 \to u=2$.
   $$L = \int_{-2}^{2} \sqrt{1 + u^2} du$$
5. **Evaluate using the formula for $\int \sqrt{a^2+u^2}du$:**
   $$\left[ \frac{u}{2}\sqrt{1+u^2} + \frac{1}{2}\ln|u + \sqrt{1+u^2}| \right]_{-2}^{2}$$
   $$= \left( \sqrt{5} + \frac{1}{2}\ln(2+\sqrt{5}) \right) - \left( -\sqrt{5} + \frac{1}{2}\ln(-2+\sqrt{5}) \right)$$
   $$= 2\sqrt{5} + \ln(2+\sqrt{5})$$
**Final Answer:** $2\sqrt{5} + \ln(2+\sqrt{5})$

## Solutions for Problem 7: Area of Parametric Curves

The area $A$ under a parametric curve is given by $A = \int_{t_1}^{t_2} y(t) \cdot x'(t) \, dt$.

---

### (i) $x = t^3 + 1, \quad y = 2t - t^2$
1. **Find $x'(t)$:**
   $$\frac{dx}{dt} = 3t^2$$
2. **Identify the limits for $t$:**
   The curve intersects the $x$-axis when $y = 0$.
   $$2t - t^2 = 0 \implies t(2 - t) = 0 \implies t = 0 \text{ and } t = 2$$
3. **Set up the integral:**
   $$A = \int_{0}^{2} (2t - t^2)(3t^2) \, dt$$
4. **Distribute and Integrate:**
   $$A = \int_{0}^{2} (6t^3 - 3t^4) \, dt = \left[ \frac{6t^4}{4} - \frac{3t^5}{5} \right]_{0}^{2}$$
5. **Evaluate:**
   $$\left( \frac{3(2^4)}{2} - \frac{3(2^5)}{5} \right) = \left( 24 - \frac{96}{5} \right) = \frac{120 - 96}{5} = \frac{24}{5}$$
**Final Answer:** $24/5$

---

### (ii) $x = \sin t, \quad y = \sin t \cos t, \quad 0 \le t \le \pi/2$
1. **Find $x'(t)$:**
   $$\frac{dx}{dt} = \cos t$$
2. **Set up the integral:**
   $$A = \int_{0}^{\pi/2} (\sin t \cos t)(\cos t) \, dt = \int_{0}^{\pi/2} \sin t \cos^2 t \, dt$$
3. **Use $u$-substitution:**
   Let $u = \cos t$, then $du = -\sin t \, dt$, so $-du = \sin t \, dt$.
4. **Change limits:**
   - When $t = 0, u = \cos(0) = 1$.
   - When $t = \pi/2, u = \cos(\pi/2) = 0$.
5. **Integrate:**
   $$\int_{1}^{0} u^2 (-du) = \int_{0}^{1} u^2 \, du$$
6. **Evaluate:**
   $$\left[ \frac{u^3}{3} \right]_{0}^{1} = \frac{1}{3} - 0 = \frac{1}{3}$$
**Final Answer:** $1/3$

## Solutions for Problem 8: Polar Coordinates

Let the curve $C$ be defined by $r = 1 + \cos\theta$.

### (i) Find an equation of the tangent line to $C$ at $\theta = \pi/4$.
1. **Find $r$ and $dr/d\theta$ at $\theta = \pi/4$:**
   - $r = 1 + \cos(\pi/4) = 1 + \frac{\sqrt{2}}{2}$
   - $\frac{dr}{d\theta} = -\sin\theta \implies \frac{dr}{d\theta}\Big|_{\pi/4} = -\frac{\sqrt{2}}{2}$
2. **Use the parametric slope formula for polar curves:**
   $$\frac{dy}{dx} = \frac{\frac{dr}{d\theta}\sin\theta + r\cos\theta}{\frac{dr}{d\theta}\cos\theta - r\sin\theta}$$
3. **Substitute values:**
   $$\frac{dy}{dx} = \frac{(-\frac{\sqrt{2}}{2})(\frac{\sqrt{2}}{2}) + (1 + \frac{\sqrt{2}}{2})(\frac{\sqrt{2}}{2})}{(-\frac{\sqrt{2}}{2})(\frac{\sqrt{2}}{2}) - (1 + \frac{\sqrt{2}}{2})(\frac{\sqrt{2}}{2})}$$
   - Numerator: $-\frac{1}{2} + \frac{\sqrt{2}}{2} + \frac{1}{2} = \frac{\sqrt{2}}{2}$
   - Denominator: $-\frac{1}{2} - \frac{\sqrt{2}}{2} - \frac{1}{2} = -1 - \frac{\sqrt{2}}{2}$
4. **Simplify the slope ($m$):**
   $$m = \frac{\frac{\sqrt{2}}{2}}{-\frac{2+\sqrt{2}}{2}} = -\frac{\sqrt{2}}{2+\sqrt{2}}$$
   Rationalizing gives $m = 1 - \sqrt{2}$.
5. **Find Cartesian coordinates $(x, y)$:**
   - $x = r\cos\theta = (1 + \frac{\sqrt{2}}{2})(\frac{\sqrt{2}}{2}) = \frac{\sqrt{2}}{2} + \frac{1}{2}$
   - $y = r\sin\theta = (1 + \frac{\sqrt{2}}{2})(\frac{\sqrt{2}}{2}) = \frac{\sqrt{2}}{2} + \frac{1}{2}$
6. **Tangent Line Equation:**
   $$y - (\frac{\sqrt{2}+1}{2}) = (1 - \sqrt{2})(x - \frac{\sqrt{2}+1}{2})$$

---

### (ii) Find the area inside the curve.
1. **Use the Polar Area formula:** $A = \int_{\alpha}^{\beta} \frac{1}{2}r^2 d\theta$.
2. **Identify limits:** To trace the full cardioid, $\theta$ goes from $0$ to $2\pi$.
   $$A = \frac{1}{2} \int_{0}^{2\pi} (1 + \cos\theta)^2 d\theta$$
3. **Expand the integrand:**
   $$A = \frac{1}{2} \int_{0}^{2\pi} (1 + 2\cos\theta + \cos^2\theta) d\theta$$
4. **Use Power-Reduction Identity:** $\cos^2\theta = \frac{1 + \cos 2\theta}{2}$.
   $$A = \frac{1}{2} \int_{0}^{2\pi} (1 + 2\cos\theta + \frac{1}{2} + \frac{1}{2}\cos 2\theta) d\theta = \frac{1}{2} \int_{0}^{2\pi} (\frac{3}{2} + 2\cos\theta + \frac{1}{2}\cos 2\theta) d\theta$$
5. **Integrate:**
   $$A = \frac{1}{2} \left[ \frac{3}{2}\theta + 2\sin\theta + \frac{1}{4}\sin 2\theta \right]_{0}^{2\pi}$$
6. **Evaluate:**
   $$A = \frac{1}{2} \left( (\frac{3}{2}(2\pi) + 0 + 0) - (0) \right) = \frac{1}{2}(3\pi) = \frac{3\pi}{2}$$
**Final Answer:** $3\pi/2$

## Solutions for Problem 9: Converting Polar to Cartesian

### Problem: Show that the Cartesian equation for the curve $r = \cos\theta$ is an equation of a circle and find its radius.

1. **Multiply by $r$:** To easily use our conversion formulas, multiply both sides of the polar equation by $r$:
   $$r^2 = r\cos\theta$$
2. **Substitute Cartesian coordinates:**
   - Replace $r^2$ with $x^2 + y^2$.
   - Replace $r\cos\theta$ with $x$.
   $$x^2 + y^2 = x$$
3. **Rearrange into standard form:** Bring $x$ to the left side:
   $$x^2 - x + y^2 = 0$$
4. **Complete the square for $x$:**
   Take half of the coefficient of $x$ (which is $-1/2$), square it ($1/4$), and add it to both sides:
   $$(x^2 - x + \frac{1}{4}) + y^2 = \frac{1}{4}$$
5. **Write in standard circle form $(x-h)^2 + (y-k)^2 = R^2$:**
   $$(x - \frac{1}{2})^2 + y^2 = \left(\frac{1}{2}\right)^2$$
6. **Identify the properties:**
   - The equation represents a circle centered at $(\frac{1}{2}, 0)$.
   - The radius $R$ is $\sqrt{1/4} = 1/2$.

**Final Answer:** This is a circle with radius $1/2$.

## Solutions for Problem 10: Converting Cartesian to Polar

To convert from Cartesian $(x, y)$ to Polar $(r, \theta)$, we use:
- $x = r\cos\theta$
- $y = r\sin\theta$
- $x^2 + y^2 = r^2$

---

### (i) $y = 3x$
1. **Substitute:** Replace $x$ and $y$ with their polar equivalents:
   $$r\sin\theta = 3(r\cos\theta)$$
2. **Simplify:** Divide both sides by $r\cos\theta$ (assuming $r \neq 0$):
   $$\frac{\sin\theta}{\cos\theta} = 3$$
3. **Use Identity:** Since $\frac{\sin\theta}{\cos\theta} = \tan\theta$:
   $$\tan\theta = 3$$
**Final Answer:** $\theta = \arctan(3)$

---

### (ii) $y = -2x^2$
1. **Substitute:** Replace $x$ and $y$:
   $$r\sin\theta = -2(r\cos\theta)^2$$
2. **Expand:**
   $$r\sin\theta = -2r^2\cos^2\theta$$
3. **Solve for $r$:** Divide both sides by $r\cos^2\theta$ (assuming $r \neq 0$):
   $$\frac{\sin\theta}{\cos^2\theta} = -2r$$
4. **Isolate $r$:**
   $$r = -\frac{1}{2} \cdot \frac{\sin\theta}{\cos\theta} \cdot \frac{1}{\cos\theta}$$
**Final Answer:** $r = -\frac{1}{2} \tan\theta \sec\theta$

---

### (iii) $x^2 - y^2 = 4$
1. **Substitute:** Replace $x$ and $y$:
   $$(r\cos\theta)^2 - (r\sin\theta)^2 = 4$$
2. **Factor out $r^2$:**
   $$r^2(\cos^2\theta - \sin^2\theta) = 4$$
3. **Use Double-Angle Identity:** Recall that $\cos^2\theta - \sin^2\theta = \cos 2\theta$:
   $$r^2\cos 2\theta = 4$$
4. **Solve for $r^2$:**
   $$r^2 = \frac{4}{\cos 2\theta}$$
**Final Answer:** $r^2 = 4\sec 2\theta$

## Solutions for Problem 11: Polar Graphs and Area

### (i) $r = 3\sin\theta, \quad 0 \le \theta \le \pi$
1. **Identify the curve:** This is a circle centered at $(0, 1.5)$ with a radius of $1.5$.
2. **Set up the Area integral:**
   $$A = \int_{0}^{\pi} \frac{1}{2} (3\sin\theta)^2 d\theta = \frac{9}{2} \int_{0}^{\pi} \sin^2\theta d\theta$$
3. **Use Power-Reduction Identity:** $\sin^2\theta = \frac{1 - \cos 2\theta}{2}$.
   $$A = \frac{9}{4} \int_{0}^{\pi} (1 - \cos 2\theta) d\theta = \frac{9}{4} \left[ \theta - \frac{1}{2}\sin 2\theta \right]_{0}^{\pi}$$
4. **Evaluate:** $\frac{9}{4} (\pi - 0) = \frac{9\pi}{4}$.
**Final Answer:** $9\pi/4$

---

### (ii) $r = 1 + \cos\theta, \quad -\pi \le \theta \le \pi$
1. **Identify the curve:** This is a cardioid symmetric about the $x$-axis.
2. **Set up the Area integral:**
   $$A = \frac{1}{2} \int_{-\pi}^{\pi} (1 + \cos\theta)^2 d\theta$$
3. **Evaluate (Using symmetry):** As calculated in Problem 8(ii), the area of this cardioid over a full rotation ($2\pi$ radians) is:
**Final Answer:** $3\pi/2$

---

### (iii) $r = \cos 2\theta, \quad 0 < \theta < \pi$
1. **Identify the curve:** This is a 4-petaled rose. The interval $0 < \theta < \pi$ covers exactly two of the four petals.
2. **Set up the Area integral:**
   $$A = \frac{1}{2} \int_{0}^{\pi} \cos^2(2\theta) d\theta$$
3. **Use Power-Reduction Identity:** $\cos^2(2\theta) = \frac{1 + \cos 4\theta}{2}$.
   $$A = \frac{1}{4} \int_{0}^{\pi} (1 + \cos 4\theta) d\theta = \frac{1}{4} \left[ \theta + \frac{1}{4}\sin 4\theta \right]_{0}^{\pi}$$
4. **Evaluate:** $\frac{1}{4} (\pi + 0) = \frac{\pi}{4}$.
**Final Answer:** $\pi/4$

---

### (iv) $r^2 = \sin 2\theta, \quad 0 < \theta < \pi/2$
1. **Identify the curve:** This is one loop of a lemniscate (infinity symbol shape).
2. **Set up the Area integral:** Note the formula is $\int \frac{1}{2} r^2 d\theta$, and we are given $r^2$ directly.
   $$A = \frac{1}{2} \int_{0}^{\pi/2} \sin 2\theta d\theta$$
3. **Integrate:**
   $$A = \frac{1}{2} \left[ -\frac{1}{2}\cos 2\theta \right]_{0}^{\pi/2} = -\frac{1}{4} [\cos(\pi) - \cos(0)]$$
4. **Evaluate:** $-\frac{1}{4} (-1 - 1) = \frac{2}{4} = \frac{1}{2}$.
**Final Answer:** $1/2$
