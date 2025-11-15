# **How to compute irrational numbers**

## **Algebraic Foundations of Roots and Irrational Numbers**

The concept of a "root" is not limited to numerical approximation; it is a fundamental concept in abstract algebra.

### **The Algebraic Landscape: Rings vs. Fields**

In abstract algebra, "groups," "rings," and "fields" are terms for sets of numbers (or other objects) based on the arithmetic operations they support. 
For this discussion, we can use simple, intuitive analogies.


### **The Ring of Integers**

A **Ring** is an algebraic structure that generalizes the properties of the integers, 
$$\mathbb{Z} = \{\dots, -2, -1, 0, 1, 2, \dots\}.$$

Intuitively, a ring is any set of numbers where you can **add, subtract, and multiply**, 
and the result of these operations will always be another number _within that same set_.

- **Addition:** $5 + 8 = 13$ (13 is in $\mathbb{Z}$)

- **Subtraction:** $5 - 8 = -3$ (-3 is in $\mathbb{Z}$)

- **Multiplication:** $5 \times 8 = 40$ (40 is in $\mathbb{Z}$)

The defining _limitation_ of a ring is division. 
If you divide two integers, 
you do not always get another integer. 
For example, $
5 / 8 = 0.625$, 
which is _not_ in the set $\mathbb{Z}$. 
Because the integers are not _closed_
under "division",
they form a ring, 
but not a _field_.

### **The Field of Rational Numbers**

A **Field** is a special, 
more powerful type of commutative ring. 
A field is a set 
where every non-zero element has a _multiplicative 
inverse_ (a "reciprocal") within the set.

Intuitively, a field is 
a set of numbers 
where you can **add, subtract, multiply, AND divide** 
by any non-zero number, 
and the result will always 
be a number _within that same set_.

The classic example 
is the set of **Rational Numbers**, 
$\mathbb{Q}$, 
which is the set of all possible fractions 
$p/q$ 
where $p$ and $q$
 are integers and $q \neq 0$.

- **Add/Subtract/Multiply:** These operations on fractions always produce another fraction.

- **Division**: This is the key. Any non-zero rational number $a/b$ has an inverse, $b/a$. Therefore, division is always possible:

  $$\frac{a/b}{c/d} = \frac{a}{b} \times \frac{d}{c} = \frac{ad}{bc}$$

  The result, $ad/bc$, is just another rational number.

In abstract algebra, 
$\mathbb{Q}$ is called as 
the __field of fractions__ of $\mathbb{Z}$; 
it is the smallest possible field that can be constructed that contains all of the integers. 
This $\mathbb{Z} \subset \mathbb{Q}$ structure 
(a ring embedded within its field) 
is the primary model for understanding more complex topics 
in algebraic number theory.

### **Polynomials Defined Over Rings and Fields**

The phrase "polynomials defined over a proper ring or field" refers to the algebraic structure known as a **Polynomial Ring**, denoted $K[X]$
where $K$ is a given ring (or field).

This simply means that 
the _coefficients_ of the polynomial 
are taken from the set $K$.

- Polynomial over a Ring (e.g., $\mathbb{Z}[X]$):

  $p(x) = 4x^3 - 7x + 2$

  The coefficients $\{4, -7, 2\}$ are all elements of the ring of integers $\mathbb{Z}$. Therefore, $p(x)$ is in $\mathbb{Z}[X]$.

- Polynomial over a Field (e.g., $\mathbb{Q}[X]$):

  $q(x) = \frac{1}{2}x^2 - \frac{5}{3}x + \frac{3}{4}$

  The coefficients $\{\frac{1}{2}, -\frac{5}{3}, \frac{3}{4}\}$ are all elements of the field of rational numbers $\mathbb{Q}$. Therefore, $q(x)$ is in $\mathbb{Q}[X]$.

