### Algebra
- Quadratic Expressions
	$ax^{2} + bx + c$
	- $a^2$ = leading term 
	- a = leading coefficient 
	- bx = 
	- c = constant term
	
- E.g. How would you write the composite function $b(ax)$ where $ax=3x^2-1$ and $bx=x^7$?
		$(3x^2-1)^7$

- E.g. Simplify $\frac{2}{\sqrt{6}-\sqrt{ 2 }}$
	- We can conjugate this irrational denominator by using principle $a^2+b^2$ --> $(a-b)(a+b)$
	- Multiple both numerator and denominator by $(a-b)$
		 $\frac{2(\sqrt{ 6 }-\sqrt{ 2 })}{\sqrt{6}(\sqrt{ 6 }-\sqrt{ 2 })-\sqrt{ 2 }(\sqrt{ 6 }-\sqrt{ 2 })}$
		 $\frac{2(\sqrt{ 6 }-\sqrt{ 2 })}{4}$
	 - Factor
		 $\frac{\sqrt{ 6 }-\sqrt{ 2 }}{2}$
### Factoring
- E.g. Solve for r.
		$p = \frac{2q + r}{qr}$
		$pqr = 2q + r$
		$pqr - r = 2q$
		$r(pq - 1) = 2q$
		$r = \frac{2q}{pq - 1}$
		
- E.g. Factor $(x^{2}- 1)(2x^{2} + 6x - 14) - (x^{2} + 3x + 4)$
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
		
- E.g. Find the point of interception for $y=4x^{2}+6x-4$ and $y=2x-1$
	- Equality statement
		 $4x^{2}+6x-4=2x-1$
	 - Combine like terms 
		  $4x^{2}+4x-3=0$
	  - Factor 
		  - To get $(4)(-3)=-12$ from multiplying: 
			  - $-12=\pm(12)(1)$  
			  - $-12=\pm(4)(3)$
			  - $-12=\pm(6)(2)$
		  - To get 4 from adding:
			  - $-12+1=-11$ | $12+(-1)=11$ 
			  - $-4+3=-1$ | $4+(-3)=1$ 
			  - $-6+2=-4$ | $6+(-2)=4$ **
	  - Re-write in factored terms 
		  $4x^2+6x-2x-3$
	  - Split bx term into 6x and -2x
		  $(4x^2+6x)-(2x-3)$
	- Factor each term
			$2x(2x+3)-1(2x+3)$
	- Factor out binomial factor
			$(2x+3)(2x-1)$
	
### Finding Expression from Graph or Values
- E.g. Solve for a and c if x-intercepts = -2, 3 and y-intercept = 12
	- Finding c using known knowledge that there's a point at (0, 12)
		$12= a(0)^{2}+ 2(0) + c$
		$12= 0 + 0 + c$
		$12= c$
	- Finding a using knowledge there's an x-value of -2
		$y= a(-2)^{2}+ 2(-2) + c$
		$y= 4a-4 + 12$
		$y= 4a +8$
		$-8= 4a$
		$-8= 4a$
		$a=-2$
		
- E.g. Consider $y=(fx)*(gx)$
  ![[Pasted image 20240913195024.png]]
	- In Q1: (-)(-) = +
	- In Q2: (-)(+) = -
	- In Q3: (+)(+) = +
	- Midpoint (between 2 x-intercepts) would be our minimum point
	
