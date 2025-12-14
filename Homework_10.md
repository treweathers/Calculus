That's a great set of problems to introduce yourself to three-dimensional geometry and vector algebra! Since you're completely new to this, I will break down each problem with step-by-step instructions and use a very similar example to help you understand the process.

Here are the step-by-step instructions and examples for all 12 problems:

---

## 🌎 3D Geometry and Vector Algebra Problems

### **Problem 1: Sphere Equation**

Show that the equation $4x^2 + 4y^2 + 4z^2 = 16x - 6y - 12$ represents a sphere, and find its center and radius.

#### **Goal: Convert the equation to the standard form of a sphere.**

The **standard form of a sphere** with center $(h, k, l)$ and radius $r$ is:
$$(x - h)^2 + (y - k)^2 + (z - l)^2 = r^2$$

#### **Step-by-Step Instructions**

1.  **Group Terms and Divide:** Gather all $x, y, z$ terms on the left side and constants on the right. If the coefficients of $x^2, y^2,$ and $z^2$ are not 1, divide the entire equation by that coefficient.
2.  **Complete the Square (for each variable):** For each variable term $x^2 + Bx$, add $\left(\frac{B}{2}\right)^2$ to both sides of the equation. This turns the expression into the perfect square $\left(x + \frac{B}{2}\right)^2$.
3.  **Identify Center and Radius:** Once in the standard form $(x - h)^2 + (y - k)^2 + (z - l)^2 = r^2$, the center is $(h, k, l)$ and the radius is $r = \sqrt{r^2}$.

#### **Similar Example**

**Example:** Show that $2x^2 + 2y^2 + 2z^2 = 12x + 8y + 4$ represents a sphere, and find its center and radius.

1.  **Group Terms and Divide:**
    $$2x^2 - 12x + 2y^2 - 8y + 2z^2 = 4$$
    Divide by 2:
    $$x^2 - 6x + y^2 - 4y + z^2 = 2$$
2.  **Complete the Square:**
    * For $x^2 - 6x$: Add $\left(\frac{-6}{2}\right)^2 = (-3)^2 = 9$.
    * For $y^2 - 4y$: Add $\left(\frac{-4}{2}\right)^2 = (-2)^2 = 4$.
    * For $z^2$: Add 0 (since there is no $z$ term).
    $$\underbrace{(x^2 - 6x + 9)}_{(x - 3)^2} + \underbrace{(y^2 - 4y + 4)}_{(y - 2)^2} + (z^2) = 2 + 9 + 4$$
    $$(x - 3)^2 + (y - 2)^2 + (z - 0)^2 = 15$$
3.  **Identify Center and Radius:**
    * The equation is in standard form, so it **represents a sphere**.
    * Center $(h, k, l)$ is **(3, 2, 0)**.
    * Radius $r = \sqrt{15}$.

---

### **Problem 2: Vector Operations and Magnitude**

Let $\mathbf{a} = 5\mathbf{i} + 3\mathbf{j}$, $\mathbf{b} = -\mathbf{i} - 2\mathbf{j}$. Find $\mathbf{a} + \mathbf{b}$, $4\mathbf{a} + 2\mathbf{b}$, $|\mathbf{a}|$ and $|\mathbf{a} - \mathbf{b}|$.

#### **Goal: Perform basic vector addition, scalar multiplication, and calculate magnitude.**

A 2D vector $\mathbf{v} = v_x\mathbf{i} + v_y\mathbf{j}$ can also be written in component form as $\mathbf{v} = \langle v_x, v_y \rangle$.

#### **Step-by-Step Instructions**

1.  **Vector Addition ($\mathbf{a} + \mathbf{b}$):** Add the corresponding components (i-terms with i-terms, j-terms with j-terms).
2.  **Scalar Multiplication and Addition ($4\mathbf{a} + 2\mathbf{b}$):** First, multiply each component of a vector by its scalar (the number in front of it). Then, add the resulting vectors component-wise.
3.  **Magnitude ($|\mathbf{a}|$):** For a vector $\mathbf{v} = \langle v_x, v_y \rangle$, the magnitude (length) is calculated as $|\mathbf{v}| = \sqrt{v_x^2 + v_y^2}$.
4.  **Magnitude of a Difference ($|\mathbf{a} - \mathbf{b}|$):** First, calculate the difference vector $\mathbf{a} - \mathbf{b}$ (subtract components). Then, calculate the magnitude of the resulting vector using the formula from step 3.

#### **Similar Example**

