# Power Series Guide
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

## 📘 Guide: Power Series Representation of Functions

The entire method for representing a function $f(x)$ as a Power Series relies on manipulating the sum of the standard **Geometric Series** until it matches the form of $f(x)$.

### The Starting Point (The Base Formula)

The foundation of nearly all power series representations is the formula for a convergent Geometric Series:

$$\frac{1}{1 - u} = \sum_{n=0}^{\infty} u^n, \quad \text{for } |u| < 1$$

Your goal is to transform the given function $f(x)$ until one part of it looks like $\frac{1}{1 - u}$.

### Phase 1: Algebraic Manipulation (The Setup)

1.  **Isolate the Geometric Form:** Algebraically manipulate the given function $f(x)$ to isolate a factor or part that is in the form $\frac{1}{1 \pm (\text{something})}$.
    * *Example:* If $f(x) = \frac{5}{2+x}$, factor out a constant from the denominator to make the first term 1:
        $$f(x) = \frac{5}{2(1 + x/2)} = \frac{5}{2} \cdot \frac{1}{1 - (-x/2)}$$
    * *Here, $C = 5/2$ and $u = -x/2$.*
2.  **Determine the Initial Power Series:** Replace the geometric form with its series equivalent, $\sum u^n$.
3.  **Find the Radius ($R$):** The series will converge for $|u| < 1$. Use this inequality to find the Radius of Convergence, $R$. (E.g., if $|-x/2| < 1$, then $|x| < 2$, so $R=2$).

### Phase 2: Calculus Manipulation (Differentiation/Integration)

If your function involves a squared denominator, $\ln(\dots)$, or $\arctan(\dots)$, you must use calculus to transform the geometric form.

| Target Function Form | Calculus Step Required | General Pattern |
| :--- | :--- | :--- |
| $\frac{1}{(1-u)^2}$ | **Differentiate** the base $\frac{1}{1-u}$ | $\frac{d}{du} \left( \frac{1}{1-u} \right) = \frac{1}{(1-u)^2}$ |
| $\frac{1}{(1-u)^3}$ | **Differentiate** the result from the line above | $\frac{d}{du} \left( \frac{1}{(1-u)^2} \right) = \frac{2}{(1-u)^3}$ |
| $\ln(1 \pm u)$ | **Integrate** a manipulated version of the base $\frac{1}{1 \pm u}$ | $\int \frac{1}{1+u} du = \ln|1+u|$ |
| $\arctan(u)$ | **Integrate** a manipulated version of the base $\frac{1}{1+u^2}$ | $\int \frac{1}{1+u^2} du = \arctan(u)$ |

**General Procedure for Applying Calculus:**

1.  **Write the series:** Start with the series for the simpler form (e.g., $\frac{1}{1-u} = \sum u^n$).
2.  **Apply the operator:** Apply the required derivative ($\frac{d}{dx}$) or integral ($\int dx$) operator to **both sides** of the equation.
    * *Note:* Differentiation changes the exponent: $\frac{d}{dx} x^n = n x^{n-1}$.
    * *Note:* Integration changes the exponent: $\int x^n dx = \frac{x^{n+1}}{n+1} + C$. (Don't forget $+C$, which is usually 0 if the series is centered at 0).
3.  **Multiply/Divide/Shift:** Finally, multiply or divide the resulting series by any remaining $x$ terms or constants to match the original function $f(x)$.

The Radius of Convergence **does not change** when you differentiate or integrate a power series.


## 🛠️ Step-by-Step Guide: Power Series Representation

**Function:** $f(x) = \frac{x^2 + x}{(1 - x)^3}$

### Phase A: Build the Denominator $\left(\frac{1}{(1-x)^3}\right)$

1.  **Start with the Base Series:** Write the known geometric series formula for $g(x) = \frac{1}{1 - x}$, ensuring you use the series notation and the first few expanded terms.
    $$\frac{1}{1 - x} = \sum_{n=0}^{\infty} x^n$$
2.  **Determine Required Derivatives:** Calculate the derivative of the base function $\frac{1}{1-x}$ until the denominator is raised to the power you need (in this case, 3).
    * $\frac{d}{dx} \left(\frac{1}{1-x}\right) = \frac{1}{(1-x)^2}$ (First Derivative)
    * $\frac{d^2}{dx^2} \left(\frac{1}{1-x}\right) = \frac{2}{(1-x)^3}$ (Second Derivative)
3.  **Apply Derivatives to the Series:** Differentiate the series from Step 1 **term-by-term** two times. *Crucially, remember that differentiation shifts the starting index.*
    * $g'(x) = \sum_{n=1}^{\infty} \frac{d}{dx} (x^n) = \sum_{n=1}^{\infty} n x^{n-1}$
    * $g''(x) = \sum_{n=2}^{\infty} \frac{d}{dx} (n x^{n-1}) = \sum_{n=2}^{\infty} n(n-1) x^{n-2}$
4.  **Isolate the Target Denominator:** Solve the relationship from Step 2 to isolate the target fraction $\frac{1}{(1-x)^3}$. Then, apply that same operation to the final series obtained in Step 3.
    $$\frac{1}{(1-x)^3} = \frac{1}{2} \cdot g''(x) = \frac{1}{2} \sum_{n=2}^{\infty} n(n-1) x^{n-2}$$

### Phase B: Incorporate the Numerator $\left(x^2 + x\right)$

5.  **Multiply by the Numerator Terms:** Substitute the series expression found in Step 4 back into the original function $f(x)$:
    $$f(x) = (x^2 + x) \cdot \left[ \frac{1}{2} \sum_{n=2}^{\infty} n(n-1) x^{n-2} \right]$$
6.  **Distribute the Powers of $x$:** Distribute the $x^2$ and $x$ terms into the summation. This means adding the exponents inside the summation:
    * $x^2 \cdot x^{n-2} = x^{n-2+2} = x^n$
    * $x \cdot x^{n-2} = x^{n-2+1} = x^{n-1}$
7.  **Split and Simplify:** You will now have two separate series.
    $$f(x) = \frac{1}{2} \sum_{n=2}^{\infty} n(n-1) x^{n} + \frac{1}{2} \sum_{n=2}^{\infty} n(n-1) x^{n-1}$$

### Phase C: Combine the Series (Optional but Best Practice)

8.  **Index Adjustment:** Adjust the index of the second series (the one with $x^{n-1}$) so that its power is also $x^n$.
    * Let $k = n-1$ (which means $n = k+1$).
    * When $n=2$, $k=1$.
    * The second series becomes: $\frac{1}{2} \sum_{k=1}^{\infty} (k+1)k x^{k}$
9.  **Combine the Series:** Since both series now have the power $x^n$ (or $x^k$) and you can choose the higher starting index (2) for $n$ to avoid having to split out terms, you can combine the coefficients.

---
