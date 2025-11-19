# Power Series Guide

## 🧩 Components of a Power Series

| Component | General Role in $\sum_{n=0}^{\infty} c_n (x-a)^n$ | Role in Your Series $f(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{6n+5}}{2n+1}$ |
| :--- | :--- | :--- |
| **$x$ (Variable)** | This is the **variable** of the function, the value you input. | $\mathbf{x}$ remains the input variable. |
| **$n$ (Index/Exponent)** | This is the **index** of the summation, starting at $n=0$ and going to $\infty$. It determines the **term number** and is used to calculate the **exponent** of $(x-a)$. | $\mathbf{n}$ is the index. The exponent on $x$ is the expression $\mathbf{6n+5}$. |
| **$a$ (Center)** | This is the **center** of the expansion, the point around which the function is being approximated. | $\mathbf{a = 0}$. Since $x = x-0$, the function is centered at 0. |
| **$c_n$ (Coefficient)** | This is the **coefficient** of the $n$-th term. It is a constant value (or expression dependent on $n$) that does not involve $x$. | The coefficient is $\mathbf{c_n = \frac{(-1)^n}{2n+1}}$. |

## 📘 Power Series Guide: Finding $R$ and the IOC

The entire goal is to transform the Ratio Test result $L$ into the final IOC notation, including the correct parentheses ( ) or brackets [ ].

#### Step 1: Find the Limit $L$ (Ratio/Root Test)

* **Test:** Use the **Ratio Test** ($\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$) or the **Root Test** ($\lim_{n \to \infty} \sqrt[n]{\left| a_n \right|}$).
* **Result:** The limit will always be in the form: $$L = K \cdot |x - a|$$
    *Where $K$ is a constant, and $a$ is the center.*

#### Step 2: Calculate the Radius of Convergence ($R$)

* **Rule:** Set $L < 1$ and solve for $|x - a|$ to get the standard form $|x - a| < R$.
* **Formula:** $R = \frac{1}{K}$.
* **Extreme Cases:**
    * If $L=0$ (e.g., $K=0$), $R=\infty$ (IOC: $(-\infty, \infty)$).
    * If $L=\infty$, $R=0$ (IOC: $\{a\}$).

#### Step 3: Determine the Initial Open Interval

* **Inequality:** Solve $|x - a| < R$ for $x$:
    $$a - R < x < a + R$$
* **Endpoints:** The boundaries are $x = a - R$ and $x = a + R$.

#### Step 4: Check the Endpoints (Mandatory!)

This step determines the final notation (parentheses vs. brackets). You must plug each endpoint value back into the *original* series and use a constant series test (AST, p-series, etc.).

| Endpoint Test Result | Notation for that Endpoint | Deciphering ( ) vs. [ ] |
| :--- | :--- | :--- |
| **Diverges** | **( )** | The series *only* converges **inside** the interval. |
| **Converges Conditionally** | **[ ]** | The series converges at that point (only due to alternating signs). |
| **Converges Absolutely** | **[ ]** | The series converges at that point. |

#### Step 5: State the Final Interval of Convergence (IOC)

Combine the results from Step 4.

| Example Scenario | Final IOC |
| :--- | :--- |
| Converges at $a-R$, Diverges at $a+R$ | $[a-R, a+R)$ |
| Diverges at $a-R$, Converges at $a+R$ | $(a-R, a+R]$ |
| Diverges at both | $(a-R, a+R)$ |
| Converges at both (like your last problem) | $[a-R, a+R]$ |

---

## 📚 Comprehensive Guide: Power Series Representations (Cont.)

That's an excellent set of questions! You've nailed the starting point, $1/(1-x)$, which is the **base case** for almost all power series representations. The strategies of differentiating and integrating are your primary tools for deriving new series from this base.

Here is a breakdown of when and how to use differentiation and integration to find power series representations:

---

## 🔑 The Power Series Base Case
## 🗺️ Power Series Strategy Map