- E.g. Find the x-intercepts of $2x^3-3x^2-29x-30$.
	- Could test a couple factors of -30, e.g. $x=-2$ by plugging it into the function and seeing if remainder is 0
		 $2(-2)^3-3(-2)^2-29(-2)-30=0$
		 $(2)(-8)-3(4)-29(-2)-30=0$
		 $0=0$
		 - Therefore $x+2$ is a factor
	 - Using synthetic division.
		 **![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf2uQ_bY1XjfOfARreYA3j6gNiMIHy1YikfkDebA5WUVywXopzJI7mkNG18Lwlqt-NHYWwTG7bVta13TdnxWWKozShz6jQtk5oIU2jR5XCOTBDObBt6UjTqsnmI8vpMaFWUpVOVM-zGScLzOdqhv-5w4Q07?key=6nzOubOsu7KFg1-d9eViDA)**
	 - Gives us $y=(x+2)(2x^2-7x-15)+0$
	 - Factor $(2x^2-7x-15)+0$
		 - To get $(2)(-15) = -30$ from multiplying:
			 - $-30=\pm(30)(1)$
			 - $-30=\pm(10)(3)$
			 - $-30=\pm(15)(2)$
			 - $-30=\pm(5)(6)$
		 - Must add together to get -7:
			 - $-10+3=-7$
		 - Re-write with -10x and 3x
			 $2x^{2}-10x+3x-15$
		 - Split terms
			 $(2x^2-10x)(3x-15)$
		 - Factor each term
			 $2x(x-5)+3(x-5)$
		 - Factor binomial term out
			 $(2x+3)(x-5)$
	 - Left with:
		 - $2x+3=0$ --> x-intercept = $\frac{-3}{2}$
		 - $x-5 =0$ --> x-intercept = $5$
		 - $x+2 =0$ --> x-intercept = $-2$
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
	
- Even and odd power functions
	  ![[Pasted image 20240912084905.png]]
		- Even functions: 
			- $y = x^{n}$ --> $+\infty$
			- These functions have a local minimum near the origin, which is a point such that the value of f is larger at all sufficiently close points
				- ![[Pasted image 20240912091917.png]] 
		- Odd functions:
			-  $y = x^{n}$ --> $-\infty$
			- These functions are one-to-one, meaning each value of y is obtained from a unique value of x, and vise versa
			
 - Sketching graphs - polynomial graphs can be obtained by combining its power function components 
	 - E.g. consider $y = p(x) = x^{3} + ax$ 
		 - Near the origin ($x = 0$), the term $ax$ dominates so that the function behaves as $y = ax$
			 - If $a = 0$, the slope would appear as a straight line near the origin 
			 - If $a > 1$, slope would appear positive near the origin
			 - If $a < 1$, slope would appear negative near the origin 
		 - At larger values of x (far from the origin), $x^3$ dominate so that the function behaves as $y = x^3$ 
		 - ![[Pasted image 20240912093934.png]]

- **Rational functions**
	- Function with a fraction
	- Example of a rational power function would be:
	  $y = \frac{Ax^n}{a^{n} + x^n}$, $x >= 0$
		- Graph will approximate $y = \frac{Ax^n}{a^n}$ closer to origin since $x^n$ is negligible at small x-values (e.g. x-value of 0.2)
			- Higher n value means graph will be flatter near origin
		- Graph will approximate $y = \frac{a^n}{x^n}$ further from origin since $a^n$ is negligible at large x-values (e.g. x-value of 25)
			- Higher x-value means graph will be sharper and eventually result in an asymptote 
		- Asymptote at y = A
		
- E.g. Is $y=\frac{\sin(x)}{2+\cos(x)}$ continuous?
	- Check if numerator is continuous
		- $\sin(x)$ is continuous on its domain 
		- Could check if numerator and denominator are simultaneously zero to find discontinuity by:
			- Plugging x-value(s) from denominator into $\sin(x)\neq{0}$
			- Remembering that $\sin(x)=0$ at $n\pi$ 
	- Check is denominator is continuous
		- $1\leq \cos(x)\leq{1}$
		- Adding 2, we get $1\leq2+\cos(x)\leq{1}$
	- Therefore yes, it's continuous
	
### Graphing Exponential Functions
- Basic exponential function: y = $ar^x$ 
	- a (constant): value stretches/compresses curve vertically
	- r: rate changes curve 
	- k: stretches/compresses curve horizontally
