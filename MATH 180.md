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
- Finding the range a function
	- E.g. $y=\frac{1}{1+e^{ax+b}}$
		- We can simplify this by looking at what would happen if we use a large and small x-value
			- Using an arbitrarily large x-value:
				- $\frac{1}{1+e^{10000}}$ for example, will mean we have a large denominator, so our y-value will be very small, approaching 0 (horizontal asymptote)
			- Using an arbitrarily small x-value:
				- $\frac{1}{1+e^{0000.1}}$ for example, will mean we have a small denominator, so our y-value will approach 1 (horizontal asymptote)
		- If we use a large a value, our curve will just be steeper ![[Pasted image 20240919191408.png]]
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
- E.g. Consider $y = e^{x}- x$
	- At $x = 0$: $e^{x} = e^0 = 1$ 
	- Larger negative x-value: $-x$ dominates at a relatively steep curve
	- Large positive x-value: $e^x$ dominates at a relatively steep curve
	- ![[Pasted image 20240912174102.png]]
	
		             
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
- $\lim_{x \to a} f(x) = L$
	- It is the y-value that is approached as a given x-value from both the right and left side (aka a two-sided limit)
	- If you have a discontinuity (e.g. hole [undefined], jump, etc) at that given x-value
		- The function will be considered not continuous there 
		- You won't have a limit there 
	- $\lim_{x \to a+}$: approaching given x-value from right 
		- Can tell us if there is a vertical asymptote or hole (removeable discontinuity) at given x-value
	- $\lim_{x \to a-}$: approaching given x-value from left 
		-  Can tell us if there is a vertical asymptote or hole (removeable discontinuity) at given x-value
	- $\lim_{x \to +\infty}$: approaching arbitrarily large and positive x-value
		- Can tell us if there is a horizontal asymptote and its location
	- $\lim_{x \to -\infty}$: approaching arbitrarily large and negative x-value
		- Can tell us if there is a horizontal asymptote and its location
	- E.g. Evaluate the limit $\lim_{ x \to -6 } \frac{\frac{\frac{1}{6}+1}{x}}{6+x}$ 
		- We can simplify this by putting fraction over 1, so that we can multiply both fractions together 
			$=\frac{\frac{\frac{\frac{1}{6}+1}{x}}{6+x}}{1}$
			$=(\frac{1}{6}+\frac{1}{x}) (\frac{1}{6+x})$ 
		- Add fractions on left (get same base then add numerators)
			$=(\frac{x}{6x}+\frac{6}{6x}) (\frac{1}{6+x})$ 
			$=(\frac{6+x}{6x}) (\frac{1}{6+x})$ 
		- Cancel out common terms 
			$=(\frac{1}{6x})(1)$
		- Simplify 
			$=\frac{1}{6x}$
		- Substitute in given x-value
			$=\frac{1}{6(-6)}$
			$=-\frac{1}{36}$ is our limit at x= -6
			
### When limit does not exist 
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
		
### Continuity
- Continuous function: a graph that has no breaks in the shape of a graph, meaning you could draw a whole function without lifting your pencil
	- All piece-wise functions are not "continuous over their domain" meaning there's a discontinuity somewhere 
	- You can have functions not defined at a point or discontinued at a point, but it's still technically "continuous over their domain" 
- Conditions for $f(x)$ to be continuous at a point 
	- $f(a)$ is defined
	- $\lim_{ x \to a }f(x)$ exists
	- $\lim_{ x \to a }f(x)=f(a)$ 
	
- Discontinuity types:
	- Jump: limit from the left and right exist but aren't equal
	- Infinite: at least one-sided limit is infinite
	- Removable (hole): limit exists but isn't equal to the function
		- I.e. undefined at that x-value 
		- E.g. $\frac{x+7}{x^{2}-49}$ isn't defined at x= -7 because denominator would be 0
	- E.g.
	   ![[Pasted image 20240914021544.png]]
		- Infinite ($\lim_{ x \to 4^+ }=-\infty$) approaching $x=4$: goes to infinity as its a vertical asymptote
			- However, we have a value at $x=4$ as $f(4)=0$ here
		- Removable at $x=2$: approaches $y=3$ from both sides but function is not defined at $x=2$ (hole)
		- Jump at $x=3$: different limit approaching from right and left 

