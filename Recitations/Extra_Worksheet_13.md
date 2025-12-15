## 🧮 Vector Calculus Practice Problems (Revised)

---

### **Problem Set (For Practice)**

#### (1) Vectors in Space.
Let $\vec{a} = \langle 1, 5, -3 \rangle$ and $\vec{b} = \langle 4, -1, 2 \rangle$.
(a) Compute $\vec{a} + \vec{b}$ and $\vec{a} - \vec{b}$.
(b) Compute the magnitude $|\vec{b}|$.
(c) Find a unit vector in the direction of $\vec{b}$.

**Steps for Solving (1)**

1.  **Vector Addition/Subtraction (a):** Add/subtract the corresponding components: $\langle a_x \pm b_x, a_y \pm b_y, a_z \pm b_z \rangle$.
2.  **Vector Magnitude (b):** $|\vec{v}| = \sqrt{v_x^2 + v_y^2 + v_z^2}$.
3.  **Unit Vector (c):** $\hat{u} = \frac{\vec{v}}{|\vec{v}|}$.

**Walk-Through for (1)**

* **Given:** $\vec{a} = \langle 1, 5, -3 \rangle$ and $\vec{b} = \langle 4, -1, 2 \rangle$.
* **(a) Compute $\vec{a} + \vec{b}$ and $\vec{a} - \vec{b}$:**
    * $\vec{a} + \vec{b} = \langle 1+4, 5+(-1), -3+2 \rangle = \langle 5, 4, -1 \rangle$.
    * $\vec{a} - \vec{b} = \langle 1-4, 5-(-1), -3-2 \rangle = \langle -3, 6, -5 \rangle$.
* **(b) Compute the magnitude $|\vec{b}|$:**
    * $|\vec{b}| = \sqrt{(4)^2 + (-1)^2 + (2)^2} = \sqrt{16 + 1 + 4} = \sqrt{21}$.
* **(c) Find a unit vector in the direction of $\vec{b}$:**
    * $\hat{b} = \frac{\vec{b}}{|\vec{b}|} = \frac{1}{\sqrt{21}} \langle 4, -1, 2 \rangle$.

---

#### (2) Dot product and projections.
(a) Compute $\vec{u} \cdot \vec{v}$ for $\vec{u} = \langle 2, -1, 4 \rangle$ and $\vec{v} = \langle 1, 3, -5 \rangle$.
(b) Find the angle $\theta$ between $\vec{u}$ and $\vec{v}$.
(c) Find the projection of $\vec{v}$ onto $\vec{u}$.

**Steps for Solving (2)**

1.  **Dot Product (a):** $\vec{u} \cdot \vec{v} = u_x v_x + u_y v_y + u_z v_z$.
2.  **Angle between Vectors (b):** $\theta = \arccos\left(\frac{\vec{u} \cdot \vec{v}}{|\vec{u}| |\vec{v}|}\right)$.
3.  **Vector Projection (c):** $\text{proj}_{\vec{u}}\vec{v} = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|^2} \vec{u}$.

**Walk-Through for (2)**

* **Given:** $\vec{u} = \langle 2, -1, 4 \rangle$ and $\vec{v} = \langle 1, 3, -5 \rangle$.
* **(a) Compute $\vec{u} \cdot \vec{v}$:**
    * $\vec{u} \cdot \vec{v} = (2)(1) + (-1)(3) + (4)(-5) = 2 - 3 - 20 = -21$.
* **(b) Find the angle $\theta$ between $\vec{u}$ and $\vec{v}$:**
    * $|\vec{u}| = \sqrt{2^2 + (-1)^2 + 4^2} = \sqrt{21}$.
    * $|\vec{v}| = \sqrt{1^2 + 3^2 + (-5)^2} = \sqrt{35}$.
    * $\theta = \arccos\left(\frac{-21}{\sqrt{21}\sqrt{35}}\right) = \arccos\left(\frac{-21}{\sqrt{735}}\right)$.
* **(c) Find the projection of $\vec{v}$ onto $\vec{u}$:**
    * $\text{proj}_{\vec{u}}\vec{v} = \frac{-21}{21} \langle 2, -1, 4 \rangle = -1 \langle 2, -1, 4 \rangle = \langle -2, 1, -4 \rangle$.

