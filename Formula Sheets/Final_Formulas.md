# 🧮 Calculus II Final Formula Sheet##Section 1: Integration, Parametric, & Polar
### **Standard Antiderivatives**
* **sin(x):** ∫ sin(x) dx = -cos(x) + C
* **cos(x):** ∫ cos(x) dx = sin(x) + C
* **sec^2(x):** ∫ sec²(x) dx = tan(x) + C
* **csc^2(x):** ∫ csc²(x) dx = -cot(x) + C
* **sec(x)tan(x):** ∫ sec(x)tan(x) dx = sec(x) + C
* **csc(x)cot(x):** ∫ csc(x)cot(x) dx = -csc(x) + C
* **tan(x):** ∫ tan(x) dx = ln|sec(x)| + C
* **sec(x):** ∫ sec(x) dx = ln|sec(x) + tan(x)| + C
* **csc(x):** ∫ csc(x) dx = -ln|csc(x) + cot(x)| + C

### **Inverse Trig Antiderivatives*** **arcsin:** ∫ 1/√(1-x²) dx = arcsin(x) + C
* **arctan:** ∫ 1/(1+x²) dx = arctan(x) + C
* **arcsec:** ∫ 1/(|x|√(x²-1)) dx = arcsec(x) + C

---

### **Parametric & Polar Operations****Parametric Equations** (x = f(t), y = g(t))

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



---

## ♾️ Section 2: Infinite Series###**Convergence Tests*** **Divergence Test:** If lim(aₙ) ≠ 0, then diverges.
* **p-Series:** Σ 1/nᵖ converges if p > 1, diverges if p ≤ 1.
* **Geometric Series:** Σ arⁿ converges if |r| < 1. Sum = a/(1-r).
* **Integral Test:** If f(x) is positive/decreasing, Σ aₙ and ∫ f(x)dx both converge or both diverge.
* **Ratio Test:** L = lim |aₙ₊₁ / aₙ|. Converges if L < 1, Diverges if L > 1.
* **Root Test:** L = lim ⁿ√|aₙ|. Converges if L < 1, Diverges if L > 1.
* **Direct Comparison:** If aₙ ≤ bₙ and Σbₙ converges, then Σaₙ converges.
* **Limit Comparison:** L = lim (aₙ / bₙ). If L is finite/positive, both series behave the same.
* **Alternating Series:** Σ (-1)ⁿ bₙ converges if bₙ is decreasing and lim(bₙ) = 0.

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

### **The Parallelogram Law***
* **Formula:** |u + v|² + |u - v|² = 2|u|² + 2|v|²

---
