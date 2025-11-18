# Sequences and Series Guide
## PART I: Core Definitions for Sequences and Series

| Term | Simple Definition | Key Intuition |
| :--- | :--- | :--- |
| **Sequence** ($a_n$) | An ordered **list of numbers** defined by a rule: $a_1, a_2, a_3, \ldots$ | The **ingredients** for the sum. |
| **Series** ($\sum a_n$) | The **sum** of all the terms in a sequence: $a_1 + a_2 + a_3 + \cdots$ | The **recipe** to find the total value. |
| **Partial Sum** ($s_N$) | The sum of the first $N$ terms: $s_N = a_1 + a_2 + \cdots + a_N$. | The **product so far**; a sequence itself. |
| **Convergence** (Series) | A series **converges** if the sequence of its partial sums ($s_N$) approaches a single, finite number $S$. | The total sum **settles down** to a fixed value. |
| **Divergence** (Series) | A series **diverges** if the sequence of its partial sums ($s_N$) does not approach a finite number (it might go to $\pm \infty$ or oscillate). | The total sum **flies off** or never stabilizes. |
| **Absolute Convergence (AC)** | A series $\sum a_n$ converges even when all terms are made positive (i.e., $\sum |a_n|$ converges). | Convergence is so strong that alternating signs are unnecessary. |
| **Conditional Convergence (CC)**| A series $\sum a_n$ converges only because of its alternating signs (i.e., $\sum a_n$ converges, but $\sum |a_n|$ diverges). | Convergence is fragile; it relies entirely on cancellation. |
| **Remainder/Error ($R_N$)** | The difference between the true sum $S$ and the partial sum $s_N$: $R_N = S - s_N$. | The **leftover amount** after adding the first $N$ terms. |

---

## PART II: The Intuitive Connection: Sequences are the *Ingredients* for Series

Think of the relationship like this:

| Concept | The Intuitive Role | What it Represents |
| :--- | :--- | :--- |
| **Sequence** ($a_n$) | The **Ingredient** (The terms) | A list of numbers that you are going to add up: $a_1, a_2, a_3, \ldots$ |
| **Series** ($\sum a_n$) | The **Recipe** (The Sum) | The instruction to add all the sequence terms together: $a_1 + a_2 + a_3 + \cdots$ |
| **Partial Sum** ($s_N$) | The **Product** (The Result so far) | The *sequence* of results you get by stopping the addition at $N$: $s_1, s_2, s_3, \ldots$ |

### The Logic of Convergence

The entire idea of a series converging relies on the relationship between two different sequences:

1.  **The Sequence of Terms ($a_n$):** This sequence must go to zero (as required by the Divergence Test).
    * **Intuition:** If the ingredients you are adding never get smaller, the total sum will obviously fly off to infinity. The terms *must* approach zero for the sum to have any chance of being finite.

2.  **The Sequence of Partial Sums ($s_N$):** This sequence must converge to a finite limit.
    * **Intuition:** The series converges if, as you add more and more ingredients, the total sum ($s_N$) stops changing significantly and settles down to one fixed number.

### The Two Crucial Limits 

A series, $\sum a_n$, converges **if and only if** the sequence of its partial sums, $s_N$, converges to a finite limit $S$.

$$\sum_{n=1}^\infty a_n = S \quad \iff \quad \lim_{N \to \infty} s_N = S$$

So, a series *is* a sequence—it's the **sequence of its partial sums ($s_N$)**—and we test its convergence by seeing if that new sequence $s_N$ converges.

This intuitive understanding reinforces why:
* **Divergence Test is First:** We check $\lim a_n$ first because if the ingredients don't go to zero, the recipe is immediately a disaster.
* **The Goal is $S$:** All the convergence tests are just indirect ways of checking whether that sequence of partial sums, $s_N$, is actually approaching a finite value $S$.

## PART III: Choosing a Convergence Test

***

## Quick Convergence Test Reference

