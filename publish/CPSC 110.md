- Submit starter before 10pm on day of lecture via:
- Handin (after replacing CWL ??? with username) 
- Check results through Handback url  
Problem set done at end of each module 
- Use look-up function to determine what function is and/or the syntax of the function you want to write
- BSL needs BEDMAS and/or order of operations specified
	- E.g.  4 * 3 ^ 2 - 5 should be written as: (- (* 4 (sqr 3)) 5)

**Racket** 
- Divided into 2 regions ![[Pasted image 20240905205151.png]]
- Commenting out done via ;; or #;
- Stepper: shows evaluations steo-by-step

**Expressions and values**
- To form an expression: < primitive >< expression >
- E.g. ![[Pasted image 20240906144638.png]]
	- "+2" is a primitive operator because it starts with a parentheses followed by an operator
	- "* 3 4" is an expression
		- "3" and "4" are operands which will be multiplied together to produce a value of "12"
	- Steps of operation, as it works inside to outside, right to left: ![[Pasted image 20240906145209.png]]
- Examples of expressions
	- (sqrt 2)
	- 1
	- "#i1.41421"
		- "#i" means inexact digit, e.g. approximate 
	- (+ 3 4) 
		; Adds 3 and 4
		; Expression = (+ 3 4) and the value it evaluates to = 7
- Examples of values
	- 1
	- "#i1.41421"
- E.g. Which of these expressions produces the average of the numbers 4, 6.2 and -12?
	- (/ (+ -8 6.2) 3)
	- (/ (+ 4 6.2 -12) 3)
	- -0.6

**Evaluating simple arrhythmic expressions**
- Includes +, -, /, sqr (square of a number), sqrt (square root of a number)
- Doesn't follow BEDMAS rules automatically 
	E.g. `(+ 1(* 3 2))`
		; Write this way so that it evaluates inner parentheses operations first and creates value to use as argument for outer expression

**Strings**
- String is an alphanumeric word or phrase, within quotations
	- E.g. "apple"
	- E.g. "1 2 3"
- String-append
	- E.g. `(string-append "Ada" " " "Love")`
		; Strings = "Ada", " ", and "Love"
- String-length
	- Gives us number of characters in a string
	- E.g. `(string-length "apple")`
- Substring 
	- Removes characters indicated based on their index position 
	- Uses 0-based indexing
	- E.g. `(substring "Caribou" 2 4)`
		- Where: 2 = a & 4 = i
			C a r  i  b o u
			0 1 2 3 4 5 6
		- Telling it to start at character 2 and go up to but not including character 4 
		- Output will be "ri"
	- E.g. `(substring "Caribou" 0 3)`
		- Output will be "Car"

**Images**
- Need to include (require 2htdp/image) at the beginning of the program
- Includes the following:
	- Circle `(circle radius "mode" "color")`
		- Takes 3 arguments: size (e.g. radius, side length, or width and height), mode (e.g. outline or solid), and colour
		- Passes arguments into the primitive "circle"
		- E.g. 
			`(above (circle 40 "solid" "red")`         
		         `(circle 40 "solid" "yellow")`
			     `(circle 40 "solid" "green"))`
	- Square `(square side-length "mode" "color")`
	- Rectangle `(circle length width "mode" "color")`
	- Text ("text")
- Image append
	- Acts as a string-append but for images
	- Includes:
		- Above stacks vertically 
		- Beside stacks horizontally 
		- Overlay stacks on top of one another 
- Rotate 
	- Arguments to include are degrees
- Images are values and all values are expressions, so we could add an image directly into the environment when using Racket
	- E.g. (define CAT ![[Pasted image 20240906160434.png]])
		`(define CAT <image>)`
		`(define RCAT (rotate -10 CAT))`
		`(define LCAT (rotate 10 CAT))`

**Constants**
- We can name constants that can be called into expressions
	- ![[Pasted image 20240906155916.png]]
	- E.g. `(define width 400)`
		 `(define height 600)`
			; Constants are width and height
			
		 `(* width height)`
			- Expression calling both constants

**Primitives**
- Primitive: built-in Racket language function 
- htdp beginner documentation, for example, in Help Desk Index can help us find primitives
	- https://docs.racket-lang.org/
- E.g. `(round (/ 3 4))`

**Functions**
- Function: one you've built yourself
- To form a function: ![[Pasted image 20240908111144.png]]
- E.g. `(define (trafficlight c)`
		  `(circle 40 "solid" c))`
			  ; Defining the function, where "trafficlight" is the function
			  ; Body of the function: "(circle 40 "solid" c)
				  ; "circle" is a primitive function
				  ; "40", "solid", "c" are operands/values
				  ; "c" is a parameter waiting to be replaced by an argument
			  ; Variable value (parameter): c (colour)
- To call a function: ![[Pasted image 20240908111300.png]]
- E.g. trafficlight
	`(define (trafficlight c)`
	  `(circle 40 "solid" c))`
	  ; Defining the function
	
	`(above (trafficlight "red")`
		   `(trafficlight "yellow")`
		   `(trafficlight "green"))`
		   ; Calling the function 
		   ; Using a "function call expression"
		   