| Target Function Type | Strategy | Step 1: Base Case Substitution | Step 2: Operation |
| :--- | :--- | :--- | :--- |
| $\frac{1}{1-3x^2}$ | **Substitution Only** | $\frac{1}{1-r}$, where $r = 3x^2$ | Plug $3x^2$ into $\sum r^n$. |
| $\frac{1}{(1-4x)^3}$ | **Differentiation** | Let $f(x) = \frac{1}{1-4x}$. | Differentiate $f(x)$ **twice** to raise the power to 3. |
| $\ln(1 - x)$ | **Integration** | Start with $f(x) = \frac{1}{1-x}$. | Integrate the series for $f(x)$. |
| $\arctan(x)$ | **Integration** | Start with $f(x) = \frac{1}{1+x^2}$. | Integrate the series for $f(x)$. |

The foundation for nearly all these problems is the **Geometric Series Formula**:

$$\frac{1}{1-u} = \sum_{n=0}^\infty u^n, \quad \text{for } |u| < 1$$

### Phase 1: Algebraic Setup (Getting to the $\frac{1}{1-u}$ Form)

* **Factor the Denominator:** If the denominator is not $1-x$ (e.g., it is $a \pm bx$), factor out the constant $a$ so the first term is $1$.
    $$\frac{C}{a \pm bx} = \frac{C}{a} \cdot \frac{1}{1 \pm (b/a)x}$$
* **Identify the Term $u$:** Rewrite the denominator in the form $1-u$. This sets the term $u$ that will be raised to the power $n$ in the series.
    * **Example:** $\frac{1}{1+5x} = \frac{1}{1 - (-5x)}$. Here, $u = -5x$.
* **Establish the Base Series:** Write the initial series $\sum_{n=0}^\infty u^n$.

### Phase 2: Calculus Manipulation (Differentiation or Integration)

Based on the function's structure, you must perform one of the following operations on your base series from Phase 1. (Note: The **Radius of Convergence**, $R$, is unchanged by these operations.)

#### Scenario A: Differentiation (Denominator raised to a power) 🧐

Use this when your function $f(x)$ contains denominators like $\frac{1}{(1-u)^2}$ or $\frac{1}{(1-u)^3}$.

* **Determine Operations (Base Case: $\mathbf{1/(1-x)^2}$):**
    * The derivative of the base function $\frac{1}{1-x}$ is exactly the target function:
        $$\frac{d}{dx} \left( \frac{1}{1-x} \right) = \frac{1}{(1-x)^2}$$
* **Differentiate Term-by-Term:** Apply the derivative $\frac{d}{dx}$ to the general term of your series, $\sum_{n=0}^\infty c_n x^n$.
    * **Rule:** $\frac{d}{dx}(c_n x^n) = c_n \cdot n x^{n-1}$.
    * **Result:** $\frac{1}{(1-x)^2} = \frac{d}{dx} \left( \sum_{n=0}^\infty x^n \right) = \sum_{n=1}^\infty n x^{n-1}$.
* **Adjust Index:** After differentiation, the series starting index increases by 1 (e.g., $\sum_{n=0} \to \sum_{n=1}$).

#### Scenario B: Integration (Logarithms or Inverse Tangent) ➕

Use this when your function $f(x)$ contains $\ln(\dots)$ or $\arctan(\dots)$.

##### **Base Case 1: Natural Logarithm $\ln(1+x)$**

* **Prepare for Integration:** Note that $\frac{d}{dx} \ln(1+x) = \frac{1}{1+x}$. The function to integrate is the $\frac{1}{1-u}$ form, where $u=-x$:
    $$\frac{1}{1+x} = \sum_{n=0}^\infty (-x)^n = \sum_{n=0}^\infty (-1)^n x^n$$
* **Integrate Term-by-Term:** Integrate the series for $\frac{1}{1+x}$:
    $$\ln(1+x) = \int \left( \sum_{n=0}^\infty (-1)^n x^n \right) dx = C + \sum_{n=0}^\infty (-1)^n \frac{x^{n+1}}{n+1}$$
* **Determine $C$:** Plug in the center $x=0$. $\ln(1+0) = 0$. The series evaluated at $x=0$ is $0$. Thus, $C=0$.

##### **Base Case 2: Inverse Tangent $\arctan(x)$**

* **Prepare for Integration:** Note that $\frac{d}{dx} \arctan(x) = \frac{1}{1+x^2}$. The function to integrate is the $\frac{1}{1-u}$ form, where $u=-x^2$:
    $$\frac{1}{1+x^2} = \sum_{n=0}^\infty (-x^2)^n = \sum_{n=0}^\infty (-1)^n x^{2n}$$
