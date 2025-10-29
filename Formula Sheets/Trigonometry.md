# 📐 Trig Cheat Sheet

**© Paul Dawkins - [https://tutorial.math.lamar.edu](https://tutorial.math.lamar.edu)**

## I. Definition of the Trig Functions

### A. Right Triangle Definition
For this definition we assume that $0 < \theta < \frac{\pi}{2}$ or $0^\circ < \theta < 90^\circ$. 

| Function | Definition | Reciprocal |
| :--- | :--- | :--- |
| $\sin(\theta)$ | $\frac{\text{opposite}}{\text{hypotenuse}}$ | $\csc(\theta) = \frac{\text{hypotenuse}}{\text{opposite}}$ |
| $\cos(\theta)$ | $\frac{\text{adjacent}}{\text{hypotenuse}}$ | $\sec(\theta) = \frac{\text{hypotenuse}}{\text{adjacent}}$ |
| $\tan(\theta)$ | $\frac{\text{opposite}}{\text{adjacent}}$ | $\cot(\theta) = \frac{\text{adjacent}}{\text{opposite}}$ |

### B. Unit Circle Definition
For this definition $\theta$ is any angle. **(x, y) is the point on the unit circle.** 

| Function | Definition | Reciprocal |
| :--- | :--- | :--- |
| $\sin(\theta)$ | $\frac{y}{1} = y$ | $\csc(\theta) = \frac{1}{y}$ |
| $\cos(\theta)$ | $\frac{x}{1} = x$ | $\sec(\theta) = \frac{1}{x}$ |
| $\tan(\theta)$ | $\frac{y}{x}$ | $\cot(\theta) = \frac{x}{y}$ |

> **Example:** For any ordered pair on the unit circle $(x, y)$: $\cos(\theta) = x$ and $\sin(\theta) = y$.
> *Example:* $\cos(\frac{5\pi}{3}) = \frac{1}{2}$, $\sin(\frac{5\pi}{3}) = -\frac{\sqrt{3}}{2}$

---

## II. Facts and Properties

### A. Domain and Range

| Function | Domain | Range |
| :--- | :--- | :--- |
| $\sin(\theta)$ | $\theta$ can be any angle | $-1 \le \sin(\theta) \le 1$ |
| $\cos(\theta)$ | $\theta$ can be any angle | $-1 \le \cos(\theta) \le 1$ |
| $\tan(\theta)$ | $\theta \ne n + \frac{1}{2} \pi, n = 0, \pm 1, \pm 2, \dots$ | $-\infty < \tan(\theta) < \infty$ |
| $\csc(\theta)$ | $\theta \ne n\pi, n = 0, \pm 1, \pm 2, \dots$ | $\csc(\theta) \ge 1 \text{ and } \csc(\theta) \le -1$ |
| $\sec(\theta)$ | $\theta \ne n + \frac{1}{2} \pi, n = 0, \pm 1, \pm 2, \dots$ | $\sec(\theta) \ge 1 \text{ and } \sec(\theta) \le -1$ |
| $\cot(\theta)$ | $\theta \ne n\pi, n = 0, \pm 1, \pm 2, \dots$ | $-\infty < \cot(\theta) < \infty$ |

### B. Period
The period, $T$, is the number such that $f(\theta + T) = f(\theta)$. If $\omega$ is a fixed number:

| Function | Period ($T$) |
| :--- | :--- |
| $\sin(\omega \theta)$ | $T = \frac{2\pi}{\omega}$ |
| $\cos(\omega \theta)$ | $T = \frac{2\pi}{\omega}$ |
| $\tan(\omega \theta)$ | $T = \frac{\pi}{\omega}$ |
| $\csc(\omega \theta)$ | $T = \frac{2\pi}{\omega}$ |
| $\sec(\omega \theta)$ | $T = \frac{2\pi}{\omega}$ |
| $\cot(\omega \theta)$ | $T = \frac{\pi}{\omega}$ |

### C. Degrees to Radians Formulas
If $x$ is in degrees and $t$ is in radians:
$$\frac{x}{180} = \frac{t}{\pi} \quad \implies \quad t = \frac{\pi x}{180} \quad \text{and} \quad x = \frac{180t}{\pi}$$

---

## III. Formulas and Identities

### A. Reciprocal Identities
* $\csc(\theta) = \frac{1}{\sin(\theta)}$
* $\sec(\theta) = \frac{1}{\cos(\theta)}$
* $\cot(\theta) = \frac{1}{\tan(\theta)}$

### B. Tangent and Cotangent Identities
* $\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)}$
* $\cot(\theta) = \frac{\cos(\theta)}{\sin(\theta)}$

