### Algebra
- Quadratic Expressions
	$ax^{2} + bx + c$
	- $a^2$ = leading term 
	- a = leading coefficient 
	- bx = 
	- c = constant term
	- 
**Factoring**
- E.g. Solve for r.
		$p = \frac{2q + r}{qr}$
		$pqr = 2q + r$
		$pqr - r = 2q$
		$r(pq - 1) = 2q$
		$r = \frac{2q}{pq - 1}$
		
- ==E.g.== Factor $(x^{2}- 1)(2x^{2} + 6x - 14) - (x^{2} + 3x + 4)$
	- Factoring out A from both terms: AB - AC --> A(B - C)
		$(x^{2}- 1)(2x^{2} + 6x - 14 - x^{2} + 3x + 4)$
	- Combine like terms for B and C
		$(x^{2}- 1)(x^{2} + 3x - 18)$
	- Factor B and C: 
		- Need to get multiply 2 terms to get -18
			- +/- 18 and 1, +/- 9 and 2, +/- 3 and 6
		- Need to add 2 terms together to get 3
			- 6 + (-3) = 3
		- Therefore:
		  $(x^{2}- 1)(x + 6)(x - 3)$
	- Factor A
		$(x - 1)(x + 1)(x + 6)(x - 3)$
		
- E.g.  Which of the following describes all values of x satisfying $x^{2} + 4 >= 5$?
		$x^{2} + 4 => 5$
		$x^{2} >= 1$
		$x >= 1, -1$
		
- E.g.
	$3x^3 + 12x^2 - 63x$
	- Numbers are multiples of 3x so can factor this out. 
	$3x(x^2 + 4x - 21)$
	- To get -21, we could have to multiply (-3)(7) * 7 = -21. 
	$(3x - 3)(x + 7)$
	
### Finding Expression from Graph or Values
- E.g. Let f(x) = x - 4. Define g(x) = f(x) + d. Find the value of d so that the range of g(x) is the set {y | y ≥ -5}.
    g(x) = (x - 4) + d
	- Sub in value of x when its at its minimum.. So 0.
	g(x) = ((0) - 4)  + d
	       = - 4 + d 
	- We’re looking for minimum y-value of -5, so we sub for y. 
	-5 = - 4 + d 
	- Rearranging to solve for d. 
	-5 + 4 = d 
	d = -1
### Transformations and Translations
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd6Gs58m4BzuzpDaMK3D6t-4PcJJ3Ua5MD4kotW7KkeGEiJxqECGDicX_n-Dc_pwOF1EpifLJE9znpdZPF30l0xE5g4gSslF6zVJE2Xc057BhYUu-F13NENQoxSOlGuvK_QBEHRFrqUsqX6bFfV1SYP1L_O?key=6nzOubOsu7KFg1-d9eViDA)

#### Graphing Exponential Functions
- Basic exponential function: y = $r^x$ 
	- If A value added (the y0 value or initial value e.g. population of 5000), then equation becomes $y = Ar^x$.
- ![[Pasted image 20240910225256.png]]
- Stretches:
	- Y-axis
		- Horizontal expansion by factor of 2
			- $y = 6^\frac{x}{2}$
			- $y = log \frac{1}{2}(x)$ 
		- Horizontal compression by factor of 2
			- $y = 6^{2x}$
			- $y = log 2(x)$
	- X-axis
		- Vertical expansion by factor of 2
			- $y = (2)6^x$
			- $y = 2log(x)$
		- Vertical compression by factor of ½ 
			- $y = (\frac{1}{2})6^x$
			- $y = \frac{1}{2}log(x)$
- Translations: 
	- Y-axis
		- Translation 2 units right
			- $y = 6^{x - 2}$
			- $y = log(x - 2)$
		- Translation 2 units left 
			- $y = 6^{x + 2}$
			- $y = log(x + 2)$
	- X-axis
		- Translation 2 units down
			- $y = 6^x - 2$
			- $y = log(x) - 2$
		- Translation 2 units up
			- $y = 6^x + 2$ 
			- $y = log(x) + 2$ 
- Reflections: 
	- Y-axis
		- Reflection of $y = 4^x$ is $y = 4^{-x}$ (same as writing $y = \frac{1}{4}^x$).
	- X-axis
		- Reflection of $y = 6^x$ is $y = -6^x$.
	- Y = x line
		- Reflection of $y = ab^x$ is  $x = ab^y$
		- Reflection of $log(\frac{x}{a}) = ylog(b)$ is $y =\frac{log(\frac{x}{a})}{log(b)}$
	- Domain (x E R) would only change if there was a reflection in the line y = x (x > 0, x E R). No other transformation would change the domain