* **Integrate Term-by-Term:** Integrate the series for $\frac{1}{1+x^2}$:
    $$\arctan(x) = \int \left( \sum_{n=0}^\infty (-1)^n x^{2n} \right) dx = C + \sum_{n=0}^\infty (-1)^n \frac{x^{2n+1}}{2n+1}$$
* **Determine $C$:** Plug in the center $x=0$. $\arctan(0) = 0$. The series evaluated at $x=0$ is $0$. Thus, $C=0$.

### Phase 3: Final Simplification and Adjustment

* **Multiply/Divide (if needed):** Multiply the resulting series by any constant coefficients or leftover powers of $x$ to exactly match the original function $f(x)$.
    * **Example:** If $f(x) = x \cdot (\text{series})$, distribute the $x$ into the summation: $x \cdot x^n = x^{n+1}$.
* **Combine Series (if needed):** If the final result is the sum of two series, adjust the index of one series so that both have the same power of $x$ (e.g., $x^k$) and then combine the general terms.

---
This guide now fully incorporates the algebraic setup, the calculus manipulation rules, and the essential base cases for both differentiation and integration scenarios. Let me know if you'd like to review any other part of the overall formula sheet!

---

## The Alternating Series Estimation Theorem

The Alternating Series Estimation Theorem provides a very simple and powerful way to estimate the error when approximating the sum of a special type of infinite series.

### Statement of the Theorem

If $S = \sum_{n=1}^\infty (-1)^{n-1} b_n$ (or $S = \sum_{n=1}^\infty (-1)^{n} b_n$) is the sum of a convergent alternating series, where the following two conditions are met:

1.  The terms are **non-increasing** in magnitude: $b_{n+1} \le b_n$ for all $n$.
2.  The limit of the terms is **zero**: $\lim_{n \to \infty} b_n = 0$.

Then, the remainder (or **error**) $R_n$ obtained by using the partial sum $S_n = b_1 - b_2 + \dots + (-1)^{n-1} b_n$ to approximate the total sum $S$ is bounded by the magnitude of the **first neglected term** $b_{n+1}$:

$$|R_n| = |S - S_n| \le b_{n+1}$$

### 💡 How It Works (Intuition)

The theorem is based on the idea that because the terms are decreasing in magnitude and alternating in sign, the partial sums "zig-zag" toward the final sum $S$, alternating between being too high and too low.

* If you stop at a positive term (say $S_{2n+1}$), the next term you skipped is negative, so your sum is an **overestimate**.
* If you stop at a negative term (say $S_{2n}$), the next term you skipped is positive, so your sum is an **underestimate**.

The actual sum $S$ must always lie between any two consecutive partial sums, $S_n$ and $S_{n+1}$. The distance between $S_n$ and $S_{n+1}$ is simply the absolute value of the next term, $|a_{n+1}| = b_{n+1}$. Therefore, the maximum error in your approximation $S_n$ cannot be larger than the size of the very next term, $b_{n+1}$.

### Application to Your Problem

In the integral approximation problem:
$$\int_{0}^{0.3} \frac{x^2}{1 + x^4} dx = \sum_{n=0}^\infty (-1)^n \frac{(0.3)^{4n+3}}{4n+3}$$

To ensure the answer is correct to **six decimal places**, the error $|R_n|$ must be less than $0.5 \times 10^{-6}$ (or $0.0000005$).

You find the smallest $n$ where the magnitude of the next term, $b_{n+1}$, is less than this error tolerance:

| $n$ (Term used) | Next Term Index $(n+1)$ | Next Term $\mathbf{b_{n+1}}$ | Magnitude $|b_{n+1}|$ |
| :---: | :---: | :---: | :---: |
| 1 | $\mathbf{2}$ | $b_2 = \frac{(0.3)^{11}}{11}$ | $\approx 0.000000161$ |

Since the magnitude of the term at $n=2$ (the first term you would skip when summing up to $n=1$) is $0.000000161$, which is $\mathbf{< 0.0000005}$, you only need to sum the terms up to $n=1$ to achieve the required six-decimal-place accuracy.

---

## 📚 Taylor and Maclaurin Series Guide