- E.g. Give the interval(s) where $h(k)= \sqrt{ 5-k }+\sqrt{ k+4 }$ is continuous
	$\sqrt{ 5-k }$ where $k\neq{5}$ because can't take sqrt $\leq{0}$
	$\sqrt{ k+4 }$ where $k\neq{-4}$ because can't take sqrt $\leq{0}$
	Therefore $(-4, 5)$
	
- E.g. Evaluate the limits ![[Pasted image 20240920091513.png|200]]
	- $\lim_{ x \to -1^+ }$
		- Using $3x^{2}+5m$, plug in x-value to determine right limit 
			$=3(-1)^{2}+5m$
			$=3+5m$
	- $\lim_{ x \to -1^{-}}$
		- Using $7x^3-2m$
			$=7(-1)^{3}-2m$
			$=-7-2m$
	- Therefore limit doesn't exist and there's a discontinuity at $x=-1$. To make function continuous there, we can solve for m
		$5m+3=-2m-7$
		$5m+2m=-7-3$
		$7m=-10$
		$m=\frac{-10}{7}$ 
		
- E.g. Make $f(x)$ continuous by determining value(s) that make $f$ continuous at $x=-4$
   ![[Pasted image 20240920092426.png|200]]
	- Determine limit approaching from left using $b-2x$
		  $=b-2(-4)$
		  $=b+8$
	  - Determine limit approaching from right using $-\frac{96}{x-b}$
		  $=-\frac{96}{-4-b}$
		  $=\frac{96}{4+b}$
	- To find point of intersection between 2 pieces of the function, we can use an equality statement to then create a composite function and determine roots where y=0
			$b+8= \frac{96}{4+b}$
		- Simplify
			$(b+8)(4+b)=96$
			$4b+b^2+32+8b=96$
			$4b+b^2+32+8b-96=0$
			$b^2+12b-64=0$
		- Factor
			$(b+16)(b-4)=0$
		- Therefore since there are 2 roots, b= -16, 4
			
				
- **Limits at an x-value**
	- **For simple functions** 
		- Power functions, polynomials, etc 
		- You can compute limits by substituting in x-value, i.e. $\lim_{ x \to a }$ $f(a)$
		- E.g. $\lim_{ x \to 5 }$ $(x^{3}-x)$
				$= ((5)^{2}- 5)$
				$= 120$
	- **For complex functions** 
		- We must do more to calculate the limit
		- Composite Functions
			- If one or both functions don't have a limit (two-sided limit) at given x-value, then the composite function won't have a limit at the given x-value
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
		 - E.g. $y=(e^x)(\sin x)$
		   ![[Pasted image 20240914003131.png|200]]
- Horizontal asymptotes
	- Similar to looking at $\lim_{ x \to \infty }$ is finding horizontal asymptotes
	- Holes (removable discontinuity): can be factored out of function, left with horizontal asymptotes
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
		![[Pasted image 20240914001832.png|200]]
- Vertical asymptotes
	- Limits at points looks for removeable discontinuities and vertical asymptotes
	- Required conditions:
		- Two sided limit with at least 1 side approaching $+\infty$ or $-\infty$
			- $lim_{ x \to a }=\infty$ or $\lim_{ x \to a }=-\infty$
	- Symmetrical
		- E.g. $y=\frac{1}{x^2}$ which has limit of $+\infty$ as x approaches 0 from both sides
		  ![[Pasted image 20240914004423.png|200]]
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

    
### Lines and slopes (Linear Functions)
- Point: $(x, y)$
- Slopes:
	- Steepness of curve
	- m=0: indicates flat line
	- + increases right and - increases left
	- Calculated with $\frac{\nabla rise}{\nabla run}$

- Slope-intercept form 
	- Written as $y=mx+b$
		- y: f(x) output, $y$-value
		- $m$: slope
		- $x$: point on a line
		- $b$: displacement 
