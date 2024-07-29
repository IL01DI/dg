# Differential calculus
A field from calculus that studies the derivative of a function.
## Some pragmatical use
- Calculate the time when a medicine takes effect to an organism.
- The design of theme parks and conduction circuits.
- In astronautics, the derivatives allow conducting corrections in a flight trajectory.
- The radars use derivatives to calculate the velocity in a stretch.
## Concept of derivative
### Derivative of the function at a point
The derivative of a function $f(x)$ at a point $x = a$ is the slope of a tangent line, $m_{r_t}$, to the function in the point $(a, f(a))$. 
$$m_{r_t} = f'(a) = tg(α)$$
#### Average rate of change
The average rate of change is being studied to know how the function varies in a determined interval.

> [!info]
> Given a function $y = f(x)$, the coefficient definition of the average rate of change for $f(x)$ in the interval $[a, b]$ is:
> $$ARC f[a, b] = \frac{f(b)-f(a)}{b-a} = \frac{Δy}{Δx}$$

> [!NOTE]
> It is also the coefficient between the variation of the function in aforementioned interval and the range of the same.

![[Screenshot 2023-08-29 12.15.58.png]]

This value gives an idea of how fast the value of a function in a defined interval changes. As seen above, the slope of the line that connects the points $(a,f(a))$ and $(b,f(b))$ coincides geometrically:
- The denominator $Δx = b -a$ is the increase of the variable.
- The numerator $Δy = f(b) - f(a)$ is the increase of the function.

<iframe src="https://www.desmos.com/calculator/cbvwt2rj8y?embed" width="250" height="250" style="border: 1px solid #ccc" frameborder=0></iframe>

Many times the average rates of change give a sufficient rough idea of the (speed, rhythm, rate) variation of the considered phenomenon in the referred interval in the information that appeared in the daily life: economic, demographic, scientific, etc.
#### Instantaneous rate of change

> [!info]
> Sometimes, when the rough of the interval tends to zero, the average rate of change of a function tends to a constant value, referring as the instantaneous rate of change, *IRC*, of a function in a point $a$. If $h$ is defined as the increase of the variable $(b - a)$ for nearby values to zero, an expression is defined as:
> $$IRC f(a)=\lim_{h \to 0} \frac{Δ y}{h} = \lim_{h \to 0} \frac{f(a + h) − f(a) }{h}$$

In other words, be any function $y = f(x)$ and $P (a, f(a))$ any fixed point of the graph; if point $Q (a + h, f(a + h))$ is taken, the line that connects $P$ with $Q$ is a secant to the graph of the function.

![[Screenshot 2023-08-29 12.15.44.png]]

When the point $Q$ travels the curve of $f$, approximating to $P$ (points $Q_1$ to $Q_4$ of the figure), the secant line that connects $P$ with $Q$ is approximating to the line that, intuitively, identifies with the tangent line to the graph of $y = f(x)$ in $P$.

![[Screenshot 2023-08-29 13.17.38.png]]

The slope of this tangent line to the curve in $P$ will already come given for a number, $m$, to the one that approximates the slopes of the secant lines that connects $P$ with $Q$, when $Q$ approximates to $P$, or rather, when $h$ approximates to $0$.
$$m = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h}$$

> [!info]
> This number is called as derivative of the function $f$ in the point $x = a$, which represents as $f'(a)$ and is equal to the limit:
> $$f'(a) = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h}$$
> If the aforementioned limit is a real number, then $f$ is derivable in $x = a$.

> [!Tip]-
> The following variables are the same:
> - $h$ is equal to $b - a$.
> - $b$ is equal to $a + h$.
> - '$b$ → $a$' is equal to '$h$ → $0$'.

#### The foundation of IRC
The average rate of change of a function in an interval allow us to know the average variation of the function in the aforementioned interval. Nevertheless, sometimes this information results insufficient, because we need to know the variation (speed, rhythm, rate) of a more precise mode. Nothing still works to know that the average velocity of a car that has circulated in a motorway stretch have been of $110 km/h$ to let us determine with certainty if in any point of the trajectory has surpassed the maximum permitted velocity, which is of $120 km/h$. So that it is habitual to find situations in the ones that we need is the instantaneous rate of the function, that is, the variation speed of the function for a determined value of a variable: the velocity in a determined instant, the acceleration in a concrete moment, etc.
From a geometric point of view, the average rate of change of a function in an interval is the slope of the secant line to the function in the interval extremes. In this application, we partake from this consideration and analyse how it occurs with the ARC when we are reducing the interval range. We find thus a way to measure the change speed of the function in a point: known as instantaneous rate of change of the function.