**Example:** Let $\mathbf{u} = 2\mathbf{i} - 4\mathbf{j}$, $\mathbf{v} = 3\mathbf{i} + \mathbf{j}$. Find $\mathbf{u} + \mathbf{v}$, $3\mathbf{u} + \mathbf{v}$, $|\mathbf{v}|$ and $|\mathbf{u} - \mathbf{v}|$.

1.  **Vector Addition:**
    $$\mathbf{u} + \mathbf{v} = (2\mathbf{i} - 4\mathbf{j}) + (3\mathbf{i} + \mathbf{j}) = (2+3)\mathbf{i} + (-4+1)\mathbf{j} = \mathbf{5\mathbf{i} - 3\mathbf{j}}$$
2.  **Scalar Multiplication and Addition:**
    $$3\mathbf{u} = 3(2\mathbf{i} - 4\mathbf{j}) = 6\mathbf{i} - 12\mathbf{j}$$
    $$3\mathbf{u} + \mathbf{v} = (6\mathbf{i} - 12\mathbf{j}) + (3\mathbf{i} + \mathbf{j}) = (6+3)\mathbf{i} + (-12+1)\mathbf{j} = \mathbf{9\mathbf{i} - 11\mathbf{j}}$$
3.  **Magnitude:**
    $$|\mathbf{v}| = |3\mathbf{i} + \mathbf{j}| = \sqrt{3^2 + 1^2} = \sqrt{9 + 1} = \mathbf{\sqrt{10}}$$
4.  **Magnitude of a Difference:**
    $$\mathbf{u} - \mathbf{v} = (2\mathbf{i} - 4\mathbf{j}) - (3\mathbf{i} + \mathbf{j}) = (2-3)\mathbf{i} + (-4-1)\mathbf{j} = -\mathbf{i} - 5\mathbf{j}$$
    $$|\mathbf{u} - \mathbf{v}| = |-\mathbf{i} - 5\mathbf{j}| = \sqrt{(-1)^2 + (-5)^2} = \sqrt{1 + 25} = \mathbf{\sqrt{26}}$$

---

### **Problem 3: Dot Product with Unit Vector**

In the picture below, if $\mathbf{u}$ is a unit vector, find $\mathbf{u} \cdot \mathbf{v}$ and $\mathbf{u} \cdot \mathbf{w}$.

(The image is missing, but typically shows two vectors $\mathbf{v}$ and $\mathbf{w}$ originating from the same point as the unit vector $\mathbf{u}$, with specific angles between them.)

#### **Goal: Calculate the dot product using magnitudes and the angle between vectors.**

The **dot product** of two vectors $\mathbf{a}$ and $\mathbf{b}$ is defined as:
$$\mathbf{a} \cdot \mathbf{b} = |\mathbf{a}||\mathbf{b}| \cos \theta$$
where $\theta$ is the angle between $\mathbf{a}$ and $\mathbf{b}$.

#### **Step-by-Step Instructions (Assuming a typical diagram setup)**

1.  **Identify Magnitudes:** Determine the lengths of the vectors. The problem states $\mathbf{u}$ is a **unit vector**, which means $|\mathbf{u}| = 1$. The lengths of $\mathbf{v}$ and $\mathbf{w}$ will be given or implied by the diagram (e.g., $|\mathbf{v}|=4, |\mathbf{w}|=6$).
2.  **Identify Angles:** Determine the angle $\theta_1$ between $\mathbf{u}$ and $\mathbf{v}$, and the angle $\theta_2$ between $\mathbf{u}$ and $\mathbf{w}$ from the diagram.
3.  **Calculate Dot Products:** Substitute the magnitudes and angles into the dot product formula for each pair.

#### **Similar Example**

**Example:** Vector $\mathbf{u}$ is a unit vector. Vector $\mathbf{v}$ has magnitude 5 and the angle between $\mathbf{u}$ and $\mathbf{v}$ is $60^\circ$. Vector $\mathbf{w}$ has magnitude 2 and is perpendicular to $\mathbf{u}$. Find $\mathbf{u} \cdot \mathbf{v}$ and $\mathbf{u} \cdot \mathbf{w}$.

1.  **Identify Magnitudes:**
    $$|\mathbf{u}| = 1$$
    $$|\mathbf{v}| = 5$$
    $$|\mathbf{w}| = 2$$
2.  **Identify Angles:**
    * Angle between $\mathbf{u}$ and $\mathbf{v}$ is $\theta_1 = 60^\circ$.
    * $\mathbf{w}$ is perpendicular to $\mathbf{u}$, so the angle between them is $\theta_2 = 90^\circ$.
