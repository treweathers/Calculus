# 🧮 Calculus II Final Review Sheet
## Section 1: See Study Guide from Midterm I

## ♾️ Section 2: Infinite Series
It looks like you are running into a **Markdown parsing error**. When you copy-paste, the line breaks (newlines) are being stripped away, causing the headers (`###`) and list items to run together into a single "wall of text."

GitHub's Markdown engine requires a physical line break for a header to render correctly. Without that gap, it treats everything as one giant paragraph. Additionally, the LaTeX I used previously might have used `$...$` delimiters, which GitHub sometimes struggles to render depending on your specific math plugin.

Here is a **GitHub-optimized version**. I have added extra line breaks and ensured the LaTeX is formatted in a way that is most compatible with standard `.md` viewers.

---

##I. Sequences and Decimal Conversion (§11.1)###1. Limits of SequencesTo find if a sequence \{a_n\} converges:

* **The Goal:** Find L = \lim_{n \to \infty} a_n.
* **Method:** Treat n as x and use L'Hôpital's Rule if you encounter \infty/\infty.
* **Analysis:** If L is a finite number, it **converges**. If it's \pm \infty or oscillates, it **diverges**.

###2. Recursive Sequences and Fish PopulationsFor a population P_n where P_n = rP_{n-1} + d:

* **Finding terms:** Plug P_0 into the formula to find P_1, then P_1 to find P_2.
* **Finding the Limit (L):** Solve the equilibrium equation: L = rL + d.
* **Shortcut:** L = \frac{d}{1-r}.

###3. Decimal to Rational NumberTo turn 0.\overline{12} into a fraction:

1. Let x = 0.1212...
2. Multiply by 10^k to move decimal to the start of the repeating block.
3. Multiply by 10^{k+m} to move decimal to the end of the block.
4. Subtract the equations to isolate x.

---

##II. Series Basics & Convergence Tests (§11.2 – 11.6)###1. Partial Sums (s_n) vs. Terms (a_n)If you are given the sum formula s_n:

* **Find a_n:** a_n = s_n - s_{n-1}.
* **Find total sum:** S = \lim_{n \to \infty} s_n.

###2. The Big Three Early Tests| Test | Condition | Conclusion |
| --- | --- | --- |
| **Divergence Test** | \lim_{n \to \infty} a_n \neq 0 | Series **Diverges** |
| **Geometric Series** | \sum ar^{n-1} | Converges if $ |
| **Telescoping Series** | Terms cancel out | Find s_n by canceling terms, then take \lim_{n \to \infty} s_n |

###3. Integral Test & Remainder (§11.3)* **Conditions:** Function f(x) must be **positive, continuous, and decreasing**.
* **Rule:** \sum a_n converges if \int_1^{\infty} f(x) dx is finite.
* **Error Bound:** R_n \leq \int_n^{\infty} f(x) dx.

###4. Ratio and Root Tests (§11.6)* **Ratio Test:** L = \lim_{n \to \infty} | \frac{a_{n+1}}{a_n} |.
* **Root Test:** L = \lim_{n \to \infty} \sqrt[n]{|a_n|}.
* **Results:** L < 1 (Abs. Conv), L > 1 (Div), L = 1 (Inconclusive).

---

##III. Power Series (§11.8 – 11.9)###1. Radius (R) and Interval (I)1. Use **Ratio Test** on the absolute value of the whole term.
2. Solve for |x - a| < R.
3. **Check Endpoints:** You must manually plug in x = a-R and x = a+R to check for convergence at the boundaries.

###2. Geometric RepresentationUse \frac{1}{1-u} = \sum_{n=0}^{\infty} u^n for |u| < 1.

---

##IV. Taylor and Maclaurin Series (§11.10 – 11.11)###1. General Formulas* **Taylor (at a):** \sum \frac{f^{(n)}(a)}{n!} (x-a)^n
* **Maclaurin (at 0):** \sum \frac{f^{(n)}(0)}{n!} x^n

###2. Taylor’s Inequality|R_n(x)| \leq \frac{M}{(n+1)!} |x - a|^{n+1} where M is the max of |f^{(n+1)}| on the interval.

###3. Common Maclaurin Series* **e^x**: \sum \frac{x^n}{n!}
* **\sin(x)**: \sum (-1)^n \frac{x^{2n+1}}{(2n+1)!}
* **\cos(x)**: \sum (-1)^n \frac{x^{2n}}{(2n)!}

---

###Analysis Tip: Hierarchy of GrowthWhen testing for divergence, remember:


---

**Would you like me to generate a specific practice problem for the "Integral Test Remainder" or "Power Series Endpoints" so you can test if the math renders correctly in your GitHub file?**
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
