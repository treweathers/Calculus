## 🧮 Vector Calculus Practice Problems

Here is a set of problems exactly like the ones you provided, along with the steps to solve them and a detailed walk-through for each.

---

### **Problem Set (For Practice)**

#### (1) Vectors in Space.
Let $\vec{a} = \langle 1, 5, -3 \rangle$ and $\vec{b} = \langle 4, -1, 2 \rangle$.
(a) Compute $\vec{a} + \vec{b}$ and $\vec{a} - \vec{b}$.
(b) Compute the magnitude $|\vec{b}|$.
(c) Find a unit vector in the direction of $\vec{b}$.

**Steps for Solving (1)**

1.  **Vector Addition/Subtraction (a):**
    * To find $\vec{a} + \vec{b}$, add the corresponding components: $\langle a_x + b_x, a_y + b_y, a_z + b_z \rangle$.
    * To find $\vec{a} - \vec{b}$, subtract the corresponding components: $\langle a_x - b_x, a_y - b_y, a_z - b_z \rangle$.
2.  **Vector Magnitude (b):**
    * For a vector $\vec{v} = \langle v_x, v_y, v_z \rangle$, the magnitude is $|\vec{v}| = \sqrt{v_x^2 + v_y^2 + v_z^2}$.
3.  **Unit Vector (c):**
    * A unit vector $\hat{u}$ in the direction of $\vec{v}$ is found by dividing the vector by its magnitude: $\hat{u} = \frac{\vec{v}}{|\vec{v}|}$.

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

1.  **Dot Product (a):**
    * For $\vec{u} = \langle u_x, u_y, u_z \rangle$ and $\vec{v} = \langle v_x, v_y, v_z \rangle$, the dot product is $\vec{u} \cdot \vec{v} = u_x v_x + u_y v_y + u_z v_z$.
2.  **Angle between Vectors (b):**
    * Use the formula $\cos(\theta) = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}| |\vec{v}|}$, which means $\theta = \arccos\left(\frac{\vec{u} \cdot \vec{v}}{|\vec{u}| |\vec{v}|}\right)$.
    * This requires computing $\vec{u} \cdot \vec{v}$ (from part a) and the magnitudes $|\vec{u}|$ and $|\vec{v}|$.
3.  **Vector Projection (c):**
    * The projection of $\vec{v}$ onto $\vec{u}$ is given by the formula $\text{proj}_{\vec{u}}\vec{v} = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|^2} \vec{u}$.

**Walk-Through for (2)**

* **Given:** $\vec{u} = \langle 2, -1, 4 \rangle$ and $\vec{v} = \langle 1, 3, -5 \rangle$.
* **(a) Compute $\vec{u} \cdot \vec{v}$:**
    * $\vec{u} \cdot \vec{v} = (2)(1) + (-1)(3) + (4)(-5) = 2 - 3 - 20 = -21$.
* **(b) Find the angle $\theta$ between $\vec{u}$ and $\vec{v}$:**
    * $|\vec{u}| = \sqrt{2^2 + (-1)^2 + 4^2} = \sqrt{4 + 1 + 16} = \sqrt{21}$.
    * $|\vec{v}| = \sqrt{1^2 + 3^2 + (-5)^2} = \sqrt{1 + 9 + 25} = \sqrt{35}$.
    * $\theta = \arccos\left(\frac{-21}{\sqrt{21}\sqrt{35}}\right) = \arccos\left(\frac{-21}{\sqrt{735}}\right)$.
* **(c) Find the projection of $\vec{v}$ onto $\vec{u}$:**
    * $|\vec{u}|^2 = 21$.
    * $\text{proj}_{\vec{u}}\vec{v} = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|^2} \vec{u} = \frac{-21}{21} \langle 2, -1, 4 \rangle = -1 \langle 2, -1, 4 \rangle = \langle -2, 1, -4 \rangle$.

---

#### (3) Cross product and area.
Let $\vec{a} = \langle 1, 0, 3 \rangle$ and $\vec{b} = \langle 2, -2, 1 \rangle$.
(a) Compute $\vec{a} \times \vec{b}$.
(b) Compute the area of the parallelogram spanned by $\vec{a}$ and $\vec{b}$.

**Steps for Solving (3)**

