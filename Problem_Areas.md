# Calc II Problem Area Review
## Integration
### Trig-Sub (3rd Step, converting back to x)
Spot on! You’ve nailed the two different paths for getting back to x.

To make it crystal clear, think of it as **two different tools** in your toolbox. You choose the tool based on what "shape" your antiderivative is in.

# Trig Substitution: The "Lone $\theta$" vs. Trig Functions

When finishing a trig substitution problem, you usually have two types of terms in your antiderivative. Here is how to handle both.

---

### 1. The Right Triangle (For Trig Functions)
If your antiderivative contains a trig function like $\sin(\theta)$, $\tan(\theta)$, or $\sec(\theta)$, you use the triangle to find the ratio of the sides.

* **When to use:** Whenever you have $\text{trig}(\theta)$.
* **How:** If your original sub was $x = 3\sin(\theta)$, you know $\text{Opposite} = x$ and $\text{Hypotenuse} = 3$. Use the Pythagorean theorem to find the third side: $\text{Adjacent} = \sqrt{9 - x^2}$.

---

### 2. Inverse Trig (For "Lone" $\theta$)
If your antiderivative contains a $\theta$ that is **not** inside a trig function, the triangle can't help you directly.

* **When to use:** Whenever you have a plain $\theta$.
* **How:** "Solve" your original substitution for $\theta$ using an inverse function.
    * If $x = 3\sin(\theta) \implies \frac{x}{3} = \sin(\theta) \implies \theta = \arcsin\left(\frac{x}{3}\right)$.

---

### A "Mixed" Example
Imagine you integrate a function and get this result:
$$2\theta + 5\tan(\theta) + C$$

If your original substitution was **$x = 2\sin(\theta)$**, here is how you would convert each part:

1.  **For the $2\theta$ (Tool: Inverse Trig):**
    * Since $\sin(\theta) = \frac{x}{2}$, then $\theta = \arcsin\left(\frac{x}{2}\right)$.
    * **Result:** $2\arcsin\left(\frac{x}{2}\right)$

2.  **For the $5\tan(\theta)$ (Tool: The Triangle):**
    * $\text{Opposite} = x$, $\text{Hypotenuse} = 2$, $\text{Adjacent} = \sqrt{4-x^2}$.
    * Since $\tan = \frac{\text{Opp}}{\text{Adj}}$, then $\tan(\theta) = \frac{x}{\sqrt{4-x^2}}$.
    * **Result:** $5\left(\frac{x}{\sqrt{4-x^2}}\right)$

**Combined Final Answer:**
$$2\arcsin\left(\frac{x}{2}\right) + \frac{5x}{\sqrt{4-x^2}} + C$$

---

### Summary Checklist

| Result Type | Conversion Method | Example Logic |
| :--- | :--- | :--- |
| **Trig Function** (e.g., $\sin\theta$) | Use the **Triangle** | $\text{SOH-CAH-TOA}$ ratios |
| **Lone $\theta$** | Use **Inverse Trig** | $\theta = \arcsin(x/a)$ |
| **Coefficients** | Multiplication | Multiply the constant by your result |
