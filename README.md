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

For this proof, we will demonstrate that $\log{ _2}{n}$ is asymptotically the same as $\log{ _5}{n}$ for any base $b$. This boils down to choosing the $c$ constant to change the base of each logarithmic function.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$<br>
Given $T(n) = \log{ _b}{n}, f(n) = \log{ _2}{n}$:<br>
$\implies \exists c, n_0: \log{ _b}{n} \leq c \cdot \log{ _2}{n} (\forall n \geq n_0)$<br>
$\implies \log{ _b}{n} \leq \frac{\log{2}}{\log{b}} \cdot \log{ _2}{n} (\forall n \geq 1)$ { $n{ _0} = 1; c = \frac{\log{2}}{\log{b}}$ }<br>
$\implies \log{ _b}{n} \leq \frac{\log{2}}{\log{b}} \cdot \frac{\log{n}}{\log{2}} (\forall n \geq 1)$<br>
$\implies \log{ _b}{n} \leq \log{ _b}{n} (\forall n \geq 1)$<br>
$\implies T$, for both logarithms are always equal for any input $n \geq 1$.<br>


The same can be done for $\log{ _5{n}}$:<br>

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$<br>
Given $T(n) = \log{ _b}{n}, f(n) = \log{ _5}{n}$:<br>
$\implies \exists c, n_0: \log{ _b}{n} \leq c \cdot \log{ _5}{n} (\forall n \geq n_0)$<br>
$\implies \log{ _b}{n} \leq \frac{\log{5}}{\log{b}} \cdot \log{ _5}{n} (\forall n \geq 1)$ { $n_0 = 1; c = \frac{\log{5}}{\log{b}}$ }<br>
$\implies \log{ _b}{n} \leq \frac{\log{5}}{\log{b}} \cdot \frac{\log{n}}{\log{5}} \forall (\forall n \geq 1)$<br>
$\implies \log{ _b}{n} \leq \log{ _b}{n} (\forall n \geq 1)$<br>
$\implies T$, for both logarithms are always equal for any input $n \geq 1$.

Both $\log{ _2}{n}$ and $\log{ _5}{n}$ are asymptotically the same as any logarithm function with a different base; therefore, $\log{ _2}{n}$ and $\log{ _5}{n}$ are asymptotically the same.

### Sources

I worked with the TA, Ali Torabi, to review notes before working on this. Additionally, I worked with Evan Kallas when finishing the markdown file.  
