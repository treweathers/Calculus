# 📐 Parametric Curves and Polar Coordinates Formula Sheet

## I. Parametric Curves ($\mathbf{x = f(t), y = g(t)}$)

| Concept | Formula |
| :--- | :--- |
| **First Derivative** (Slope) | $$\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{g'(t)}{f'(t)}$$ |
| **Second Derivative** (Concavity) | $$\frac{d^2y}{dx^2} = \frac{\frac{d}{dt}\left(\frac{dy}{dx}\right)}{dx/dt}$$ |
| **Arc Length** (Length of Curve) | $$L = \int_{\alpha}^{\beta} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} \,dt$$ |
| **Surface Area of Revolution** (Around $x$-axis) | $$SA = \int_{\alpha}^{\beta} 2\pi y \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} \,dt$$ |
| **Surface Area of Revolution** (Around $y$-axis) | $$SA = \int_{\alpha}^{\beta} 2\pi x \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} \,dt$$ |

---

## II. Polar Coordinates ($\mathbf{r = f(\theta)}$)

### A. Conversion Formulas (Polar $\leftrightarrow$ Cartesian)

| Conversion | Formula |
| :--- | :--- |
| **Polar to Cartesian** | $x = r \cos \theta$ |
| | $y = r \sin \theta$ |
| **Cartesian to Polar** | $r^2 = x^2 + y^2$ |
| | $\tan \theta = \frac{y}{x}$ |

### B. Calculus Formulas in Polar Coordinates

| Concept | Formula |
| :--- | :--- |
| **Area** (Bounded by $r = f(\theta)$) | $$A = \int_{\alpha}^{\beta} \frac{1}{2} r^2 \,d\theta$$ |
| **Slope** ($\frac{dy}{dx}$) | $\frac{dy}{dx} = \frac{r \cos \theta + \sin \theta \frac{dr}{d\theta}}{-r \sin \theta + \cos \theta \frac{dr}{d\theta}}$ |
| **Arc Length** (Length of Curve) | $$L = \int_{\alpha}^{\beta} \sqrt{r^2 + \left(\frac{dr}{d\theta}\right)^2} \,d\theta$$ |