### C. Pythagorean Identities
* $\sin^2(\theta) + \cos^2(\theta) = 1$
* $\tan^2(\theta) + 1 = \sec^2(\theta)$
* $1 + \cot^2(\theta) = \csc^2(\theta)$

### D. Even/Odd Formulas
* $\sin(-\theta) = -\sin(\theta)$
* $\cos(-\theta) = \cos(\theta)$
* $\tan(-\theta) = -\tan(\theta)$
* $\csc(-\theta) = -\csc(\theta)$
* $\sec(-\theta) = \sec(\theta)$
* $\cot(-\theta) = -\cot(\theta)$

### E. Periodic Formulas
(If $n$ is an integer)
* $\sin(\theta + 2\pi n) = \sin(\theta)$
* $\cos(\theta + 2\pi n) = \cos(\theta)$
* $\csc(\theta + 2\pi n) = \csc(\theta)$
* $\sec(\theta + 2\pi n) = \sec(\theta)$
* $\tan(\theta + \pi n) = \tan(\theta)$
* $\cot(\theta + \pi n) = \cot(\theta)$

### F. Cofunction Formulas
* $\sin(\frac{\pi}{2} - \theta) = \cos(\theta)$
* $\cos(\frac{\pi}{2} - \theta) = \sin(\theta)$
* $\csc(\frac{\pi}{2} - \theta) = \sec(\theta)$
* $\sec(\frac{\pi}{2} - \theta) = \csc(\theta)$
* $\tan(\frac{\pi}{2} - \theta) = \cot(\theta)$
* $\cot(\frac{\pi}{2} - \theta) = \tan(\theta)$

---

## IV. Complex Identities

### A. Double Angle Formulas
* $\sin(2\theta) = 2 \sin(\theta) \cos(\theta)$
* $\cos(2\theta) = \cos^2(\theta) - \sin^2(\theta) = 2 \cos^2(\theta) - 1 = 1 - 2 \sin^2(\theta)$
* $\tan(2\theta) = \frac{2 \tan(\theta)}{1 - \tan^2(\theta)}$

### B. Half Angle Formulas
* $\sin(\frac{\theta}{2}) = \pm \sqrt{\frac{1 - \cos(\theta)}{2}}$
* $\cos(\frac{\theta}{2}) = \pm \sqrt{\frac{1 + \cos(\theta)}{2}}$
* $\tan(\frac{\theta}{2}) = \pm \sqrt{\frac{1 - \cos(\theta)}{1 + \cos(\theta)}}$

### C. Half Angle Formulas (Alternate Form)
* $\sin^2(\theta) = \frac{1}{2} (1 - \cos(2\theta))$
* $\cos^2(\theta) = \frac{1}{2} (1 + \cos(2\theta))$
* $\tan^2(\theta) = \frac{1 - \cos(2\theta)}{1 + \cos(2\theta)}$

### D. Sum and Difference Formulas
* $\sin(\alpha \pm \beta) = \sin(\alpha) \cos(\beta) \pm \cos(\alpha) \sin(\beta)$
* $\cos(\alpha \pm \beta) = \cos(\alpha) \cos(\beta) \mp \sin(\alpha) \sin(\beta)$
* $\tan(\alpha \pm \beta) = \frac{\tan(\alpha) \pm \tan(\beta)}{1 \mp \tan(\alpha) \tan(\beta)}$