---

#### (3) Cross product and area.
Let $\vec{a} = \langle 1, 0, 3 \rangle$ and $\vec{b} = \langle 2, -2, 1 \rangle$.
(a) Compute $\vec{a} \times \vec{b}$.
(b) Compute the area of the parallelogram spanned by $\vec{a}$ and $\vec{b}$.

**Steps for Solving (3)**

1.  **Cross Product (a):** Use the component formula: $\vec{a} \times \vec{b} = \langle a_y b_z - a_z b_y, a_z b_x - a_x b_z, a_x b_y - a_y b_x \rangle$.
2.  **Area of Parallelogram (b):** Area $= |\vec{a} \times \vec{b}|$.

**Walk-Through for (3)**

* **Given:** $\vec{a} = \langle 1, 0, 3 \rangle$ and $\vec{b} = \langle 2, -2, 1 \rangle$.
* **(a) Compute $\vec{a} \times \vec{b}$:**
    * **i-component ($x$):** $(0)(1) - (3)(-2) = 0 - (-6) = 6$
    * **j-component ($y$):** $(3)(2) - (1)(1) = 6 - 1 = 5$
    * **k-component ($z$):** $(1)(-2) - (0)(2) = -2 - 0 = -2$
    * $\vec{a} \times \vec{b} = \langle 6, 5, -2 \rangle$.
* **(b) Compute the area of the parallelogram:**
    * Area $= |\vec{a} \times \vec{b}| = |\langle 6, 5, -2 \rangle| = \sqrt{6^2 + 5^2 + (-2)^2} = \sqrt{36 + 25 + 4} = \sqrt{65}$.

---

#### (4) Lines in space.
Let a line $L$ pass through the point $P_0(0, 5, -1)$ and be parallel to the vector $\vec{d} = \langle -3, 1, 5 \rangle$.
(a) Write a vector equation for $L$.
(b) Write parametric equations for $L$.
(c) Find the point where $L$ intersects the $xy$-plane (where $z=0$).

**Steps for Solving (4)**

1.  **Vector Equation (a):** $\vec{r}(t) = \vec{r}_0 + t\vec{d}$.
2.  **Parametric Equations (b):** $x = x_0 + t d_x$, $y = y_0 + t d_y$, $z = z_0 + t d_z$.
3.  **Intersection with a Plane (c):** Set $z=0$ to solve for $t$, then substitute $t$ into $x$ and $y$.

**Walk-Through for (4)**

* **Given:** Point $P_0(0, 5, -1)$, Direction vector $\vec{d} = \langle -3, 1, 5 \rangle$.
* **(a) Write a vector equation for $L$:**
    * $\vec{r}(t) = \langle 0, 5, -1 \rangle + t \langle -3, 1, 5 \rangle$.
* **(b) Write parametric equations for $L$:**
    * $x = -3t$, $y = 5 + t$, $z = -1 + 5t$.
* **(c) Find the point where $L$ intersects the plane $z=0$:**
    * $0 = -1 + 5t \implies t = 1/5$.
    * $x = -3(1/5) = -3/5$.
    * $y = 5 + 1/5 = 26/5$.
    * Intersection point is $(-3/5, 26/5, 0)$.

---

#### (5) Planes in space.
Consider the plane passing through the points $P(2, 0, 0)$, $Q(0, 3, 0)$, and $R(0, 0, 4)$.
(a) Find two direction vectors in the plane.
(b) Compute a normal vector $\vec{n}$ to the plane.
(c) Find the equation of the plane in the form $ax + by + cz = d$.

**Steps for Solving (5)**

1.  **Direction Vectors (a):** $\vec{PQ} = Q - P$, $\vec{PR} = R - P$.
2.  **Normal Vector (b):** $\vec{n} = \vec{PQ} \times \vec{PR}$. Use the component formula for the cross product.
3.  **Equation of the Plane (c):** $a(x-x_0) + b(y-y_0) + c(z-z_0) = 0$.

**Walk-Through for (5)**

