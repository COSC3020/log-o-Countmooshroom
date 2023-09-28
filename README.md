[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11730511&assignment_repo_type=AssignmentRepo)
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

To start, we'll use $log_{2} n$ as our function.

$T(n) \in O(log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot log_{2} n \forall n \geq n_0$

We know some logarithm properties that will help us.

$log_{b} a = \frac{log_{x} a}{log_{x} b} = \frac{1}{log_{x} b} \cdot log_{x} a$

Therefore, we know this:

$log_{2} n = \frac{1}{log_{5} 2} \cdot log_{5} n$

By substitution,

$c \cdot log_{2} n = c \cdot \frac{1}{log_{5} 2} \cdot log_{5} n$

Let $d$ be the constant $c \cdot \frac{1}{log_{5} 2}$

$c \cdot log_{2} n = d \cdot log_{5} n$

We can put this into our original definition:

$T(n) \in O(log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot log_{2} n \forall n \geq n_0$

$T(n) \in O(log_{5} n) \iff \exists c, n_0: T(n) \leq d \cdot log_{5} n \forall n \geq n_0$

Since there exists a constant $c$ that works here, there also exists a constant $d$ that works.  Therefore, any $T(n)$ that is in the set $O(log_{2} n)$ must also be in the set $O(log_{5} n)$

<br><br>

Using the same method, we can prove the opposite is also true.

We'll use $log_{5} n$ as our function.

$T(n) \in O(log_{5} n) \iff \exists c, n_0: T(n) \leq c \cdot log_{5} n \forall n \geq n_0$

We know some logarithm properties that will help us.

$log_{b} a = \frac{log_{x} a}{log_{x} b} = \frac{1}{log_{x} b} \cdot log_{x} a$

Therefore, we know this:

$log_{5} n = \frac{1}{log_{2} 5} \cdot log_{2} n$

By substitution,

$c \cdot log_{5} n = c \cdot \frac{1}{log_{2} 5} \cdot log_{2} n$

Let $d$ be the constant $c \cdot \frac{1}{log_{2} 5}$

$c \cdot log_{5} n = d \cdot log_{2} n$

We can put this into our original definition:

$T(n) \in O(log_{5} n) \iff \exists c, n_0: T(n) \leq c \cdot log_{5} n \forall n \geq n_0$

$T(n) \in O(log_{2} n) \iff \exists c, n_0: T(n) \leq d \cdot log_{2} n \forall n \geq n_0$

Therefore, any $T(n)$ that is in the set $O(log_{5} n)$ must also be in the set $O(log_{2} n)$

<br>

Thus, $O(\log_{2} n)$ is the same as $O(\log_{5} n)$
