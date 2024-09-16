- Submit starter before 10pm on day of lecture via:
- Handin (after replacing CWL ??? with username) 
- Check results through Handback url  
Problem set done at end of each module 
- Use look-up function to determine what function is and/or the syntax of the function you want to write
- BSL needs BEDMAS and/or order of operations specified
	- E.g.  4 * 3 ^ 2 - 5 should be written as: (- (* 4 (sqr 3)) 5)

### **Racket** 
- Divided into 2 regions ![[Pasted image 20240905205151.png]]
- Commenting out done via ;; or #;
- Stepper: shows evaluations steo-by-step

### **Expressions and values**
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

### **Evaluating simple arrhythmic expressions**
- Includes +, -, /, sqr (square of a number), sqrt (square root of a number)
- Doesn't follow BEDMAS rules automatically 
	E.g. `(+ 1(* 3 2))`
		; Write this way so that it evaluates inner parentheses operations first and creates value to use as argument for outer expression

### **Strings**
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

### **Images**
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

### **Constants**
- We can name constants that can be called into expressions
	- ![[Pasted image 20240906155916.png]]
	- E.g. `(define width 400)`
		 `(define height 600)`
			; Constants are width and height
			
		 `(* width height)`
			- Expression calling both constants

### **Primitives**
- Primitive: built-in Racket language function 
- htdp beginner documentation, for example, in Help Desk Index can help us find primitives
	- https://docs.racket-lang.org/
- E.g. `(round (/ 3 4))`

