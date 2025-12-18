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
