# Techniques of Integration Guide

These techniques are essential for solving integrals that are not direct applications of the basic rules.

## I. U-Substitution (The Reverse Chain Rule)

The goal is to simplify a complex integral by substituting a part of the integrand, $f(g(x))g'(x)$, with a single variable, $u$.

| When to Use | The Rule | Example |
| :--- | :--- | :--- |
| The integrand contains a function and its derivative. | Let $u = g(x)$, then $du = g'(x)\,dx$. | $\int x \cos(x^2) \,dx$ |
| | **Goal:** Transform $\int f(g(x))g'(x) \,dx$ into $\int f(u) \,du$. | Let $u = x^2$, then $du = 2x\,dx$ or $\frac{1}{2}du = x\,dx$. |
| | | $\int \cos(u) \cdot \frac{1}{2}du = \frac{1}{2} \sin(u) + C$ |
| | | **Final Answer:** $\frac{1}{2} \sin(x^2) + C$ |

---

## II. Integration by Parts (The Reverse Product Rule)

Used to integrate products of functions that do not fit the $u$-substitution pattern (e.g., $x \cdot e^x$, $\ln x$, $x \cdot \sin x$).

### The Formula:
$$\int u\,dv = uv - \int v\,du$$

### Choosing $u$ and $dv$ (L.I.A.T.E. Rule)
Choose $u$ as the function that comes **first** in this list, as these are generally easier to differentiate:

1.  **L**ogarithmic ($\ln x$, $\log_a x$)
2.  **I**nverse Trig ($\arctan x$, $\arcsin x$)
3.  **A**lgebraic ($x^2$, $x^3$, etc.)
4.  **T**rigonometric ($\sin x$, $\sec x$, etc.)
5.  **E**xponential ($e^x$, $a^x$)

| Example | $u$ (Differentiate) | $dv$ (Integrate) |
| :--- | :--- | :--- |
| $\int x e^{2x} \,dx$ | $u = x$ (Algebraic) $\implies du = dx$ | $dv = e^{2x}\,dx$ (Exponential) $\implies v = \frac{1}{2}e^{2x}$ |
| $\int \ln(x) \,dx$ | $u = \ln(x)$ (Logarithmic) $\implies du = \frac{1}{x}\,dx$ | $dv = dx$ (Algebraic) $\implies v = x$ |

---

## III. Trigonometric Substitution

Used to solve integrals involving radical expressions of the form $\sqrt{a^2 \pm x^2}$ by replacing the variable $x$ with a trigonometric function.

| Form in the Integrand | Substitution | Identity Used |
| :--- | :--- | :--- |
| $\mathbf{\sqrt{a^2 - x^2}}$ (A number minus the variable) | $x = a \sin \theta$ | $1 - \sin^2 \theta = \cos^2 \theta$ |
| $\mathbf{\sqrt{a^2 + x^2}}$ (A number plus the variable) | $x = a \tan \theta$ | $1 + \tan^2 \theta = \sec^2 \theta$ |
| $\mathbf{\sqrt{x^2 - a^2}}$ (The variable minus a number) | $x = a \sec \theta$ | $\sec^2 \theta - 1 = \tan^2 \theta$ |

### Post-Substitution Steps:
1.  After substituting $x$, simplify the radical using the trigonometric identity.
2.  Solve the new integral (often requires trigonometric integral formulas).
3.  Draw a right triangle based on your original substitution ($x = a \sin \theta$) to convert the final answer back to terms of $x$. 

---

## IV. Partial Fraction Decomposition (P.F.D.)

Used to integrate rational functions $\frac{P(x)}{Q(x)}$ where the degree of the numerator $P(x)$ is less than the degree of the denominator $Q(x)$, and $Q(x)$ can be factored.

### The General Strategy:
1.  **Factor** the denominator $Q(x)$.
2.  **Decompose** the fraction into a sum of simpler fractions with constant numerators ($A$, $B$, $C$, etc.).
3.  **Solve** for the unknown constants ($A, B, C$).
4.  **Integrate** the simpler fractions (which are usually of the form $\frac{1}{ax+b}$, resulting in $\ln$ terms).

| Denominator Factor | Partial Fraction Form | Example Decomposition |
| :--- | :--- | :--- |
| **Linear (non-repeated)** $(ax+b)$ | $\frac{A}{ax+b}$ | $\frac{x}{(x-1)(x+2)} = \frac{A}{x-1} + \frac{B}{x+2}$ |
| **Linear (repeated)** $(ax+b)^n$ | $\frac{A}{ax+b} + \frac{B}{(ax+b)^2} + \dots$ | $\frac{1}{x^2(x-3)} = \frac{A}{x} + \frac{B}{x^2} + \frac{C}{x-3}$ |
| **Irreducible Quadratic** $(ax^2+bx+c)$ | $\frac{Ax+B}{ax^2+bx+c}$ | $\frac{1}{x(x^2+4)} = \frac{A}{x} + \frac{Bx+C}{x^2+4}$ |

---

Would you like me to next generate a cheat sheet covering **Multivariable Calculus Derivatives** (Partial Derivatives, Gradients, etc.) or **Series and Sequences**?