- Point-slope form 
	- A line passing through a point with a slope
	- Written as $y_{1}-y_{0}=m(x_{1}-x_{0})+b$
		- $y_{1}$ and $y_{0}$: $f(x)$ output
		- $m$: slope
		- $x_{1}$ and $x_{0}$: distinct points on the line
		- $b$: displacement 
	- E.g. Write the point-slope form of a linear function with slope of 3, which passes through (1, -3)
		- $y-(-3) = 3(x-1)$

- E.g. At time t=3s, she reaches point x=1cm
     At t=5s, she reaches x=5cm
	- Slope (speed) using points (3, 1) and (5, 5):
		- $\frac{5-1}{(5-3)}=2cm/s$
	- Using slope intercept formula ($y=mx+b$), we solve for b (displacement) 
		- $(y_{2}-y_{1}=m(x_{2}-x_{1})+b)$
		- Where slope $(m) = 2cm/s$, at $point (3, 1)$
			$x_{2}-x_{1} = m(t_{2}-t_{1})$
			$x_{2}-1 = 2(t_{2}-3)$
			$x=2t-5$
- Finding slope through re-arranging formula
	- E.g. $2y-x=9x+1$
		$y=\frac{1}{2}(10x)+\frac{1}{2}$
	- E.g. $9(y+1x)=5-8x$
		- Distribute 9 on left and re-arrange right 
			$9y+9x=-8x+5$
		- Move y-affecting variables to right 
			$y+9x=\frac{1}{9}(-8x)+\frac{5}{9}$
		- Move x-affecting variables to right 
			$y=\frac{1}{9}(-8x-9x)+\frac{5}{9}$
			$y=\frac{1}{9}(-17x)+\frac{5}{9}$
		- Slope is $m=-\frac{17}{9}$

### Derivatives
- If y-intercept of f(x) is unknown, we can draw a line which intersects 2 points on the curve, this gives us our secant line 
- Derivative is a visual line of instantaneous slope at given x-value of f(x)
- Curve at a point in a line that intersects the curve at that point and whose slope captures the instantaneous rate of change
	- Formula for secant line: $f'(x)= \frac{f(x+h)-f(x)}{h}$
		- Where $f(x+h)$ gives us the secant offset
		- Subtracting $f(x)$ removes the original function 
		- Dividing by $h$ cancels out the change 
	- Taking the limit at the secant line gives us the tangent line 
		- Represents our instantaneous rate of change of f(x)
		- Formula for tangent line: $f'(x)= \lim_{ h \to 0 }\frac{f(x+h)-f(x)}{h}$
- From this, we can find: 
	- At $m=0$ --> $x=0$
	- When slope of f(x) is negative, then tangent line is negative 
	- When slope of f(x) is positive, then tangent line is positive 
- E.g. $f(x)= 4x^{2}+ 3x + 11$
$$\begin{align}
\text{Setting up to find secant line} \\
f'(x)= \frac{(4(x+h)^{2}+3(x+h)+11)-(4x^{2}+3x+11)}{h} \\
f'(x)= \frac{4(x+h)(x+h)+3x+3h+11-(4x^{2}+3x+11)}{h} \\
f'(x)= \frac{4(x^{2}+ 2xh + h^{2}+3x+3h+11)-(4x^{2}+3x+11)}{h} \\
f'(x)= \frac{4x^{2}+ 8xh + 4h^{2}+3x+3h+11-4x^{2}+3x+11}{h} \\
f'(x)= \frac{4x^{2}+ 4h^{2}+ 8xh + 3h}{h} \\
f'(x)=4h+8x+3 \\
\text{Finding tangent line by subbing h=0} \\\
\lim_{ h \to 0 } f'(x) = 4(0)+8+3 \\
\lim_{ h \to 0 } f'(x) = 8x+3  \\ \\