Start by applying the **Divergence Test** ($\lim a_n$): if the limit isn't zero, the series diverges—stop. If the limit is zero, proceed to test for **Absolute Convergence** by considering $\sum |a_n|$. For this series, use the **Ratio** or **Root Test** (good for factorials/powers), the **Limit Comparison Test** (to compare with $p$-series or geometric), or the **Integral Test** (if $f(x)$ is decreasing and positive). If the absolute series converges, the original series converges. If the absolute series diverges, and the original series is alternating, apply the **Alternating Series Test** to check for **Conditional Convergence**.

***

## 🧐 Comprehensive Convergence Test Checklist for $\sum a_n$

### Step 1: The **Divergence Test** (The First Check)

* **Goal:** To quickly determine if the series must **diverge**.
* **Check:** Calculate $\lim_{n \to \infty} a_n$.
* **Result:**
    * If $\lim_{n \to \infty} a_n \neq 0$ (or the limit does not exist), then the series **diverges**. Stop here.
    * If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**. Proceed to Step 2.

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
* **Direct Comparison Test:** Find a convergent series $\sum b_n$ such that $|a_n| \le b_n$, or a divergent series $\sum d_n$ such that $|a_n| \ge d_n$.
* **Limit Comparison Test:** Find a known series $\sum b_n$. Calculate $L = \lim_{n \to \infty} \frac{|a_n|}{b_n}$. If $0 < L < \infty$, then $\sum |a_n|$ and $\sum b_n$ have the **same convergence behavior**.

#### C. **Integral Test** (Useful when $|a_n|$ can be written as $f(n)$ where $f(x)$ is continuous, positive, and decreasing)

* **Where it fits in:** The Integral Test is a comparison tool, best used when the term $a_n$ is complicated but easily integrated (e.g., terms involving $\ln n$ or complex rational functions).
* **Check:** Consider $f(x) = |a_x|$. If the improper integral $\int_1^\infty f(x) dx$ **converges**, then $\sum |a_n|$ **converges**. If the integral **diverges**, the series **diverges**.

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

The goal is to choose the **most efficient** test based on the **form** of the series term, $a_n$.

## 1. Initial Checks (The Must-Do's)

1.  **Check $\lim a_n$ (The Divergence Test):**
    * If $\lim_{n\to\infty} a_n \ne 0$, the series **DIVERGES**. **STOP.**
  
2.  **Check $\sum |a_n|$ (The Absolute Convergence Test):**
    * Use Ratio, Root, or Comparison Tests on the positive series $\sum |a_n|$.
    * If $\sum |a_n|$ converges, the original series is **Absolutely Convergent (AC)**. **STOP.**

3.  **Check AST (The Conditional Convergence Test):**
    * If $\sum |a_n|$ diverges, **THEN** proceed to the Alternating Series Test (AST) on $b_n$.
    * If AST conditions are met, the series is **Conditionally Convergent (CC)**.

### 🛑 Check 1: The Divergence Test (Always First!)

| Test | Logic | Condition / Conclusion |
| :--- | :--- | :--- |
| **Divergence Test** | Are the terms even getting small enough to consider convergence? | Calculate $L = \lim_{n\to\infty} a_n$. If $L \ne 0$ (or $L$ DNE), the series **DIVERGES**. (If $L=0$, the test is inconclusive; proceed to Check 2). |

---

##### EXCEPTION: The Strategy of Skipping the Limit - Why the Divergence Test is Often "Skipped" for Factorials:**
For a complex factorial series like $2(f) \sum \frac{(2n)!}{(n!)^2}$, determining the limit $\lim_{n\to\infty} a_n$ **is nearly impossible without using the Ratio Test first.**

| Factorial Series | The Strategy | The Rationale |
| :--- | :--- | :--- |
| **Simple Factorials** (e.g., $1/n!$) | $\lim a_n = 0$. (Easy) | $n!$ grows so fast it dominates everything, making the limit $0$. Divergence Test fails. |
| **Complex Factorials** (e.g., 2f) | **Skip $\lim a_n$ calculation** and go **immediately to the Ratio Test.** | You cannot easily determine the growth rate of $\frac{(2n)!}{(n!)^2}$ without calculating $L = \lim \frac{a_{n+1}}{a_n}$. The Ratio Test calculates the limit of the *ratio* of terms, which is often easier than the limit of the *terms* themselves. |

