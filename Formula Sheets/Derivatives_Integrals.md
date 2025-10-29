That's a fantastic request! You are absolutely right to aim for the most complete set of fundamental rules. Many of the frequently encountered forms (like $\int \sec^2(x) \,dx$) come directly from knowing all the basic derivatives.

I have compiled a comprehensive **Calculus Derivative and Antiderivative Cheat Sheet** that includes all six standard and inverse trigonometric functions, and a complete set of Exponential and Logarithmic rules, including the crucial Chain Rule versions.

***

# 🎯 Complete Calculus Cheat Sheet: Derivatives & Antiderivatives

## I. Derivatives (Trigonometric & Inverse)

### A. Standard & Reciprocal Functions
| Function | Derivative |
| :--- | :--- |
| $\frac{d}{dx}(\sin x)$ | $\cos x$ |
| $\frac{d}{dx}(\cos x)$ | $-\sin x$ |
| $\frac{d}{dx}(\tan x)$ | $\sec^2 x$ |
| $\frac{d}{dx}(\cot x)$ | $-\csc^2 x$ |
| $\frac{d}{dx}(\sec x)$ | $\sec x \tan x$ |
| $\frac{d}{dx}(\csc x)$ | $-\csc x \cot x$ |

### B. Inverse Trigonometric Functions
| Function | Derivative |
| :--- | :--- |
| $\frac{d}{dx}(\arcsin x)$ | $\frac{1}{\sqrt{1-x^2}}$ |
| $\frac{d}{dx}(\arccos x)$ | $-\frac{1}{\sqrt{1-x^2}}$ |
| $\frac{d}{dx}(\arctan x)$ | $\frac{1}{1+x^2}$ |
| $\frac{d}{dx}(\text{arccot } x)$ | $-\frac{1}{1+x^2}$ |
| $\frac{d}{dx}(\text{arcsec } x)$ | $\frac{1}{|x|\sqrt{x^2-1}}$ |
| $\frac{d}{dx}(\text{arccsc } x)$ | $-\frac{1}{|x|\sqrt{x^2-1}}$ |

---

## II. Derivatives (Exponential & Logarithmic)

| Function | Basic Rule | Chain Rule Version ($\mathbf{f(x)}$ is the inner function) |
| :--- | :--- | :--- |
| **Natural Exponential** | $\frac{d}{dx}(e^x) = e^x$ | $\frac{d}{dx}(e^{f(x)}) = e^{f(x)} \cdot f'(x)$ |
| **General Exponential** | $\frac{d}{dx}(a^x) = a^x \ln(a)$ | $\frac{d}{dx}(a^{f(x)}) = a^{f(x)} \ln(a) \cdot f'(x)$ |
| **Natural Logarithm** | $\frac{d}{dx}(\ln x) = \frac{1}{x}$ | $\frac{d}{dx}(\ln(f(x))) = \frac{f'(x)}{f(x)}$ |
| **General Logarithm** | $\frac{d}{dx}(\log_a x) = \frac{1}{x \ln(a)}$ | $\frac{d}{dx}(\log_a (f(x))) = \frac{f'(x)}{f(x) \ln(a)}$ |

---

## III. Antiderivatives (Indefinite Integrals)

### A. Algebraic & Exponential Rules
| Integral | Result ($\int f(x) \,dx$) |
| :--- | :--- |
| **Power Rule** | $\int x^n \,dx = \frac{x^{n+1}}{n+1} + C \quad (n \ne -1)$ |
| **Logarithmic** | $\int \frac{1}{x} \,dx = \ln |x| + C$ |
| $\int e^x \,dx$ | $e^x + C$ |
| $\int a^x \,dx$ | $\frac{a^x}{\ln(a)} + C$ |
| $\int \ln(x) \,dx$ | $x \ln(x) - x + C$ |
| $\int \log_a(x) \,dx$ | $\frac{x \ln(x) - x}{\ln(a)} + C$ |

### B. Trigonometric Integrals
These integrals are the direct inverses of the derivatives in Section I.A.

| Integral | Result | Integral | Result |
| :--- | :--- | :--- | :--- |
| $\int \sin(x) \,dx$ | $-\cos(x) + C$ | $\int \tan(x) \,dx$ | $\ln |\sec(x)| + C$ |
| $\int \cos(x) \,dx$ | $\sin(x) + C$ | $\int \cot(x) \,dx$ | $\ln |\sin(x)| + C$ |
| $\int \sec^2(x) \,dx$ | $\tan(x) + C$ | $\int \sec(x) \,dx$ | $\ln |\sec(x) + \tan(x)| + C$ |
| $\int \csc^2(x) \,dx$ | $-\cot(x) + C$ | $\int \csc(x) \,dx$ | $\ln |\csc(x) - \cot(x)| + C$ |
| $\int \sec(x)\tan(x) \,dx$ | $\sec(x) + C$ | $\int \frac{1}{\sqrt{a^2 - x^2}} \,dx$ | $\arcsin(\frac{x}{a}) + C$ |
| $\int \csc(x)\cot(x) \,dx$ | $-\csc(x) + C$ | $\int \frac{1}{a^2 + x^2} \,dx$ | $\frac{1}{a} \arctan(\frac{x}{a}) + C$ |
| | | $\int \frac{1}{x\sqrt{x^2 - a^2}} \,dx$ | $\frac{1}{a} \arcsec(\frac{|x|}{a}) + C$ |

---