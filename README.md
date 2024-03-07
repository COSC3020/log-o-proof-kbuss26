[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

### Proof

For this proof, we will demonstrate that $\log{ _2}{n}$ is asymptotically the same as $\log{ _5}{n}$. This boils down to manipulating the $c$ constant with the change the base of each logarithmic function.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$<br>
Given $f(n) = \log{ _2}{n}$:<br>
$\implies \exists c, n_0: T(n) \leq c \cdot \log{ _2}{n} (\forall n \geq n_0)$<br>
$\implies \exists c, n_0: T(n) \leq c \cdot \frac{\log{n}}{\log{2}} (\forall n \geq n_0)$<br>
$\implies \exists c, n_0: T(n) \leq \frac{1}{\log{2}}c \cdot \log{n} (\forall n \geq n_0)$<br>


Given $f(n) = \log{ _5}{n}$:<br>
$\implies \exists c, n_0: T(n) \leq c \cdot \log{ _5}{n} (\forall n \geq n_0)$<br>
$\implies \exists c, n_0: T(n) \leq c \cdot \frac{\log{n}}{\log{5}} (\forall n \geq n_0)$<br>
$\implies \exists c, n_0: T(n) \leq \frac{1}{\log{5}}c \cdot \log{n} (\forall n \geq n_0)$<br>

Using change of base, we can derive $\log{n}$ from both $\log{ _2}{n}$ and $\log{ _5}{n}$ since the change of base between log functions is a constant multiple which can be manipulated by $c$ in $O(n)$. Therefore, $\log{ _2}{n}$ and $\log{ _5}{n}$ are asymptotically the same. Q.E.D.

### Sources

I worked with the TA, Ali Torabi, to review notes before working on this. Additionally, I worked with Evan Kallas and Ishita Patel when finishing and adjusting the markdown file.  