###### **In short:** When $a_n$ is complex and involves factorials, the Ratio Test is the most efficient (and often the *only* practical) way to analyze its behavior. We prioritize the Ratio Test because its calculation *also* reveals the convergence status.

### 🔍 Check 2: Special Forms (Easiest Tests)

| Series Form | Test | Logic | Condition / Conclusion |
| :--- | :--- | :--- | :--- |
| **Simple Power** $\sum \frac{1}{n^p}$ | **$p$-Series Test** | Does it match the form $\sum 1/n^p$? | **Converges** if $p > 1$. **Diverges** if $p \le 1$. |
| **Exponential** $\sum a r^n$ | **Geometric Series Test** | Does it match the form $\sum ar^n$? | **Converges** if $|r| < 1$. **Diverges** if $|r| \ge 1$. (Can also find the sum). |
| **Difference** $\sum (b_n - b_{n+1})$ | **Telescoping Test** | Can the term be rewritten as a difference that will cancel? | **Converges** if $\lim_{N\to\infty} s_N$ is finite. |

---

##### NOTE: Finding the Sum as a Clue
When a series problem asks you to **find the sum**, it is a very strong clue that the series belongs to one of the few categories for which an exact sum formula exists. 

| Series Type | Term Form ($a_n$) | Sum Formula ($S$) |
| :--- | :--- | :--- |
| **Geometric Series** | $a \cdot r^n$ | $S = \frac{a}{1-r}$ (if $|r| < 1$) |
| **Telescoping Series** | $f(n) - f(n+k)$ (after PFD) | $S = \lim_{N\to\infty} s_N$ (Found by canceling interior terms) |

If you determine convergence using LCT, Ratio, or Root Test, but the question demands the sum, you must backtrack and check for a Geometric or Telescoping form!

---


## 2. Main Tests (The Decision Matrix)

If the series doesn't fit a special form, look at the dominant term structure to decide between the major tests. 

| Series Term Structure | Recommended Test | Logic / Why Choose It |
| :--- | :--- | :--- |
| **Factorials** ($n!$) **or Mixed Exponentials** ($3^n/n!$) | **Ratio Test** | Factorials and most exponentials simplify beautifully under the ratio $\frac{a_{n+1}}{a_n}$. It cancels factorials entirely. |
| **Entire term raised to $n$** $\sum (f(n))^n$ | **Root Test** | The $n$-th root immediately eliminates the exponent, leaving a simple limit of $f(n)$. |
| **Alternating Signs** $\sum (-1)^n b_n$ | **Alternating Series Test (AST)** | If the series is alternating, this is **required** to check for conditional convergence. (Must still check $\sum |a_n|$ first!) |
| **Polynomials / Roots** $\frac{n^2+1}{n^4-3}$ | **Limit Comparison Test (LCT)** | This is the *safest* and most versatile test for rational/root functions. Choose $b_n$ by looking at the highest power terms. |
| **Complicated Denominator** $\frac{1}{n (\ln n)^2}$ | **Integral Test** | Use if the function $f(x)$ is easy to integrate but hard to compare (especially involving $\ln x$ or $\arctan x$). |
| **Bounded Numerator** $\frac{\sin n}{n^2}$ | **Direct Comparison Test** | Use when the numerator is clearly bounded (like $\sin n$ or $\cos n$), making it easy to create a larger, known convergent series (like $\sum 1/n^2$). |

---

## 3. The Alternating Series Protocol (AC vs CC)

If your series is alternating, you must follow this protocol after checking the **Divergence Test** ($\lim_{n\to\infty} a_n \neq 0$ means Divergence):

### Step 1: Test for Absolute Convergence (AC)

* **Test / Logic:** Consider the corresponding series of absolute values, $\sum |a_n| = \sum b_n$.
* **Conclusion:** Apply any standard convergence test ($p$-Series, Ratio, Root, LCT, Integral, etc.) to $\sum b_n$.

### Step 2: Determine if Absolutely Convergent (AC) or Move to Conditional