- When $a > 1$, as the base increases, the function becomes steeper 
- Functions with negative exponent integer are expressed as $f(x)= \frac{1}{x^{n}}$
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
	 - ![[Pasted image 20240913123625.png]]
	 - Only positive y-values 
	 - Passes through point (0, 1) because $e^{0} = 1$
	 - Appearance: 
		 - Large negative x-values: $e^x$ is close to 0
		 - Large positive x-values: $e^x$ is large and positive
	 - $\lim_{ x \to -\infty }e^x$ 
			  
 - $log(x)$
	 - ![[Pasted image 20240913123837.png]]
	 - Treated as $ln(x)$ in this course
	 - Inverse of exponential function 
	 - Passes through point (0, 1) because $log(0) = 1$
	 - Domain: ($0, \infty$)
	 - Appearance: 
		 - Large x-values: $log(x)$ is large and positive 
		 - Small x-values: $log(x)$ is large and negative
	 - $\lim_{ x \to \infty }\log(x)$
	 
 - $\frac{1}{x}$
	 - ![[Pasted image 20240912183320.png]]
	 - Domain and range are all non-zero numbers
	 -  Appearance: 
		 - Large x-values: $\frac{1}{x}$ is close to 0
		 - Close to x = 0: $\frac{1}{x}$ is very large (positive or negative)
	 - Asymptotes:
		 - Vertical: at $x=0$, has limit of $+\infty$ as x approaches 0 from right and $\infty$ as x approaches 0 from the left
		 - Horizontal: $y=0$
		 
 - $\sqrt x$
	 - ![[Pasted image 20240912183954.png]]
	 - Domain and range are $[0, \infty)$
	 - Appearance: 
		 - Large x-values: $\sqrt x$ is very large 
	 - Irrational number: a real number that cannot be expressed as a ratio of integers
		 - Classic examples are $\sqrt2$ and $\pi$
		 
 - $|x|$
	 - ![[Pasted image 20240912184050.png]]
	 - Take absolute value of x before plugging it into formula (e.g. if $y=\frac{1}{|x|}$ and $x = -10$ therefore $y=\frac{1}{{10}}$)
	 - Only positive y-values, range: $[0, \infty]$
	 - Appearance: 
		 - Large x-values: $|x|$ is very large 
	 - E.g. for $\sin(|x|)$: 
		 - Graph when $x\leq{0}$ mirrors graph when $x\geq{0}$
		   ![[Pasted image 20240913114702.png]]
			 - Where blue is $\sin(|x|)$ and green is $\sin(x)$
### Sin, Cosine, and Tan
- Formula:
		$x^{2}+ y^{2} = r^2$
- Given a point on the unit circle (x, y) corresponding to an angle ($\theta$), we can find:
	- The sin = the y-coordinate
	- The cos = the x-coordinate 
- We can plot the degrees of sin($\theta$) and cos($\theta$) to graph them on a line, which reveals the functions of sin(x), cos(x), and tan(x) ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfw2Hq2kkOrfmz-ChJ1X7xJcYSQQ95NNd3SC1Ri_-pluiis_VgVMep93dFgzlKxsCFJFjhnCDmVNDWuB_DpE-k8NoEIqoOKVoftNlALIrdYvhTfHB9N7oZFzf7wEVrugbIKTelRor6mvmEnluQF3fie_jTv?key=6nzOubOsu7KFg1-d9eViDA)
    
 - $sin(x)$
	 - ![[Pasted image 20240912183216.png]]
	 - $y = sin(\theta) = \frac{y(opposite)}{r(hypotenuse)}$
	 - Inverse $\frac{1}{sin(\theta)}$ is $y = csc(\theta) = \frac{r}{y}$
	 - Behaviour:
		 - Passes through point (0, 0)
		 - y-values increase from $0$ --> $π^2$ where it reaches y = 1
		- y-values decrease from $π^2$ --> $3π^2$ where it reaches y = -1
		- Sin($\theta$) reaches 1 full revolution at 2π
- $cos(x)$
	 - ![[Pasted image 20240912183233.png]]
	 - $y = cos(\theta) = \frac{x(adjacent)}{r(hypotenuse)}$
	 - Inverse $\frac{1}{cos(\theta)}$ is $y = sec(\theta) = \frac{r}{x}$
	 - Behaviour:
		 - Passes through point (0, 1)
		 - x-values decrease from 0 --> π where it reaches x = -1
		- x-values increase from π --> 2π where it reaches x = 1
