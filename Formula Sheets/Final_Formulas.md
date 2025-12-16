---

##🧮 Section 1: Integration, Parametric, & Polar###**Standard Antiderivatives*** **\int \sin(x) \, dx = -\cos(x) + C**
* **\int \cos(x) \, dx = \sin(x) + C**
* **\int \sec^2(x) \, dx = \tan(x) + C**
* **\int \csc^2(x) \, dx = -\cot(x) + C**
* **\int \sec(x)\tan(x) \, dx = \sec(x) + C**
* **\int \csc(x)\cot(x) \, dx = -\csc(x) + C**
* **\int \tan(x) \, dx = \ln|\sec(x)| + C**
* **\int \sec(x) \, dx = \ln|\sec(x) + \tan(x)| + C**
* **\int \csc(x) \, dx = -\ln|\csc(x) + \cot(x)| + C**

###**Inverse Trig Antiderivatives*** **\int \frac{1}{\sqrt{1-x^2}} \, dx = \arcsin(x) + C**
* **\int \frac{1}{1+x^2} \, dx = \arctan(x) + C**
* **\int \frac{1}{|x|\sqrt{x^2-1}} \, dx = \text{arcsec}(x) + C**

###**Parametric Equations**For a curve defined by x = f(t) and y = g(t):

* **Tangent Slope (\frac{dy}{dx}):** \frac{dy/dt}{dx/dt}
* Numerator: 1st derivative of y with respect to t.
* Denominator: 1st derivative of x with respect to t.


* **Arc Length (S):** \int_{a}^{b} \sqrt{(\frac{dx}{dt})^2 + (\frac{dy}{dt})^2} \, dt
* Inside the root: Sum of the squares of the 1st derivatives of x and y.



###**Polar Coordinates**For a curve r = f(\theta):

* **Tangent Slope (\frac{dy}{dx}):** \frac{(dr/d\theta)\sin\theta + r\cos\theta}{(dr/d\theta)\cos\theta - r\sin\theta}
* Uses the 1st derivative of the radius function (dr/d\theta).


* **Area of a Region (A):** \int_{\alpha}^{\beta} \frac{1}{2} r^2 \, d\theta
* The function r is squared before integrating.


* **Arc Length (S):** \int_{\alpha}^{\beta} \sqrt{r^2 + (\frac{dr}{d\theta})^2} \, d\theta
* Inside the root: Square the radius function and add the square of its 1st derivative.



---

##♾️ Section 2: Infinite Series###**Convergence Tests*** **Divergence Test:** If \lim_{n \to \infty} a_n \neq 0, the series diverges.
* **Geometric Series:** \sum ar^n converges if |r| < 1. Sum = \frac{a}{1-r}.
* **p-Series:** \sum \frac{1}{n^p} converges if p > 1.
* **Integral Test:** If f(x) is positive, continuous, and decreasing, \sum a_n and \int f(x)dx behave the same.
* **Ratio Test:** Let L = \lim_{n \to \infty} |\frac{a_{n+1}}{a_n}|. Converges if L < 1, diverges if L > 1.
* **Alternating Series Test:** \sum (-1)^n b_n converges if b_{n+1} \leq b_n and \lim_{n \to \infty} b_n = 0.

---

###**Extended Convergence Tests*** **Divergence Test (n^{th} term test):** If \lim_{n \to \infty} a_n \neq 0, the series diverges.
* *Note:* If the limit is 0, the test is inconclusive.


* **Integral Test:** If f(x) is positive, continuous, and decreasing for x \ge 1:
* \sum a_n converges if \int_{1}^{\infty} f(x) dx converges.


* **Direct Comparison Test (DCT):** Compare a_n to a known series b_n (usually a p-series or geometric):
* If a_n \le b_n and \sum b_n converges, then \sum a_n converges.
* If a_n \ge b_n and \sum b_n diverges, then \sum a_n diverges.


* **Limit Comparison Test (LCT):** Solve L = \lim_{n \to \infty} \frac{a_n}{b_n}.
* If L is a finite, positive number, both series do the same thing (both converge or both diverge).