> [!todo]+ 1st activity
> **The travelled metres for a car to start is given for the function $f(t) = t²$.**
> 1. **What average velocity will take between the instants $t = 3s$ and $t = 3,1s$?**
> 2. **What instantaneous velocity will have in $t = 3s$?**
> 
> > [!success]- Solution
> > 1. Calculate the average velocity:
> > $$velocity_{average} = \frac{space_{travelled}}{time_{spent}} =$$
> > $$= \frac{f(3,1)-f(3)}{3,1-3} = \frac{9,61-9}{0,1} = 6,1ms^-¹$$
> > 1. The previous reasoning is not valid to find the velocity in $t = 3s$, because the time spent in an instant is 0 and division to 0 is undefined. The calculated average velocity will still be more similar to the instantaneous velocity when the more close is the selected value to $t = 3s$. Therefore, the instantaneous velocity can define like a limit:
> > $$v(3) = \lim_{h \to 0} \frac{f(3 + h) − f(3) }{h}  =$$
> > $$= \lim_{h \to 0} \frac{(3+h)²-(3)²}{h} = \lim_{h \to 0} \frac{(6+h)}{h} =$$
> > $$= \lim_{h \to 0} (6+h) = 6ms^-¹$$
> > Then, the velocity of the car for $t = 3s$ is $6 ms^-¹$.

> [!example]- Example
> To calculate the derivative function of $f(x) = x²$ in the abscissa point $x = 2$, the definition can be applied:
> 	$$f'(2) = \lim_{h \to 0} \frac{f(2+h)-f(2)}{h} = \lim_{h \to 0} \frac{f(2+h)²-2²}{h} = \lim_{h \to 0} \frac{4+h²+4h-4}{h} = \lim_{h \to 0} \frac{h(h+4)}{h} = \lim_{h \to 0} (h+4) = 4$$

> [!todo]+ 2nd activity
> **Calculate, if they exist, the following derivative of functions in each point.**
> 1. **$f(x) = \frac{2}{x-1}$ in $x = -2$**
> 2. **$g(x) = \sqrt[3]{x}$ in $x = 0$**
> 
> > [!success]- Solution
> > 1. Using the definition, calculate the derivative in $x = -2$:
> > $$f'(-2) = \lim_{h \to 0} \frac{f(-2+h)-f(-2)}{h} = \lim_{h \to 0} \frac{\frac{2}{-2+h-1} - \frac{2}{-2-1}}{h} = \lim_{h \to 0} \frac{\frac{2}{h-3} + \frac{2}{3}}{h} = \lim_{h \to 0} \frac{2h}{3h(h-3)} = \lim_{h \to 0} \frac{2}{3h-9} = - \frac{2}{9}$$
> > As the limit exists and is finite, the derivative is $f'(-2) = - \frac{2}{9}$.
> > 2. Applying the definition again for $x = 0$:
> > $$g'(0) = \lim_{h \to 0} \frac{g(0+h)-g(0)}{h} = \lim_{h \to 0} \frac{\sqrt[3]{h}}{h} = \lim_{h \to 0} \frac{h · \frac{1}{3}}{h} = \lim_{h \to 0} \frac{1}{h · \frac{2}{3}} = +∞$$
> > As the limit is not finite, the function is not derivable in the point $x = 0$.

## Geometric interpretation of the derivative
### Derivative like slope of the tangent line

> [!info]
> Geometrically, $f'(a)$ represents the value of the slope of the tangent line to the graph of $y =  f(x)$ in the point $P (a, f(a))$, being the equation of aforementioned tangent line:
> $$y - f(a) = f'(a)(x-a)$$

> [!NOTE]
> In a similar view, when $b$ is approximating to $a$, which converts to an existing line. Thus, $b$ is the same $tg(α)$ of $a$.
> $$\begin{aligned}
> tg(β) = \frac{f(b)-f(a)}{b-a} = m_{r_s} \\
> \lim_{b \to a} \frac{f(b) − f(a) }{b-a} = \lim_{b \to a} (m_{r_s}) \\
> f'(a) = tg(α) = \lim_{b \to a} \frac{f(b) − f(a) }{b-a} = m_{r_t}
> \end{aligned}$$

