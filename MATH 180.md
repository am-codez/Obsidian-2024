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

#### Graphing Power Functions
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
	
### Graphing Exponential Functions
- Basic exponential function: y = $ar^x$ 
	- a (constant): value stretches/compresses curve vertically
	- r: rate changes curve 
	- k: stretches/compresses curve horizontally
- When $a > 1$, as the base increases, the function becomes steeper 
- ![[Pasted image 20240912173103.png]]
- Stretches:
	- Horizontal expansion by factor of 2
		- $y = 6^\frac{x}{2}$
	- Horizontal compression by factor of 2
		- $y = 6^{2x}$
	- Vertical expansion by factor of 2
		- $y = (2)6^x$
	- Vertical compression by factor of ½ 
		- $y = (\frac{1}{2})6^x$
- Translations: 
	- Translation 2 units right/left
		- $y = 6^{x -/+ 2}$
	- Translation 2 units down/up
		- $y = 6^x -/+ 2$
- Reflections: 
	- Y-axis
		- Reflection of $y = 4^x$ is $y = 4^{-x}$ (same as writing $y = \frac{1}{4}^x$).
	- X-axis
		- Reflection of $y = 6^x$ is $y = -6^x$.
	- Y = x line
		- Reflection of $y = ab^x$ is  $x = ab^y$
- E.g. Consider $y = e^{x}- x$
	- At $x = 0$: $e^{x} = e^0 = 1$ 
	- Larger negative x-value: $-x$ dominates at a relatively steep curve
	- Large positive x-value: $e^x$ dominates at a relatively steep curve
	- ![[Pasted image 20240912174102.png]]
	
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
		             
 ### Special Functions
 - $e^x$
	 - ![[Pasted image 20240912175348.png]]
	 - Only positive y-values 
	 - Passes through point (0, 1) because $e^{0} = 1$
	 - Appearance: 
		 - Large negative x-values: $e^x$ is close to 0
		 - Large positive x-values: $e^x$ is large and positive 
 - $log(x)$
	 - ![[Pasted image 20240912180029.png]]
	 - Treated as $ln(x)$ in this course
	 - Inverse of exponential function 
	 - Passes through point (0, 1) because $log(0) = 1$
	 - Domain: ($0, \infty$)
	 - Appearance: 
		 - Large x-values: $log(x)$ is large and positive 
		 - Small x-values: $log(x)$ is large and negative
 - $\frac{1}{x}$
	 - ![[Pasted image 20240912183320.png]]
	 - Domain and range are all non-zero numbers
	 -  Appearance: 
		 - Large x-values: $\frac{1}{x}$ is close to 0
		 - Close to x = 0: $\frac{1}{x}$ is very large (positive or negative)
 - $\sqrt x$
	 - ![[Pasted image 20240912183954.png]]
	 - Domain and range are $[0, \infty)$
	 - Appearance: 
		 - Large x-values: $\sqrt x$ is very large 
 - $|x|$
	 - ![[Pasted image 20240912184050.png]]
	 - If $x \geq$ 0: +x
		 - If $x \leq 0$: -x
	 - Only positive y-values
		 - Range: $[0, \infty]$
	 - Appearance: 
		 - Large x-values: $\sqrt x$ is very large 
		 
### Sin, Cosine, and Tan
- Formula:
		$x^{2}+ y^{2} = r^2$
- **![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXc5EhCLo5IOT2RukhmvNFqQ_cVcLkloRCwQol5M96RK025aE-0Yx2JVVSHJoDczKCfx4kNm31T3gM8e6QrhpC-bQPEFDnyV5ZDLFU-BE58meaiuZjDJ4i98B4z3vrIq7ndrzsXw72iXZtzNWn5CLC8LwzNc?key=6nzOubOsu7KFg1-d9eViDA)**
	- Given a point on the unit circle (x, y) corresponding to an angle ($\theta$), we can find:
		- The sin = the y-coordinate
		- The cos = the x-coordinate 
- We can plot the degrees of sin($\theta$) and cos($\theta$)
	- y = sin($\theta$): 
		- y-values increase from $0$ --> $π^2$ where it reaches y = 1
		- y-values decrease from $π^2$ --> $3π^2$ where it reaches y = -1
		- Sin($\theta$) reaches 1 full revolution at 2π
	- x = cos($\theta$): 
		- x-values decrease from 0 --> π where it reaches x = -1
		- x-values increase from π --> 2π where it reaches x = 1
- We can take these points and also graph them on a line, which reveals the functions of sin(x), cos(x), and tan(x) ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfw2Hq2kkOrfmz-ChJ1X7xJcYSQQ95NNd3SC1Ri_-pluiis_VgVMep93dFgzlKxsCFJFjhnCDmVNDWuB_DpE-k8NoEIqoOKVoftNlALIrdYvhTfHB9N7oZFzf7wEVrugbIKTelRor6mvmEnluQF3fie_jTv?key=6nzOubOsu7KFg1-d9eViDA)
	- Where x-axis is the angle ($\theta$) and y-axis is the trig ratio output 
	- The functions allow you to get the ratio defined when looking at the output of y = sin($\theta$), y = cos($\theta$), y = tan($\theta$)
	- E.g. at point $\frac{π}{2}$ on the graph, if we check the unit circle at $\frac{\pi}{2}$, we see our (x, y) coordinate is (0, 1). Therefore, sine is 1 and cosine is 0 which aligns with our graph
    
 - $sin(x)$
	 - ![[Pasted image 20240912183216.png]]
	 - Range (-1, 1)
	 - Passes through point (0, 0)
	 - $y = sin(\theta) = \frac{y(opposite)}{r(hypotenuse)}$
	 - Inverse $\frac{1}{sin(\theta)}$ is $y = csc(\theta) = \frac{r}{y}$
- $cos(x)$
	 - ![[Pasted image 20240912183233.png]]
	 - Range (-1, 1)
	 - Passes through point (0, 1)
	 - $y = cos(\theta) = \frac{x(adjacent)}{r(hypotenuse)}$
	 - Inverse $\frac{1}{cos(\theta)}$ is $y = sec(\theta) = \frac{r}{x}$
- $tan(x)$
	 - ![[Pasted image 20240912183253.png]]
	 - Not defined for $x = n\pi + \frac{\pi}{2}$
		 - Where n is any integer
	 - Passes through point (0, 0)
	 - $y = tan(\theta) = \frac{y(opposite)}{x(adjacent)}$
	 - Inverse $\frac{1}{tan(\theta)}$ is $y = cot(\theta) = \frac{x}{y}$

### Limits
- Helps us describe behaviour or function close to some point of interest
	- Helpful for functions that are not continuous or not defined somewhere
	- $\lim_{x \to a} f(x) = L$
		- Limit of f(x) as x approaches a is L
- Piece-wise function
	- Function defied by several pieces rather than a single formula 
		- ![[Pasted image 20240912193606.png]]
	- We evaluation function at a particular value of x on a case-by-case basis 
		![[Pasted image 20240912191538.png]]
		- Filled circle: at point (x, y), the function takes on the value  $f(x) = y$ meaning at point (3, 9) --> $f(3) = 9$
		- Empty circle (hole): not on the graph of $y = f(x)$ meaning at point (3, 6) --> $f(3) \neq 6$
		- As we move closer to $x=3$, function moves closer and closer to 6 but doesn't reach it because there's an asymptote (undefined if we try to compute)
			- ![[Pasted image 20240912193303.png]]
			- Thus we can say $\lim_{ x \to 3 } f(x) = 6$
				- However $f(3)=9$
		