1.  **Cross Product (a):**
    * Use the determinant formula for the cross product: $\vec{a} \times \vec{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ a_x & a_y & a_z \\ b_x & b_y & b_z \end{vmatrix}$.
2.  **Area of Parallelogram (b):**
    * The area of the parallelogram spanned by vectors $\vec{a}$ and $\vec{b}$ is equal to the magnitude of their cross product: Area $= |\vec{a} \times \vec{b}|$.

**Walk-Through for (3)**

* **Given:** $\vec{a} = \langle 1, 0, 3 \rangle$ and $\vec{b} = \langle 2, -2, 1 \rangle$.
* **(a) Compute $\vec{a} \times \vec{b}$:**
    * 
    $$
    \vec{a} \times \vec{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 0 & 3 \\ 2 & -2 & 1 \end{vmatrix}
    $$
    * $\mathbf{i}( (0)(1) - (3)(-2) ) - \mathbf{j}( (1)(1) - (3)(2) ) + \mathbf{k}( (1)(-2) - (0)(2) )$
    * $\mathbf{i}(0 - (-6)) - \mathbf{j}(1 - 6) + \mathbf{k}(-2 - 0)$
    * $6\mathbf{i} + 5\mathbf{j} - 2\mathbf{k} = \langle 6, 5, -2 \rangle$.
* **(b) Compute the area of the parallelogram:**
    * Area $= |\vec{a} \times \vec{b}| = |\langle 6, 5, -2 \rangle| = \sqrt{6^2 + 5^2 + (-2)^2} = \sqrt{36 + 25 + 4} = \sqrt{65}$.

---

#### (4) Lines in space.
Let a line $L$ pass through the point $P_0(0, 5, -1)$ and be parallel to the vector $\vec{d} = \langle -3, 1, 5 \rangle$.
(a) Write a vector equation for $L$.
(b) Write parametric equations for $L$.
(c) Find the point where $L$ intersects the $xy$-plane (where $z=0$).

**Steps for Solving (4)**

1.  **Vector Equation (a):**
    * The vector equation of a line is $\vec{r}(t) = \vec{r}_0 + t\vec{d}$, where $\vec{r}_0$ is the position vector of a point on the line, and $\vec{d}$ is the direction vector.
2.  **Parametric Equations (b):**
    * If $\vec{r}(t) = \langle x_0 + t d_x, y_0 + t d_y, z_0 + t d_z \rangle$, the parametric equations are $x = x_0 + t d_x$, $y = y_0 + t d_y$, $z = z_0 + t d_z$.
3.  **Intersection with a Plane (c):**
    * Set the component corresponding to the plane's equation (e.g., $z=0$) equal to the parametric equation for that component, and solve for the parameter $t$.
    * Substitute the value of $t$ back into the $x$ and $y$ parametric equations to find the coordinates of the intersection point.

**Walk-Through for (4)**

* **Given:** Point $P_0(0, 5, -1)$, Direction vector $\vec{d} = \langle -3, 1, 5 \rangle$.
* **(a) Write a vector equation for $L$:**
    * $\vec{r}(t) = \langle 0, 5, -1 \rangle + t \langle -3, 1, 5 \rangle$.
* **(b) Write parametric equations for $L$:**
    * $x = 0 + t(-3) \implies x = -3t$
    * $y = 5 + t(1) \implies y = 5 + t$
    * $z = -1 + t(5) \implies z = -1 + 5t$
* **(c) Find the point where $L$ intersects the plane $z=0$:**
    * Set the $z$ parametric equation to $0$: $0 = -1 + 5t \implies 5t = 1 \implies t = 1/5$.
    * Substitute $t = 1/5$ into $x$ and $y$:
        * $x = -3(1/5) = -3/5$.
        * $y = 5 + 1/5 = 25/5 + 1/5 = 26/5$.
    * The intersection point is $(-3/5, 26/5, 0)$.

---

#### (5) Planes in space.
Consider the plane passing through the points $P(2, 0, 0)$, $Q(0, 3, 0)$, and $R(0, 0, 4)$.
(a) Find two direction vectors in the plane.
(b) Compute a normal vector $\vec{n}$ to the plane.
(c) Find the equation of the plane in the form $ax + by + cz = d$.

**Steps for Solving (5)**

1.  **Direction Vectors (a):**
    * Given three points $P, Q, R$, form two vectors within the plane, e.g., $\vec{PQ}$ and $\vec{PR}$.
    * $\vec{PQ} = Q - P$ and $\vec{PR} = R - P$.
2.  **Normal Vector (b):**
    * A normal vector $\vec{n}$ is perpendicular to the plane, and can be found by taking the cross product of the two direction vectors: $\vec{n} = \vec{PQ} \times \vec{PR}$.
3.  **Equation of the Plane (c):**
    * The scalar equation of a plane is $\vec{n} \cdot (\vec{r} - \vec{r}_0) = 0$, or $a(x-x_0) + b(y-y_0) + c(z-z_0) = 0$, where $\vec{n} = \langle a, b, c \rangle$ and $P(x_0, y_0, z_0)$ is a point on the plane.
    * Simplify this to the form $ax + by + cz = d$.

**Walk-Through for (5)**

* **Given:** $P(2, 0, 0)$, $Q(0, 3, 0)$, $R(0, 0, 4)$.
* **(a) Find two direction vectors:**
    * $\vec{PQ} = Q - P = \langle 0-2, 3-0, 0-0 \rangle = \langle -2, 3, 0 \rangle$.
    * $\vec{PR} = R - P = \langle 0-2, 0-0, 4-0 \rangle = \langle -2, 0, 4 \rangle$.
* **(b) Compute a normal vector $\vec{n}$:**
    * 
    $$
    \vec{n} = \vec{PQ} \times \vec{PR} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ -2 & 3 & 0 \\ -2 & 0 & 4 \end{vmatrix}
    $$
    * $\mathbf{i}( (3)(4) - (0)(0) ) - \mathbf{j}( (-2)(4) - (0)(-2) ) + \mathbf{k}( (-2)(0) - (3)(-2) )$
    * $\mathbf{i}(12) - \mathbf{j}(-8) + \mathbf{k}(6) = \langle 12, 8, 6 \rangle$. (Can simplify by dividing by 2 to $\langle 6, 4, 3 \rangle$, but we'll use $\langle 12, 8, 6 \rangle$ for the walk-through).
* **(c) Find the equation of the plane:**
    * Using $\vec{n} = \langle 12, 8, 6 \rangle$ and point $P(2, 0, 0)$:
    * $12(x-2) + 8(y-0) + 6(z-0) = 0$
    * $12x - 24 + 8y + 6z = 0$
    * $12x + 8y + 6z = 24$. (Dividing by 2 gives $6x + 4y + 3z = 12$).

---

#### (6) Distance to a plane.
Find the distance from the point $A(1, 4, 3)$ to the plane $x - 2y + 2z = 9$.

**Steps for Solving (6)**

1.  **Identify Components:**
    * The point is $P_1(x_1, y_1, z_1)$.
    * The plane equation is $ax + by + cz + d = 0$. (Note: convert $ax + by + cz = d$ to $ax + by + cz - d = 0$).
2.  **Apply Distance Formula:**
    * The distance $D$ from a point $P_1(x_1, y_1, z_1)$ to the plane $ax+by+cz+d=0$ is:
    $$
    D = \frac{|ax_1 + by_1 + cz_1 + d|}{\sqrt{a^2 + b^2 + c^2}}
    $$

**Walk-Through for (6)**

* **Given:** Point $A(1, 4, 3)$, Plane $x - 2y + 2z = 9 \implies x - 2y + 2z - 9 = 0$.
* **Identify Components:**
    * $(x_1, y_1, z_1) = (1, 4, 3)$.
    * $a=1, b=-2, c=2, d=-9$.
* **Apply Distance Formula:**
    $$
    D = \frac{|(1)(1) + (-2)(4) + (2)(3) + (-9)|}{\sqrt{1^2 + (-2)^2 + 2^2}}
    $$
    $$
    D = \frac{|1 - 8 + 6 - 9|}{\sqrt{1 + 4 + 4}}
    $$
    $$
    D = \frac{|-10|}{\sqrt{9}} = \frac{10}{3}
    $$

---

#### (7) Triple product and volume.
Given $\vec{u} = \langle 3, 1, 0 \rangle$, $\vec{v} = \langle 0, 2, 4 \rangle$, and $\vec{w} = \langle -1, 0, 1 \rangle$:
(a) Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$.
(b) Interpret the absolute value as a geometric quantity.

**Steps for Solving (7)**

1.  **Scalar Triple Product (a):**
    * The scalar triple product $\vec{u} \cdot (\vec{v} \times \vec{w})$ is computed as the determinant of the matrix whose rows are the components of the three vectors:
    $$
    \vec{u} \cdot (\vec{v} \times \vec{w}) = \begin{vmatrix} u_x & u_y & u_z \\ v_x & v_y & v_z \\ w_x & w_y & w_z \end{vmatrix}
    $$
2.  **Geometric Interpretation (b):**
    * The absolute value of the scalar triple product, $|\vec{u} \cdot (\vec{v} \times \vec{w})|$, represents the volume of the parallelepiped (a 3D version of a parallelogram) spanned by the three vectors $\vec{u}, \vec{v}, \vec{w}$.

**Walk-Through for (7)**

* **Given:** $\vec{u} = \langle 3, 1, 0 \rangle$, $\vec{v} = \langle 0, 2, 4 \rangle$, $\vec{w} = \langle -1, 0, 1 \rangle$.
* **(a) Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$:**
    * 
    $$
    \begin{vmatrix} 3 & 1 & 0 \\ 0 & 2 & 4 \\ -1 & 0 & 1 \end{vmatrix}
    $$
    * $3 \begin{vmatrix} 2 & 4 \\ 0 & 1 \end{vmatrix} - 1 \begin{vmatrix} 0 & 4 \\ -1 & 1 \end{vmatrix} + 0 \begin{vmatrix} 0 & 2 \\ -1 & 0 \end{vmatrix}$
    * $3((2)(1) - (4)(0)) - 1((0)(1) - (4)(-1)) + 0$
    * $3(2 - 0) - 1(0 - (-4))$
    * $3(2) - 1(4) = 6 - 4 = 2$.
* **(b) Interpret the absolute value:**
    * The absolute value is $|2| = 2$.
    * The geometric quantity is the **Volume of the parallelepiped** spanned by $\vec{u}, \vec{v}, \vec{w}$, which is **2** cubic units.

---

#### (8) Parallelogram Law (Identity).
Show that for all nonzero vectors $\vec{a}$ and $\vec{b}$ one has the equality:
$$
|\vec{a} + \vec{b}|^2 + |\vec{a} - \vec{b}|^2 = 2|\vec{a}|^2 + 2|\vec{b}|^2
$$
Interpret it geometrically by drawing a picture of a parallelogram with sides determined by the vectors $\vec{a}$ and $\vec{b}$ starting at the same vertex.

**Steps for Solving (8)**

1.  **Use the Dot Product Identity:**
    * Recall that the squared magnitude of a vector is the dot product of the vector with itself: $|\vec{v}|^2 = \vec{v} \cdot \vec{v}$.
2.  **Expand the Left-Hand Side (LHS):**
    * Expand $|\vec{a} + \vec{b}|^2 = (\vec{a} + \vec{b}) \cdot (\vec{a} + \vec{b})$ using the distributive property (FOIL).
    * Expand $|\vec{a} - \vec{b}|^2 = (\vec{a} - \vec{b}) \cdot (\vec{a} - \vec{b})$ using the distributive property.
3.  **Simplify and Combine:**
    * Use the commutative property of the dot product: $\vec{a} \cdot \vec{b} = \vec{b} \cdot \vec{a}$.
    * Combine the terms of $|\vec{a} + \vec{b}|^2$ and $|\vec{a} - \vec{b}|^2$ to show they equal the Right-Hand Side (RHS).
4.  **Geometric Interpretation:**
    * The vectors $\vec{a}$ and $\vec{b}$ form adjacent sides of a parallelogram.
    * The vector $\vec{a} + \vec{b}$ is the **main diagonal** of the parallelogram.
    * The vector $\vec{a} - \vec{b}$ (or $\vec{b} - \vec{a}$) is the **shorter diagonal** of the parallelogram.
    * The identity relates the squares of the diagonal lengths to the squares of the side lengths.

**Walk-Through for (8)**

* **Expand $|\vec{a} + \vec{b}|^2$:**
    $$
    |\vec{a} + \vec{b}|^2 = (\vec{a} + \vec{b}) \cdot (\vec{a} + \vec{b}) = \vec{a}\cdot\vec{a} + \vec{a}\cdot\vec{b} + \vec{b}\cdot\vec{a} + \vec{b}\cdot\vec{b}
    $$
    $$
    |\vec{a} + \vec{b}|^2 = |\vec{a}|^2 + 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2 \quad \text{(Equation I)}
    $$
* **Expand $|\vec{a} - \vec{b}|^2$:**
    $$
    |\vec{a} - \vec{b}|^2 = (\vec{a} - \vec{b}) \cdot (\vec{a} - \vec{b}) = \vec{a}\cdot\vec{a} - \vec{a}\cdot\vec{b} - \vec{b}\cdot\vec{a} + \vec{b}\cdot\vec{b}
    $$
    $$
    |\vec{a} - \vec{b}|^2 = |\vec{a}|^2 - 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2 \quad \text{(Equation II)}
    $$
* **Combine LHS (I + II):**
    $$
    |\vec{a} + \vec{b}|^2 + |\vec{a} - \vec{b}|^2 = \left(|\vec{a}|^2 + 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2\right) + \left(|\vec{a}|^2 - 2(\vec{a}\cdot\vec{b}) + |\vec{b}|^2\right)
    $$
    $$
    |\vec{a} + \vec{b}|^2 + |\vec{a} - \vec{b}|^2 = 2|\vec{a}|^2 + 2|\vec{b}|^2
    $$
    * The identity is proven.
* **Geometric Interpretation (Parallelogram Law):**
    * 
    * The Parallelogram Law states that the **sum of the squares of the lengths of the diagonals** ($|\vec{a} + \vec{b}|^2 + |\vec{a} - \vec{b}|^2$) of a parallelogram is equal to the **sum of the squares of the lengths of its four sides** ($|\vec{a}|^2 + |\vec{b}|^2 + |\vec{a}|^2 + |\vec{b}|^2$).

---

## 🔑 Answer Key with Step-by-Step Solutions (Original Problems)

Here are the step-by-step solutions for the original problems you provided.

### (1) Vectors in Space.
Let $\vec{u} = \langle 3, -1, 2 \rangle$ and $\vec{v} = \langle -2, 4, 1 \rangle$.

**(a) Compute $\vec{u} + \vec{v}$ and $\vec{u} - \vec{v}$.**
* **Step 1:** For $\vec{u} + \vec{v}$, add corresponding components:
    $$
    \vec{u} + \vec{v} = \langle 3 + (-2), -1 + 4, 2 + 1 \rangle = \langle 1, 3, 3 \rangle
    $$
* **Step 2:** For $\vec{u} - \vec{v}$, subtract corresponding components:
    $$
    \vec{u} - \vec{v} = \langle 3 - (-2), -1 - 4, 2 - 1 \rangle = \langle 5, -5, 1 \rangle
    $$
* **Answer:** $\vec{u} + \vec{v} = \langle 1, 3, 3 \rangle$, $\vec{u} - \vec{v} = \langle 5, -5, 1 \rangle$.

**(b) Compute the magnitude $|\vec{u}|$.**
* **Step 1:** Use the magnitude formula $|\vec{u}| = \sqrt{u_x^2 + u_y^2 + u_z^2}$:
    $$
    |\vec{u}| = \sqrt{3^2 + (-1)^2 + 2^2} = \sqrt{9 + 1 + 4}
    $$
* **Step 2:** Simplify the expression:
    $$
    |\vec{u}| = \sqrt{14}
    $$
* **Answer:** $|\vec{u}| = \sqrt{14}$.

**(c) Find a unit vector in the direction of $\vec{u}$.**
* **Step 1:** Divide the vector $\vec{u}$ by its magnitude $|\vec{u}|$ (from part b):
    $$
    \hat{u} = \frac{\vec{u}}{|\vec{u}|} = \frac{1}{\sqrt{14}} \langle 3, -1, 2 \rangle
    $$
* **Answer:** $\frac{1}{\sqrt{14}} \langle 3, -1, 2 \rangle$.

---

### (2) Dot product and projections.
Let $\vec{u} = \langle 1, 2, 3 \rangle$ and $\vec{v} = \langle -2, 0, 5 \rangle$.

**(a) Compute $\vec{u} \cdot \vec{v}$.**
* **Step 1:** Use the dot product formula $\vec{u} \cdot \vec{v} = u_x v_x + u_y v_y + u_z v_z$:
    $$
    \vec{u} \cdot \vec{v} = (1)(-2) + (2)(0) + (3)(5) = -2 + 0 + 15
    $$
* **Step 2:** Compute the final value:
    $$
    \vec{u} \cdot \vec{v} = 13
    $$
* **Answer:** 13.

**(b) Find the angle between $\vec{u}$ and $\vec{v}$.**
* **Step 1:** Compute the magnitudes of $\vec{u}$ and $\vec{v}$:
    $$
    |\vec{u}| = \sqrt{1^2 + 2^2 + 3^2} = \sqrt{1 + 4 + 9} = \sqrt{14}
    $$
    $$
    |\vec{v}| = \sqrt{(-2)^2 + 0^2 + 5^2} = \sqrt{4 + 0 + 25} = \sqrt{29}
    $$
* **Step 2:** Use the angle formula $\theta = \arccos\left(\frac{\vec{u} \cdot \vec{v}}{|\vec{u}| |\vec{v}|}\right)$, using $\vec{u} \cdot \vec{v}=13$ from part (a):
    $$
    \theta = \arccos\left(\frac{13}{\sqrt{14}\sqrt{29}}\right)
    $$
* **Answer:** $\theta = \arccos\left(\frac{13}{\sqrt{14}\sqrt{29}}\right)$.

**(c) Find the projection of $\vec{v}$ onto $\vec{u}$.**
* **Step 1:** Use the vector projection formula $\text{proj}_{\vec{u}}\vec{v} = \frac{\vec{u} \cdot \vec{v}}{|\vec{u}|^2} \vec{u}$. We use $\vec{u} \cdot \vec{v}=13$ and $|\vec{u}|^2 = 14$:
    $$
    \text{proj}_{\vec{u}}\vec{v} = \frac{13}{(\sqrt{14})^2} \langle 1, 2, 3 \rangle
    $$
* **Step 2:** Simplify the expression:
    $$
    \text{proj}_{\vec{u}}\vec{v} = \frac{13}{14} \langle 1, 2, 3 \rangle
    $$
* **Answer:** $\frac{13}{14} \langle 1, 2, 3 \rangle$.

---

### (3) Cross product and area.
Let $\vec{a} = \langle 2, 1, -3 \rangle$ and $\vec{b} = \langle -1, 4, 2 \rangle$.

**(a) Compute $\vec{a} \times \vec{b}$.**
* **Step 1:** Set up the determinant for the cross product:
    $$
    \vec{a} \times \vec{b} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & 1 & -3 \\ -1 & 4 & 2 \end{vmatrix}
    $$
* **Step 2:** Compute the determinant:
    * $\mathbf{i}$ component: $(1)(2) - (-3)(4) = 2 - (-12) = 14$
    * $\mathbf{j}$ component: $-[(2)(2) - (-3)(-1)] = -[4 - 3] = -1$
    * $\mathbf{k}$ component: $(2)(4) - (1)(-1) = 8 - (-1) = 9$
* **Step 3:** Write the resulting vector:
    $$
    \vec{a} \times \vec{b} = \langle 14, -1, 9 \rangle
    $$
* **Answer:** $\langle 14, -1, 9 \rangle$.

**(b) Compute the area of the parallelogram spanned by $\vec{a}$ and $\vec{b}$.**
* **Step 1:** The area is the magnitude of the cross product $|\vec{a} \times \vec{b}|$, using the result from part (a):
    $$
    \text{Area} = |\langle 14, -1, 9 \rangle| = \sqrt{14^2 + (-1)^2 + 9^2}
    $$
* **Step 2:** Compute the values and simplify:
    $$
    \text{Area} = \sqrt{196 + 1 + 81} = \sqrt{278}
    $$
* **Answer:** $\sqrt{278}$.

---

### (4) Lines in space.
Let a line $L$ pass through the point $(1, -2, 3)$ and be parallel to the vector $\vec{d} = \langle 4, 0, -1 \rangle$.

**(a) Write a vector equation for $L$.**
* **Step 1:** Use the formula $\vec{r}(t) = \vec{r}_0 + t\vec{d}$, where $\vec{r}_0 = \langle 1, -2, 3 \rangle$ and $\vec{d} = \langle 4, 0, -1 \rangle$:
    $$
    \vec{r}(t) = \langle 1, -2, 3 \rangle + t\langle 4, 0, -1 \rangle
    $$
* **Answer:** $\vec{r}(t) = \langle 1, -2, 3 \rangle + t\langle 4, 0, -1 \rangle$.

**(b) Write parametric equations for $L$.**
* **Step 1:** Separate the vector equation into components $x(t)$, $y(t)$, and $z(t)$:
    * $x = 1 + 4t$
    * $y = -2 + 0t = -2$
    * $z = 3 + (-1)t = 3 - t$
* **Answer:** $x = 1 + 4t$, $y = -2$, $z = 3 - t$.

**(c) Find the point where $L$ intersects the plane $z = 0$.**
* **Step 1:** Set the $z$ parametric equation equal to $0$ and solve for $t$:
    $$
    0 = 3 - t \implies t = 3
    $$
* **Step 2:** Substitute $t=3$ into the $x$ and $y$ parametric equations:
    * $x = 1 + 4(3) = 1 + 12 = 13$
    * $y = -2$ (since it is constant)
* **Step 3:** The intersection point is $(x, y, z)$:
    $$
    (13, -2, 0)
    $$
* **Answer:** $(13, -2, 0)$.

---

### (5) Planes in space.
Consider the plane passing through the points $P(1, 1, 0)$, $Q(3, -2, 1)$, and $R(0, 1, 4)$.

**(a) Find two direction vectors in the plane.**
* **Step 1:** Find vector $\vec{PQ} = Q - P$:
    $$
    \vec{PQ} = \langle 3-1, -2-1, 1-0 \rangle = \langle 2, -3, 1 \rangle
    $$
* **Step 2:** Find vector $\vec{PR} = R - P$:
    $$
    \vec{PR} = \langle 0-1, 1-1, 4-0 \rangle = \langle -1, 0, 4 \rangle
    $$
* **Answer:** $\vec{PQ} = \langle 2, -3, 1 \rangle$, $\vec{PR} = \langle -1, 0, 4 \rangle$.

**(b) Compute a normal vector.**
* **Step 1:** The normal vector $\vec{n}$ is the cross product of the two direction vectors $\vec{PQ} \times \vec{PR}$:
    $$
    \vec{n} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 2 & -3 & 1 \\ -1 & 0 & 4 \end{vmatrix}
    $$
* **Step 2:** Compute the determinant:
    * $\mathbf{i}$ component: $(-3)(4) - (1)(0) = -12 - 0 = -12$
    * $\mathbf{j}$ component: $-[(2)(4) - (1)(-1)] = -[8 - (-1)] = -9$
    * $\mathbf{k}$ component: $(2)(0) - (-3)(-1) = 0 - 3 = -3$
* **Step 3:** The resulting vector is $\langle -12, -9, -3 \rangle$. To simplify, we can use a parallel vector by multiplying by $-1/3$:
    $$
    \vec{n} = \langle 4, 3, 1 \rangle
    $$
* **Answer:** $\vec{n} = \langle 4, 3, 1 \rangle$.

**(c) Find the equation of the plane in the form $ax + by + cz = d$.**
* **Step 1:** Use the scalar equation $a(x-x_0) + b(y-y_0) + c(z-z_0) = 0$ with $\vec{n} = \langle 4, 3, 1 \rangle$ and the point $P(1, 1, 0)$:
    $$
    4(x-1) + 3(y-1) + 1(z-0) = 0
    $$
* **Step 2:** Distribute and simplify:
    $$
    4x - 4 + 3y - 3 + z = 0
    $$
    $$
    4x + 3y + z - 7 = 0
    $$
* **Step 3:** Rearrange to the form $ax + by + cz = d$:
    $$
    4x + 3y + z = 7
    $$
* **Answer:** $4x + 3y + z = 7$.

---

### (6) Distance to a plane.
Find the distance from the point $A(2, 1, 2)$ to the plane $2x - y + 2z = 5$.

* **Step 1:** Identify $P_1(x_1, y_1, z_1) = (2, 1, 2)$ and convert the plane equation to $ax + by + cz + d = 0$:
    $$
    2x - y + 2z - 5 = 0 \implies a=2, b=-1, c=2, d=-5
    $$
* **Step 2:** Use the distance formula $D = \frac{|ax_1 + by_1 + cz_1 + d|}{\sqrt{a^2 + b^2 + c^2}}$:
    $$
    D = \frac{|(2)(2) + (-1)(1) + (2)(2) + (-5)|}{\sqrt{2^2 + (-1)^2 + 2^2}}
    $$
* **Step 3:** Simplify the numerator and denominator:
    $$
    D = \frac{|4 - 1 + 4 - 5|}{\sqrt{4 + 1 + 4}} = \frac{|2|}{\sqrt{9}}
    $$
* **Step 4:** Compute the final distance:
    $$
    D = \frac{2}{3}
    $$
* **Answer:** $\frac{2}{3}$.

---

### (7) Triple product and volume.
Given $\vec{u} = \langle 1, 0, 2 \rangle$, $\vec{v} = \langle -1, 3, 1 \rangle$, and $\vec{w} = \langle 2, 1, 0 \rangle$.

**(a) Compute $\vec{u} \cdot (\vec{v} \times \vec{w})$.**
* **Step 1:** Compute the scalar triple product using the determinant:
    $$
    \vec{u} \cdot (\vec{v} \times \vec{w}) = \begin{vmatrix} 1 & 0 & 2 \\ -1 & 3 & 1 \\ 2 & 1 & 0 \end{vmatrix}
    $$
* **Step 2:** Compute the determinant by expanding along the first row:
    * $1 \begin{vmatrix} 3 & 1 \\ 1 & 0 \end{vmatrix} - 0 \begin{vmatrix} -1 & 1 \\ 2 & 0 \end{vmatrix} + 2 \begin{vmatrix} -1 & 3 \\ 2 & 1 \end{vmatrix}$
    * $1((3)(0) - (1)(1)) - 0 + 2((-1)(1) - (3)(2))$
    * $1(0 - 1) + 2(-1 - 6) = -1 + 2(-7)$
    * $-1 - 14 = -15$
* **Answer:** $-15$.

**(b) Interpret the absolute value as a geometric quantity.**
* **Step 1:** The geometric quantity is the absolute value of the scalar triple product:
    $$
    |\vec{u} \cdot (\vec{v} \times \vec{w})| = |-15| = 15
    $$
* **Step 2:** State the geometric interpretation:
    * The value **15** represents the **Volume of the parallelepiped** spanned by the vectors $\vec{u}, \vec{v}, \vec{w}$.
* **Answer:** Volume $= 15$.

---

### (8) Parallelogram Law (Identity).
Show that for all nonzero vectors $\vec{u}$ and $\vec{v}$ one has the equality: $|\vec{u} + \vec{v}|^2 + |\vec{u} - \vec{v}|^2 = 2|\vec{u}|^2 + 2|\vec{v}|^2$. Interpret it geometrically.

* **Step 1: Expand the LHS using $|\vec{a}|^2 = \vec{a} \cdot \vec{a}$:**
    $$
    \text{LHS} = |\vec{u} + \vec{v}|^2 + |\vec{u} - \vec{v}|^2
    $$
    $$
    = (\vec{u} + \vec{v}) \cdot (\vec{u} + \vec{v}) + (\vec{u} - \vec{v}) \cdot (\vec{u} - \vec{v})
    $$
* **Step 2: Use the distributive property and $\vec{u} \cdot \vec{v} = \vec{v} \cdot \vec{u}$:**
    $$
    = (\vec{u}\cdot\vec{u} + 2\vec{u}\cdot\vec{v} + \vec{v}\cdot\vec{v}) + (\vec{u}\cdot\vec{u} - 2\vec{u}\cdot\vec{v} + \vec{v}\cdot\vec{v})
    $$
* **Step 3: Simplify by canceling and grouping terms:**
    $$
    = \vec{u}\cdot\vec{u} + \vec{u}\cdot\vec{u} + \vec{v}\cdot\vec{v} + \vec{v}\cdot\vec{v} + (2\vec{u}\cdot\vec{v} - 2\vec{u}\cdot\vec{v})
    $$
    $$
    = 2(\vec{u}\cdot\vec{u}) + 2(\vec{v}\cdot\vec{v})
    $$
* **Step 4: Convert back to magnitudes to show equality with the RHS:**
    $$
    = 2|\vec{u}|^2 + 2|\vec{v}|^2 = \text{RHS}
    $$
* **Geometric Interpretation:**
    * This equality is known as the **Parallelogram Law**.
    * The vectors $\vec{u}$ and $\vec{v}$ form the adjacent sides of a parallelogram.
    * The vectors $\vec{u} + \vec{v}$ and $\vec{u} - \vec{v}$ represent the two diagonals of the parallelogram.
    * The law states that the **sum of the squares of the lengths of the diagonals** of a parallelogram is equal to the **sum of the squares of the lengths of its four sides** ($2|\vec{u}|^2 + 2|\vec{v}|^2 = |\vec{u}|^2 + |\vec{v}|^2 + |\vec{u}|^2 + |\vec{v}|^2$).
