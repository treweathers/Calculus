Spot on! You’ve nailed the two different paths for getting back to x.

To make it crystal clear, think of it as **two different tools** in your toolbox. You choose the tool based on what "shape" your antiderivative is in.

---

### Tool 1: The Right Triangle (For Trig Functions)

If your antiderivative contains a trig function like \sin(\theta), \tan(\theta), or \sec(\theta), you use the triangle to find the ratio of the sides.

* **When to use:** Whenever you have \text{trig}(\theta).
* **How:** If your original sub was x = 3\sin(\theta), you know \text{Opposite}=x and \text{Hypotenuse}=3. Use the Pythagorean theorem to find the third side (\text{Adjacent} = \sqrt{9 - x^2}). Then just read the ratio for whatever trig function you're looking at.

### Tool 2: Inverse Trig (For "Lone" \theta)

If your antiderivative contains a \theta that is **not** inside a trig function (it's just standing there by itself), the triangle can't help you directly because there's no ratio to read.

* **When to use:** Whenever you have a plain \theta.
* **How:** You "solve" your original substitution for \theta.
> If x = 3\sin(\theta) \implies \frac{x}{3} = \sin(\theta) \implies \theta = \arcsin\left(\frac{x}{3}\right).



---

### A "Mixed" Example

Imagine you integrate a function and get this result:


If your original substitution was x = 2\sin(\theta), here is how you would convert each part:

1. **For the 2\theta:** Use Tool 2. Since \sin(\theta) = \frac{x}{2}, then \theta = \arcsin(\frac{x}{2}).
* Result: 2\arcsin\left(\frac{x}{2}\right)


2. **For the 5\tan(\theta):** Use Tool 1 (The Triangle).
* Opposite = x, Hypotenuse = 2, Adjacent = \sqrt{4-x^2}.
* Since \tan = \frac{\text{Opp}}{\text{Adj}}, then \tan(\theta) = \frac{x}{\sqrt{4-x^2}}.
* Result: 5\left(\frac{x}{\sqrt{4-x^2}}\right)



**Combined Final Answer:**


---

### Summary Checklist

* **Trig function left?** \rightarrow Use the triangle to get a fraction of sides.
* **Plain \theta left?** \rightarrow Use the inverse function (arcsin/arctan/arcsec).
* **Coefficients?** \rightarrow Just multiply them by whatever you found (like the 2 and 5 in the example above).

Does that help clear up the "when and why" for using the inverse functions? Would you like a practice problem that specifically results in both a \theta and a trig function?
