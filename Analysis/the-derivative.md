- What is differentiability 
- How it arose and single variable intuition
- Generalization to maps between Euclidean spaces

Implicit Differentiation
- On a more rigorous level: Implicit Function Theorem TA2 pg. 158
- On a less rigorous level: just rely on the chain rule

The "derivative" should originally be thought of as the slope of a tangent line to a curve. Specifically, it is the slope of the limiting secant line between points $P = (x, y)$ and $Q = (x + \Delta x, y + \Delta y)$ on the curve $y(x)$. It follows that the slope of the secant line through these two points is
$$\frac{\Delta y}{\Delta x}$$
We represent the corresponding *limiting slope* as $\Delta x \to 0$ with the following compact symbol suggested by Leibniz
$$\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \frac{dy}{dx}$$
Geometrically, we have taken the secant line through two nearby points $P$ and $Q$ and then let the point $Q$ approach $P$.\
To compute the derivative of a given function $y(x)$, you do the following four step delta process:
1. Give $x$ an increment of $\Delta x$.
2. Compute the corresponding change in $y$:
$$\Delta y = y(x + \Delta x) - y(x)$$
3. Compute the ratio of the changes:
$$\frac{\Delta y}{\Delta x}$$
4. Take the limit as $\Delta x$ aproaches $0$. 

## Formal Differentiation
Abstractions of differentiation: define important formulas from four step delta process\
Corresponding main rules plus examples:\
Formal differentiation of an algebraic function is a sequence of simpler abstract differentiations.\
However, one shouldn't forget that the derivative is actually defined by the four-step rule and the rules that come from it. All derivatives one might wish to find can be found, in principle, by the direct application of the four-step rule, but to carry out the delta process (Hamming MoM pg. 202) in full every time is wasted energy.\
Need to give some epsilon-delta proofs