# 🧮 Calculus II Final Review Sheet
## Section 1: See Study Guide from Midterm I

## ♾️ Section 2: Infinite Series
## 1. Sequences & Recursive Models (§11.1)A sequence is a list of numbers \{a_n\}. A sequence **converges** if \lim_{n \to \infty} a_n = L (a finite number).

* **Recursive to Limit:** For P_n = rP_{n-1} + d, if the limit exists, then L = rL + d.
* **How-to:** Solve for L. For example, if P_n = 0.8P_{n-1} + 200, then L = 0.8L + 200 \implies 0.2L = 200 \implies L = 1000.


* **Decimal to Rational:** * **Step 1:** Set x = 0.12\overline{34}.
* **Step 2:** Multiply by 10^k to move to the start of the repeat: 100x = 12.3434...
* **Step 3:** Multiply by 10^{k+m} to move one full period: 10000x = 1234.3434...
* **Step 4:** Subtract (Eq 2 - Eq 1) to cancel the decimals and solve for x.



---

## 2. Series Fundamentals (§11.2)A series \sum a_n is the sum of a sequence.

* **Partial Sums (s_n):** The sum of the first n terms.
* **To find a_n:** a_n = s_n - s_{n-1}.
* **The Sum:** S = \lim_{n \to \infty} s_n.


* **Geometric Series:** \sum_{n=1}^{\infty} ar^{n-1}
* **Convergence:** Converges if |r| < 1.
* **Sum formula:** S = \frac{a}{1-r} (where a is the **first term**).


* **Divergence Test:** If \lim_{n \to \infty} a_n \neq 0, the series **diverges**. (Note: If it equals 0, the test is inconclusive!)

---

## 3. The Integral Test & Estimation (§11.3)Use when a_n = f(n) and f(x) is **positive, continuous, and decreasing**.

* **The Test:** \sum a_n converges if \int_{1}^{\infty} f(x) dx converges.
* **Remainder Estimate (R_n):** To bound the error of a partial sum s_n:


* **Sum Bounds:** s_n + \int_{n+1}^{\infty} f(x)dx \leq S \leq s_n + \int_{n}^{\infty} f(x)dx.



---