* **If $\sum |a_n|$ CONVERGES:** The original alternating series $\sum a_n$ is **Absolutely Convergent (AC)**. You are finished.
* **If $\sum |a_n|$ DIVERGES:** The series is *not* Absolutely Convergent. Proceed to Step 3 to test for Conditional Convergence.

### Step 3: Test for Conditional Convergence (CC) using the Alternating Series Test (AST)

* **Test / Logic:** The original alternating series $\sum a_n$ is of the form $\sum (-1)^n b_n$ or $\sum (-1)^{n-1} b_n$ where $b_n = |a_n| > 0$.
    * **Condition 1:** Check if $\lim_{n\to\infty} b_n = 0$.
    * **Condition 2:** Check if $b_n$ is decreasing (i.e., $b_{n+1} \leq b_n$).
* **Conclusion:**
    * If **BOTH** conditions pass, the series is **Conditionally Convergent (CC)**.
    * If **Condition 1 FAILS** (and you haven't already done the Divergence Test), the series **DIVERGES** (by the Divergence Test).
    * If **Condition 1 passes but Condition 2 FAILS**, the series might still converge, but it often **DIVERGES** in common examples. However, in most Calculus II contexts, failure of Condition 2 means you cannot rely on AST, and the series is typically considered **Divergent** unless proven otherwise by another test.
 
---

## PART IV: References
### **I. Sequences ($\{a_n\}$) & Preliminary Tests**

| Concept | Condition/Test | Formula/Notes |
| :--- | :--- | :--- |
| **Limit** (Convergence) | Converges if $\lim_{n \to \infty} a_n = L$ (a finite number). |
| **Monotonic Convergence Thm.** | A bounded, monotonic sequence **must** converge. |
| **$n^{th}$-Term Test** (Divergence Test) | If $\lim_{n \to \infty} a_n \neq 0$, the series **Diverges**. |
| **CAUTION** | If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive**. |

---

### **II. Fundamental Series Types ($\sum_{n=1}^\infty a_n$)**

### **1. Geometric Series**

* **General Form:** $\sum_{n=0}^{\infty} a r^n$
* **Convergence Condition(s):** Converges if the common ratio $|r| < 1$.
* **Divergence Condition(s):** Diverges if $|r| \ge 1$.
* **Key Test/Sum Formula (if $|r| < 1$):** The sum is $S = \frac{a}{1 - r}$. 

---

### **2. $p$-Series**

* **General Form:** $\sum_{n=1}^{\infty} \frac{1}{n^p}$
* **Convergence Condition(s):** Converges if the exponent $p > 1$.
* **Divergence Condition(s):** Diverges if $p \le 1$.
* **Key Test/Sum Formula:** The value of $p$ is the defining factor; often tested with the **Integral Test** for justification.

---

### **3. Harmonic Series**

* **General Form:** $\sum_{n=1}^{\infty} \frac{1}{n}$
* **Convergence Condition(s):** Always **Diverges**.
* **Key Test/Sum Formula:** Special case of $p$-series where $p=1$.

---

### **4. Telescoping Series**

* **General Form:** $\sum_{n=1}^{\infty} (b_n - b_{n+1})$ (often obtained after using partial fractions).
* **Convergence Condition(s):** Converges if $\lim_{N \to \infty} S_N$ exists.
* **Key Test/Sum Formula:**
    1.  Find the $N$-th partial sum $S_N$ by writing out the first few terms (which cancel).
    2.  The sum is $S = \lim_{N \to \infty} S_N$.

---

##### Algebraic Manipulation Needed (Example): Geometric Series
The series is:
$$\sum_{n=0}^\infty 2^n \cdot 3^{-2n+1}$$

Here are the key exponential rules you need to apply, along with the steps to rewrite the term $\left(2^n \cdot 3^{-2n+1}\right)$, without calculating the final result:



<u> **Step-by-Step Guide to Rewriting the Series Term** </u>



| Rule to Apply  | General Form | Application to $3^{-2n+1}$ |
| :--- | :--- | :--- |
| **Product Rule for Exponents** | $b^{x+y} = b^x \cdot b^y$ | Rewrite the term with the sum in the exponent as a product: $3^{-2n+1} = 3^{-2n} \cdot 3^1$. |
| **Negative Exponent Rule** | $b^{-x} = \frac{1}{b^x}$ | Apply this to the term with the negative exponent: $3^{-2n} = \frac{1}{3^{2n}}$. |
| **Power of a Power Rule** | $b^{xy} = (b^x)^y$ | Rewrite the term with a multiple of $n$ in the exponent to isolate $n$: $3^{2n} = (3^2)^n$. |

---

##### **Action Steps (for example)**
1.  **Separate the Constant Factor ($3^1$):** Use the **Product Rule** to split the term $3^{-2n+1}$ into a product of a constant and a term involving $n$.
2.  **Handle the Negative Exponent:** Use the **Negative Exponent Rule** to move the term involving $-2n$ from the numerator to the denominator (or write it as a fraction).
3.  **Isolate $n$ in the Exponent:** Use the **Power of a Power Rule** on the base of the resulting term so that the exponent becomes *exactly* $n$. (e.g., $b^{kn} = (b^k)^n$).
4.  **Combine Terms with Exponent $n$:** Once both the $2^n$ term and the rewritten $3^{(\ldots)n}$ term both have the same exponent $n$, combine them using the rule $a^n b^n = (ab)^n$.
5.  **Identify $a$ and $r$:** The result will be in the form $a \cdot r^n$, allowing you to clearly identify the initial constant ($a$) and the common ratio ($r$).


##### What Determines the Number of Terms Before Cancellation: Telescoping Series
The number of terms you calculate is simply the number required to confirm which terms at the beginning *do not* have a corresponding negative term to cancel them. For a difference of $k$, the **first $k$ positive terms** will survive the cancellation. It's all about how far apart the indices are in the difference $b_n - b_{n+k}$.

The number of terms you need to write out before the cancellation pattern is established depends entirely on the **difference in the indices** within the terms of the series.

In short, you must expand until the largest negative index term is matched by a subsequent positive index term.



<u><h5> 1. The Simple Case (Difference of 1) </h5></u> 



In the problem we just solved, the term was in the form:

$$a_n = b_n - b_{n+1}$$

The difference in the index is **$1$**. 

* $b_8$ is the first positive term.
* The term $b_8$ will be cancelled by the $b_n$ in the term $b_8 - b_{n}$ where $n=8$. Wait, no, that's incorrect.
* The first negative term is $-b_9$ (from $n=8$).
* The first subsequent positive term is $+b_9$ (from $n=9$).

Because the terms $\pm b_k$ are adjacent, only the first positive term ($b_8$) and the last negative term ($-b_{N+1}$) remain. You only needed to write out two terms ($n=8$ and $n=9$) to see the pattern.



<u><h5> 2. The Complex Case (Difference of $k > 1$) </h5></u>



If the term were written in the form:

$$a_n = b_n - b_{n+k} \quad (\text{where } k > 1)$$

The difference in the index is $k$. In this case, you must write out $k$ terms (or $k+1$ terms) to see the full pattern.

**Example: If $a_n = b_n - b_{n+3}$ (Difference of 3)**

You would need to write out terms for $n=1, 2, 3, 4, \dots$

$$s_N = \underbrace{(b_1 - b_4)}_{n=1} + \underbrace{(b_2 - b_5)}_{n=2} + \underbrace{(b_3 - b_6)}_{n=3} + \underbrace{(b_4 - b_7)}_{n=4} + \cdots$$

* $b_1, b_2, b_3$ remain (the first three terms).
* The first term to cancel is $b_4$ (it cancels the $-b_4$ from $n=1$).
* Therefore, you need to write enough terms until the first negative term that cancels appears, which often requires $k+1$ terms in the expansion to be certain.

---

### **III. Convergence Tests for $\sum_{n=1}^\infty a_n$** (Infinite Series)

### **1. Direct Comparison Test (DCT)**

* **When to Use:** $a_n$ and $b_n$ are **positive** and a clear **term-by-term inequality** $0 \leq a_n \leq b_n$ or $0 \leq b_n \leq a_n$ can be established (eventually).
* **Condition for Convergence:** **If $0 \leq a_n \leq b_n$** for all $n$ (eventually) **AND $\sum b_n$ converges, then $\sum a_n$ converges.**
* **Condition for Divergence:** **If $0 \leq b_n \leq a_n$** for all $n$ (eventually) **AND $\sum b_n$ diverges, then $\sum a_n$ diverges.**

### **2. Integral Test**

* **When to Use:** $a_n = f(n)$ is **positive, continuous, and decreasing.**
* **Condition for Convergence:** $\int_{1}^{\infty} f(x) \, dx$ converges.
* **Condition for Divergence:** $\int_{1}^{\infty} f(x) \, dx$ diverges.

### **3. Limit Comparison Test (LCT)**

* **When to Use:** $a_n$ and $b_n$ are **positive** and **algebraically similar** (e.g., rational functions or similar dominant terms).
* **Condition for Convergence:** $\lim_{n \to \infty} \frac{a_n}{b_n} = L$, where $0 < L < \infty$. If $\sum b_n$ converges, so does $\sum a_n$.
* **Condition for Divergence:** $\lim_{n \to \infty} \frac{a_n}{b_n} = L$, where $0 < L < \infty$. If $\sum b_n$ diverges, so does $\sum a_n$.

### **4. Alternating Series Test (AST)**

* **When to Use:** Series **alternates sign**: $\sum (-1)^n b_n$ where $b_n > 0$.
* **Condition for Convergence:** Both must hold:
    1.  $\lim_{n \to \infty} b_n = 0$ **AND**
    2.  $b_{n+1} \leq b_n$ (eventually).
* **Condition for Divergence:** Fails either of the two conditions.

### **5. Ratio Test**

* **When to Use:** $a_n$ involves **factorials** ($n!$) or **exponents** ($r^n$).
* **Condition for Convergence:** $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| < 1$.
* **Condition for Divergence:** $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| > 1$ or $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = \infty$.

### **6. Root Test**

* **When to Use:** $a_n$ involves an **$n$-th power**: $(\dots)^n$.
* **Condition for Convergence:** $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} < 1$.
* **Condition for Divergence:** $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} > 1$ or $\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|} = \infty$.