- $tan(x)$
	 - ![[Pasted image 20240912183253.png]]
	 - $y = tan(\theta) = \frac{y(opposite)}{x(adjacent)}$
	 - Inverse $\frac{1}{tan(\theta)}$ is $y = cot(\theta) = \frac{x}{y}$
	 - Behaviour:
		 - Not defined for $x = n\pi + \frac{\pi}{2}$
			 - Where n is any integer
		 - Passes through point (0, 0)
	 - $\\lim_{ x \to \frac{\pi}{2}^+ }\tan(x)=-\infty$
			- Approaching from right of $\frac{\pi}{2}$
	 
 - Eg. if $tan(\theta)= \frac{4}{3},0\leq\theta\leq\frac{\pi}{2}$, find $\sin(\theta)$ and $\cos(\theta)$?
		- opp (y-value) = 3 
		- adj (x-value) = 4
		- Finding hyp
			$r^2=a^2+b^2$
			$r^2=(4)^2+(3)^2$
			$r^2=16+9$
			$r=\sqrt{25}$
			$r=5$
		- $\cos(\theta)=\frac{4}{5}$
		- $\sin(\theta)=\frac{3}{5}$

### Limits
- Helps us describe behaviour or function close to some point of interest, if as x approaches a certain value, it never reaches a particular y-value
- Helpful for functions that are not continuous or not defined somewhere
- $\lim_{x \to a} f(x) = L$
	- Limit of f(x) as x approaches a is L if approaching a limit from the left and right, we say the limit exists and L is not in the domain of the function
		- Also referred to as a two-sided limit
		- However, we can have data points at the limit
			- If not, we would say f(a) does exist
	- $\lim_{x \to a+}$: approaching x-value from right (above)
	- $\lim_{x \to a-}$: approaching x-value from left (below)
- ![[Pasted image 20240913224803.png]]
- **Continuity**
	- Continuous function: a graph that has no breaks in the shape of a graph, meaning you could draw a whole function without lifting your pencil
		- No rational function is a continuous function
		- Conditions for $f(x)$ to be continuous at a point 
			- $f(a)$ is defined
			- $\lim_{ x \to a }f(x)$ exists
			- $\lim_{ x \to a }f(x)=f(a)$ 
		- E.g. Make $g(x)$ continuous by determining value(s) that make $g$ continuous
		  ![[Pasted image 20240919142913.png]]
			  $$\begin{align}
x^{2}+2=4x-1 \\
Roots  \\
x^2+2-4x+1=0 \\
x^2-4x+3=0 \\
(x+3)(x-1)=0 \\
roots:x=1,-3 \\
\end{align}$$
			- Determining 2 d values that make $f(x)$ continuous
$$\begin{align}
d=3 \\
(3)^2+2=11 \\
(4)(3)-1=11 \\
 \\
 d=1 \\
(1)^2+2=11 \\
(1)(3)-1=11 
\end{align}$$
- E.g. ![[Pasted image 20240919144359.png]]
$$\begin{align}
cb+6 \\
cb^2-6 \\ \\
c(3)+6=c(3)^2-6 \\
3c+6=9c-6 \\
6+6=9c-3c \\
12=6c \\
\frac{12}{6} =c \\
2=c
\end{align}$$
- E.g. Give the interval(s) where $h(k)= \sqrt{ 5-k }+\sqrt{ k+4 }$ is continuous
	$\sqrt{ 5-k }$ where $k\neq{5}$ because can't take sqrt $\leq{0}$
	$\sqrt{ k+4 }$ where $k\neq{-4}$ because can't take sqrt $\leq{0}$
	Therefore $(-4, 5)$
	
- Discontinuity types:
	- Jump: limit from the left and right exist but aren't equal
	- Infinite: at least one-sided limit is infinite
	- Removable: limit exists but isn't equal to the function
		- I.e. undefined at that x-value 
