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
| Feature | Parametric (x=f(t), y=g(t)) | Polar (r=f(\theta)) |
| --- | --- | --- |
| **Tangent Slope** | `(dy/dt) / (dx/dt)` | `[(dr/dθ)sinθ + rcosθ] / [(dr/dθ)cosθ - rsinθ]` |
|  | **Operation:** Divide 1st degree derivative of **y** by 1st degree derivative of **x**. | **Operation:** Combine 1st degree derivative of **r** and original function **r**. |
| **Arc Length** | `∫ √[(dx/dt)² + (dy/dt)²] dt` | `∫ √[r² + (dr/dθ)²] dθ` |
|  | **Operation:** Square 1st degree derivatives, sum them, and square root. | **Operation:** Sum the square of **r** and the square of its 1st degree derivative. |
| **Area (A)** | *Varies by boundary* | `∫ 1/2 [r(θ)]² dθ` |
|  |  | **Operation:** Square the function **r** before integrating. |


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