### **Functions**
- Function: one you've built yourself
- To form a function: 
	- `(define (function-name? v)`
		  `(expression-condition) o)`
	  - function-name? = name of function
	  - v = variable placeholder (e.g. "i" for image", "s" for string, etc)
	  - expression-condition = primatives (if, and, or, >, <, =, cond, circle, etc) 
	  - o = output based on condition
	
- To call a function (function call expression):
	- `(function-name? v)`
		- v = passed argument 
			- E.g. circle 40 "solid" "red"
				- "circle" is the primative 
				- "40", "solid", "red" are operands/values
		- Can be nested within another expression
		
- E.g. trafficlight
	`(define (trafficlight c) ;;defined function where "c" is variable`
	  `(circle 40 "solid" c))`
	
	`(trafficlight (string-append "re" "d")) ;;called function`
	- Order of function operation:
		 1. Evaluates primitive call by reducing operand `(string-append "re" "d")`
			`(trafficlight "red")`
		2. Passes "c" argument (`red`) into body of the function for evaluation
			`(circle 40 "solid" "red")
		3. Function call `trafficlight` is now gone and we evaluate primitive call `circle` with values `40`, `solid`, `red`
				![[Pasted image 20240908115724.png]]

### **Booleans**		
- Predicates are primitives or functions that produce a boolean value 
- True and false
- Primatives:
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
	 
### **If Statements**
- Evaluates and returns true or false (including false is not necessary though as its assumed)
- Able to nest conditional primitives into if statements
		`(define LOWER 10)`
		`(define UPPER 20)`

		(define (foo x y)
		  (if (and (> x LOWER) (< x UPPER))
	      (- x (* y 2))
	      (+ x (* y 3))))

		(foo (* 3 4) (+ 0 2))
- Primitives:
	- `and` 
		- Short circuits and stops evaluating if false statement found 
		- E.g. 
		  `(if (and (image? i)(< (image-width i) (image-height i))) #true)`
	- `or`
		- Only compares first 2 predicates
		- Accepts either to return "true"
		- E.g. 
		  `(if (or (< 2 1)(> 3 2)) #true #false)`
	- `not`
		- Only compares first 2 predicates
		- Accepts only 1 to return "true"
		- E.g. 
		  `(if (not (< 2 1)(> 3 2)) #true #false)`
	- `con`
		- Last case should be an "else" statement
		- E.g. 
		  `(cond [(> 8 7) "Charlie"]`
			   `[(= 6 6) "Dog"])`
		   - Next step in evaluation would be 
			 `(cond [true "Charlie"]
					`[(= 6 6) "Dog"])`

- E.g. 
	`(require 2htdp/image) ;;required image tag`

	`(define i1 (rectangle 10 20 "solid" "red")) ;;defining i1`
	`(define i2 (rectangle 40 20 "solid" "red")) ;;defining i2`

	`(if (< (image-width img1) ;;if statement with nested primative call`
		 `(image-height img1))`
	     `"tall" "wide")`
	     
	- Order of evaluation: 
		1. Reduce operands `(image-width i1)` to its value (the actual image)
			`(image-width <picture>)`
		2. Reduces operands in primitive call `image-width` to a value `20`
			`(if (< 20 (image-height i1))`
		        `"tall" "wide")`
		3. Reduces operands in primitive call `image-height` to a value `10`
			`(if (< 20 10)`
		        `"tall" "wide")`
		4. Evaluates predicate and returns `false` as i1's height is more than its width
			`(if false "tall" "wide")`
		5. Returns `wide`

![[Pasted image 20240912125458.png]]
![[Pasted image 20240912125537.png]]
### **HtDF Recipe**
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
			- When we take images and produce an output, they are combined into just 1 image 
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

### **HtDD Recipe**
- Used to define our own data types
- Uses tags:
	- `(@htdd ...)` where ... is Data Type Definition (e.g. GradeStanding)
	- `(@dd-template-rules ...)` where ... is a Data Definition followed by specific data types for all cases
		- Data Definitions:
			- `atomic-non-distinct` :type predicate 
				- Is String, Number, Boolean, Image?
				- Use: 
					- Intervals 
						- Fixed numbers or naturals within a range, e.g. 0-100
				- E.g. `(string=? x)(... x)`
			- `atomic-distinct`: equality predicate with guard 
				- Is this specific String, Number, Boolean, Image?
				- Use: 
					- Enumeration
						- Fixed number of distinct items, e.g. "H", "P", "F", "T"
						- Doesn't need examples as they would not be helpful to include
				- E.g. `(string=? x "red")(...)`
			- `self-reference`
				- Use: information in the program's domain is of arbitrary size (empty for now)
				- Form natural recursion with call to this type's template function
				- In order to be well-formed, a self-referential data definition must:
					- Have at least one case without self reference (the base case(s))
					- Have at least one case with self reference
				- E.g. `(fn-for-los (rest los))`
			- `reference`
				- Use: References to other data definitions you have defined 
					- Call to other type's template function
				- E.g. `(fn-for-lod (dir-subdirs d)  
						`(fn-for-dir (first lod))`
			- `compound`
				- Use: $\geq{2}$ values naturally belong together 
					- Position (x, y data)
					- E.g. `(ball? x)`
						  `(... (ball-x x) (ball-y x))`
						  `(... (fn-for-ball (game-ball g))`
		- Itemization: 
			- Used to reference $\geq{2}$ subclasses, at least one of which is not a distinct data item 
			- `(one-of (cond [(and(Q)A])`: pairs one expected input per subclass
				- Requires the use of a guard for cond statements
				- E.g. 0-100, 120-150, and "H", "P", "F", "T"- 
- Includes:
	2. A possible structure definition (not until compound data) 
	3. A type comment that defines type name and describes how to form data 
	4. An interpretation to describe correspondence between information and data
	5. One or more examples of the data
	6. A template for a 1 argument function operating on data of this type
		-  If the template is a cond, from a one-of type you MUST NOT:
			- Delete the cond
			- Reorder the QA pairs (e.g. swap "minor" and "adult" order)
			- Edit the questions (check-expect)
			- Delete any QA pair
			- Add any QA pair
		- Basically just edit the (...) in the template and nothing else
- E.g. 
```
;DATA TYPE "GRADESTANDING" DEFINITION
(@htdd GradeStanding)
;GradeStanding is one of..
     ;Natural (0-100)
     ;"H"
     ;"P"
     ;"F"
     ;"T"

;Interpretation: a percentage grade or a standing 

;Constraint: If natural then is in range [0, 100]

;Examples where..
     ;Purpose is to assist reader of the code
     ;"GS" named based on data type definition name (GradeStanding)
(define GS1 50)   ;Example
(define GS2 "P")  ;Example

(@dd-template-rules one-of ;HTDD template tag, using one-of data type 
                    atomic-non-distinct ;Handles Natural case
                    atomic-distinct     ;Handles "H" case
                    atomic-distinct     ;Handles "P" case
                    atomic-distinct     ;Handles "F" case
                    atomic-distinct)    ;Handles "T" case

(define (fn-for-grade-standing gs) ;HTDD template, takes 1 parameter (gs)
  (cond [(number? gs)(... gs)]                            ;Handles Natural
        [(and (string? gs)(string=? gs "H"))(...)]        ;Handles "H"
        [(and (string? gs)(string=? gs "P"))(...)]        ;Handles "P" 
        [(and (string? gs)(string=? gs "F"))(...)]        ;Handles "F" 
        [else (...)]))                                    ;Handles "T"

;FUNCTION "EXCELLENT?" DEFINITION
(@htdf excellent?) ;HDTF tag

(@signature GradeStanding -> Boolean) ;Signature using our created data type

;Purpose: produces true if the grade/standing is >= 90

;Stub where..
     ;"gs" is input data
     ;"true" is example of an output
     ;To be commented out at a later time
;(define (excellent? gs) true) 

;Check-Expects
(check-expect (excellent? 89) false)  ;Below boundary for Natural
(check-expect (excellent? 90) true)   ;At boundary for Natural
(check-expect (excellent? 91) true)   ;Above boundary for Natural
(check-expect (excellent? "H") false) ;for "H"
(check-expect (excellent? "H") false) ;for "P"
(check-expect (excellent? "H") false) ;for "F"
(check-expect (excellent? "H") false) ;for "T"

(@template-origin GradeStanding) ;Template origin tag

(@template                  ;HTDF template, takes 1 parameter (gs)
 (define (excellent? gs) 
   (cond [(number? gs)(... gs)]                            ;Handles Natural
         [(and (string? gs)(string=? gs "H"))(...)]        ;Handles "H"
         [(and (string? gs)(string=? gs "P"))(...)]        ;Handles "P" 
         [(and (string? gs)(string=? gs "F"))(...)]        ;Handles "F" 
         [else (...)])))                                   ;Handles "T"

(define (excellent? gs)      ;Function body code, should only edit the (...)
  (cond [(number? gs)(>= gs 90)]                          ;Handles Natural
        [(and (string? gs)(string=? gs "H"))false]        ;Handles "H"
        [(and (string? gs)(string=? gs "P"))false]        ;Handles "P" 
        [(and (string? gs)(string=? gs "F"))false]        ;Handles "F" 
        [else false]))                                    ;Handles "T"
```