It is important to note that 
the set of all polynomials $K[X]$ is _itself_ a ring,
namely,
you can add, subtract, and multiply polynomials to get another polynomial. However, 
$K[X]$ is _not_ a field. 
The reason is the same as for the integers: 
division is not always possible _within the set_. 
For example, the element $x$ is a polynomial. 
Its multiplicative inverse is $1/x$, 
which is a _rational function_, not a polynomial. 
Since $x$ has no inverse in $K[X]$, 
the polynomial ring is not a field.

### **The Emergence of Irrationality from Rational Polynomials**

This brings us to the central conceptual question: how can a polynomial with "normal" rational coefficients have "weird" irrational roots? This phenomenon reveals a fundamental "incompleteness" in the field of rational numbers.

First, we must formally define our number sets:

- **Rational Numbers ($\mathbb{Q}$):** All real numbers that _can_ be expressed as a ratio of two integers, $p/q$. Their __decimal expansions__ either terminate or repeat.

- **Irrational Numbers ($\mathbb{R}\setminus\mathbb{Q}$):** All real numbers that _cannot_ be expressed as a ratio $p/q$. Their decimal expansions are non-terminating and non-repeating. Famous examples include $\pi$, $e$, and $\sqrt{2}$.

- **Algebraic Numbers:** Any number (rational or irrational) that is a root of a polynomial with _integer coefficients_. For example, $\sqrt{2}$ is algebraic because it is a root of $x^2 - 2 = 0$. $5/8$ is also algebraic, as it is the root of $8x - 5 = 0$.

- **Transcendental Numbers:** Real numbers that are _not_ algebraic. This means they are not the root of _any_ polynomial with integer coefficients. $\pi$ and $e$ are the most famous examples.


Let us consider an example for $\sqrt{2}$, namely, the polynomial $p(x) = x^2 - 2 = 0$.

1. **The Coefficients:** The coefficients of this polynomial are $\\{1, 0, -2\\}$. All of these are integers.

2. **The Definition:** Therefore, $p(x)$ is "defined over" the ring of integers $\mathbb{Z}$ (it is in $\mathbb{Z}[X]$) and, by extension, it is also defined over the field of rational numbers $\mathbb{Q}$ (it is in $\mathbb{Q}[X]$).

3. **The Roots:** We know from basic algebra that the roots of this equation are $x = \pm\sqrt{2}$.

4. **The Question:** Are these roots $\pm\sqrt{2}$ rational (in $\mathbb{Q}$) or irrational (not in $\mathbb{Q}$)? Can you compute $\sqrt{2}$ explicitly?

We will see how to compute $\sqrt{2}$ explicitly in the next section.

## **Numerical Root-Finding Algorithms**

In mathematics and computational science, a vast number of problems can be reduced to a single, canonical form: finding the "root" or "zero" of a function.Given a continuous function $f(x)$, the root-finding problem seeks to find a value $x$ such that the function's value is zero, satisfying the equation:

$$f(x) = 0$$

This simple expression is the universal target for a class of algorithms known as root-finding algorithms. The versatility of this approach is not immediately obvious, but it extends to nearly any problem requiring a solution to an equation. For instance, a problem that asks to find the intersection of two different functions, $h(x)$ and $g(x)$, can be transformed into the canonical form by defining a new function $f(x) = h(x) - g(x)$. The $x$-value where $f(x) = 0$ is precisely the point where $h(x) = g(x)$. Similarly, optimization problems, which seek to find a function's minimum or maximum, can be solved by finding the roots of the function's _derivative_, $f'(x) = 0$, to locate the critical points.

Numerical methods for solving $f(x) = 0$ are broadly categorized into two philosophies, distinguished by the information they require:

1. **Bracketing Methods:** These methods require the user to provide an initial interval $[a, b]$ that is _known_ to contain a root. Their strategy is to "trap" the root within this bracket and then systematically shrink the bracket until the root is isolated to the desired precision.

2. **Open Methods:** These methods do not require an initial bracket. Instead, they require one or more initial _guesses_ for the root. Their strategy is to use local information about the function such as its value and slope to generate a sequence of new, hopefully better, guesses that converge toward the root.