> [!example]-
> To calculate the equation of the tangent line to the graph of $f(x) = x²$ the following way proceeds:
> 
> ![[Screenshot 2023-08-29 18.12.35.png]]
> 
> 1. The equation of the tangent line is $y - f(2) = f'(2)(x - 2)$.
> 2. In this case, it has to $f(2) = f'(2) = 4$.
> 3. Thus, the tangent line is $y - 4 = 4(x - 2) ⇒ y = 4x - 4$.

### Applications of the geometric interpretation of the derivative
For the identity between the derivative value of a function in a point and the slope of the tangent line to the graph of the function in this point, several important applications follow:

- Observing the graph of $f$, it can know what sign will have the derivative in each point.

> [!EXAMPLE]- 1st example
> Based on the graph of the function $y = f(x)$, it can determine the derivative sign of $f$ in $x = 0$, $x = 1$, $x = 2$, just observe the inclination of the tangents to the graph of $f$ in aforementioned points:
> 
> ![[Screenshot 2023-08-29 18.12.35.png]]
> 
> - The tangent line in $0$ is a positive slope line, then $f'(0) > 0$.
> - In the abscissa point $1$, is a horizontal line, then $f'(1) = 0$.
> - For $x = 2$, is the negative slope line, then $f'(2) < 0$.

- If it knows the derivative value of a function in each point, it can know the (behaviour, performance) of the graph of the function.

> [!EXAMPLE]- 2nd example
> In the graph, the blue line represents the derivative values of a function $f$ in each point. Based on this graph, it can sketch the graph of $f$ (red curve):
> 
> ![[Screenshot 2023-08-30 21.45.46.png]]
> 
> - In $x = 1$, the derivative is $0$, then the function should have a point of horizontal tangent.
> - For $x > 1$, $f'(x)>0$, then the tangents to the graph of $f$ are positive slope lines.
> - For $x < 1$, $f'(x) < 0$, the the tangents to the graph of $f$ are negative slope lines.

- The tangent slope of the curve in a point is calculated by obtaining a limit, the derivative. If this limit does not exist, it means that there is no tangent line in that point. If the (side, lateral) limits are both $+∞$ or $-∞$, the tangent is vertical.