---


<h5><u> 💡 Factorials: Simplification in the Ratio Test </u></h5>


| Factorial Ratio | Full Expansion | Final Simplification |
| :--- | :--- | :--- |
| $\frac{(n+1)!}{n!}$ | $\frac{(n+1) \cdot n!}{n!}$ | $n+1$ |
| $\frac{n!}{(n+1)!}$ | $\frac{n!}{(n+1) \cdot n!}$ | $\frac{1}{n+1}$ |
| $\frac{(2n+2)!}{(2n)!}$ | $\frac{(2n+2)(2n+1)(2n)!}{(2n)!}$ | $(2n+2)(2n+1)$ |
| $\frac{(2n)!}{(2n+2)!}$ | $\frac{(2n)!}{(2n+2)(2n+1)(2n)!}$ | $\frac{1}{(2n+2)(2n+1)}$ |

###### Whenever you see a factorial in a series, your first instinct should be to reach for the **Ratio Test**, as it is specifically designed to exploit these cancellation properties. 

---

## 📘 Guide to Series Estimation & Error Bounds

### Part 1: Alternating Series Estimation Theorem (ASET)

The ASET is used **only** for alternating series $\sum (-1)^n b_n$ (where $b_n > 0$) that meet the conditions of the Alternating Series Test (AST). The primary goal is to find how many terms ($N$) are needed to reach a desired accuracy.