This distinction creates a fundamental trade-off in numerical analysis. Bracketing methods are often described as slower, but they guarantee convergence, provided the initial bracket is valid. Open methods are generally much faster, but they come with no such guarantee and may diverge or fail if the initial guess is poor. Remark that this diverge or fail is closely related to the 'chaotic behavior' in the term of dynamical systems.

This is not merely a trade-off between speed and safety, but one of _prerequisite information_. A bracketing method like Bisection requires _topological_ information about the function: the knowledge that a sign change occurs over an interval $[a, b]$. Finding such a bracket can be a significant computational task in itself. Conversely, an open method like Newton's requires less initial data (only a single guess $x_0$) but demands different, _local_ information: the function $f(x)$ must be _differentiable_, and its derivative $f'(x)$ must be known and computable. This difference in requirements dictates the choice of algorithm long before the first iteration is run.

## **Bisection method**

The Bisection method is the most reliable and straightforward of all root-finding algorithms. Its mathematical foundation is not a complex formula but a fundamental property of continuous functions: the **Intermediate Value Theorem (IVT)**.

### **Theoretical Foundation: The Intermediate Value Theorem**

The IVT states that if a function $f(x)$ is continuous on a closed interval $[a, b]$, and the function's values at the endpoints, $f(a)$ and $f(b)$, have opposite signs (i.e., $f(a) \cdot f(b) < 0$), then there must exist at least one value $c$within the open interval $(a, b)$ such that $f(c) = 0$.

The Bisection method weaponizes this theorem. The initial bracket $[a, b]$ is the _guarantee_ that a root is trapped inside. The algorithm's entire purpose is to shrink this trap by "bisecting" it, or cutting it in half, at every step.

### **The Algorithm**

The iterative procedure for the Bisection method is as follows:

1. **Initialization:**

   - Define the continuous function $f(x)$.

   - Find a starting interval $[a_0, b_0]$ that "brackets" a root, meaning $f(a_0) \cdot f(b_0) < 0$.

   - Define a stopping tolerance $\epsilon$ (for the error in $f(x)$) and a maximum number of iterations $N$.

2. **Iteration:** For $n = 0, 1, 2, \dots, N$:

3. **Calculate Midpoint**: Compute the midpoint $m_n$ (the bisection point) of the current interval:

   $$m_n = \frac{a_n + b_n}{2}$$

4. **Evaluate:** Calculate the function's value at the midpoint, $f(m_n)$.

5. **Check for Solution:** If the process has converged (e.g., $|f(m_n)| < \epsilon$ or the interval width $(b_n - a_n)/2$is smaller than a desired precision), stop and return $m_n$ as the approximate root.

6. **Update Interval (The Bisection):**

   - If $f(a_n) \cdot f(m_n) < 0$, the sign change is in the _left half_ of the interval. The root is now trapped in $[a_n, m_n]$. Set the new interval to $[a_{n+1}, b_{n+1}] = [a_n, m_n]$.

   - Otherwise, the sign change must be in the _right half_ (i.e., $f(m_n) \cdot f(b_n) < 0$). The root is trapped in $[m_n, b_n]$. Set the new interval to $[a_{n+1}, b_{n+1}] = [m_n, b_n]$.

7. **Fail-safe:** If the loop completes $N$ iterations without converging, stop and report that a solution was not found within the maximum iteration count.


### **Convergence Analysis: Linear and Predictable**

The Bisection method's rate of convergence is described as **linear**. This is often presented as a disadvantage when compared to the "quadratic" convergence of Newton's method. However, this description is incomplete and undersells the Bisection method's greatest strength.

At each iteration, the size of the interval $[a, b]$ is divided by $2$. This means that after $N$ iterations, the width of the interval containing the root is precisely $\frac{b_0 - a_0}{2^N}$. The absolute error of the midpoint $m_N$ is bounded by half of this width: $|x_\infty - m_N| \le \frac{b_0 - a_0}{2^{N+1}}$.