> [!EXAMPLE]- 3rd example
> To find the tangent lines to the graph of the function $f(x)$ in the point $x = 0$, it determines the slope first:
> 
> ![[Screenshot 2023-08-30 00.17.50.png]]
> $$
> f'(0) = \lim_{h \to 0} \frac{f(0+h)-f(0)}{h} = \lim_{h \to 0} \frac{|h|-0}{h} = \lim_{h \to 0} \frac{|h|}{h} =
> $$
> $$
> =
> \left\{
> \begin{array}{cl}
> \lim_{h \to 0^-} \frac{|h|}{h} = \lim_{h \to 0^-} \frac{-h}{h} = -1\\
> \lim_{h \to 0^+} \frac{|h|}{h} = \lim_{h \to 0^+} \frac{+h}{h} = 1
> \end{array}
> \right.
> $$
> As the (side, lateral) limits do not coincide, the limit does not exist and, consequently, neither the tangent line exist in that point. Also, $f(x) = |x|$ is not derivable in $x = 0$, because in that point there is a (sudden, abrupt) change in the form that varies the function [the graph has "a peak" in $x = 0$].

### Derivative and continuity

> [!INFO]
> If $f'(a)$ exists, then $f$ is continuous in $a$. However, if $f$ is continuous in $a$, it does not have the reason to exists $f'(a)$.

If a function $f$ is derivable in a point, so it should also be continuous in a point and lack of derivative in that point.
To demonstrate this, it is enough to see if $\lim_{h \to 0} \frac{f(a+h)-f(a)}{h}$ is a number, like the denominator tends to zero, the numerator should also tend to zero, $\lim_{h \to 0} f(a+h) = f(a)$. Then $f$ is continuous in $a$.
The contrary situation, though, is not always true and can give, for example, in the absolute value function $f(x) = |x|$ for $x = 0$ or in defined functions to (slice, piece), which leads to the concept of (side, lateral) derivatives.

> [!INFO]
> (Side, Lateral) derivatives define to the left and to the right, respectively, of a function $f$ in the point $x = a$ like the limits:
> $$\begin{aligned}
> f'(a^-) = \lim_{h \to 0^-} \frac{f(a+h)-f(a)}{h} \\
> f'(a^+) = \lim_{h \to 0^+} \frac{f(a+h)-f(a)}{h}
> \end{aligned}$$
> If the (side, lateral) derivatives coincide, then $\lim_{h \to 0} \frac{f(a+h)-f(a)}{h}$ exist and $f$ is derivable in $a$.

> [!EXAMPLE]-
> To determine if $f'(0)$ exists to function $f(x) = x²$, calculate their (side, lateral) derivatives:
> $$\begin{aligned}
> f'(0^-) = \lim_{h \to 0^-} \frac{f(0+h)-f(0)}{h} = \frac{f(h)}{h} = \frac{h²}{h} = h = 0 \\
> f'(0^+) = \lim_{h \to 0^+} \frac{f(0+h)-f(0)}{h} = \frac{f(h)}{h} = \frac{h²}{h} = h = 0
> \end{aligned}$$
> As their (side, lateral) derivatives coincide, the derivative in $x = 0$ exists and its value is $f'(0) = 0$.

### Derivative function

> [!INFO]
> The function that every number $x$ of the domain of $f$ assigns the number $f'(x)$, if exists, named as the derivative function of $f$ or derivative of $f$ and usually represents as $f'$ or as $Df$ (differential). 

> [!EXAMPLE]-
> To calculate the derivative function of f(x) = x², it can the apply the definition:
> $$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = \lim_{(x+h)²-x²}{h} =$$
> $$= \lim_{h \to 0} \frac{x²+2xh+h²-x²}{h} = \lim_{h \to 0} \frac{h(2x+h)}{h} = 2x$$

In this case, it obtains the general expression of the derivative for the function, unlike the derivative in a point where it obtains a numeric value.
Also, it can define the derivative of $f'$ or second derivative of $f$, which represents as $f'$. In the same way, the $f'' = (f')'$, $f'^v$, etc.

> [!todo]+ Activity
> **Sketch the graph of the function f'(x) based on the graph of  $y = f(x)$:**
> 
> ![[Screenshot 2023-08-30 08.44.11.png]]
> 
> > [!success]- Solution
> > 1. It has to study the inclination of the tangent line in each point to the graph.
> > 2. $f'(2) = f'(6) = 0$ ⇒ the graph of $y = f'(x)$ cut to the abscissa axis in $2$ and in $6$.
> > 3. For $x < 2$ or $x > 6$, the tangent to $y = f(x)$$ has the positive slope, then $f'(x) > 0$.
> > 4. If $2 < x < 6$, the tangent slope is negative and $f'(x) < 0$.
> > 
> >  ![[Screenshot 2023-08-30 08.46.07.png]]

### Derivatives of the operations with functions
#### Derivative of the constant function $f(x) = k$

> [!info]
> If $f(x) = k$, with $k ∈ i$, then the derivative of $f$ in each point $x$ is void: $f'(x) = 0$

This result demonstrate by applying the derivative definition:
$$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = \lim_{h \to 0} \frac{k-k}{h} = \lim_{h \to 0} \frac{0}{h} = 0$$
#### Derivative of $f(x) = x^n$, $n  = 1$, $2$, $3$, etc.

> [!info]
> If $f(x) = x^n$ with $n$ natural, then the derivative of $f$ in a point $x$ is: $f'(x) = nx^{n^-}¹$

Applying the derivative definition for a point $x$:
$$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = \lim_{h \to 0} \frac{(x+h)^n - x^n}{h}$$
Working out $(x + h)^n$ for the binomial of Newton:
$$\begin{aligned}
(x+h)^n = x^n + \binom{n}{1}x^{n-}¹h + \binom{n}{2}x^{n-}²h² + ⋯ + \binom{n}{n-1}xh^{n-}¹ + h^n \\
\lim_{h \to 0} \frac{x^n + nx^{n-}¹ +h²(⋯) - x^n}{h} =
\lim_{h \to 0} \frac{h(nx^{n-}¹ + h(⋯))}{h} =
\lim_{h \to 0} (nx^{n-}¹ + h(⋯)) = nx^{n-}¹
\end{aligned}$$
Therefore, $f'(x) = nx^{n-}¹$.
#### Derivative of the addition
To calculate the derivative of $F(x) = f(x) + g(x)$ where, for example, $f(x) = x³$ and $g(x) = x²$, it can apply the derivative definition:
$$
F'(x) = \lim_{h \to 0} \frac{F(x+h)-F(x)}{h} =
\lim_{h \to 0} \frac{(x+h)³+(x+h)²-(x³+x²}{h}
$$
This last fraction can describe as the addition of the two fractions that appeared if the derivatives of $f(x) = x³$ and $g(x) = x²$. Thus:
$$F'(x) = \lim_{h \to 0} \bigg[\frac{(x+h)³-x³}{h} + \frac{(x+h)²-x²}{h}\bigg] = \lim_{h \to 0} \frac{(x+h)³-x³}{h} + \lim_{h \to 0} \frac{(x+h)²-x²}{h} = 3x² + 2x = f'(x) + g'(x)$$
In the same way it deduces the derivative of the addition of any two functions.

> [!info]
> If $f$ and $g$ have derivative in the abscissa point $x$, then, the function $F(x) = f(x) + g(x)$ have too derivative in the abscissa point $x$, and it verifies that:
> $$F'(x) = f'(x) + g'(x)$$

#### Derivative of $F(x) = k·f(x)$, where $k$ is a real number

> [!info]
> If $F(x) = k · f(x)$, with $k∈ i$, then the derivative of $F$ in any point $x$ is:
> $$F'(x) = k · f'(x)$$

This result demonstrate too by applying to the derivative definition:
$$F'(x) = \lim_{h \to 0} \frac{F(x+h)-F(x)}{h} = \lim_{h \to 0} \frac{kf(x+h)-kf(x)}{h} = \lim_{h \to 0} k · \frac{f(x+h)-f(x)}{h} = k · f'(x)$$
#### Derivative of a polynomial function
It deduces based on the three previous results.

> [!info]
> If $f(x) = a_{n}x^n + a_{n-1}x^{n-}¹ + ⋯ + a_{2}x² + a_{1}x + a_0$, then:
> $$f'(x) = na_{n}x^{n-}¹ + (n-1)a_{n-1}x^{n-}² + ⋯ + 2a_{2}x + a_1$$


> [!example]-
> - $f(x) = 8$ ⇒ $f'(x) = 0$
> - $f(x) = -5x³$ ⇒ $f'(x) = -15x²$
> - $f(x) = x⁷$ ⇒ $f'(x) = 7x⁶$
> - $f(x) = x + x³$ ⇒ $f'(x) = 1 + 3x²$
> - $f(x) = 3x⁴ - 2x² + 6x - 1$ ⇒ $f'(x) = 12x³ - 4x + 6$

It has to observe that, while derivate a polynomial function, its grade reduces to one unit. Therefore, the successive derivatives of order $n + 1$ of a polynomial of grade $n$ are always equal to $0$.

> [!todo]+ Activity
> **Calculate the successive derivatives of the function $f(x) = 2x⁵ - x⁴ + 4x³ + x - 5$.**
> > [!success]- Solution
> > $$f'(x) = 10x⁴ - 4x³ + 12x² + 1 f^{iv}(x) = 240x - 24$$
> > $$f''(x) = 40x³ - 12x² + 24x f^{v}(x) = 240$$
> > $$f'''(x) = 120x² - 24x + 24 f^{vi}(x) = 0$$
> > It proves thus that, to be $f$ a polynomial of grade 5, all their derivatives starting at the sixth are voids.

#### Derivative of the square of a function

> [!info]
> If $F(x) = [f(x)]²$, and $f$ is derivable in a point $x$, then: $F'(x) = 2f(x)f'(x)$

To demonstrate, it applies the derivative definition to the function $F(x) = [f(x)]²$:
- The numerator writes as addition & difference, being $[f(x)]² = f²(x)$.
$$F'(x) = \lim_{h \to 0} \frac{F(x+h)-F(x)}{h} =$$
- The properties of the limits to rewrite the fraction.
$$= \lim_{h \to 0} \frac{(f(x+h)+f(x))(f(x+h)-f(x))}{h} =$$
- $f$ is continuous as it is derivable.
$$= \lim_{h \to 0} (f(x+h)+f(x)) · \lim_{h \to 0} \frac{f(x+h)-f(x)}{h} = 2f(x)ff'(x)$$
#### Derivative of the product

> [!info] 
> If $f$ and $g$ are derivable in the point $x$, $F(x) = f(x)g(x)$ is too derivable and verifies as:
> $$F'(x) = f'(x)g(x) + f(x)g'(x)$$

To demonstrate, it calculates the derivative of $(f+g)²$ of two different forms:
$$
[(f+g)²]'=
\left\{
\begin{array}{cl}
(f²+2fg+g²)' = 2ff' + 2(fg)' + 2gg' \\
2(f+g)(f+g)' = 2(f+g)(f'+g') = 2ff' + 2fg' + 2gf'
\end{array}
\right\}
⇒ (fg)' = fg' + gf'
$$
#### Derivative of the coefficient
Applying the previous obtained result for the derivative of the product, it can calculate the derivative of the coefficient of two functions in the points that doesn't annul the denominator. For that, it writes $f = \frac{f}{g} · g$, it derivates the equality and solves:
$$
f' = \bigg(\frac{f}{g} · g\bigg)' = \frac{f}{g} · g' + g · \bigg(\frac{f} {g}\bigg)'
⇒ \bigg(\frac{f}{g}\bigg)' = \frac{f' - \frac{fg'}{g}}{g} = \frac{f'g-fg'}{g²}
$$

> [!info]
> If $f$ and $g$ are derivable in the point $x$, with $g(x) ≠ 0$, then $F(x) = \frac{f(x)}{g(x)}$ is derivable too and verifies as:
> $\bigg(\frac{f(x)}{g(x)}\bigg)' = \frac{f'(x)g'(x)}{(g(x))²}$, if $g(x) ≠ 0$

#### Derivative of the square root of a function
If $F(x) = \sqrt{f(x)}$, and $f$ is derivable in a point $x$, then $F(x)$ is derivable too and verifies as:
$$F'(x) = \frac{f'(x)}{2 \sqrt{f(x)}}$$
To demonstrate this result, it has to remember how much is the value of the derivative of the square of a function, and it gives reason in the following way:
Like $\big(\sqrt{f}\big)² = f$, then $\big[\big(\sqrt{f}\big)²\big]' = f'$, that is, $2 \sqrt{f}\big(\sqrt{f}\big)' = f'$ ⇒ $\big(\sqrt{f}\big)' = \frac{f'}{2 \sqrt{f}}$.

> [!example]-
> - Derivative of the square of a function
> $$f(x) = (2x+3)² ⇒ f'(x) = 2(2x+3)2 = 8x + 12$$
> - Derivative of the coefficient of two functions
> $$f(x) = \frac{x²-1}{x} ⇒ f'(x) = \frac{2x·x-(x²-1)·1}{x²} = \frac{x²+1}{x²}$$
> - Derivative of the product of two functions
> $$f(x) = x(x²-3) ⇒ f'(x) = 1(x²-3) + x · 2x = 3x² - 3$$
> - Derivative of the square root of a function
> $$f(x) = \sqrt{x²+1} ⇒ f'(x) = \frac{2x}{2 \sqrt{x²+1}} = \frac{x}{\sqrt{x²+1}}$$

> [!todo]+ Activity
> **Calculate the derivatives of the following functions.**
> 1. **$f(x) = (x³-3x)²$**
> 2. **$f(x) = (x⁴-1)(2x²+x-5)$**
> 3. **$f(x) = x(x²+3)(x²-2x)$**
> 4. **$f(x) = \sqrt{x}(3x³+4x-2)$**
> 5. **$f(x) = \frac{x-7}{x-3}$**
> 6. **$f(x) = \bigg(\frac{x+2}{x-3}\bigg)²$**
> 
> > [!success]- Solution
> > 1. Using the derivative of the square of a function:
> >  $$f'(x) = 2(x³-3)(x³-3x)' = 2(x³-3x)(3x²-3) = 6(x³-3x)(x²-1) = 6(x⁵-4x³+3x) = 6x⁵-24x³+18x$$
> >2. With the derivative of a product and of polynomials:
> >$$f'(x) = (x⁴-1)'(2x²+x-5)+(x⁴-1)(2x²+x-5)' = 4x³(2x²+x-5)+(x⁴-1)(4x+1) = 8x⁵+4x⁴-20x³+4x⁵+x⁴-4x-1 = 12x⁵+5x⁴-20x³-4-1$$
> >3. In this case, it uses the derivative of a product twice:
> > $$f'(x) = x'(x²+3)(x²-2x)+x(x²+3)'(x²-2x)+x(x²+3)(x²-2x)' = 1(x²+3)(x²-2x)+x2x(x²-2x)+x(x²+3)(2x-2) = x⁴-2x³+3x²-6x+2x⁴-4x³+2x⁴-2x³+6x²-6x = 5x⁴-8x³+9x²-12x$$
> > 4. Using the derivative of a product and of a square root:
> > 5. With the derivative of a coefficient:
> > $$f'(x) = \frac{(x-7)'(x-3)-(x-7)(x-3)'}{(x-3)²} = \frac{1(x-3)-(x-7)1}{(x-3)²} = \frac{10}{(x-3)²}$$
> > 6. With the derivative of a coefficient and of the square of a function:
> > $$f'(x) = 2 \bigg(\frac{x+2}{x-3}\bigg) \bigg(\frac{x+2}{x-3}\bigg)' = 2 \bigg(\frac{x+2}{x-3})\frac{1(x-3)-(x+2)1}{(x-3)²} = - \frac{10(x+2)}{(x-3)³}$$

### Derivative of the composed function
#### Chain rule
The derivation rules, seen until now, allow for calculating the derivative of functions like, for example $t(x) = (x²+1)⁴$, although for that, it would have to conduct the laborious task of working out the polynomial. The problem simplifies a lot if it writes $t(x)$ as the result of the composition of two functions.

> [!example]- 1st example
> The function $t(x) = (x²+1)⁴$ can derivate working out the power:
> $$t(x) = (x²+1)⁴ = x⁸ + 4x⁶ + 6x⁴ + 4x² + 1 ⇒ t'(x) = 8x⁷ + 24x⁵ + 24x³ + 8x$$
> On the other hand, it can write $t(x)$ as composition of the functions $g(x) = x² + 1$ and $f(x) = x⁴$. In this way, it has: $$t(x) = (f∘g)(x) = f(x²+1) = (x²+1)⁴$$
> If the previous functions derivates, $f'(x) = 4x³$, $g'(x) = 2x$, and conduct the product $f'(g(x)) · g'(x)$ it reaches to:
> $$f'(g(x)) · g'(x) = 4(x²+1)³ · 2x = 8x(x⁶+3x⁴+3x²+1) = 8x⁷ + 24x⁵ + 24x³ + 8x$$
> Result that coincides with the previously obtained for $t'(x)$.

The calculation of derivatives as composition of functions are known as chain rule.

> [!info] 
> If $g(x)$ have derivative in $x$ and $f(x)$ have derivative in $g(x)$, then the function $(f∘g)(x)$ have derivative in $x$ and is $(f∘g)'(x) = f'(g(x)) · g'(x)$.

The demonstration utilizes the derivative definition and the composition of functions:
$$(f∘g)'(x) = \lim_{h \to 0} \frac{(f∘g)(x+h)-(f∘g)(x)}{h} =  \lim_{h \to 0} \frac{f(g(x+h))-f(g(x))}{h}$$
If $g(x+h) - g(x) ≠ 0$, this last expression can describe as:
$$\lim_{h \to 0} \frac{f(g(x+h))-f(g(x))}{g(x+h)-g(x)} · \frac{g(x+h)-g(x)}{h} = \lim_{h \to 0} \frac{f(g(x+h))-f(g(x))}{g(x+h)-g(x)} · \lim_{h \to 0} \frac{g(x+h)-g(x)}{h} = f'(g(x)) · g'(x)$$

> [!example]- 2nd example
> To calculate the derivative of $f(x) = (5x²-x)³$, apply the chain rule:
> $$f'(x) = 3(5x²-x)²(10x-1) = 750x⁵-375x⁴+60x³-3x²$$

#### Successive application of the chain rule
If a function obtains by composition of three or more functions, to obtain its derivative it applies the associativity of the composition and the chain rule.

> [!info]
> In this way, for this composition of functions $j(x) = (f∘g∘h)(x)$, its derivative will calculate as:
> $$j'(x) = (f∘g∘h)'(x) = f'((g∘h)(x)) · g'(h(x)) · h'(x)$$


> [!example]-
> To derivate the function $j(x) = \big(\sqrt{3x-2}+5 \big)³$, it procedes thus:
> It writes as $j(x) = (f∘g∘h)(x)$, with $f(x) = x³$; $g(x) = \sqrt{x} + 5$ and $h(x) = 3x - 2$. Therefore, its derivative will be:
> $$j'(x) = 3\big(\sqrt{3x-2}+5 \big)² \bigg(\frac{1}{2 \sqrt{3x-2}}\bigg)3 = \frac{9 \big(\sqrt{3x-2}+5 \big)²}{2 \sqrt{3x-2}}$$


> [!todo]+ Activity
> **Calculate the derivative of the following functions.**
> 1. $f(x) = x \sqrt{2x²+3x-1}$
> 2. $f(x) = \frac{4x}{(x²+5)³}$
> 
> > [!success]- Solution
> > It applies the derivation rules of the product and of the coefficient, respectively, and the chain rule.
>> 1. $$f'(x) = (x)' \sqrt{2x²+3x-1}+x\Big(\sqrt{2x²+3x-1}\Big)' = 1\sqrt{2x²+3x-1} + x \Bigg(\frac{1}{2\sqrt{2x²+3x-1}}(4x+3)\Bigg) = \sqrt{2x²+3x-1} + \frac{4x²+3x}{2\sqrt{2x²+3x-1}} = \frac{8x²+9x-2}{2\sqrt{2x²+3x-1}}$$
>> 2. $$f'(x) = \frac{4(x²+5)³-4x·3(x²+5)²·2x}{(x²+5)⁶} = \frac{4(x²+5)-24x²}{(x²+5)⁴} = \frac{-20x²+20}{(x²+5)⁴}$$

#### Derivative of the inverse function
If given two functions, $f$ and $g$, one is the inverse or reciprocal of the other, $(f∘g)(x) = x$ and $(g∘f)(x) = x$, then their graphs are symmetrical with respect to the bisector of the first quadrant.
Furthermore, if $f(x)$ allows non-horizontal tangent in the point $P (a, f(a))$, then $g(x)$ will allow non-vertical tangents in the point $Q(f(a),a)$, that is to say, if $f'(a) ≠ 0$, then $g'(f(a))$ will exist.
To find the derivative of $g$, inverse to $f$, it can apply the chain rule.

> [!example]- 1st example
> To calculate the derivative of a function like $g(x) = \sqrt[3]{x}$, find first the inverse of $y = \sqrt[3]{x}, which will be $y = x³$, now that $\Big(\sqrt[3]{x}\Big)³ = x$.
> 
> In this last expression, the two members of the equality derivates by applying the chain rule when derivates the function of the left. In this way, it obtains the equality $3\Big(\sqrt[3]{x}\Big)' = 1$ and solving it reaches to the expression: $\Big(\sqrt[3]{x}\Big)' = \frac{1}{3(\sqrt[3]{x})²}$.

> [!example]- 2nd example
> If $f$ and $f^-¹$ exist and are derivable, then thee  dderivative of the inverse function is:
> $$(f^-¹)'(x) = \frac{1}{f'(f^-¹(x))}$$

This result obtains by deriving the relation $(f∘f^-¹)(x) = x$.
$$f'(f^-¹(x))·(f^-¹)'(x) = 1 ⇒ (fˆ^-¹)'(x) = \frac{1}{f'(f^-¹(x))}$$

> [!todo]+ 1st activity
> **Deduce the derivate of the function $f(x) = \sqrt[3]{x²}$.**
> > [!success]- Solution
> > Being $\Big(\sqrt[3]{x²}\Big)³ = x²$ and derivating both members of equality it obtains:
> > $$3\Big(\sqrt[3]{x²}\Big)² \Big(\sqrt[3]{x²}\Big)' = 2x ⇒ \Big(\sqrt[3]{x²}\Big)' = \frac{2x}{3\Big(\sqrt[3]{x²}\Big)²} = \frac{2x}{3x\frac{4}{3}} = \frac{2}{3x\frac{1}{3}} = \frac{2}{3\sqrt[3]{x}}$$
> > > [!tip]-
> > > To generalize the result of $f(x) = \sqrt[n]{x²}$, it proceeds from a similar way:
> > > $$\begin{aligned}
> > > \Big(\sqrt[n]{x²}\Big)^n = x² ⇒ n\Big(\sqrt[n]{x²}\Big)^{n-1} \Big(\sqrt[n]{x²}\Big)' = 2x \\
> > > \Big(\sqrt[n]{x²}\Big)' = \frac{2x}{n\Big(\sqrt[n]{x²}\Big)^{n-1}} = \frac{2x}{nx \frac{2n-2}{n}} = \frac{2}{nx\frac{n-2}{n}}
> > > \end{aligned}$$

> [!todo]+ 2nd activity
> **Calculate the derivative in the point $x = 2$ of the inverse of the function $f(x) = x⁵+x$.**
> > [!success]- Solution
> > For the function $f$, results impossible to obtain an explicit expression for its inverse, $g = f^-¹$.
> > 
> > Like $(g∘f)(x) = x ⇒ g'(x⁵+x) = x$, deriving this expression it has $g'(x⁵+x)(5x⁴+1) = 1 ⇒ g'(x⁵+x) = \frac{1}{(5x⁴+1)}$.
> >
> > It has to calculate $g'(2)$, then $x⁵ + x = 2$, of which real solution is $x = 1$, thus: $g'(2) = \frac{1}{5·1+1} = \frac{1}{6}$.
# Integral calculus