| Step | Goal | General Procedure | Formula Used |
| :--- | :--- | :--- | :--- |
| **1. Prove Convergence** | Show the series converges. | Verify the two conditions of the AST: **(a)** $\lim_{n \to \infty} b_n = 0$ and **(b)** $b_{n+1} \le b_n$. | $b_n = |a_n|$ |
| **2. Set up the Error Bound** | Determine the number of terms ($N$) required for the desired accuracy ($\text{Error} < \text{Tolerance}$). | The **error** ($\lvert R_N \rvert$) is less than the **absolute value of the first unused term** ($b_{N+1}$). | $\lvert R_N \rvert \le b_{N+1} < \text{Tolerance}$ |
| **3. Solve for $N$** | Find the smallest integer $N$. | **Substitute** the formula for $b_{N+1}$ into the inequality and solve for $N$ (usually by **Trial and Error** or by creating a table of values). | $\frac{1}{(N+1) \cdot \dots} < \text{Tolerance}$ |
| **4. Calculate the Estimate** | Find the sum accurate to the tolerance. | Calculate the $N^{th}$ partial sum ($S_N$) by adding the first $N$ terms of the original alternating series. | $S_N = \sum_{n=1}^N a_n = a_1 + a_2 + \dots + a_N$ |

---

### Part 2: The Integral Test Remainder (Error) Bound