* **Given:** $P(2, 0, 0)$, $Q(0, 3, 0)$, $R(0, 0, 4)$.
* **(a) Find two direction vectors:**
    * $\vec{PQ} = \langle -2, 3, 0 \rangle$.
    * $\vec{PR} = \langle -2, 0, 4 \rangle$.
* **(b) Compute a normal vector $\vec{n}$:** $\vec{n} = \vec{PQ} \times \vec{PR}$.
    * **i-component ($x$):** $(3)(4) - (0)(0) = 12$
    * **j-component ($y$):** $(0)(-2) - (-2)(4) = 0 - (-8) = 8$
    * **k-component ($z$):** $(-2)(0) - (3)(-2) = 0 - (-6) = 6$
    * $\vec{n} = \langle 12, 8, 6 \rangle$. (Using $\langle 6, 4, 3 \rangle$ is simpler and also correct).
* **(c) Find the equation of the plane:**
    * Using $\vec{n} = \langle 12, 8, 6 \rangle$ and point $P(2, 0, 0)$:
    * $12(x-2) + 8(y-0) + 6(z-0) = 0$
    * $12x + 8y + 6z = 24$. (Dividing by 2 gives $6x + 4y + 3z = 12$).

---

#### (6) Distance to a plane.
Find the distance from the point $A(1, 4, 3)$ to the plane $x - 2y + 2z = 9$.

**Steps for Solving (6)**

1.  **Identify Components:** $P_1(x_1, y_1, z_1)$ and plane $ax + by + cz + d = 0$.
2.  **Apply Distance Formula:** $D = \frac{|ax_1 + by_1 + cz_1 + d|}{\sqrt{a^2 + b^2 + c^2}}$.

**Walk-Through for (6)**

* **Given:** Point $A(1, 4, 3)$, Plane $x - 2y + 2z - 9 = 0$.
* **Identify Components:** $(x_1, y_1, z_1) = (1, 4, 3)$, $a=1, b=-2, c=2, d=-9$.
* **Apply Distance Formula:**
    $$
    D = \frac{|(1)(1) + (-2)(4) + (2)(3) + (-9)|}{\sqrt{1^2 + (-2)^2 + 2^2}}
    $$
    $$
    D = \frac{|1 - 8 + 6 - 9|}{\sqrt{1 + 4 + 4}} = \frac{|-10|}{\sqrt{9}} = \frac{10}{3}
    $$

---

#### (7) Triple product and volume.
Given $\vec{u} = \langle 3, 1, 0 \rangle$, $\vec{v} = \langle 0, 2, 4 \rangle$, and $\vec{w} = \langle -1, 0, 1 \rangle$.
(a) Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$.
(b) Interpret the absolute value as a geometric quantity.

**Steps for Solving (7)**

1.  **Scalar Triple Product (a):** Calculate $\vec{v} \times \vec{w}$ first, then take the dot product $\vec{u} \cdot (\vec{v} \times \vec{w})$.
2.  **Geometric Interpretation (b):** The absolute value is the Volume of the parallelepiped.

**Walk-Through for (7)**

* **Given:** $\vec{u} = \langle 3, 1, 0 \rangle$, $\vec{v} = \langle 0, 2, 4 \rangle$, $\vec{w} = \langle -1, 0, 1 \rangle$.
* **(a) Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$:**
    * **Step 1: Compute $\vec{v} \times \vec{w}$**
        * **i-component:** $(2)(1) - (4)(0) = 2$
        * **j-component:** $(4)(-1) - (0)(1) = -4$
        * **k-component:** $(0)(0) - (2)(-1) = 2$
        * $\vec{v} \times \vec{w} = \langle 2, -4, 2 \rangle$.
    * **Step 2: Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$**
        * $\vec{u} \cdot (\vec{v} \times \vec{w}) = (3)(2) + (1)(-4) + (0)(2) = 6 - 4 + 0 = 2$.
* **(b) Interpret the absolute value:**
    * Volume $= |\vec{u} \cdot (\vec{v} \times \vec{w})| = |2| = 2$.
    * The geometric quantity is the **Volume of the parallelepiped** spanned by $\vec{u}, \vec{v}, \vec{w}$, which is **2** cubic units.