\text{Now is we take any x-value, we can find our y-value} \\
\text{(e.g. x=4 so y=35)}
\end{align}$$
- E.g. Find the derivative at $f(x)=\frac{4}{x}$ using complex fraction rules
$$\begin{align}
\text{Finding slope of the tangent line} \\
\lim_{ h \to 0 }= \frac{\frac{4}{x+h}-\frac{4}{x}}{h} \\
\text{Get a common base} \\
\lim_{ h \to 0 }= \frac{\frac{4(x)}{x(x+h)}-\frac{4(x+h)}{x(x+h)}}{h} \\
\text{Combine fractions} \\
\lim_{ h \to 0 }= \frac{\frac{4x-4(x+h)}{x(x+h)}}{h}  \\
\text{Expand} \\
\lim_{ h \to 0 }= \frac{\frac{4x-4x-4h}{x(x+h)}}{h} \\
\text{Simplify} \\
\lim_{ h \to 0 }= \frac{\frac{-4h}{x(x+h)}}{h}  \\
\text{Apply fraction rule} \frac{\frac{a}{b}}{c}=\frac{a}{b*c} \\
\lim_{ h \to 0 }= \frac{-4h}{(x(x+h))(h)} \\
\text{Simplify} \\
\lim_{ h \to 0 }= \frac{-4}{x(x+h)}  \\
\text{Take lim h approaching 0 to get tangent line} slope\\
\lim_{ h \to 0 }= \frac{-4}{x(x+0)} \\
\lim_{ h \to 0 }= \frac{-4}{x(x)} \\
\lim_{ h \to 0 }= \frac{-4}{x^2} \\
\text{Slope of tangent line (derivative) is} f'(x)=\frac{-4}{x^{2}}  \\
 \\
\text{Finding output of tangent line at } x=6 \\
f'(6)= \frac{-4}{36} \to \frac{-2}{18} \to \frac{-1}{9}  \\
\text{Now have a point at } (6, \frac{-1}{9}) \\
 \\
\text{Equation of tangent line at x=6} \\
\text{Using point-slope formula} y-y_{1}=m(x-x_{1}) \\
y-\frac{-1}{9}=\frac{-4}{x^{2}}(x-6) \\
\text{Simplify} \\
y- 
\end{align}$$
!!!
- Function is differentiable at $x=a$ if $f'(a)$ exists
	- Functions can be defined but not differentiable at a given x-value