This error bound is deterministic. It does not depend on the function's shape, its derivative, or the initial guess (beyond the bracket width). Each iteration adds exactly "one bit of accuracy". The term "linear convergence" refers to the fact that the error is reduced by a constant factor $1/2$ at each step.

The profound value of this is its _predictability_. One can calculate _in advance_ the number of iterations $N$ required to achieve any desired precision $\epsilon$. By rearranging the error bound formula, $N$ must satisfy $N > \log_2\left(\frac{b_0 - a_0}{\epsilon}\right) - 1$.

This predictability is an invaluable asset in safety-critical systems. While other methods may be "faster" on average, they are also unpredictable; they may fail to converge or take an unexpectedly long time. The Bisection method is the "fallback method when all else fails". It may be the "square wheel," but it is a wheel that is guaranteed to reach its destination, making it more robust than a "round wheel" that might oscillate wildly or fly off the axle.

## **The Newton-Raphson Method**

The Newton-Raphson method (or simply Newton's method) is the canonical "open" method and is celebrated for its remarkable speed. Its core idea is not based on trapping the root but on using calculus to refine a guess.

### **Geometric Intuition: The Tangent Line**

The method operates on a simple, powerful geometric intuition: a "local linear approximation".

1. **Start with a Guess:** Begin with a single initial guess, $x\_0$, which is hopefully close to the true root.

2. **Find the Point:** Locate the point on the function's curve: $(x\_0, f(x\_0))$.

3. **Draw the Tangent:** Draw the tangent line to the function at that exact point. The slope of this line is given by the derivative, $f'(x_0)$.

4. **Find the Intercept:** The x-intercept of this tangent line (the point where it crosses the x-axis, $y=0$) becomes the _next, improved guess_, $x_1$.

5. **Iterate:** This new guess $x_1$ is almost always closer to the true root than $x\_0$ was. The process is then repeated from $x_1$. A new tangent is drawn at $(x_1, f(x_1))$, its x-intercept becomes $x_2$, and so on.Visually, the algorithm appears to "slide down" the tangent lines at each step, homing in on the root with incredible speed.

### **Derivation of the Iterative Formula**

This geometric process is formalized by a simple algebraic derivation.

1. The equation for a line passing through $(x_n, f(x_n))$ with a slope of $m = f'(x_n)$ is given by the point-slope formula:

   $$y - f(x_n) = f'(x_n) \cdot (x - x_n)$$

2. To find the x-intercept of this line, we set $y = 0$ and define the new $x$-value as our next guess, $x_{n+1}$:

   $$0 - f(x_n) = f'(x_n) \cdot (x_{n+1} - x_n)$$

3. Assuming the derivative is not zero ($f'(x_n) \neq 0$), we can solve for $x_{n+1}$:

   $$-\frac{f(x_n)}{f'(x_n)} = x_{n+1} - x_n$$

4. This yields the famous Newton-Raphson iterative formula:

   $$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}.$$

### **Prerequisites and Costs**

The power of this method comes with strict prerequisites:

- The function $f(x)$ _must_ be differentiable.

- The derivative $f'(x)$ must be known and analytically computable. This is a significant prerequisite that is not always available in "real-world" problems.

- The computational cost per iteration is _two_ function evaluations: one for $f(x\_n)$ and one for $f'(x\_n)$.


### **Convergence Analysis: Quadratic and Local**

The primary advantage of Newton's method is its **quadratic** rate of convergence. 
This is a much faster classification than "linear." 
Quadratric convergence means that the number of correct decimal digits _roughly doubles with each iteration_. 
If one guess is accurate to 3 digits, the next is likely accurate to 6, then 12, then 24.
However, this incredible speed is _conditional_ and _local_. 
The "quadratic" label only applies if:

1. The initial guess $x_0$ is "sufficiently close" to the true root $r$.

2. The root $r$ is a _simple root_, meaning its multiplicity is $1$.

If these conditions are not met, the method's behavior becomes pathological. Its "instability" is its defining weakness.

- **Divergence:** A poor initial guess can cause $f'(x_n)$ to be small, sending the next guess $x_{n+1}$ "out beyond Pluto," leading to iterations that diverge to infinity.

- **Oscillatory Behavior:** The iterations can get "stuck" in a loop, bouncing between two or more values and never converging to the root.

- **Failure at $f'(x_n) = 0$:** If any iteration lands on a point where the tangent is horizontal (a local min/max), $f'(x_n) = 0$, causing a division-by-zero error and catastrophic failure.

- **Degradation to Linear Convergence:** A more subtle and common failure occurs when finding a root with a _multiplicity greater than 1_ (e.g., $f(x) = (x-2)^2$). At such a root $r$, the derivative $f'(r)$ is _also_ zero. As the iterations $x_n$ approach $r$, the $f'(x_n)$ term in the denominator also approaches zero, which "slows convergence down to linear".

This last point is critical. It explains real-world scenarios, such as one noted for calculating $\arcsin(x)$ near $x=0.99$, where the Bisection method (200 iterations) was _dramatically faster_ than Newton's (1000 iterations).This is not user error; it is a feature of the problem. Near the "edges," the function's derivative was likely behaving badly (approaching zero or infinity), trapping Newton's method in a region of slow, linear convergence, while the robust Bisection method "gained its bit" of accuracy every single time. The "quadratic" label, therefore, is a best-case scenario, not a guarantee.


### **Comparison: Speed vs. Stability vs. Cost**

The simple narrative of "fast Newton's vs. slow Bisection" is insufficient for expert application. A more nuanced comparison must account for the total computational cost and the guarantees of success.

A simple comparison of iteration counts, however, can be misleading. A more holistic analysis must account for the _computational cost per iteration_.
In many real-world applications, such as large-scale scientific simulations, the evaluation of the function $f(x)$ is the primary performance bottleneck, potentially taking seconds, hours, or even days.

In this context, the cost-per-iteration is:

- **Bisection:** 1 function evaluation ($f(m)$).

- **Newton's:** 2 function evaluations ($f(x_n)$ and $f'(x_n)$).

If $f(x)$ is a complex simulation, and $f'(x)$ is an equally complex analytical derivative, Newton's method costs _twice as much_ per step. 
If the derivative $f'(x)$ is not known analytically, 
it must be _approximated_ numerically, for example, using a finite difference: 
$f'(x) \approx \frac{f(x+h) - f(x-h)}{2h}$. 
This approximation requires _two additional $f$ evaluations_, making the total cost for _one_ Newton's step _three_ function evaluations (one for $f(x\_n)$ and two to approximate $f'(x\_n)$).

This cost-benefit analysis is precisely why the **Secant Method** was developed.The Secant method is a clever hybrid that acts like Newton's method but avoids the need for $f'(x)$. 
It approximates the tangent line with a _secant line_ drawn through the two _previous_ guesses. Its iterative formula is:

$$x_{n+1} = x_n - \frac{f(x_n)(x_n - x_{n-1})}{f(x_n) - f(x_{n-1})}$$

Its properties are an excellent compromise:

- **Cost:** It requires only _one new $f$ evaluation_ per iteration (reusing $f(x\_{n-1})$ from the previous step).

- **Convergence:** Its convergence rate is **superlinear** (formally, $\phi \approx 1.618$), which is slower than Newton's quadratic but _significantly_ faster than Bisection's linear rate.

- **Prerequisites:** It requires two initial guesses, but no derivative.

For many real-world problems where the derivative is unknown and function evaluations are expensive, the Secant method is often the practical optimum.

## **Implementation in Python: An Executable Reference**

The theoretical differences between the methods become concrete when implemented in code. The following Python implementations are robust, documented, and include fail-safes such as a maximum iteration count.