- E.g. ![[Pasted image 20240919120700.png]]
- E.g. ![[Pasted image 20240914021544.png]]
	- $\lim_{ x \to 4^+ }=-\infty$:
		- infinite (goes to infinity so can't continue here)
	- x=2: 
		- removable (just doesn't equal function at point)
		- x approaches 3 from both sides but function defined at that point is y=4
	- x=3 
		- jump (doesn't exist so can't equal it there)
		- redefined function at that point by setting $f(3)=3$
	- x=4 
		- limit does not exist here, so function is discontinuous here
			
- **Rules**
	- **When limit does not exist** 
		- Right-hand and left-hand limits differ or only one exist
			- E.g.
			  ![[Pasted image 20240913210032.png]]
				- $\lim_{ x \to 1^- }=2$
					- Approaches $y=2$
				- $\lim_{ x \to 1^+ }=-2$
					- Gets close to $y= -2$
				-  $\lim_{ x \to 1}=$ does not exist
					- Right and left limits differ
				
		- The graph oscillates
			- E.g. $\sin(x)$
			
- **Limits at an x-value**
	- **For continuous functions** 
		- Power functions, polynomials, etc 
		- You can compute limits by substituting in x-value, i.e. $\lim_{ x \to a }$ $f(a)$
		- E.g. $\lim_{ x \to 5 }$ $(x^{3}-x)$
				$= ((5)^{2}- 5)$
				$= 120$
	- **For non-continuous functions** 
		- We must do more to calculate the limit
		- Composite Functions
			- Addition
				- $\lim_{ x \to a } (f(x) + g(x)) = F + G$
				- Limit is sum of the limits
			- Subtraction
				- $\lim_{ x \to a } (f(x) - g(x)) = F - G$
				- Limit is difference of the limits
			- Multiplication
				- $\lim_{ x \to a } (f(x) * g(x)) = F * G$
				- Limit is product of the limits
			- Division
				- $\lim_{ x \to a } (f(x)/g(x)) = \frac{F}{G}$
				- Limit is the division of the limits as long as g(x)'s limit is not 0
		- E.g. $\lim_{ x \to 2 } \frac{x-2}{x^{2}+x-6}$?
				$= \lim_{ x \to 2 } \frac{2-2}{(2)^{2}+2-6}$
				$=\frac{0}{0}$
				$=DNE$ (indeterminate form)
			- Means we know nothing about the limit without doing more work by transforming function
				- Can factor function
					$\lim_{ x \to 2 } \frac{x-2}{(x+3)(x-2)}$
					$\lim_{ x \to 2 } \frac{1}{x+3}$
				- Then evaluate limit approaching $x=2$
					$\lim_{ x \to 2 } \frac{1}{2+3}$
					$\lim_{ x \to 2 } \frac{1}{5}$ 
			- Therefore:
				- $\frac{1}{x+3}$ --> $x = \frac{1}{5}$
				- undefined --> $x \neq 2$
				- As x approaches 2, limit is $\frac{1}{5}$
				
	- **Limits at infinity (Horizontal Asymptotes)**
		- Try to work out what is the biggest term in the numerator and denominator and use them
		- E.g. $\lim_{ x \to \infty } = \frac{7x^3+8x^2+9x+10}{2x^3+3x^2+4x^4+5}$?
			 - Small x-values: graph behaves like smallest power value $\frac{10}{5}$
			 - At large x-values: graph behaves like largest power value, so in this case limit as x approaches infinity.. 
				 $=\\lim_{ x \to \infty }\frac{7x^3}{4x^4}$
				 $=\\lim_{ x \to \infty }\frac{7}{4}*\frac{1}{x}$
				 $=\\lim_{ x \to \infty }0$ therefore approaches but never reaches $y=0$
		 - E.g. $\\lim_{ x \to -\infty }\frac{\sqrt{ 4x^2+1}}{5x-1}$
			 - Pull out largest factors, we get numerator: $5x$ and denominator: $\sqrt{ 4x^{2 }}= 2x$
			 - However, since we're taking $\lim_{ x -\to \infty }$, $2x$ becomes $|x|=-x$, therefore..
				 $\lim_{ x \to -\infty} \frac{-2x}{5}$
	- **Familiar functions**
		- Have limits we can see based on the appearance of a graph

- **Piece-wise function**
	- Function defined by several pieces rather than a single formula 
	- We evaluation function at a particular value of x on a case-by-case basis 
		![[Pasted image 20240912191538.png]]
		- Filled circle: at point (x, y), the function takes on the value $f(x) = y$ meaning at point (3, 9) --> $f(3) = 9$
		- Empty circle (hole): not on the graph of $y = f(x)$ meaning at point (3, 6) --> $f(3) \neq 6$
		- As we move closer to $x=3$ from the right and left, function moves closer and closer to $y=6$ but doesn't reach it because there's an asymptote 
			- ![[Pasted image 20240912193303.png]]
		- Thus we can say $\lim_{ x \to 3 } f(x) = 6$
			- However $f(3)=9$
			
	- E.g. ![[Pasted image 20240919093159.png]]
$$\begin{align}
f(-2)=11 \\
f(-1)= 11 \\
f(0)=10 \\ 
 \\
f(8)=2\\
f(9)=1 \\ 
f(10)=27.2 \\
\end{align}$$
		$\lim_{ x \to -1^- }=11$
		- $x<-1=11$
		$\lim_{ x \to -1^+ }=11$
		- $-1\leq x<9=-x+10 \to -(-1)+10=11$
		$\lim_{ x \to -1 }=11$
		$\lim_{ x \to 9^- }=1$
		- $-x+10 \to -(9)+10=1$
		$\lim_{ x \to 9^+ }=10$
		- $10e^{x-9} \to 10e^{9-9} =10$
		$\lim_{ x \to 9 }=DNE$
			
				
- E.g. Consider $\frac{x-1}{x+3}$
	- What is $\lim_{ x \to \infty }f(x)$?
		- Large positive x-value:
			$=\\lim_{ x \to \infty }\frac{x}{x}$
			$=\lim_{ x \to \infty }1$
	- What is $\lim_{ x \to -\infty }f(x)$?
		- Left-hand limit
		- Large negative x-value
			$=\\lim_{ x \to -\infty }\frac{x}{x}$
			$=\lim_{ x \to -\infty }1$
	- What is $\lim_{ x \to -3^+}f(x)$? 
		- Right-hand limit
		- Approaching from right so we know x is close to -3 but a bit bigger, so can evaluate at x=-2.9 to determine limit 
		  ![[Pasted image 20240913132213.png]]
			$=\frac{-2.9-1}{-2.9+3}$
			$=\frac{-3.9}{0.1}$
			$=-3$ 
			- Therefore approaching $-\infty$
			$=\lim_{ x \to -3^+}-\infty$
	- What is $\lim_{ x \to -3^-}f(x)$: 
		- Approaching from left so we know x is close to -3 but a bit smaller, so can evaluate at x=-3.1 to determine limit 
			$=\frac{-3.1-1}{-3.1+3}$
			$=\frac{-4.1}{-0.1}$
			$=4.1$ 
			- Therefore x approaching $\infty$
			$=\lim_{ x \to -3^-}\infty$
### Asymptotes
- **Rules**
	- Can have infinite number of vertical asymptotes (e.g. tan(x)) but only 0-2 horizontal asymptotes
	 - Functions can cross their horizontal asymptote 
		 - E.g. $y=(e^x)(\sin x)$)![[Pasted image 20240914003131.png]]
- Horizontal asymptotes
	- Similar to looking at $\lim_{ x \to \infty }$
	- Look at largest numerator and denominator and cancel out common factors
		- If either is a rational number, take + or -
			- E.g. $\frac{x-5}{(\sqrt{ 4x^{2+3x+2 })}}$
				- Unable to factor expression
				$\frac{x}{\sqrt{ 4x^{2 }}}$
				$=\frac{x}{\pm(2x)}$
				$=\pm\frac{{1}}{2}$
	- E.g. $\frac{x^2-12x-15}{13-13x}$
		- Dominating factor
			$\frac{x^2}{-13x}$
		- Cancelling out common factors
			$\frac{x}{-13}$
		- Simplify
			$\frac{1}{-13}$
			
	- E.g. $\frac{3x^4}{1+x^{4}}$
		- Dominating factors
			$=\frac{3x^4}{x^4}$
		- Cancelling out common factors
			$=3$
		![[Pasted image 20240914001832.png]]
- Vertical asymptotes
	- Required conditions:
		- Two sided limit with at least 1 side approaching $+\infty$ or $-\infty$
			- $lim_{ x \to a }=\infty$ or $\lim_{ x \to a }=-\infty$
	- Symmetrical
		- E.g. $y=\frac{1}{x^2}$ which has limit of $+\infty$ as x approaches 0 from both sides
		  ![[Pasted image 20240914004423.png]]
	- Asymmetrical
		- E.g. $y=log(x)$
		
- E.g. ![[Pasted image 20240919105411.png]]
- E.g. Consider $y=e^{\frac{1}{x}}$ 
	- Vertical asymptotes:
		- We can look first at what happens to $\frac{1}{x}$ as x approaches 0
			- Approaching from the right
			  $lim_{ x \to 0^+} \frac{1}{x}=+\infty$ 
				- Thus $e^{\frac{1}{x}}$ --> $e^{+\infty} = \infty$
				- Because as x-value becomes very large and positive, $e^x$ grows very quickly 
			- Approaching from the left 
			  $lim_{ x \to 0^-} \frac{1}{x}=0$ 
				- Thus $e^{\frac{1}{x}}$ --> $e^{-\infty} = 0$
				- Because as x-value becomes very large and negative, $e^x$ very approaches 0
		- Because $e^\frac{1}{x}$ does not approach $\pm \infty$ as x approaches 0, we don't have vertical asymptotes
	- Horizontal asymptotes:
		- We can look first at what happens to $\frac{1}{x}$ as x approaches $\pm \infty$
			- Approaching from the right
			  $lim_{ x \to \infty^+} \frac{1}{x}=0$ 
				- When x-value becomes very large and positive, $\frac{1}{x}$ quickly approaches 0
				- Thus $e^{\frac{1}{x}}$ --> $e^{0} = 1$
			- Approaching from the left 
			  $lim_{ x \to \infty^-} \frac{1}{x}=0$ 
				-  When x-value becomes very large and negative, $\frac{1}{x}$ quickly approaches 0
				- Thus $e^{\frac{1}{x}}$ --> $e^{0} = 1$
		- Because $e^\frac{1}{x}$ approaches $\pm \infty$ as x approach 1, we have a horizontal asymptote at $y=1$

    
- ![[Pasted image 20240913134625.png]]
	- If $x\neq{2}$: no continuities as denominator would be 0
	- At $x=2$: should check for continuity by seeing if $f(x)=k$
		- If we plug it in as it, we would get 0/0
		- Factor first
			$=\frac{x^3-2x^2}{x-2}$
			$=\frac{x^2(x-2)}{x-2}$
			$=x^2$
		- Plugging in $x=2$
			$=(2)^2$
			$=4$
		- Therefore at $x=2$, k needs to equal 4 at $x=2$, so we add a point there
- Slopes:
	- E.g. At time t=3s, she reaches point x=1cm. At t=5s, she reaches x=5cm
		- Slope (speed) using points (3, 1) and (5, 5):
			- $\frac{5-1}{(5-3)}=2cm/s$
		- Using slope intercept formula ($y=mx+b$), we solve for b (displacement) 
			- $(y_{2}-y_{1}=m(x_{2}-x_{1})+b)$
			- Where slope $(m) = 2cm/s$, at $point (3, 1)$
				$x_{2}-x_{1} = m(t_{2}-t_{1})$
				$x_{2}-1 = 2(t_{2}-3)$
				$x=2t-5$

$$*\begin{align}
(x^2)
\end{align}$$


(x+2)(x+4) / x(x+8)(x+2) -> (x+4)/(x)(x+8)