3.  **Calculate Dot Products:**
    * **$\mathbf{u} \cdot \mathbf{v}$:**
        $$\mathbf{u} \cdot \mathbf{v} = |\mathbf{u}||\mathbf{v}| \cos 60^\circ = (1)(5) \left(\frac{1}{2}\right) = \mathbf{2.5}$$
    * **$\mathbf{u} \cdot \mathbf{w}$:**
        $$\mathbf{u} \cdot \mathbf{w} = |\mathbf{u}||\mathbf{w}| \cos 90^\circ = (1)(2) (0) = \mathbf{0}$$

---

### **Problem 4: Orthogonal, Parallel, or Neither**

Determine whether the given vectors are orthogonal, parallel, or neither.
(a) $\mathbf{u} = \langle -5 , 4 , -2 \rangle$, $\mathbf{v} = \langle 3 , 4 , -1 \rangle$
(b) $\mathbf{u} = 9\mathbf{i} - 6\mathbf{j} + 3\mathbf{k}$, $\mathbf{v} = -6\mathbf{i} + 4\mathbf{j} - 2\mathbf{k}$
(c) $\mathbf{u} = \langle c , c , c \rangle$, $\mathbf{v} = \langle c , 0 , -c \rangle$

#### **Goal: Use the dot product and scalar multiple tests.**

* **Orthogonal (Perpendicular):** Two non-zero vectors $\mathbf{u}$ and $\mathbf{v}$ are orthogonal if their **dot product is zero**: $\mathbf{u} \cdot \mathbf{v} = 0$.
* **Parallel:** Two non-zero vectors $\mathbf{u}$ and $\mathbf{v}$ are parallel if one is a **scalar multiple** of the other: $\mathbf{v} = k\mathbf{u}$ for some scalar $k$.

#### **Step-by-Step Instructions**

1.  **Check for Parallel:** See if the components are proportional. Can you find a number $k$ such that $v_x = k u_x$, $v_y = k u_y$, and $v_z = k u_z$?
2.  **Check for Orthogonal:** Calculate the dot product $\mathbf{u} \cdot \mathbf{v} = u_x v_x + u_y v_y + u_z v_z$. If the result is 0, they are orthogonal.
3.  **Conclusion:** If the vectors are not parallel (Step 1 failed) and not orthogonal (Step 2 failed), they are **neither**.

#### **Similar Example**

**Example:** Determine if $\mathbf{a} = \langle 1, -2, 3 \rangle$ and $\mathbf{b} = \langle 2, -4, 6 \rangle$ are orthogonal, parallel, or neither.

1.  **Check for Parallel:** Is $\mathbf{b} = k\mathbf{a}$?
    * $2 = k(1) \implies k=2$
    * $-4 = k(-2) \implies k=2$
    * $6 = k(3) \implies k=2$
    Since $\mathbf{b} = 2\mathbf{a}$, the vectors are **parallel**. (If the $k$ values were different, you would proceed to Step 2.)

**Example:** Determine if $\mathbf{r} = \langle 4, 1, -2 \rangle$ and $\mathbf{s} = \langle -2, 6, 1 \rangle$ are orthogonal, parallel, or neither.

1.  **Check for Parallel:** Is $\mathbf{s} = k\mathbf{r}$?
    * $-2 = k(4) \implies k = -1/2$
    * $6 = k(1) \implies k = 6$
    Since the $k$ values are different, the vectors are **not parallel**.
2.  **Check for Orthogonal:**
    $$\mathbf{r} \cdot \mathbf{s} = (4)(-2) + (1)(6) + (-2)(1) = -8 + 6 - 2 = -4$$
    Since $\mathbf{r} \cdot \mathbf{s} \neq 0$, the vectors are **not orthogonal**.
3.  **Conclusion:** The vectors are **neither** orthogonal nor parallel.

---

### **Problem 5: Angle Between Vectors**

Find the values of $x$ such that the angle between the vectors $\mathbf{a} = \langle 2 , 1 , -1 \rangle$ and $\mathbf{b} = \langle 1 , x , 0 \rangle$ is $45^\circ$.

#### **Goal: Use the dot product formula to solve for the unknown variable.**

The relationship between the dot product, magnitudes, and the angle is:
$$\mathbf{a} \cdot \mathbf{b} = |\mathbf{a}||\mathbf{b}| \cos \theta$$
Rearranging to solve for the cosine of the angle:
$$\cos \theta = \frac{\mathbf{a} \cdot \mathbf{b}}{|\mathbf{a}||\mathbf{b}|}$$

#### **Step-by-Step Instructions**

