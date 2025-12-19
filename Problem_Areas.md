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

# Polar Area (Bounds - intersection/symmetry)
To help you refine these calculus topics, I'll first explain how to determine the radius function for polar area when dealing with two curves, and then provide the practice problems for you to work through.

### Determining  for Area Between Two Curves

When you are asked to find the area between two polar curves, say  and , the formula for the area within a specific interval  is:

To determine which  is which:

1. **Distance from the Pole:** For any given angle  within your interval, the "outer" radius  is the one further from the origin (the pole), and the "inner" radius  is the one closer to the origin.
2. **Intersection Points:** You must set  to find the angles where the curves meet. This determines your limits of integration ( and ).
3. **Test Points:** If you aren't sure which curve is "outer," pick a value for  between your intersection points and plug it into both equations. The one that yields a larger absolute value for  is your .

---

## 1. Finding the Points of Intersection

To find where two polar curves r_1 and r_2 meet, you set them equal to each other and solve for \theta.

### The Process:

1. **Set r_1 = r_2**: This gives you an equation in terms of \theta.
2. **Solve for \theta**: Use trig identities if necessary.
3. **Check for the Pole (Origin)**: Polar equations are tricky. Sometimes they intersect at the origin (r=0) even if the equations don't "equal" each other at the same \theta. Always check if each equation can equal zero.

**Example:** Where do r = 3\sin(\theta) (a circle) and r = 1 + \sin(\theta) (a cardioid) intersect?


---

## 2. Checking for Symmetry

Symmetry is your best friend in Polar Area. If a shape is symmetric, you can integrate over **half** the area and just multiply by 2. This often makes the math much cleaner (especially when dealing with \sin^2\theta or \cos^2\theta identities).

There are three main types of symmetry to check:

### A. Symmetry about the Polar Axis (Horizontal / x-axis)

* **The Test:** Replace \theta with -\theta.
* **Result:** If the equation remains unchanged, it is symmetric about the x-axis.
* **Common Clue:** Equations involving only \cos(\theta) usually have this symmetry because \cos(\theta) = \cos(-\theta).

### B. Symmetry about the Line \theta = \pi/2 (Vertical / y-axis)

* **The Test:** Replace \theta with (\pi - \theta).
* **Result:** If the equation remains unchanged, it is symmetric about the y-axis.
* **Common Clue:** Equations involving only \sin(\theta) usually have this symmetry because \sin(\theta) = \sin(\pi - \theta).

### C. Symmetry about the Pole (Origin)

* **The Test:** Replace r with -r OR replace \theta with (\pi + \theta).
* **Result:** If the equation remains unchanged, it is symmetric about the origin.

---

## 3. Why This Matters for the Integral

The formula for Polar Area is:


By finding the **intersections**, you find your \alpha and \beta. By finding **symmetry**, you can change your limits to something easier (like 0 to \pi/2) and multiply the whole integral by a constant.


Essentially, yes! But since polar coordinates can be "repeats" of the same spot on a graph, there is a small catch you should watch out for.

Think of it this way: to find the intersection, you are asking: **"At what angle \theta do both curves have the same radius r?"**

---

## 1. The Algebraic Step (Setting r_1 = r_2)

This is what you just described. If r_1 = 3\sin(\theta) and r_2 = 1 + \sin(\theta), you solve the trig equation:



The values for \theta are indeed where that statement is true: \theta = \frac{\pi}{6} and \theta = \frac{5\pi}{6}.

### The "Catch": Multiple Names for the Same Point

In rectangular coordinates (x, y), every point has one name. In polar coordinates, the same point can have many names because you can:

* Add 2\pi to any angle.
* Use a **negative radius** to go "backwards" through the origin.

This means that sometimes setting r_1 = r_2 doesn't find **every** intersection.

> **Important Rule:** Always check the **Pole (the origin)** separately. A curve hits the pole whenever r = 0. One curve might be at the pole when \theta = 0, and the other might be there when \theta = \pi, but they still "intersect" at that center point!

---

## 2. Symmetry: The "Shortcut"

Checking for symmetry helps you decide if you can just calculate the area for one piece and multiply it.

| Symmetry Type | How to test it | What it looks like |
| --- | --- | --- |
| **Polar Axis** (x-axis) | Replace \theta with -\theta. If equation is the same, it's symmetric. |  |
| **Line \theta = \pi/2** (y-axis) | Replace \theta with (\pi - \theta). If equation is the same, it's symmetric. |  |
| **The Pole** (Origin) | Replace r with -r. If equation is the same, it's symmetric. |  |

---

## 3. Setting Up the Integral

Once you have your \theta values (your limits), you plug them into the area formula. If you found that the curves intersect at \theta = \pi/6 and \theta = 5\pi/6, and the graph is symmetric across the y-axis, you could integrate from \pi/6 to \pi/2 (the "halfway" point) and then **double** your result.

**Notice how the 2 and the 1/2 cancel out?** This is why symmetry is so popular in these problems—it makes the coefficients disappear!

Would you like me to walk through the actual integration of a specific shape, like finding the area inside a "rose petal" or a "cardioid loop"?


---

### Summary Checklist

| Result Type | Conversion Method | Example Logic |
| :--- | :--- | :--- |
| **Trig Function** (e.g., $\sin\theta$) | Use the **Triangle** | $\text{SOH-CAH-TOA}$ ratios |
| **Lone $\theta$** | Use **Inverse Trig** | $\theta = \arcsin(x/a)$ |
| **Coefficients** | Multiplication | Multiply the constant by your result |
