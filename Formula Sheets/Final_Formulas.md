# 🧮 Calculus II Final Formula Sheet
## Section 1: Integration, Parametric, & Polar
### **Standard Antiderivatives**
* **sec(x)tan(x):** ∫ sec(x)tan(x) dx = sec(x) + C
* **csc(x)cot(x):** ∫ csc(x)cot(x) dx = -csc(x) + C
* **tan(x):** ∫ tan(x) dx = ln|sec(x)| + C
* **sec(x):** ∫ sec(x) dx = ln|sec(x) + tan(x)| + C
* **csc(x):** ∫ csc(x) dx = -ln|csc(x) + cot(x)| + C

---

### **Parametric & Polar Operations**
**Parametric Equations** (x = f(t), y = g(t))

* **Tangent Slope:** (dy/dt) / (dx/dt)
* *Operation:* Divide the 1st degree derivative of y by the 1st degree derivative of x.


* **Arc Length:** ∫ √[(dx/dt)² + (dy/dt)²] dt
* *Operation:* Square the 1st degree derivatives, sum them, and take the square root.



**Polar Coordinates** (r = f(θ))

* **Tangent Slope:** [(dr/dθ)sinθ + rcosθ] / [(dr/dθ)cosθ - rsinθ]
* *Operation:* Combine the 1st degree derivative of r and the original function r.


* **Area of a Region:** ∫ 1/2 [r(θ)]² dθ
* *Operation:* Square the function r before integrating.


* **Arc Length:** ∫ √[r² + (dr/dθ)²] dθ
* *Operation:* Sum of the square of r and the square of its 1st degree derivative.
Certainly! Here is the standalone section for Parametric and Polar operations, formatted into a clean, GitHub-friendly chart and list for your study guide.

---

### **Parametric & Polar Operations Reference**
| Feature | Parametric (x=f(t), y=g(t)) | Polar (r=f(\theta)) |
| --- | --- | --- |
| **Tangent Slope** | `(dy/dt) / (dx/dt)` | `[(dr/dθ)sinθ + rcosθ] / [(dr/dθ)cosθ - rsinθ]` |
|  | **Operation:** Divide 1st degree derivative of **y** by 1st degree derivative of **x**. | **Operation:** Combine 1st degree derivative of **r** and original function **r**. |
| **Arc Length** | `∫ √[(dx/dt)² + (dy/dt)²] dt` | `∫ √[r² + (dr/dθ)²] dθ` |
|  | **Operation:** Square 1st degree derivatives, sum them, and square root. | **Operation:** Sum the square of **r** and the square of its 1st degree derivative. |
| **Area (A)** | *Varies by boundary* | `∫ 1/2 [r(θ)]² dθ` |
|  |  | **Operation:** Square the function **r** before integrating. |

---

###**Quick Execution Guide*** **Parametric:** You are always hunting for **1st degree derivatives** (x' and y'). Once you have those, you are just plugging them into the ratios or the Pythagorean-style arc length formula.
* **Polar:** You need the **original r** and the **1st degree derivative r'**. Remember that for Area, the function itself gets squared, but for Arc Length, both the function and its derivative get squared.

Would you like me to re-output the **entire** formula sheet one last time with this specific table style integrated into Section 1?

---

###**Operational Checklist**####**Parametric Logic*** **Derivatives Needed:** x'(t) and y'(t) (1st degree).
* **For Slope:** Divide y'(t) by x'(t).
* **For Arc Length:** Square both 1st derivatives \rightarrow Add them \rightarrow Root them \rightarrow Integrate.

####**Polar Logic*** **Derivatives Needed:** r'(\theta) (1st degree).
* **For Slope:** Use r'(\theta) in the product rule expansion (y' over x').
* **For Area:** Square the original r function \rightarrow Multiply by 0.5 \rightarrow Integrate.
* **For Arc Length:** Square original r \rightarrow Square r'(\theta) \rightarrow Add them \rightarrow Root them \rightarrow Integrate.

---

Would you like me to rewrite the **Series** or **3D Geometry** sections in this same "wonky-free" table format?

---

###**Operational Checklist****Parametric (x(t), y(t)):**

* **Slope:** Calculate x'(t) and y'(t), then divide y'/x'.
* **Arc Length:** Find x' and y', square them, add them, and integrate the root.

**Polar (r(\theta)):**

* **Slope:** Find r'. Use dy = r'\sin\theta + r\cos\theta and dx = r'\cos\theta - r\sin\theta.
* **Area:** Square r, multiply by 0.5, and integrate.
* **Arc Length:** Square r, square r', add them, and integrate the root.

Would you like me to rewrite any other sections of the formula sheet to match this specific "clean table" style?

---

###**Operational Breakdown****For Parametric Equations:**

* **To find the Slope:** Calculate x'(t) and y'(t) separately, then put y' over x'.
* **To find the Arc Length:** 1. Find derivatives x'(t) and y'(t).
2. Square both results.
3. Add them together.
4. Place the sum under a square root inside the integral.

**For Polar Coordinates:**

* **To find the Slope:** 1. Find r'(\theta).
2. Follow the product rule-based formula: y' = r'\sin\theta + r\cos\theta and x' = r'\cos\theta - r\sin\theta.
* **To find the Area:** Simply square your radius function r, multiply by 1/2, and integrate.
* **To find the Arc Length:** 1. Find the derivative r'(\theta).
2. Square the original function r.
3. Square the derivative r'.
4. Add them and take the square root inside the integral.

---

Would you like me to generate a few practice problems specifically to test these Polar and Parametric formulas?

---

## ♾️ Section 2: Infinite Series
### **Known Maclaurin Series**
| Function | Sigma Notation (Power Series) | First Few Terms | ROC |
| --- | --- | --- | --- |
| **Geometric** | Σ xⁿ | 1 + x + x² + x³ + ... | R = 1 |
| **eˣ** | Σ xⁿ / n! | 1 + x + x²/2! + x³/3! + ... | R = ∞ |
| **sin(x)** | Σ (-1)ⁿ x²ⁿ⁺¹ / (2n+1)! | x - x³/3! + x⁵/5! - ... | R = ∞ |
| **cos(x)** | Σ (-1)ⁿ x²ⁿ / (2n)! | 1 - x²/2! + x⁴/4! - ... | R = ∞ |
| **ln(1+x)** | Σ (-1)ⁿ⁻¹ xⁿ / n | x - x²/2 + x³/3 - x⁴/4 + ... | R = 1 |
| **arctan(x)** | Σ (-1)ⁿ x²ⁿ⁺¹ / (2n+1) | x - x³/3 + x⁵/5 - ... | R = 1 |
| **(1+x)ᵏ** | Σ (k over n) xⁿ | 1 + kx + [k(k-1)/2!]x² + ... | R = 1 |

---

## 🧊 Section 3: 3D Geometry & Vectors
### **Vector Operations**
* **Magnitude:** |v| = √(v₁² + v₂² + v₃²)
* **Unit Vector:** v / |v|
* **Dot Product:** u₁v₁ + u₂v₂ + u₃v₃
* **Angle between Vectors:** cos(θ) = (u · v) / (|u||v|)
* **Vector Projection:** proj_u(v) = [(u · v) / |u|²] * u
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