1.  **Calculate the Dot Product ($\mathbf{a} \cdot \mathbf{b}$):** Multiply corresponding components and add the results.
2.  **Calculate Magnitudes ($|\mathbf{a}|, |\mathbf{b}|$):** Use the magnitude formula $\sqrt{v_x^2 + v_y^2 + v_z^2}$.
3.  **Set up the Equation:** Substitute $\mathbf{a} \cdot \mathbf{b}$, $|\mathbf{a}|$, $|\mathbf{b}|$, and the known value of $\cos 45^\circ$ into the formula.
4.  **Solve for $x$:** Algebraically manipulate the equation to isolate and solve for $x$.

#### **Similar Example**

**Example:** Find the values of $k$ such that the angle between $\mathbf{u} = \langle 1 , 0 , 1 \rangle$ and $\mathbf{v} = \langle k , 1 , 0 \rangle$ is $60^\circ$.

1.  **Dot Product:**
    $$\mathbf{u} \cdot \mathbf{v} = (1)(k) + (0)(1) + (1)(0) = k$$
2.  **Magnitudes:**
    $$|\mathbf{u}| = \sqrt{1^2 + 0^2 + 1^2} = \sqrt{2}$$
    $$|\mathbf{v}| = \sqrt{k^2 + 1^2 + 0^2} = \sqrt{k^2 + 1}$$
3.  **Set up the Equation:** $\cos 60^\circ = \frac{1}{2}$.
    $$\cos 60^\circ = \frac{\mathbf{u} \cdot \mathbf{v}}{|\mathbf{u}||\mathbf{v}|} \implies \frac{1}{2} = \frac{k}{\sqrt{2} \sqrt{k^2 + 1}}$$
4.  **Solve for $k$:**
    $$\sqrt{2} \sqrt{k^2 + 1} = 2k$$
    Square both sides:
    $$2 (k^2 + 1) = 4k^2$$
    $$2k^2 + 2 = 4k^2$$
    $$2 = 2k^2$$
    $$1 = k^2 \implies k = \pm 1$$
    * **Check for valid solutions:** Because the angle $\theta$ in the dot product formula is typically between $0$ and $\pi$, and $\cos 60^\circ$ is positive, the dot product $k$ **must be positive**.
    * $k = 1$: $\mathbf{u} \cdot \mathbf{v} = 1 > 0$ (Valid)
    * $k = -1$: $\mathbf{u} \cdot \mathbf{v} = -1 < 0$ (Invalid - this gives $120^\circ$)
    The only value is $\mathbf{k=1}$.

---

### **Problem 6: Distance from a Point to a Line**

Use a scalar projection to show that the distance $d$ from a point $P_1(x_1, y_1)$ to the line $ax + by + c = 0$ is
$$d = \frac{|ax_1 + by_1 + c|}{\sqrt{a^2 + b^2}}$$
Use this formula to find the distance from the point $(-2, 3)$ to the line $3x - 4y + 5 = 0$.

#### **Goal: Apply the derived formula for distance.**

You are asked to *show the derivation* first (which is a theoretical step using projections, as the problem states) and then *use the formula*. For a newcomer, I will focus on the application of the formula, which is the calculation part.

The **distance $d$** from a point $P_1(x_1, y_1)$ to a line $ax + by + c = 0$ is:
$$d = \frac{|ax_1 + by_1 + c|}{\sqrt{a^2 + b^2}}$$

#### **Step-by-Step Instructions (Application)**

1.  **Identify Variables:** Identify the point's coordinates $(x_1, y_1)$ and the line's coefficients $a, b, c$ from the equation $ax + by + c = 0$.
2.  **Substitute into Numerator:** Calculate the value of $|ax_1 + by_1 + c|$. This is simply plugging the point into the left side of the line equation.
3.  **Calculate Denominator:** Calculate the value of the denominator $\sqrt{a^2 + b^2}$.
4.  **Compute Distance:** Divide the numerator by the denominator.

#### **Similar Example**

**Example:** Find the distance from the point $(1, -5)$ to the line $2x + 3y - 6 = 0$.

1.  **Identify Variables:**
    * Point $(x_1, y_1) = (1, -5)$
    * Line coefficients: $a=2, b=3, c=-6$
2.  **Substitute into Numerator:**
    $$|ax_1 + by_1 + c| = |(2)(1) + (3)(-5) + (-6)| = |2 - 15 - 6| = |-19| = 19$$
3.  **Calculate Denominator:**
    $$\sqrt{a^2 + b^2} = \sqrt{2^2 + 3^2} = \sqrt{4 + 9} = \sqrt{13}$$
4.  **Compute Distance:**
    $$d = \frac{|ax_1 + by_1 + c|}{\sqrt{a^2 + b^2}} = \mathbf{\frac{19}{\sqrt{13}}}$$

---

### **Problem 7: Cross Product and Orthogonality**