## 4. Comparison, Ratio, & Root Tests (§11.4 - 11.6)| Test | Usage | Condition for Convergence |
| --- | --- | --- |
| **Comparison** | Compare a_n to p-series or geometric. | a_n \leq b_n and \sum b_n conv. |
| **Limit Comp.** | Use when a_n "looks like" b_n. | \lim (a_n / b_n) = C > 0. |
| **Ratio Test** | Best for **factorials (n!)** or a^n. | $L = \lim |
| **Root Test** | Best for ( \text{expression} )^n. | $L = \lim \sqrt[n]{ |
| **Alt. Series** | \sum (-1)^n b_n. | b_{n+1} \leq b_n and \lim b_n = 0. |

* **Absolute vs. Conditional:** * **Absolute:** \sum |a_n| converges.
* **Conditional:** \sum a_n converges, but \sum |a_n| diverges (e.g., Alternating Harmonic Series).



---

## 5. Power Series & Radius (§11.8 - 11.9)A series of the form \sum c_n(x-a)^n.

* **Finding Interval of Convergence (I):** 1.  Perform the **Ratio Test** on the whole term.
2.  Set L < 1 and solve for |x-a| < R.
3.  **Crucial:** You **must** test the endpoints individually by plugging them back into the original series for x.
* **Geometric Representation:** \frac{1}{1-u} = \sum_{n=0}^{\infty} u^n for |u| < 1.
* Use this to transform functions like \frac{x}{1+x^2} into series by substituting u = -x^2 and multiplying by x.



---

## 6. Taylor & Maclaurin Series (§11.10 - 11.11)* **Formula:** f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n. (Maclaurin is just a=0).
* **Taylor’s Inequality (Error Bound):** 


where M is the maximum value of |f^{(n+1)}(x)| on the given interval.

### Common Maclaurin Series to Memorize:* e^x = \sum \frac{x^n}{n!}
* \sin(x) = \sum (-1)^n \frac{x^{2n+1}}{(2n+1)!}
* \cos(x) = \sum (-1)^n \frac{x^{2n}}{(2n)!}
* \frac{1}{1-x} = \sum x^n

---

##💡 Pro-Tips for the Exam:1. **Check for Divergence First:** It takes 5 seconds to see if \lim a_n \neq 0. Do this before doing a complex Ratio Test.
2. **Integration of Series:** If you need to integrate a function that doesn't have an easy antiderivative (like e^{-x^2}), convert it to a power series first, then integrate term-by-term.
3. **Alternating Series Accuracy:** The error in an alternating series s_n is always less than the first neglected term: |R_n| \leq b_{n+1}. Use this to find how many terms you need for a specific decimal accuracy.

**Would you like me to walk through a specific example of one of these tests, like the Ratio Test or finding a Taylor Error Bound?**
### **Convergence Tests**
* **Divergence Test:** If lim(aₙ) ≠ 0, then diverges.
* **p-Series:** Σ 1/nᵖ converges if p > 1, diverges if p ≤ 1.
* **Geometric Series:** Σ arⁿ converges if |r| < 1. Sum = a/(1-r).
* **Integral Test:** If f(x) is positive/decreasing, Σ aₙ and ∫ f(x)dx both converge or both diverge.
* **Ratio Test:** L = lim |aₙ₊₁ / aₙ|. Converges if L < 1, Diverges if L > 1.
* **Root Test:** L = lim ⁿ√|aₙ|. Converges if L < 1, Diverges if L > 1.
* **Direct Comparison:** If aₙ ≤ bₙ and Σbₙ converges, then Σaₙ converges.
* **Limit Comparison:** L = lim (aₙ / bₙ). If L is finite/positive, both series behave the same.
* **Alternating Series:** Σ (-1)ⁿ bₙ converges if bₙ is decreasing and lim(bₙ) = 0.

This review sheet covers the core of Calculus II/III material regarding sequences and series. Use this as a checklist for your Midterm II preparation.

---

##1. Sequences & Recursive Models (§11.1)A sequence is a list of numbers \{a_n\}. A sequence **converges** if \lim_{n \to \infty} a_n = L (a finite number).

* **Recursive to Limit:** For P_n = rP_{n-1} + d, if the limit exists, then L = rL + d.
* **How-to:** Solve for L. For example, if P_n = 0.8P_{n-1} + 200, then L = 0.8L + 200 \implies 0.2L = 200 \implies L = 1000.


* **Decimal to Rational:** * **Step 1:** Set x = 0.12\overline{34}.
* **Step 2:** Multiply by 10^k to move to the start of the repeat: 100x = 12.3434...
* **Step 3:** Multiply by 10^{k+m} to move one full period: 10000x = 1234.3434...
* **Step 4:** Subtract (Eq 2 - Eq 1) to cancel the decimals and solve for x.



---

##2. Series Fundamentals (§11.2)A series \sum a_n is the sum of a sequence.

* **Partial Sums (s_n):** The sum of the first n terms.
* **To find a_n:** a_n = s_n - s_{n-1}.
* **The Sum:** S = \lim_{n \to \infty} s_n.


* **Geometric Series:** \sum_{n=1}^{\infty} ar^{n-1}
* **Convergence:** Converges if |r| < 1.
* **Sum formula:** S = \frac{a}{1-r} (where a is the **first term**).


* **Divergence Test:** If \lim_{n \to \infty} a_n \neq 0, the series **diverges**. (Note: If it equals 0, the test is inconclusive!)

---

##3. The Integral Test & Estimation (§11.3)Use when a_n = f(n) and f(x) is **positive, continuous, and decreasing**.

* **The Test:** \sum a_n converges if \int_{1}^{\infty} f(x) dx converges.
* **Remainder Estimate (R_n):** To bound the error of a partial sum s_n:


* **Sum Bounds:** s_n + \int_{n+1}^{\infty} f(x)dx \leq S \leq s_n + \int_{n}^{\infty} f(x)dx.



---

##4. Comparison, Ratio, & Root Tests (§11.4 - 11.6)| Test | Usage | Condition for Convergence |
| --- | --- | --- |
| **Comparison** | Compare a_n to p-series or geometric. | a_n \leq b_n and \sum b_n conv. |
| **Limit Comp.** | Use when a_n "looks like" b_n. | \lim (a_n / b_n) = C > 0. |
| **Ratio Test** | Best for **factorials (n!)** or a^n. | $L = \lim |
| **Root Test** | Best for ( \text{expression} )^n. | $L = \lim \sqrt[n]{ |
| **Alt. Series** | \sum (-1)^n b_n. | b_{n+1} \leq b_n and \lim b_n = 0. |

* **Absolute vs. Conditional:** * **Absolute:** \sum |a_n| converges.
* **Conditional:** \sum a_n converges, but \sum |a_n| diverges (e.g., Alternating Harmonic Series).



---

##5. Power Series & Radius (§11.8 - 11.9)A series of the form \sum c_n(x-a)^n.

* **Finding Interval of Convergence (I):** 1.  Perform the **Ratio Test** on the whole term.
2.  Set L < 1 and solve for |x-a| < R.
3.  **Crucial:** You **must** test the endpoints individually by plugging them back into the original series for x.
* **Geometric Representation:** \frac{1}{1-u} = \sum_{n=0}^{\infty} u^n for |u| < 1.
* Use this to transform functions like \frac{x}{1+x^2} into series by substituting u = -x^2 and multiplying by x.



---

##6. Taylor & Maclaurin Series (§11.10 - 11.11)* **Formula:** f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n. (Maclaurin is just a=0).
* **Taylor’s Inequality (Error Bound):** 


where M is the maximum value of |f^{(n+1)}(x)| on the given interval.

###Common Maclaurin Series to Memorize:* e^x = \sum \frac{x^n}{n!}
* \sin(x) = \sum (-1)^n \frac{x^{2n+1}}{(2n+1)!}
* \cos(x) = \sum (-1)^n \frac{x^{2n}}{(2n)!}
* \frac{1}{1-x} = \sum x^n

---

##💡 Pro-Tips for the Exam:1. **Check for Divergence First:** It takes 5 seconds to see if \lim a_n \neq 0. Do this before doing a complex Ratio Test.
2. **Integration of Series:** If you need to integrate a function that doesn't have an easy antiderivative (like e^{-x^2}), convert it to a power series first, then integrate term-by-term.
3. **Alternating Series Accuracy:** The error in an alternating series s_n is always less than the first neglected term: |R_n| \leq b_{n+1}. Use this to find how many terms you need for a specific decimal accuracy.

**Would you like me to walk through a specific example of one of these tests, like the Ratio Test or finding a Taylor Error Bound?**

### III. Convergence Tests for $\sum a_n$


## Quick Convergence Test Reference

Start by applying the **Divergence Test** ($\lim a_n$): if the limit isn't zero, the series diverges—stop. If the limit is zero, proceed to test for **Absolute Convergence** by considering $\sum |a_n|$. For this series, use the **Ratio** or **Root Test** (good for factorials/powers), the **Comparison Tests** (use **Limit Comparison** for rational functions; **Direct Comparison** only if the inequality is obvious), or the **Integral Test** (if $f(x)$ is decreasing and positive, and $f(x)$ is easily integrable, like $\frac{1}{x \ln x}$). If the absolute series converges, the original series converges. If the absolute series diverges, and the original series is alternating, apply the **Alternating Series Test** to check for **Conditional Convergence**.

---

## 🧐 Comprehensive Convergence Test Checklist for $\sum a_n$

### Step 1: The **Divergence Test** (The First Check)

* **Goal:** To quickly determine if the series must **diverge**.
* **Check:** Calculate $\lim_{n \to \infty} a_n$.
* **Result:**
    * If $\lim_{n \to \infty} a_n \neq 0$ (or the limit does not exist), then the series **diverges**. Stop here.
    * If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**. Proceed to Step 2. (Note: Skip this initial limit calculation and go straight to the **Ratio/Root Test** if $a_n$ contains factorials or exponents of $n$).

---

### Step 2: Test for **Absolute Convergence**

Absolute convergence means the series $\sum |a_n|$ converges. If this series converges, the original series $\sum a_n$ is absolutely convergent and therefore converges.

* **Form the Absolute Series:** Consider the series of absolute values, $\sum |a_n|$.
* **Apply Tests for Absolute Convergence:** Use one of the following tests on $\sum |a_n|$:

#### A. **Ratio Test** or **Root Test** (For terms involving $n!$, products of functions, or $n$ in the exponent)

* **Ratio Test:** Calculate $L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$.
* **Root Test:** Calculate $L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.
* **Result (for either test):**
    * If $L < 1$, the series $\sum |a_n|$ **converges**, so $\sum a_n$ is **absolutely convergent** (and therefore convergent). Stop here.
    * If $L > 1$ or $L = \infty$, the series **diverges**. Stop here.
    * If $L = 1$, the test is **inconclusive**. Try a Comparison or Integral Test.

#### B. **Comparison Tests** (Useful when $|a_n|$ is similar to a known series)

* **Use when taking the absolute value is helpful:** This is particularly helpful when $|a_n|$ simplifies to a known convergent or divergent series (like a $p$-series or Geometric series).

* **Direct Comparison Test (DCT):**
    * **Use:** Only if the required **inequality is simple and obvious** (e.g., $n^2+5 > n^2 \implies \frac{1}{n^2+5} < \frac{1}{n^2}$).
    * **Requires:** Finding a convergent series $\sum b_n$ such that $|a_n| \le b_n$, or a divergent series $\sum d_n$ such that $|a_n| \ge d_n$.

* **Limit Comparison Test (LCT):**
    * **Use:** **Most commonly** for rational or algebraic functions. It's much easier as it avoids proving inequalities.
    * **Requires:** Find a known series $\sum b_n$ (usually the simplified dominant terms). Calculate $L = \lim_{n \to \infty} \frac{|a_n|}{b_n}$. If $0 < L < \infty$, then $\sum |a_n|$ and $\sum b_n$ have the **same convergence behavior**.

#### C. **Integral Test** (Used when $f(x)$ is continuous, positive, decreasing, and easily integrable)

* **Where it fits in:** The Integral Test is a comparison tool, best used when the term $a_n$ contains terms like $\ln n$ or complex functions that integrate cleanly using $u$-substitution.
* **Check:** Consider $f(x) = |a_x|$. The series $\sum |a_n|$ converges if and only if the improper integral $\int_1^\infty f(x) dx$ **converges** (is a finite number). If the integral **diverges**, the series also **diverges**. 

---

### Step 3: Test for **Conditional Convergence** (If Step 2 Fails)

This step only applies if:
1.  The series $\sum |a_n|$ **diverged** in Step 2.
2.  The original series $\sum a_n$ is an **Alternating Series** (terms must alternate sign, e.g., $\sum (-1)^n b_n$).

* **When the series fails absolute convergence tests:** This is precisely when you apply the **Alternating Series Test (AST)**—only if the series is alternating and you've confirmed $\sum |a_n|$ diverges.
* **Apply the Alternating Series Test:** For the series $\sum (-1)^n b_n$ (where $b_n = |a_n|$ is positive), check two conditions:
    1.  $b_n$ is **decreasing** (i.e., $b_{n+1} \le b_n$ for all $n$).
    2.  $\lim_{n \to \infty} b_n = 0$.
* **Result:** If **both conditions are met**, the series $\sum a_n$ **converges conditionally**.
* **Final Result:** If the series $\sum |a_n|$ **diverged** AND the **Alternating Series Test failed**, the series $\sum a_n$ **diverges**.

#### **1. Divergence Test ($n$-th Term Test)**
* **Condition:** If $\lim_{n\to\infty} a_n \neq 0$ (or DNE), then $\sum a_n$ **Diverges**.
* **Note:** If $\lim_{n\to\infty} a_n = 0$, the test is **inconclusive**.

#### **2. Integral Test**
* **Condition:** If $f(x)$ is positive, continuous, and decreasing on $[k, \infty)$, then $\sum_{n=k}^\infty a_n$ and $\int_k^\infty f(x) dx$ either **both converge or both diverge**.

#### **3. Comparison Test (Direct)**
* **Conditions:** Let $0 < a_n \leq b_n$.
    * If the larger series $\sum b_n$ **converges**, then $\sum a_n$ **converges**.
    * If the smaller series $\sum a_n$ **diverges**, then $\sum b_n$ **diverges**.
* **Note:** Requires non-negative terms.

#### **4. Limit Comparison Test (LCT)**
* **Condition:** Let $L = \lim_{n\to\infty} \frac{a_n}{b_n}$. If $L$ is a **finite, positive number ($L>0$)**, then $\sum a_n$ and $\sum b_n$ **either both converge or both diverge**.
* **Note:** Requires $a_n > 0$ and $b_n > 0$.

#### **5. Ratio Test**
* **Condition:** Calculate $L = \lim_{n\to\infty} \left| \frac{a_{n+1}}{a_n} \right|$.
    * If $L < 1$, the series **converges absolutely**.
    * If $L > 1$, the series **diverges**.
    * If $L=1$, the test is **inconclusive**.

#### **6. Root Test**
* **Condition:** Calculate $L = \lim_{n\to\infty} \sqrt[n]{|a_n|}$.
    * If $L < 1$, the series **converges absolutely**.
    * If $L > 1$, the series **diverges**.
    * If $L=1$, the test is **inconclusive**.

#### **7. Alternating Series Test (AST)**
* **Applies to:** $\sum_{n=1}^\infty (-1)^{n}b_n$ or $\sum_{n=1}^\infty (-1)^{n-1}b_n$, where $b_n > 0$.
* **Conditions for Convergence:** The series converges if **both** conditions are met:
    1.  $\lim_{n\to\infty} b_n = 0$
    2.  $b_{n+1} \leq b_n$ (the terms are decreasing in magnitude)
* **Alternating Series Remainder:** The error $|R_N|$ in using $S_N$ to approximate the sum $S$ is bounded by the magnitude of the next term: $|R_N| = |S - S_N| \leq b_{N+1}$.


### **Known Maclaurin Series**
| Function | Sigma Notation (Power Series) | First Few Terms | ROC |
| --- | --- | --- | --- |
| **Geometric** | Σ xⁿ | 1 + x + x² + x³ + ... | R = 1 |
| **eˣ** | Σ xⁿ / n! | 1 + x + x²/2! + x³/3! + ... | R = ∞ |

---

## 🧊 Section 3: 3D Geometry & Vectors
### **Vector Operations**
* **Magnitude:** |v| = √(v₁² + v₂² + v₃²)
* **Unit Vector:** v / |v|
* **Dot Product:** u₁v₁ + u₂v₂ + u₃v₃
* **Cross Product:** ⟨u₂v₃-u₃v₂, u₃v₁-u₁v₃, u₁v₂-u₂v₁⟩
* **Area of Parallelogram:** Magnitude of the cross product: |u × v|
* **Volume of Parallelepiped:** Absolute value of triple product: |u · (v × w)|

### **Lines and Planes**
* **Line Equation:** r(t) = P₀ + t⟨d₁, d₂, d₃⟩
* **Plane Equation:** a(x - x₀) + b(y - y₀) + c(z - z₀) = 0
  * *Note:* ⟨a, b, c⟩ is the Normal Vector.
* **Distance (Point to Plane):** D = |ax₁ + by₁ + cz₁ + d| / √(a² + b² + c²)

### **The Parallelogram Law**
* **Formula:** |u + v|² + |u - v|² = 2|u|² + 2|v|²

---