* **Ratio Test:** L = \lim_{n \to \infty} |\frac{a_{n+1}}{a_n}|.
* Converges if L < 1; Diverges if L > 1; Inconclusive if L = 1.


* **Root Test:** L = \lim_{n \to \infty} \sqrt[n]{|a_n|}.
* Useful when the entire general term is raised to the n^{th} power.
* Converges if L < 1; Diverges if L > 1; Inconclusive if L = 1.


* **Alternating Series Test (AST):** For \sum (-1)^n b_n:
* Converges if \lim_{n \to \infty} b_n = 0 AND b_{n+1} \le b_n (terms are decreasing).



---

###**Quick Tips for the Series Section*** **Absolute vs. Conditional Convergence:** A series is **absolutely convergent** if \sum |a_n| converges. It is **conditionally convergent** if \sum a_n converges but \sum |a_n| diverges (common with the Alternating Harmonic Series).
* **The p-series Shortcut:** \sum \frac{1}{n^p} converges if p > 1 and diverges if p \le 1.

Would you like me to add a "Strategy Guide" section that explains which test to pick based on what the formula looks like (e.g., when to use Ratio vs. LCT)?

###**Common Maclaurin Series*** **Geometric:** \frac{1}{1-x} = 1 + x + x^2 + x^3 + \dots
* ROC: |x| < 1


* **Exponential:** e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots
* ROC: (-\infty, \infty)


* **Sine:** \sin(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots
* ROC: (-\infty, \infty)


* **Cosine:** \cos(x) = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots
* ROC: (-\infty, \infty)


* **Logarithm:** \ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \dots
* ROC: -1 < x \leq 1


* **Arctangent:** \arctan(x) = x - \frac{x^3}{3} + \frac{x^5}{5} - \dots
* ROC: |x| \leq 1


* **Binomial:** (1+x)^k = 1 + kx + \frac{k(k-1)}{2!}x^2 + \dots
* ROC: |x| < 1



---

##🧊 Section 3: 3D Geometry & Vectors###**Vector Basics*** **Magnitude:** |\vec{v}| = \sqrt{v_1^2 + v_2^2 + v_3^2}
* **Unit Vector:** \hat{u} = \frac{\vec{v}}{|\vec{v}|} (Scale each component by the reciprocal of the magnitude).

###**Products & Projections*** **Dot Product:** \vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + u_3v_3
* Yields a **scalar**. \vec{u} \cdot \vec{v} = 0 means vectors are orthogonal.


* **Angle Between Vectors:** \theta = \arccos\left(\frac{\vec{u} \cdot \vec{v}}{|\vec{u}| |\vec{v}|}\right)
* **Vector Projection:** \text{proj}_{\vec{u}}\vec{v} = (\frac{\vec{u} \cdot \vec{v}}{|\vec{u}|^2})\vec{u}
* **Cross Product:** \vec{a} \times \vec{b} = \langle a_2b_3 - a_3b_2, a_3b_1 - a_1b_3, a_1b_2 - a_2b_1 \rangle
* Yields a **vector** orthogonal to both \vec{a} and \vec{b}.


* **Scalar Triple Product:** \vec{u} \cdot (\vec{v} \times \vec{w})
* Result: **Volume** of a parallelepiped.



###**Lines & Planes*** **Line Equation:** \vec{r}(t) = \vec{P_0} + t\vec{d}
* \vec{P_0} is a point on the line; \vec{d} is the direction vector.


* **Plane Equation:** a(x-x_0) + b(y-y_0) + c(z-z_0) = 0
* \langle a, b, c \rangle is the **normal vector** (\vec{n}).
* (x_0, y_0, z_0) is a point on the plane.


* **Distance (Point to Plane):** D = \frac{|ax_1 + by_1 + cz_1 + d|}{\sqrt{a^2 + b^2 + c^2}}
* Numerator: Plug the point into the plane equation (ax+by+cz+d=0).
* Denominator: Magnitude of the normal vector.



###**The Parallelogram Law*** **Formula:** |\vec{u} + \vec{v}|^2 + |\vec{u} - \vec{v}|^2 = 2|\vec{u}|^2 + 2|\vec{v}|^2
* **Interpretation:** The sum of the squares of the diagonals equals the sum of the squares of the four sides.