- E.g. trafficlight 2
	`(define (trafficlight c)`
		`(circle 40 "solid" c))`
		; Defining the function
		  
	`(trafficlight (string-append "re" "d"))`
		; First tries to evaluate the function call (trafficlight()) but needs to evaluate primitive call before this
		; Evaluates the primitive call by educing the operand "(string-append "re" "d")"" to a value/argument "red"
			`(trafficlight "red")`
		; Now the function call sees the argument, it replaces parameter "c" with this argument "red" in the body of the function 
			`(circle 40 "solid" "red")
		; Function call is now gone as we're no longer calling "trafficlight" and we're just evaluating a primitive call where "circle" is the primitive and "40", "solid", and "red" are operands but because they are already values, just need to apply primitive to those values 
				![[Pasted image 20240908115724.png]]

**Booleans**		
- Predicates are primitives or functions that produce a boolean value 
- True and false
- Includes:
	- =
	- > and <
	- = > and < =
	- string=?
- E.g. `(define width 100)`
	 `(define height 100)`

	 `(> width height)`
	 ; Assesses whether width is larger than height, in this case, returns "false"
	 ; Where ">" is a primitive 
- E.g. `(require 2htdp/image)`

		`(define img1 (rectangle 10 20 "solid" "red"))`
		`(define img2 (rectangle 40 20 "solid" "red"))`

		`(< (image-width img1)(image-width img2))`
	 ; Returns value of true
	 
**If Statements**
- Primitives:
	- AND - short circuits and stops evaluating if false statement found
	- OR - only compares first 2 predicates, e.g. `(if (or (< 2 1)(> 3 2)) #true #false)`
	- NOT
- Conditions:
	- E.g. Next step in evaluation of 
	  `(cond [(> 8 7) "Charlie"]`
		  `[(= 6 6) "Dog"])`
	  - Would be `(cond [true "Charlie"]
				 `[(= 6 6) "Dog"])`
	- Best practice to present last case with "else" statement

- E.g. 
	`(require 2htdp/image)`

	`(define img1 (rectangle 10 20 "solid" "red"))`
	`(define img2 (rectangle 40 20 "solid" "red"))`

	`(if (< (image-width img1)`
		 `(image-height img1))`
	    `"tall" "wide")`
	; First tries to reduce all of its operands to values 
	; "(image-width img1)" is an expression which needs to be reduced to its value (the actual image)
		`(image-width <picture>)`
	; Then it uses the primitive "image-width" to reduce the operand to a value "20"
		`(if (< 20`
		 `(image-height img1))`
	     `"tall" "wide")`
	; "(image-height img1)" is an expression which needs to be reduced to its value (the actual image)
		`(image-height <picture>)`
	; Then it uses the primitive "image-height" to reduce the operand to a value "10"
		`(if (< 20 10)`
	     `"tall" "wide")`
	; Evaluates predicate and returns value of false as img1's height is more than its width
			`(if false "tall" "wide")`
	; Therefore prints "wide"
- E.g. Nesting conditional primitives into if statements
		`(define LOWER 10)`
		`(define UPPER 20)`

		(define (foo x y)
		  (if (and (> x LOWER) (< x UPPER))
	      (- x (* y 2))
	      (+ x (* y 3))))

		(foo (* 3 4) (+ 0 2))

![[Pasted image 20240912125458.png]]
![[Pasted image 20240912125537.png]]
**HtDF Recipe**
- Breaks down larger problems into small ones but makes easy functions harder to design
- Code coverage:
	- If code is highlighted, indicates we have poor coverag
	- Means code wasn't evaluated, which can tell us that we haven't tested all scenarios
- Recipe:
	1. Signature, purpose and stub
		- Signature: type(s) of data the function consumes and produces 
			- Number (+ and - integers), Natural (0 and + integers) String, Image, Boolean
			- E.g. `(@signature Image Image -> Boolean)`
			- We template on input parameter
		- Purpose: gives description of what the function produces in terms of what it consumes
		- Stub: has correct function name and number of parameters, and produce dummy results of correct type
			- Kind of arbitrary but common variables to add to stub, template, code
				- String: input/output = str, s, "", "abc"
				- Integer: input (n) and output (0, n) 
				- Boolean: output = true, false
			- E.g. `(define (double n) 0)`
				- Where 'n' is the variable for number and '0' is the dummy value type for output integer
	2. Define examples, wrap each in check-expect 
		- Example wrapped in check-expect: illustrate what the function does, also serving as unit tests for the function
				`(check-expect (double 3) 6)`
				`(check-expect (double 4.2) 8.4)`
		- Thorough tests (at least 2) show cases using all types of inputs for bugs, and lets reader know purpose of a function - need to test above, at, and below the boundaries
		- Decide on what to do in weird cases (e.g. if 2 images are same height, output image1)
	3. Template and inventory 
		- Template: body of the template is the outline of the function, will be commented out or deleted later on
				`; (define (double n)
					`(... n))`
	4. Code the function body 
		- Code body: shows why the template makes the function work (stepper)
				`(define (double n)`
					`(* 2 n))`
	5. Test and debug until correct
		-  Test: if running, should indicate that they both passed
- E.g. Design a function, called pleuralize, that converts a word into its pleural form (i.e. adds an 's')
	- Tag
		`(@htdf pleuralize)`
	- Signature
		`(@signature String -> String)`
	- Purpose
		`; Add 's' to end of each word consumed`
	- Stub
		`(define (pluralize str) "")`
	- Check-expects
		`(check-expect (pluralize "cat") "cats")
		`(check-expect (pluralize "dogs") "dogss")`
	- Template
		`(define (pluralize str)
		  `(... str))`
	  - Code
		  `(define (pluralize str)
		  `(string-append str "s"))`
		  
- E.g. Design a function, called image>?, that takes two images and determines whether the first is larger than the second.`
	`(@htdf image>?)                           ;HTDF tag`
	
	`(@signature Image Image -> Boolean)       ;Signature`
	
	`; Produces true if image is larger, otherwise false` 
	
	`;(define (image>? i1 i2) false)           ;Stub - used to test here and now if the function works, comment out later 
	
	`; Check sums: above, at, and below a boundary` 
	`(check-expect (image>?                     ;rectangle vs rectangle i1>i2`
		 `(rectangle 10 30 "solid" "red")`
		 `(rectangle 29 10 "solid" "red")) true)`
	`(check-expect (image>?                     ;rectangle vs rectangle i1<i2`
		 `(rectangle 10 29 "solid" "red")`
		 `(rectangle 30 10 "solid" "red")) false)`
	`(check-expect (image>?                    ;rectangle vs rectangle i1=i2`
		 `(rectangle 10 30 "solid" "red")`
		 `(rectangle 30 10 "solid" "red")) false)`
	`(check-expect (image>?                   ;circle vs circle`
		`(circle 20 "solid" "red")`
		`(circle 19 "solid" "red")) true)`
			
	`(@template-origin Image)                ;Template tag`
		
	`(@template                              ;Template`
		`(define (image>? i1 i2)`
		 `(... i1 i2)))`
		
	`(define (image>? i1 i2)                ;Code`
		`(> (* (image-width i1) (image-height i1))`
		 `(* (image-width i2) (image-height i2))))``

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

**HTDD Recipe**
- Used to create our 
- Includes:
	- Type comment
	- Interpretation
- Data definition:
	- Simple Atomic Data: String, Number, Natural
		- `atomic-non-distinct` : type predicate
			- E.g. `(string=? x)`
		- `atomic-distinct`: equality predicate with guard
			- E.g. `(string=? x "red")`
	- Interval: numbers within a certain range 
		- E.g. 0-100
	- Enumeration: fixed number of distinct items
		- E.g. "H", "P", "F", "T"
		- Doesn't need examples as they would not be helpful to include
	- Itemization: two or more subclasses, at least one of which is not a distinct data item 
		- `one-of`: pairs one expected input per subclass
		- E.g. 0-100, 120-150, and "H", "P", "F", "T"
	- Compound Data: two or more values naturally belong together 
		- `compound`
		- E.g. x,y data
	- Self-referential or Mutually Referential: information in the program's domain is of arbitrary size (empty for now)
		- `self-reference`
		- In order to be well-formed, a self-referential data definition must:
			- Have at least one case without self reference (the base case(s))
			- Have at least one case with self reference
	- References to Other Data Definitions: references to other data definitions you have defined 
		- `reference`
- E.g. 
	`(@htdd Status) ; HTDD tag`
	
	`; Purpose - interpret the legal status of a person`
	
	`(@dd-template-rules one-of                   ; Status 2 cases`
	                    `atomic-distinct  ; "minor"`
	                    `atomic-distinct) ; "adult"`
	
	`(define (fn-for-status s) ; Template created for data definition` 
	  `(cond [(string=? s "minor") (...)]`
	        `[(string=? s "adult") (...)]))`
	
	
	
	`(@htdf can-vote?) ; HTDF tag`
	
	`(@signature Status -> Boolean)                ; Signature (created our own data definition)`
	
	`; Purpose - produce true if a person with given status is eligible to vote`
	
	`(check-expect (can-vote? "minor") false)`
	`(check-expect (can-vote? "adult") true)`
	
	`;(define (can-vote? s) true) ; Stub`
	
	`(@template-origin Status) ; Template tag`
	
	`(@template ; Template where "s" is string`
	 `(define (can-vote? s)`   
	   `(cond [(string=? s "minor") (...)]`
	         `[(string=? s "adult") (...)])))`
	
	`(define (can-vote? s)`   
	  `(cond [(string=? s "minor") false]`
	        `[(string=? s "adult") true]))`



;; if the template is a cond, from a one-of type you MUST NOT:
;;  - delete the cond
;;  - reorder the QA pairs (e.g. swap "minor" and "adult" order)
;;  - edit the questions (check-expect)
;;  - delete any QA pair
;;  - add any QA pair
;; basically just edit the (...) in the template and nothing else