---

#### (8) Parallelogram Law (Identity).
Show that for all nonzero vectors $\vec{a}$ and $\vec{b}$ one has the equality: $|\vec{a} + \vec{b}|^2 + |\vec{a} - \vec{b}|^2 = 2|\vec{a}|^2 + 2|\vec{b}|^2$. Interpret it geometrically.

**Steps for Solving (8)**

1.  **Use $|\vec{v}|^2 = \vec{v} \cdot \vec{v}$** to expand the left-hand side (LHS).
2.  **Simplify** the dot product terms using $\vec{a}\cdot\vec{b} = \vec{b}\cdot\vec{a}$.
3.  **Group** the terms to match the right-hand side (RHS).

**Walk-Through for (8)**

* **Expand $|\vec{a} + \vec{b}|^2$:**
    $$
    |\vec{a} + \vec{b}|^2 = (\vec{a} + \vec{b}) \cdot (\vec{a} + \vec{b}) = |\vec{a}|^2 + 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2 \quad \text{(Eq. I)}
    $$
* **Expand $|\vec{a} - \vec{b}|^2$:**
    $$
    |\vec{a} - \vec{b}|^2 = (\vec{a} - \vec{b}) \cdot (\vec{a} - \vec{b}) = |\vec{a}|^2 - 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2 \quad \text{(Eq. II)}
    $$
* **Combine LHS (I + II):**
    $$
    |\vec{a} + \vec{b}|^2 + |\vec{a} - \vec{b}|^2 = (|\vec{a}|^2 + 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2) + (|\vec{a}|^2 - 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2)
    $$
    $$
    = 2|\vec{a}|^2 + 2|\vec{b}|^2
    $$
* **Geometric Interpretation (Parallelogram Law):**
    * The identity states that the **sum of the squares of the lengths of the diagonals** ($|\vec{a} + \vec{b}|^2 + |\vec{a} - \vec{b}|^2$) of a parallelogram is equal to the **sum of the squares of the lengths of its four sides** ($2|\vec{a}|^2 + 2|\vec{b}|^2$).

---

## 🔑 Answer Key with Step-by-Step Solutions (Original Problems - Revised Notation)

Here are the step-by-step solutions for the original problems, using linear notation for cross products and determinants.

### (1) Vectors in Space.
Let $\vec{u} = \langle 3, -1, 2 \rangle$ and $\vec{v} = \langle -2, 4, 1 \rangle$.

**(a) Compute $\vec{u} + \vec{v}$ and $\vec{u} - \vec{v}$.**
* **Step 1:** $\vec{u} + \vec{v} = \langle 3+(-2), -1+4, 2+1 \rangle = \langle 1, 3, 3 \rangle$.
* **Step 2:** $\vec{u} - \vec{v} = \langle 3-(-2), -1-4, 2-1 \rangle = \langle 5, -5, 1 \rangle$.
* **Answer:** $\vec{u} + \vec{v} = \langle 1, 3, 3 \rangle$, $\vec{u} - \vec{v} = \langle 5, -5, 1 \rangle$.

**(b) Compute the magnitude $|\vec{u}|$.**
* **Step 1:** $|\vec{u}| = \sqrt{3^2 + (-1)^2 + 2^2} = \sqrt{9 + 1 + 4} = \sqrt{14}$.
* **Answer:** $|\vec{u}| = \sqrt{14}$.

**(c) Find a unit vector in the direction of $\vec{u}$.**
* **Step 1:** $\hat{u} = \frac{\vec{u}}{|\vec{u}|} = \frac{1}{\sqrt{14}} \langle 3, -1, 2 \rangle$.
* **Answer:** $\frac{1}{\sqrt{14}} \langle 3, -1, 2 \rangle$.

---

### (2) Dot product and projections.
Let $\vec{u} = \langle 1, 2, 3 \rangle$ and $\vec{v} = \langle -2, 0, 5 \rangle$.

**(a) Compute $\vec{u} \cdot \vec{v}$.**
* **Step 1:** $\vec{u} \cdot \vec{v} = (1)(-2) + (2)(0) + (3)(5) = -2 + 0 + 15 = 13$.
* **Answer:** 13.

