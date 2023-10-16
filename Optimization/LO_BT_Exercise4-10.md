# Exercise 4.10 (Sadddle Points of the Langrangian)
ref: B&T LO pg. 190
## Question
Consider the standard form problem of minimizing $c^{\text{T}}x$ subject to $Ax =b$ and $x \succeq 0$. We define the *Langrangian* by
$$
\mathcal{L}(x, p) := c^{\text{T}}x + p^{\text{T}}(b - Ax).
$$
Consider the following "game" : player 1 chooses some $x \succeq 0$ and player 2 chooses some $p$; then player 1 pays to player 2 the amount $\mathcal{L}(x, p)$. Player 1 would like to minimize $\mathcal{L}(x, p)$, while player 2 would like to maximize it.
\
A pair $(x^*, p^*)$, with $x^* \succeq 0$, is called an *equilibrium* point (or a *saddle point*, or a *Nash equilibrium*) if
$$
\mathcal{L}(x^*, p) \le \mathcal{L}(x^*, p^*) \le \mathcal{L}(x, p^*), \quad \forall x \succeq 0, \forall \; p.
$$
(Thus, we have an equilibrium if no player is able to improve her performance by unilaterally modifiying her choice.)\
Show that a pair $(x^*, p^*)$ is an equilibrium if and only if $x^*$ and $p^*$ are optimal solutions to the standard form problem under consideration and its dual, respectively.

## Response
Before writing the formal proof, we first recall a standard from optimization problem and its dual. Specifically, a standard form problem can be written as

$$
\begin{equation*}
\begin{array}{lll}
\underset{x}{\text{minimize}} \quad & c^{\text{T}}x & \\
\text{subject to} \quad & Ax = b \\
& x \succeq 0,
\end{array}
\end{equation*}
$$

with its corresponding dual taking the form

$$
\begin{equation*}
\begin{array}{lll}
\underset{p}{\text{maximize}} \quad & p^{\text{T}}b & \\
\text{subject to} \quad & p^{\text{T}}A \preceq c^{\text{T}}.
\end{array}
\end{equation*}
$$

Proof. ($\Leftarrow$) Suppose that $x^{*}$ and $p^*$ are optimal solutions to their respective optimization problems. We evaluate the Langrangian at the three above posited points:
$$
L(x^*, p) = c^{\text{T}}x^* + p^{\text{T}}(b - Ax^*) = c^{\text{T}}x^* + p^{\text{T}}(b - b) = c^{\text{T}}x^* \quad \forall p,
$$
where we obtained the first equality since if $x^*$ is an optimal point then it must also be feasible and thus $Ax^* = b$. In an equivalent manner we note that $L(x^*, p^*) = c^{\text{T}}x^*$. Finally, 

$$
\begin{align*}
L(x, p^*) = c^{\text{T}}x + p^{*^{\text{T}}}(b - Ax) &= c^{\text{T}}x + p^{*^{\text{T}}}b - p^{*^{\text{T}}}Ax \\
&= c^{\text{T}}x + c^{\text{T}}x^* - p^{*^{\text{T}}}Ax \quad \text{(strong duality)} \\
&\ge c^{\text{T}}x + c^{\text{T}}x^* - c^{\text{T}}x = c^{\text{T}}x^*, \quad \forall \; x \succeq 0
\end{align*}
$$
where the inequality in the final line comes from the fact that $p^*$ is an optimal solution to the dual problem and thus must be feasible. That is, $p^{*^{\text{T}}}A \preceq c^{\text{T}}$ and since $x$ is nonnegative, $p^{*^{\text{T}}}Ax \le c^{\text{T}}x \Leftrightarrow -p^{*^{\text{T}}}Ax \ge -c^{\text{T}}x$. The three of these evaluations give us our desired inequality
$$
\mathcal{L}(x^*, p) = c^{\text{T}}x^* \le \mathcal{L}(x^*, p^*) = c^{\text{T}}x^*\le \mathcal{L}(x, p^*), \quad \forall x \succeq 0, \forall \; p.
$$

($\Rightarrow$) We now start with the assumption that
$$
\mathcal{L}(x^*, p) \le \mathcal{L}(x^*, p^*) \le \mathcal{L}(x, p^*), \quad \forall x \succeq 0, \forall \; p,
$$
and aim to show that $x^*$ and $p^*$ are optimal solutions to their respective optimization problems. We suppose for the sake of contradiction that $x^*$ or $p^*$ is *not* an optimal solution to its respective optimization problem. Proceeding with the assumption that $x^*$ is a non-optimal BFS but $p^*$ is, the second inequality becomes
$$
c^{\text{T}}x^* + p^{*^{\text{T}}}(b - Ax^{*}) \le c^{\text{T}}x + p^{*^{\text{T}}}(b - Ax) 
$$

**need to finish**

## Reflection
What does this proof show? 
\
**Question**: is the contradiction proof correct?