- E.g. 
  ![[Pasted image 20240912104907.png]]
	- For $y = e^x$, when x = 0 --> y = 1
	- a (constant): value stretches/compresses curve vertically
	- r: rate changes curve 
	- k: stretches/compresses curve horizontally
	
- Exponent laws:
	- Power of a power property
		- This property states that when multiplying two powers with the same base, we add the exponents
		- Can raise any element in an expression to the power of 1 and not change the expression
		- E.g. $(5^6)(5^2)= 5^8$
		- E.g. $(49^{x-1})(7^{2x-3})$ 
	          $= ([7^2]^{x-1})(7^{2x-3})$  
	          $= (7^{2x-2})(7^{2x-3})$ 
	          $= 7^{4x-5}$
	- Quotient of powers property
		- This property states that when dividing two powers with the same base, we subtract the exponents
		- E.g. $\frac{5^6}{5^2} = 5^4$
	- Rational exponent property 
		- E.g. $5^{\frac{6}{2}} = (^2\sqrt5)^6$
		- E.g. $P(t) = Po(7)^{\frac{t}{5}}$
		             $= Po(5\sqrt7)^t$
		             $= Po(7^{\frac{1}{5}})^t$  
		             $= Po(1.48)$
- Power function has the form: $y = f(x) = K * x^n$
	- K is a constant
		- Referred to as the "coefficient"
		- Scales the vertical behaviour (i.e. stretches the graph along the y-axis)
- Power functions ($y = n^x$) with positive power integers (n = 2, . . . , 5 ) intersect at: 
	- x = 0 
	- x = 1
	- if $ax^{n}= bx^{m}$ --> $x^{n - m} = \frac{b}{a}$
		- E.g. $y = 3x^4$ and $y = 27x^2$
			- Intersect at $3x^{4} = 27x^2$
			$3x^{4} = 27x^2$
			$27x^{2} - 3x^{2} = 0$
			$3x^2(9 - x^2) = 0$
			- 3 solutions:
				$3x^{2} = 0$
				$x = 0$

				$9 - x^2 = 0$
				$9 = x^2$
				$x = \sqrt 9$
				$x = \frac{+}{-}3$
				- Because + and - x-value when sqrt 
- The greater the power n, the flatter the graph near the origin and the steeper the graph beyond x > 1
	- Close to the origin, the functions with lower powers dominate, while far from the origin, the higher powers dominate
- All power functions are continuous and unbounded
- Irrational number: a real number that cannot be expressed as a ratio of integers
	- Classic examples are $\sqrt2$ and $\pi$
- Even and odd power functions
	- ![[Pasted image 20240912084905.png]]
		- Even functions: 
			- $y = x^{n}$ --> $+\infty$
			- These functions have a local minimum near the origin, which is a point such that the value of f is larger at all sufficiently close points
				- ![[Pasted image 20240912091917.png]] 
		- Odd functions:
			-  $y = x^{n}$ --> $-\infty$
			- These functions are one-to-one, meaning each value of y is obtained from a unique value of x, and vise versa
- Determine if power function is even using f(-x) = f(x)
	- E.g. $f(x) = x^{2} - 3x^4$
		- Taking the f(-x) of f(x)
			$f(-x) = (-x)^{2} - 3(-x)^{4}$
			 $= x^2 - 3x^2$
		 - Shows that when n is even, $(-1)^{n} = 1$
 - Sketching graphs - polynomial graphs can be obtained by combining its power function components 
	 - E.g. consider $y = p(x) = x^{3} + ax$ 
		 - Near the origin ($x = 0$), the term $ax$ dominates so that the function behaves as $y = ax$
			 - If $a = 0$, the slope would appear as a straight line near the origin 
			 - If $a > 1$, slope would appear positive near the origin
			 - If $a < 1$, slope would appear negative near the origin 
		 - At larger values of x (far from the origin), $x^3$ dominate so that the function behaves as $y = x^3$
		 - ![[Pasted image 20240912093934.png]]
		 - ![[Pasted image 20240912094800.png]]
		 - ==!!!!!!==
- Rational functions
	- Function with a fraction
	- Example of a rational power function would be:
	  $y = \frac{Ax^n}{a^{n} + x^n}$, $x >= 0$
		- Graph will approximate $y = \frac{Ax^n}{a^n}$ closer to origin since $x^n$ is negligible at small x-values
			- Higher n value means graph will be flatter near origin
		- Graph will approximate $y = \frac{a^n}{x^n}$ further from origin since $a^n$ is negligible at large x-values
			- Higher x-value means graph will be sharper and eventually result in an asymptote 
		- Asymptote at y = A