**(b) Find the angle between $\vec{u}$ and $\vec{v}$.**
* **Step 1:** Magnitudes: $|\vec{u}| = \sqrt{14}$, $|\vec{v}| = \sqrt{4 + 25} = \sqrt{29}$.
* **Step 2:** $\theta = \arccos\left(\frac{13}{\sqrt{14}\sqrt{29}}\right)$.
* **Answer:** $\theta = \arccos\left(\frac{13}{\sqrt{14}\sqrt{29}}\right)$.

**(c) Find the projection of $\vec{v}$ onto $\vec{u}$.**
* **Step 1:** $\text{proj}_{\vec{u}}\vec{v} = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|^2} \vec{u} = \frac{13}{14} \langle 1, 2, 3 \rangle$.
* **Answer:** $\frac{13}{14} \langle 1, 2, 3 \rangle$.

---

### (3) Cross product and area.
Let $\vec{a} = \langle 2, 1, -3 \rangle$ and $\vec{b} = \langle -1, 4, 2 \rangle$.

**(a) Compute $\vec{a} \times \vec{b}$.**
* **Step 1:** Use the component formula: $\vec{a} \times \vec{b} = \langle a_y b_z - a_z b_y, a_z b_x - a_x b_z, a_x b_y - a_y b_x \rangle$.
    * **x-comp:** $(1)(2) - (-3)(4) = 2 - (-12) = 14$
    * **y-comp:** $(-3)(-1) - (2)(2) = 3 - 4 = -1$
    * **z-comp:** $(2)(4) - (1)(-1) = 8 - (-1) = 9$
* **Answer:** $\langle 14, -1, 9 \rangle$.

**(b) Compute the area of the parallelogram spanned by $\vec{a}$ and $\vec{b}$.**
* **Step 1:** Area $= |\vec{a} \times \vec{b}| = \sqrt{14^2 + (-1)^2 + 9^2} = \sqrt{196 + 1 + 81} = \sqrt{278}$.
* **Answer:** $\sqrt{278}$.

---

### (4) Lines in space.
Let a line $L$ pass through the point $(1, -2, 3)$ and be parallel to the vector $\vec{d} = \langle 4, 0, -1 \rangle$.

**(a) Write a vector equation for $L$.**
* **Step 1:** $\vec{r}(t) = \langle 1, -2, 3 \rangle + t\langle 4, 0, -1 \rangle$.
* **Answer:** $\vec{r}(t) = \langle 1, -2, 3 \rangle + t\langle 4, 0, -1 \rangle$.

**(b) Write parametric equations for $L$.**
* **Step 1:** $x = 1 + 4t$, $y = -2 + 0t = -2$, $z = 3 - t$.
* **Answer:** $x = 1 + 4t$, $y = -2$, $z = 3 - t$.

**(c) Find the point where $L$ intersects the plane $z = 0$.**
* **Step 1:** Set $z=0$: $0 = 3 - t \implies t = 3$.
* **Step 2:** Substitute $t=3$: $x = 1 + 4(3) = 13$, $y = -2$.
* **Step 3:** Intersection point $(13, -2, 0)$.
* **Answer:** $(13, -2, 0)$.

---

### (5) Planes in space.
Consider the plane passing through the points $P(1, 1, 0)$, $Q(3, -2, 1)$, and $R(0, 1, 4)$.

**(a) Find two direction vectors in the plane.**
* **Step 1:** $\vec{PQ} = Q - P = \langle 2, -3, 1 \rangle$.
* **Step 2:** $\vec{PR} = R - P = \langle -1, 0, 4 \rangle$.
* **Answer:** $\vec{PQ} = \langle 2, -3, 1 \rangle$, $\vec{PR} = \langle -1, 0, 4 \rangle$.

**(b) Compute a normal vector.**
* **Step 1:** Compute $\vec{n} = \vec{PQ} \times \vec{PR}$.
    * **x-comp:** $(-3)(4) - (1)(0) = -12$
    * **y-comp:** $(1)(-1) - (2)(4) = -1 - 8 = -9$
    * **z-comp:** $(2)(0) - (-3)(-1) = 0 - 3 = -3$