Taylor and Maclaurin series are infinite polynomial representations of a function $f(x)$ centered at a point $a$. They are used to approximate functions, evaluate difficult integrals, and solve differential equations.

---

## 1. 📝 Definitions and Formulas

### Taylor Series
A **Taylor series** is a power series representation of a function $f(x)$ centered at an arbitrary point $\mathbf{x=a}$.

The formula for the Taylor series of $f(x)$ centered at $a$ is:
$$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!} (x-a)^n$$
$$f(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \dots$$

### Maclaurin Series
A **Maclaurin series** is simply a special case of the Taylor series where the center is $\mathbf{a=0}$.

The formula for the Maclaurin series of $f(x)$ is:
$$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!} x^n$$
$$f(x) = f(0) + \frac{f'(0)}{1!}x + \frac{f''(0)}{2!}x^2 + \frac{f'''(0)}{3!}x^3 + \dots$$

---

## 2. 🪜 Step-by-Step Construction Guide

This is the standard process for finding the Taylor series for a function $f(x)$ centered at $a$.

### Step 1: Calculate Derivatives
Find the first few derivatives of the function $f(x)$:
$$f'(x), f''(x), f'''(x), \dots, f^{(n)}(x)$$

### Step 2: Evaluate at the Center (a)
Evaluate the function and all derivatives found in Step 1 at the center $\mathbf{x=a}$:
$$f(a), f'(a), f''(a), f'''(a), \dots, f^{(n)}(a)$$
The goal is to find a pattern or formula for the general term $f^{(n)}(a)$.

### Step 3: Substitute into the Series Formula
Substitute the values from Step 2 into the general Taylor series formula:
$$\sum_{n=0}^\infty \frac{f^{(n)}(a)}{n!} (x-a)^n$$

### Step 4: Determine the Radius of Convergence ($R$)
Use the **Ratio Test** to find the radius of convergence $R$ for the resulting power series:
$$L = \lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right|$$
The series converges if $L < 1$. Solve the inequality $L < 1$ for $|x-a|$ to find $R$.

---

## 3. 🧠 Essential Maclaurin Series (Memorization)

Knowing these common series allows you to avoid the lengthy differentiation process and instead use substitution, multiplication, and integration to find new series.

| Function ($f(x)$) | Maclaurin Series $\sum_{n=0}^\infty a_n x^n$ | Radius of Convergence ($R$) |
| :--- | :--- | :--- |
| $\frac{1}{1-x}$ | $\sum_{n=0}^\infty x^n = 1 + x + x^2 + x^3 + \dots$ | $R=1$ |
| $e^x$ | $\sum_{n=0}^\infty \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots$ | $R=\infty$ |
| $\sin(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$ | $R=\infty$ |
| $\cos(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots$ | $R=\infty$ |
| $\ln(1+x)$ | $\sum_{n=1}^\infty \frac{(-1)^{n-1} x^{n}}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \dots$ | $R=1$ |
| $\arctan(x)$ | $\sum_{n=0}^\infty \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots$ | $R=1$ |

---

## 4. 🛠️ Key Manipulation Techniques

Once you know the basic series, you can find series for related functions without repeating the steps in Section 2.

| Technique | Example to find series for $f(x) = \frac{1}{1+2x}$ | Result |
| :--- | :--- | :--- |
| **Substitution** | Start with $\frac{1}{1-u}$. Substitute $\mathbf{u=-2x}$. | $\sum_{n=0}^\infty (-2x)^n = \sum_{n=0}^\infty (-1)^n 2^n x^n$ |
| **Differentiation** | Start with $\arctan(x)$ series. $\frac{d}{dx}(\arctan(x)) = \frac{1}{1+x^2}$. | Differentiate $\arctan(x)$ series term-by-term to get the $\frac{1}{1+x^2}$ series. |
| **Integration** | Start with $\frac{1}{1-x}$ series. $\int \frac{1}{1-x} dx = -\ln|1-x|$. | Integrate $\frac{1}{1-x}$ series term-by-term to get the $\ln(1-x)$ series. |
| **Multiplication** | To find the series for $x^3 e^x$: | Multiply the $e^x$ series by $\mathbf{x^3}$: $x^3 \sum \frac{x^n}{n!} = \sum \frac{x^{n+3}}{n!}$ |