- When $f'(x)$ cannot be found (differentiable):
	- Won't be differentiable approaching a vertical asymptote 
	- Can't take tangent line (slope) of vertical line 
		- $f'(x) \to \infty$ so DNE
	- If point is sharp, we can't take slope there (slope of function on one side differs from slope on other side)
		- $f'(x) DNE$
	- If point is at a discontinuations (e.g. jump where limit doesn't exist), we can't take slope there ![[Pasted image 20240920135101.png|100]]

- E.g. ![[Pasted image 20240920123744.png]]
	- h= distance between 2 points on secant line 
	- Basically bring h closer and closer to x=0 so that slope of secant line equals slope of tangent line 
	- We can do that by evaluating f(x) at x=1 ![[Pasted image 20240920124343.png]]
	- Can't use y=mx+b because we don't know y-intercept
		- But point-slope form is more useful in most cases because we don't always know this
		  $slope= \frac{y_{1}-y_{0}}{x_{1}-x_{0}}$

### Approximating derivative
- E.g. 
	- Find the derivative of $\sin(x)$ when $x=0$
		- Given: tangent line to $y=\sin(x)$ at origin is $y=x$, is: $x=0$ and $y=0$
			$y=f(a) + f'(a)(x-a)$
			$y=f(0) + f'(0)(x-0)$
			$y=f'(0)x$
		- Therefore tangent line is $y=x$, then $f'(0)=1$
	- Find linear approximation of $\sin(0.001)$
		- Near $x=0$, $\sin(x)= x$ (close enough)
			- $\sin(0.001)$ approximately $\sin(0.00)$

### Easier ways to find slope
- Power rule:
	- If $f(x)= ax^b$ then $f'(x)=abx^{b-1}$
	- E.g. $f(x)= 4x^{2}+ 3x + 11$ 
	$$\begin{align} 
\text{First term} \\
&=(4)(x)^2 \\
&=(4)(2)(x)^{2-1} &\\
&=8x \\
\text{Second term} \\
&=(3)(1)(x)^1 \\
&=(3)(1)(x)^{1-1} \\
&=3 \\
\text{Third term, a constant, cancelled out}  \\
\text{as vertical displacement doesn't matter to find slope} \\
&=(11)(0)(x)^{0-1} \\
&=0 \\ \\
\text{Therefore} f'(x)=8x+3
\end{align}$$
- Product rule:
	- If $(f(x))(g(x))$ --> $(f)(g')+(f')(g)$
- Quotient rule:
	- If $\frac{f(x)}{g(x)}$ --> $\frac{(g(x))(f'(x))-(f(x))(g(x))}{g(x)^{2}}$
	- E.g. 
	   ![[Pasted image 20240925183006.png|400]]
- Chain rule:
	- To reduce taking derivative of parentheses contents
	- If $f(x)=(a)(f(x))^b$ --> $f'(x)=(a)(b)(f(x))^{b-1}(f'(x))$
	- E.g. $f(x)=\frac{(x^{2}+12x-5)^2}{3x^{2}-6x+2}$
	$$\begin{align} \\
\text{Finding f'(x) inner parentheses using } f'=(a)(b)(x)^{b-1} \\
f'&= (1)(2)(x)^{2-1} \\
&=2x \\ \\
f'&=(12)(1)(x)^{1-1} \\
f'&=12 \\
\text{Therefore} f'=2x+12 \\ \\
\text{Finding f'(x) in its entirity} \\
f'(x)&=(a)(f(x))^{b-1}(f'(x)) \\
&=(1)(2)(x^{2}+12x-5)^{2-1}(2x+12) \\
&=(2x^2+24x-10)(2x+12) \\
&=4x^{3}+24x^2+48x^2+288x-20x-120 \\
&=4x^3+72x^2+268x-120
\end{align}$$


### Exponent rules
- Power of a power property
	-  $(a^{b})(a^{c)}= a^{b+c}$
	- This property states that when multiplying two powers with the same base, we add the exponents
	- Can raise any element in an expression to the power of 1 and not change the expression
	- E.g. $(49^{x-1})(7^{2x-3})$
		 $= ([7^2]^{x-1})(7^{2x-3})$  
		 $= (7^{2x-2})(7^{2x-3})$  
		 $= 7^{4x-5}$
- Quotient of powers property
	- $\frac{a^{b}}{(a^{c)}}= a^{b-c}$
	- This property states that when dividing two powers with the same base, we subtract the exponents.
	- E.g. $5^6 / 5^2 = 54$
- Rational exponent property 
	- E.g. $5^{\frac{6}{2}} = (^2\sqrt{ 5 })^6$
- Negative exponent property
	- A number with a negative exponent should be put to the denominator, and vice versa
	- Taking the reciprocal of the equation 
		- E.g. $P(t) = Po(7)^{\frac{t}{5}}$
						  $= Po(5\sqrt{7})^t$
						  $= Po(7^{\frac{1}{5}})^t$   
						  $= Po(1.48)$
- No rule for $a^{b}+a^c$
- E.g. ${\lim_{h\to 0 }}= b^x+h$ 
	${\lim_{h\to 0 }}= (b^x)(b^h)$
	${\lim_{h\to 0 }}= b^x(\frac{b^h-1}{h})$
	- Simplify to $b^{x}\lim_{h\to 0 }= \frac{b^{h}-1}{h}$

Differential equation: 
- Given derivative equation f'(x) and asked to solve for f(x)
- Derivative function should be the same as f(x)
- E.g. $y'(x)=y(x)$ --> $(e^{x})'=e^x$
	- Rate of change people getting sick $f'(x)$ depends on how many people are sick $f(x)$
- E.g. $y-e^x=0$
		$y=e^x$

### Relationship between function and derivative graphs
- If the slope of f(x) is negative, then the graph of f’(x) will be below the x-axis
- If the slope of f(x) is positive, then the graph of f’(x) will be above the x-axis
- All extremes of f(x) will become x-intercepts of f’(x) ![[Pasted image 20240926092639.png]]