Find the cross product of $\mathbf{a} = t \mathbf{i} + \cos t \mathbf{j} + \sin t \mathbf{k}$ and $\mathbf{b} = \mathbf{i} - \sin t \mathbf{j} + \cos t \mathbf{k}$, and verify that it is orthogonal to both $\mathbf{a}$ and $\mathbf{b}$.

#### **Goal: Calculate the cross product and verify orthogonality using the dot product.**

The **cross product** $\mathbf{a} \times \mathbf{b}$ results in a new vector that is **orthogonal (perpendicular)** to both $\mathbf{a}$ and $\mathbf{b}$.

The cross product can be calculated using a determinant:
$$\mathbf{a} \times \mathbf{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ a_x & a_y & a_z \\ b_x & b_y & b_z \end{vmatrix}$$

#### **Step-by-Step Instructions**

1.  **Set up the Determinant:** Write the components of $\mathbf{a}$ and $\mathbf{b}$ in the determinant matrix.
2.  **Calculate the Cross Product ($\mathbf{a} \times \mathbf{b}$):** Expand the determinant along the first row (the $\mathbf{i}, \mathbf{j}, \mathbf{k}$ row).
    $$\mathbf{i} \begin{vmatrix} a_y & a_z \\ b_y & b_z \end{vmatrix} - \mathbf{j} \begin{vmatrix} a_x & a_z \\ b_x & b_z \end{vmatrix} + \mathbf{k} \begin{vmatrix} a_x & a_y \\ b_x & b_y \end{vmatrix}$$
3.  **Verify Orthogonality:** Calculate the dot product of the resulting vector (let's call it $\mathbf{c}$) with the original vectors: $\mathbf{c} \cdot \mathbf{a}$ and $\mathbf{c} \cdot \mathbf{b}$. **Both results must be zero** to verify orthogonality.

#### **Similar Example**

**Example:** Find the cross product of $\mathbf{u} = \mathbf{i} + 2\mathbf{j} - \mathbf{k}$ and $\mathbf{v} = 3\mathbf{i} + \mathbf{j} + \mathbf{k}$, and verify orthogonality.

1.  **Set up the Determinant:** $\mathbf{u} = \langle 1, 2, -1 \rangle$, $\mathbf{v} = \langle 3, 1, 1 \rangle$.
    $$\mathbf{u} \times \mathbf{v} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 2 & -1 \\ 3 & 1 & 1 \end{vmatrix}$$
2.  **Calculate the Cross Product ($\mathbf{c} = \mathbf{u} \times \mathbf{v}$):**
    $$\mathbf{i}( (2)(1) - (-1)(1) ) - \mathbf{j}( (1)(1) - (-1)(3) ) + \mathbf{k}( (1)(1) - (2)(3) )$$
    $$\mathbf{i}(2 - (-1)) - \mathbf{j}(1 - (-3)) + \mathbf{k}(1 - 6)$$
    $$\mathbf{c} = \mathbf{3\mathbf{i} - 4\mathbf{j} - 5\mathbf{k}}$$
3.  **Verify Orthogonality:**
    * **$\mathbf{c} \cdot \mathbf{u}$:**
        $$\langle 3, -4, -5 \rangle \cdot \langle 1, 2, -1 \rangle = (3)(1) + (-4)(2) + (-5)(-1) = 3 - 8 + 5 = 0 \quad (\text{Orthogonal})$$
    * **$\mathbf{c} \cdot \mathbf{v}$:**
        $$\langle 3, -4, -5 \rangle \cdot \langle 3, 1, 1 \rangle = (3)(3) + (-4)(1) + (-5)(1) = 9 - 4 - 5 = 0 \quad (\text{Orthogonal})$$

---

### **Problem 8: Area of a Parallelogram**

Find the area of the parallelogram with vertices $P(1 , 0 , 2)$, $Q(3 , 3 , 3)$, $R(7 , 5 , 8)$ and $S(5, 2, 7)$.

#### **Goal: Use the cross product to find the area of the parallelogram.**

The **area of a parallelogram** with adjacent sides given by vectors $\mathbf{a}$ and $\mathbf{b}$ is the magnitude of their cross product:
$$\text{Area} = |\mathbf{a} \times \mathbf{b}|$$

#### **Step-by-Step Instructions**

1.  **Determine Adjacent Vectors:** Choose a starting vertex (e.g., $P$) and create two adjacent side vectors from it (e.g., $\vec{PQ}$ and $\vec{PS}$).
    $$\vec{PQ} = Q - P = \langle 3-1, 3-0, 3-2 \rangle$$
    $$\vec{PS} = S - P = \langle 5-1, 2-0, 7-2 \rangle$$
2.  **Calculate the Cross Product ($\vec{PQ} \times \vec{PS}$):** Use the determinant method from Problem 7.
3.  **Calculate the Magnitude:** Calculate the magnitude of the resulting vector $\mathbf{c} = \vec{PQ} \times \vec{PS}$ using the magnitude formula:
    $$|\mathbf{c}| = \sqrt{c_x^2 + c_y^2 + c_z^2}$$

#### **Similar Example**

**Example:** Find the area of the parallelogram with adjacent side vectors $\mathbf{a} = \langle 1, -1, 0 \rangle$ and $\mathbf{b} = \langle 2, 1, 3 \rangle$.

1.  **Determine Adjacent Vectors:** (Given as $\mathbf{a}$ and $\mathbf{b}$.)
2.  **Calculate the Cross Product ($\mathbf{c} = \mathbf{a} \times \mathbf{b}$):**
    $$\mathbf{c} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & -1 & 0 \\ 2 & 1 & 3 \end{vmatrix}$$
    $$\mathbf{c} = \mathbf{i}( (-1)(3) - (0)(1) ) - \mathbf{j}( (1)(3) - (0)(2) ) + \mathbf{k}( (1)(1) - (-1)(2) )$$
    $$\mathbf{c} = \mathbf{i}(-3) - \mathbf{j}(3) + \mathbf{k}(1 - (-2)) = \mathbf{-3\mathbf{i} - 3\mathbf{j} + 3\mathbf{k}}$$
3.  **Calculate the Magnitude (Area):**
    $$\text{Area} = |\mathbf{c}| = \sqrt{(-3)^2 + (-3)^2 + 3^2} = \sqrt{9 + 9 + 9} = \sqrt{27} = \mathbf{3\sqrt{3}}$$

---

### **Problem 9: Coplanar Points (Scalar Triple Product)**

Use the scalar triple product to determine whether the points $A(1 , 3 , 2)$, $B(3 , -1 , 6)$, $C(5 , 2 , 0)$ and $D(3, 6, -4)$ lie in the same plane.

#### **Goal: Check if the volume of the parallelepiped formed by three vectors is zero.**

Four points ($A, B, C, D$) are **coplanar** (lie in the same plane) if the volume of the parallelepiped formed by the three vectors created from these points (e.g., $\vec{AB}, \vec{AC}, \vec{AD}$) is zero.

The **volume** $V$ is the absolute value of the scalar triple product:
$$V = |\vec{AB} \cdot (\vec{AC} \times \vec{AD})|$$
This is calculated by the determinant of the $3 \times 3$ matrix formed by the components of the three vectors.

#### **Step-by-Step Instructions**

1.  **Create Three Vectors:** Choose one point (e.g., $A$) as the origin and form three vectors to the other three points.
    $$\mathbf{u} = \vec{AB} = B - A$$
    $$\mathbf{v} = \vec{AC} = C - A$$
    $$\mathbf{w} = \vec{AD} = D - A$$
2.  **Calculate the Scalar Triple Product:** Set up the determinant using the components of $\mathbf{u}, \mathbf{v}, \mathbf{w}$.
    $$\mathbf{u} \cdot (\mathbf{v} \times \mathbf{w}) = \begin{vmatrix} u_x & u_y & u_z \\ v_x & v_y & v_z \\ w_x & w_y & w_z \end{vmatrix}$$
3.  **Determine Coplanarity:** If the result of the determinant is **zero**, the volume is zero, and the four points are **coplanar**.

#### **Similar Example**

**Example:** Determine whether the points $P(1, 0, 0)$, $Q(0, 1, 0)$, $R(0, 0, 1)$, and $S(1, 1, 1)$ lie in the same plane.

1.  **Create Three Vectors (starting from $P$):**
    $$\mathbf{u} = \vec{PQ} = Q - P = \langle 0-1, 1-0, 0-0 \rangle = \langle -1, 1, 0 \rangle$$
    $$\mathbf{v} = \vec{PR} = R - P = \langle 0-1, 0-0, 1-0 \rangle = \langle -1, 0, 1 \rangle$$
    $$\mathbf{w} = \vec{PS} = S - P = \langle 1-1, 1-0, 1-0 \rangle = \langle 0, 1, 1 \rangle$$
2.  **Calculate the Scalar Triple Product:**
    $$\mathbf{u} \cdot (\mathbf{v} \times \mathbf{w}) = \begin{vmatrix} -1 & 1 & 0 \\ -1 & 0 & 1 \\ 0 & 1 & 1 \end{vmatrix}$$
    Expand along the first row:
    $$-1 \begin{vmatrix} 0 & 1 \\ 1 & 1 \end{vmatrix} - 1 \begin{vmatrix} -1 & 1 \\ 0 & 1 \end{vmatrix} + 0 \begin{vmatrix} -1 & 0 \\ 0 & 1 \end{vmatrix}$$
    $$-1(0 - 1) - 1(-1 - 0) + 0$$
    $$-1(-1) - 1(-1) = 1 + 1 = 2$$
3.  **Determine Coplanarity:** Since the scalar triple product is $2 \neq 0$, the volume is not zero, and the points are **NOT coplanar**.

---

### **Problem 10: Equation of a Parallel Plane**

Find an equation of the plane through the point $(9 , -4 , -5)$ and parallel to the plane $z = 2x - 3y$.

#### **Goal: Use the normal vector of the parallel plane to find the new plane's equation.**

The **equation of a plane** is $a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$, where $(x_0, y_0, z_0)$ is a point on the plane, and $\mathbf{n} = \langle a, b, c \rangle$ is the **normal vector** (perpendicular to the plane).

If two planes are **parallel**, they share the same (or a proportional) **normal vector**.

#### **Step-by-Step Instructions**

1.  **Find the Normal Vector ($\mathbf{n}$):** Rewrite the given plane's equation in the standard form $ax + by + cz + d = 0$. The coefficients of $x, y, z$ are the components of the normal vector $\mathbf{n} = \langle a, b, c \rangle$.
2.  **Identify Point:** The new plane must pass through the given point $(x_0, y_0, z_0)$.
3.  **Write the Equation:** Substitute $\mathbf{n}$ and the point into the plane equation formula: $a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$.

#### **Similar Example**

**Example:** Find an equation of the plane through the point $(-1, 2, 4)$ and parallel to the plane $x - 5y + 3z = 7$.

1.  **Find the Normal Vector:** The given plane is $1x - 5y + 3z - 7 = 0$.
    The normal vector is $\mathbf{n} = \langle a, b, c \rangle = \mathbf{\langle 1, -5, 3 \rangle}$.
2.  **Identify Point:**
    $$(x_0, y_0, z_0) = (-1, 2, 4)$$
3.  **Write the Equation:**
    $$a(x - x_0) + b(y - y_0) + c(z - z_0) = 0$$
    $$1(x - (-1)) + (-5)(y - 2) + 3(z - 4) = 0$$
    $$1(x + 1) - 5(y - 2) + 3(z - 4) = 0$$
    $$x + 1 - 5y + 10 + 3z - 12 = 0$$
    $$x - 5y + 3z - 1 = 0 \quad \text{or} \quad \mathbf{x - 5y + 3z = 1}$$

---

### **Problem 11: Equation of a Plane Containing a Line**

Find an equation for the plane that goes through the point $(6 , -1 , 3)$ and contains the line with symmetric equations $x/3 = y + 4 = z/2$.

#### **Goal: Find a normal vector using two direction vectors within the plane.**

To define a plane, you need a point and a normal vector $\mathbf{n}$.
1.  The line provides one **direction vector** $\mathbf{v}$ and one **point** $P_0$.
2.  The given point $P_1$ and the line's point $P_0$ form a second **direction vector** $\vec{P_0 P_1}$.
3.  The normal vector $\mathbf{n}$ is the cross product of these two direction vectors: $\mathbf{n} = \mathbf{v} \times \vec{P_0 P_1}$.

#### **Step-by-Step Instructions**

1.  **Extract Line Information (Point $P_0$ and Direction $\mathbf{v}$):**
    The symmetric equations $\frac{x-x_0}{a} = \frac{y-y_0}{b} = \frac{z-z_0}{c}$ give the direction vector $\mathbf{v} = \langle a, b, c \rangle$ and the point $P_0(x_0, y_0, z_0)$.
2.  **Form a Second Vector ($\vec{P_0 P_1}$):** Use the point $P_0$ from the line and the given point $P_1(6, -1, 3)$ to form the vector $\vec{P_0 P_1} = P_1 - P_0$.
3.  **Find the Normal Vector ($\mathbf{n}$):** Calculate the cross product $\mathbf{n} = \mathbf{v} \times \vec{P_0 P_1}$.
4.  **Write the Equation:** Use the normal vector $\mathbf{n} = \langle a, b, c \rangle$ and the given point $P_1(x_1, y_1, z_1)$ in the plane equation: $a(x - x_1) + b(y - y_1) + c(z - z_1) = 0$.

#### **Similar Example**

**Example:** Find an equation for the plane that contains the point $P_1(1, 1, 1)$ and the line $x-2 = \frac{y+1}{2} = \frac{z}{1}$.

1.  **Extract Line Information:**
    $x-2 = \frac{y-(-1)}{2} = \frac{z-0}{1}$
    * Point on the line: $P_0(2, -1, 0)$
    * Direction vector: $\mathbf{v} = \langle 1, 2, 1 \rangle$
2.  **Form a Second Vector:**
    $$\vec{P_0 P_1} = P_1 - P_0 = \langle 1-2, 1-(-1), 1-0 \rangle = \langle -1, 2, 1 \rangle$$
3.  **Find the Normal Vector ($\mathbf{n} = \mathbf{v} \times \vec{P_0 P_1}$):**
    $$\mathbf{n} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 2 & 1 \\ -1 & 2 & 1 \end{vmatrix} = \mathbf{i}(2-2) - \mathbf{j}(1-(-1)) + \mathbf{k}(2-(-2))$$
    $$\mathbf{n} = 0\mathbf{i} - 2\mathbf{j} + 4\mathbf{k} = \langle 0, -2, 4 \rangle$$
4.  **Write the Equation (Using $P_1$):**
    $$0(x - 1) + (-2)(y - 1) + 4(z - 1) = 0$$
    $$-2y + 2 + 4z - 4 = 0$$
    $$-2y + 4z - 2 = 0$$
    Divide by -2 to simplify: $\mathbf{y - 2z = -1}$ (or $\mathbf{y - 2z + 1 = 0}$)

---

### **Problem 12: Distance Between Parallel Planes**

Verify that the planes $6z = 4y - 2x$ and $9z = 1 - 3x + 6y$ are parallel, and find the distance between them.

#### **Goal: Verify parallel status using normal vectors, then calculate the distance.**

1.  **Parallel Check:** Two planes are parallel if their normal vectors $\mathbf{n}_1$ and $\mathbf{n}_2$ are parallel (i.e., $\mathbf{n}_2 = k \mathbf{n}_1$).
2.  **Distance Formula:** The distance $d$ between two parallel planes $ax + by + cz + d_1 = 0$ and $ax + by + cz + d_2 = 0$ is:
    $$d = \frac{|d_1 - d_2|}{\sqrt{a^2 + b^2 + c^2}}$$

#### **Step-by-Step Instructions**

1.  **Find Normal Vectors:** Write both plane equations in the standard form $ax + by + cz + d = 0$. Extract the normal vectors $\mathbf{n}_1$ and $\mathbf{n}_2$.
2.  **Verify Parallel:** Check if $\mathbf{n}_2 = k \mathbf{n}_1$ for some scalar $k$.
3.  **Adjust Plane Equations (if necessary):** Before using the distance formula, you **must** ensure the $a, b, c$ coefficients are identical. Multiply the first plane's equation by the scalar $k$ found in Step 2 to match the coefficients of the second plane.
4.  **Apply Distance Formula:** Identify the new $d_1, d_2$ values and the common $a, b, c$ values, then apply the formula.

#### **Similar Example**

**Example:** Verify that $2x - 2y + z = 1$ and $4x - 4y + 2z = 5$ are parallel, and find the distance between them.

1.  **Find Normal Vectors:**
    * Plane 1: $2x - 2y + z - 1 = 0$. $\mathbf{n}_1 = \langle 2, -2, 1 \rangle$.
    * Plane 2: $4x - 4y + 2z - 5 = 0$. $\mathbf{n}_2 = \langle 4, -4, 2 \rangle$.
2.  **Verify Parallel:**
    Since $\langle 4, -4, 2 \rangle = 2 \langle 2, -2, 1 \rangle$, we have $\mathbf{n}_2 = 2 \mathbf{n}_1$.
    The planes are **parallel**.
3.  **Adjust Plane Equations:** Plane 2 is already in the form $4x + 4y + 2z + d_2 = 0$.
    We use the coefficients $a=4, b=-4, c=2$.
    * Plane 2: $4x - 4y + 2z - 5 = 0 \implies d_2 = -5$.
    * Plane 1 (Multiply by $k=2$): $2(2x - 2y + z = 1) \implies 4x - 4y + 2z = 2$
        $$4x - 4y + 2z - 2 = 0 \implies d_1 = -2$$
4.  **Apply Distance Formula:**
    $$d = \frac{|d_1 - d_2|}{\sqrt{a^2 + b^2 + c^2}} = \frac{|(-2) - (-5)|}{\sqrt{4^2 + (-4)^2 + 2^2}} = \frac{|-2 + 5|}{\sqrt{16 + 16 + 4}} = \frac{3}{\sqrt{36}} = \frac{3}{6} = \mathbf{\frac{1}{2}}$$

---

I hope these examples and step-by-step guides help you successfully work through your problems!

Would you like me to go through your original Problem 1 (or any other problem) using these new steps, or would you prefer to try it yourself first?