### E. Product to Sum Formulas
* $\sin(\alpha) \sin(\beta) = \frac{1}{2} [\cos(\alpha - \beta) - \cos(\alpha + \beta)]$
* $\cos(\alpha) \cos(\beta) = \frac{1}{2} [\cos(\alpha - \beta) + \cos(\alpha + \beta)]$
* $\sin(\alpha) \cos(\beta) = \frac{1}{2} [\sin(\alpha + \beta) + \sin(\alpha - \beta)]$
* $\cos(\alpha) \sin(\beta) = \frac{1}{2} [\sin(\alpha + \beta) - \sin(\alpha - \beta)]$

### F. Sum to Product Formulas
* $\sin(\alpha) + \sin(\beta) = 2 \sin(\frac{\alpha + \beta}{2}) \cos(\frac{\alpha - \beta}{2})$
* $\sin(\alpha) - \sin(\beta) = 2 \cos(\frac{\alpha + \beta}{2}) \sin(\frac{\alpha - \beta}{2})$
* $\cos(\alpha) + \cos(\beta) = 2 \cos(\frac{\alpha + \beta}{2}) \cos(\frac{\alpha - \beta}{2})$
* $\cos(\alpha) - \cos(\beta) = -2 \sin(\frac{\alpha + \beta}{2}) \sin(\frac{\alpha - \beta}{2})$

---

## V. Inverse Trig Functions

### A. Definition
* $y = \sin^{-1}(x)$ is equivalent to $x = \sin(y)$
* $y = \cos^{-1}(x)$ is equivalent to $x = \cos(y)$
* $y = \tan^{-1}(x)$ is equivalent to $x = \tan(y)$

> **Alternate Notation:** $\sin^{-1}(x) = \arcsin(x)$, $\cos^{-1}(x) = \arccos(x)$, $\tan^{-1}(x) = \arctan(x)$

### B. Domain and Range

| Function | Domain | Range |
| :--- | :--- | :--- |
| $y = \sin^{-1}(x)$ | $-1 \le x \le 1$ | $-\frac{\pi}{2} \le y \le \frac{\pi}{2}$ |
| $y = \cos^{-1}(x)$ | $-1 \le x \le 1$ | $0 \le y \le \pi$ |
| $y = \tan^{-1}(x)$ | $-\infty < x < \infty$ | $-\frac{\pi}{2} < y < \frac{\pi}{2}$ |

### C. Inverse Properties
* $\cos(\cos^{-1}(x)) = x$
* $\cos^{-1}(\cos(\theta)) = \theta$
* $\sin(\sin^{-1}(x)) = x$
* $\sin^{-1}(\sin(\theta)) = \theta$
* $\tan(\tan^{-1}(x)) = x$
* $\tan^{-1}(\tan(\theta)) = \theta$

---

## VI. Law of Sines, Cosines, and Tangents

### A. Law of Sines
$$\frac{\sin(\alpha)}{a} = \frac{\sin(\beta)}{b} = \frac{\sin(\gamma)}{c}$$

### B. Law of Cosines
* $a^2 = b^2 + c^2 - 2bc \cos(\alpha)$
* $b^2 = a^2 + c^2 - 2ac \cos(\beta)$
* $c^2 = a^2 + b^2 - 2ab \cos(\gamma)$

### C. Law of Tangents
$$\frac{a - b}{a + b} = \frac{\tan \frac{1}{2} (\alpha - \beta)}{\tan \frac{1}{2} (\alpha + \beta)}$$
$$\frac{b - c}{b + c} = \frac{\tan \frac{1}{2} (\beta - \gamma)}{\tan \frac{1}{2} (\beta + \gamma)}$$
$$\frac{a - c}{a + c} = \frac{\tan \frac{1}{2} (\alpha - \gamma)}{\tan \frac{1}{2} (\alpha + \gamma)}$$

### D. Mollweide’s Formula
$$\frac{a + b}{c} = \frac{\cos \frac{1}{2} (\alpha - \beta)}{\sin \frac{1}{2} \gamma}$$

***
This sheet covers a great deal of trigonometry! Would you like me to elaborate on any specific section, like the graph properties of the functions or a step-by-step example of using one of these identities?