* **Step 2:** $\vec{n} = \langle -12, -9, -3 \rangle$. (Using the parallel vector $\langle 4, 3, 1 \rangle$ is simplest).
* **Answer:** $\vec{n} = \langle 4, 3, 1 \rangle$.

**(c) Find the equation of the plane in the form $ax + by + cz = d$.**
* **Step 1:** $4(x-1) + 3(y-1) + 1(z-0) = 0$.
* **Step 2:** $4x - 4 + 3y - 3 + z = 0 \implies 4x + 3y + z = 7$.
* **Answer:** $4x + 3y + z = 7$.

---

### (6) Distance to a plane.
Find the distance from the point $A(2, 1, 2)$ to the plane $2x - y + 2z = 5$.

* **Step 1:** $P_1(2, 1, 2)$, Plane $2x - y + 2z - 5 = 0$. $a=2, b=-1, c=2, d=-5$.
* **Step 2:** $D = \frac{|(2)(2) + (-1)(1) + (2)(2) + (-5)|}{\sqrt{2^2 + (-1)^2 + 2^2}} = \frac{|4 - 1 + 4 - 5|}{\sqrt{9}} = \frac{|2|}{3}$.
* **Answer:** $\frac{2}{3}$.

---

### (7) Triple product and volume.
Given $\vec{u} = \langle 1, 0, 2 \rangle$, $\vec{v} = \langle -1, 3, 1 \rangle$, and $\vec{w} = \langle 2, 1, 0 \rangle$.

**(a) Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$.**
* **Step 1:** Compute $\vec{v} \times \vec{w}$.
    * **x-comp:** $(3)(0) - (1)(1) = -1$
    * **y-comp:** $(1)(2) - (-1)(0) = 2$
    * **z-comp:** $(-1)(1) - (3)(2) = -1 - 6 = -7$
    * $\vec{v} \times \vec{w} = \langle -1, 2, -7 \rangle$.
* **Step 2:** Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$: $(1)(-1) + (0)(2) + (2)(-7) = -1 + 0 - 14 = -15$.
* **Answer:** $-15$.

**(b) Interpret the absolute value as a geometric quantity.**
* **Step 1:** The absolute value is $|-15| = 15$.
* **Step 2:** The geometric quantity is the **Volume of the parallelepiped** spanned by $\vec{u}, \vec{v}, \vec{w}$.
* **Answer:** Volume $= 15$.

---

### (8) Show that for all nonzero vectors $\vec{u}$ and $\vec{v}$ one has the equality: $|\vec{u} + \vec{v}|^2 + |\vec{u} - \vec{v}|^2 = 2|\vec{u}|^2 + 2|\vec{v}|^2$. Interpret it geometrically.

* **Step 1:** Expand the LHS using $|\vec{a}|^2 = \vec{a} \cdot \vec{a}$:
    $$
    |\vec{u} + \vec{v}|^2 + |\vec{u} - \vec{v}|^2 = (\vec{u}\cdot\vec{u} + 2\vec{u}\cdot\vec{v} + \vec{v}\cdot\vec{v}) + (\vec{u}\cdot\vec{u} - 2\vec{u}\cdot\vec{v} + \vec{v}\cdot\vec{v})
    $$
* **Step 2:** Simplify by cancelling the cross terms ($2\vec{u}\cdot\vec{v} - 2\vec{u}\cdot\vec{v}=0$):
    $$
    = 2(\vec{u}\cdot\vec{u}) + 2(\vec{v}\cdot\vec{v})
    $$
* **Step 3:** Convert back to magnitudes:
    $$
    = 2|\vec{u}|^2 + 2|\vec{v}|^2
    $$
* **Geometric Interpretation:** This is the **Parallelogram Law**, stating that the sum of the squares of the lengths of the diagonals of a parallelogram equals the sum of the squares of the lengths of its four sides.
* **Answer:** $\text{LHS} = 2|\vec{u}|^2 + 2|\vec{v}|^2 = \text{RHS}$. Geometrically, it is the **Parallelogram Law**.