This bound is used for a positive-term series $\sum a_n$ that meets the conditions of the Integral Test (i.e., $f(x)=a_n$ is continuous, positive, and decreasing). The primary goal is to bound the error in the approximation.

| Step | Goal | General Procedure | Formula Used |
| :--- | :--- | :--- | :--- |
| **1. Prove Convergence** | Show the series converges. | Verify the **Integral Test conditions** (positive, continuous, decreasing) and show the associated improper integral converges. (Alternatively, use the P-Series Test if applicable). | $\sum a_n \text{ converges if } \int_k^\infty f(x) \, dx \text{ converges}$ |
| **2. Determine the Remainder ($R_N$) Bounds** | Find the lower and upper bounds for the error when using $S_N$ as the estimate. | The remainder ($R_N$) is bounded by two improper integrals using $N$ and $N+1$.  | $\int_{N+1}^\infty f(x) \, dx \le R_N \le \int_{N}^\infty f(x) \, dx$ |
| **3. Evaluate the Integrals** | Calculate the numerical values for the lower and upper bounds. | Evaluate the two improper integrals $\int_{N+1}^\infty f(x) \, dx$ and $\int_{N}^\infty f(x) \, dx$. | $\int_a^\infty f(x) \, dx = \lim_{t \to \infty} \left[ F(x) \right]_a^t$ |
| **4. Formulate the Final Interval** | State the most accurate interval for the true sum $S$. | Add the $N^{th}$ partial sum ($S_N$) to the remainder bounds determined in Step 2. | $S_N + \int_{N+1}^\infty f(x) \, dx \le S \le S_N + \int_{N}^\infty f(x) \, dx$ |

---

### **IV. Power Series, Taylor Series, and Maclaurin Series**

### **A. Power Series and Convergence**

A power series centered at $a$ has the form $\sum_{n=0}^{\infty} c_n (x-a)^n$.

1.  **Radius of Convergence ($R$):** Found by applying the **Ratio Test** to $\sum_{n=0}^{\infty} \left| c_n (x-a)^n \right|$.
    $$\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = L \cdot |x-a|$$
    Set $L \cdot |x-a| < 1$ and solve for $|x-a| < R$.

2.  **Interval of Convergence (IOC):** The interval $(a-R, a+R)$, plus the two endpoints.
    * **Crucial Step:** The endpoints $x = a-R$ and $x = a+R$ **must** be tested individually using any of the convergence tests (AST, $p$-Series, etc.) to determine if the series converges at those points.

---

### **B. Taylor and Maclaurin Series**

| Series Type | Definition (Formula) | Center |
| :--- | :--- | :--- |
| **Taylor Series** | $$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$$ | $x=a$ |
| **Maclaurin Series** | $$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$$ | $x=0$ |

#### **C. Common Maclaurin Series**

| Function $f(x)$ | Maclaurin Series | IOC ($R$) |
| :--- | :--- | :--- |
| **Geometric** | $\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n$ | $(-1, 1)$, $R=1$ |
| **$e^x$** | $e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\sin(x)$** | $\sin(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\cos(x)$** | $\cos(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!}$ | $(-\infty, \infty)$, $R=\infty$ |
| **$\arctan(x)$** | $\arctan(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$ | $[-1, 1]$, $R=1$ |
