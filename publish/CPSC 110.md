https://cs110.students.cs.ubc.ca/bank/tile.png
### **Racket** 
- Divided into 2 regions ![[Pasted image 20240905205151.png]]
- Commenting out done via ;; or #;
- Stepper: shows evaluations step-by-step
- Style guides:
	- Comments that need to stay: `;;`
		- E.g. `;;Purpose`
	- Comments that can be removed: `;`
		- E.g. `;(define (cat x) x) ;stub`

### **Primitives**
- Primitive: built-in Racket language function 
- Aka "primitive operators"
- htdp beginner documentation, for example, in Help Desk Index can help us find primitives
	- https://docs.racket-lang.org/
- E.g. `(round (/ 3 4))`
### **Expressions and values**
- To form an expression: 
   ![[Pasted image 20240906144638.png]]
- Expressions reduce operands to values which can be used as arguments
- Examples of expressions
	- (sqrt 2)
	- 1
	- "#i1.41421"
	- (+ 3 4) 
- Examples of values
	- 1
	- "#i1.41421"
- When creating check-expects and output value is an inexact number (e.g. sqrt 2), use `(check-within)`
	- E.g. `(check-within (distance 3 0 0 4) 1.0 2.0)`

### **Evaluating simple arrhythmic expressions**
- Primitives:  
	- +
	- -
	- /
	- sqr (square of a number)
	- sqrt (square root of a number)
- "#i" means inexact digit, e.g. approximate 
- Doesn't follow BEDMAS rules automatically 
	- Works inside to outside, right to left
	- Write in a way so that it evaluates inner parentheses operations first and creates value to use as argument for outer expression
- E.g.  Write 4 * 3 ^ 2 - 5
  `(- (* 4 (sqr 3)) 5)`
### **Strings**
- String is an alphanumeric word or phrase, within quotations
	- E.g. "apple", "1 2 3"
- `string-append`
	- E.g. `(string-append "Ada" " " "Love")`
	- E.g. `(string-append "Ada" s)`
		- Where l = defined string variable
- `string-length`
	- Gives us number of characters in a string
	- E.g. `(string-length "apples")`
		- A P P L E S
		  0 1 2 3 4 5
		- Returns `6` due to zero-indexing
- `substring` 
	- Removes characters indicated based on their index position 
	- E.g. `(substring "Caribou" 2 4)`
			C a r  i  b o u
			0 1 2 3 4 5 6
		- We start at character 2 (`a`) and go up to but don't include character 4 (`i`) 
		- Output will be `ri` due to zero-based indexing

### **Images**
- Need to include (require 2htdp/image) at the beginning of the program
- Includes:
	- Circle `(circle radius "mode" "color")`
		- Takes 3 arguments: size (e.g. radius, side length, or width and height), mode (e.g. outline or solid), and colour
		- Passes arguments into the primitive "circle"
		- E.g. 
			`(above (circle 40 "solid" "red")`         
		         `(circle 40 "solid" "yellow")`
			     `(circle 40 "solid" "green"))`
	- Square `(square side-length "mode" "color")`
	- Rectangle `(circle width length "mode" "color")`
	- Text ("text")
- `image-append`
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
		  `(cond [(> 1 2) "bigger"]`
		        `[(= 1 2) "equal"]`
		        `[(< 1 2) "smaller"])`
			- Order of evaluation:
				1. Evaluates `[(> 1 2) "bigger"]`
					- Results in `(cond [false "bigger"]`
							        `[(= 1 2) "equal"]`
							        `[(< 1 2) "smaller"])`
				2. Evaluates `[(= 1 2) "equal"]`
					- Results in `[false "equal"]
					         `[(< 1 2) "smaller"])``
				3. Evaluates `[(< 1 2) "smaller"]`
					- Results in `[true "smaller"`
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

### Local Functions
- The function definition can call one or more built-in abstract functions or helper functions under its single top-level function 
- Can be used as a failure handle 
	  `(@template-origin X try-catch)`
	  `(@template`   
		 `(define (fn-for-x x)`
			 `(local [(define try (fn-that-might-fail <args>))]`
			     `(if (not (false? try))`
			         `try`
			         `<some alternative result>))))`
- E.g. 
```
(@htdd Song)
(define-struct song (title artist length))
;; Song is (make-song String String Natural)
;; interp. a song with a title, artist, and length in seconds
(define S1 (make-song "Dreaming" "Blondie" 188))
(define S2 (make-song "I Walk The Line" "Johnny Cash" 165))
(define S3 (make-song "Wannabe" "Spice Girls" 174))

(@dd-template-rules compound)
(define (fn-for-song s)
  (... (song-title s)
       (song-artist s)
       (song-length s)))
       

(@htdf get-songs-longer-than-n)
(@signature (listof Song) Natural -> (listof Song))
;; produce all songs in list with length > given length

(check-expect (get-songs-longer-than-n empty 120) empty)
(check-expect (get-songs-longer-than-n (list S1 S2 S3) 189) empty)
(check-expect (get-songs-longer-than-n (list S1 S2 S3) 188) empty)
(check-expect (get-songs-longer-than-n (list S1 S2 S3) 187) (list S1))
(check-expect (get-songs-longer-than-n (list S1 S2 S3) 173) (list S1 S3))

;(define (get-songs-longer-than-n los length) empty) ;stub

(@template-origin use-abstract-fn)
(define (get-songs-longer-than-n los length)
  (local [(@template-origin Song)
          (define (longer? s)
            (> (song-length s) length))]
    (filter longer? los)))
```
    
![[Pasted image 20240912125458.png]]
![[Pasted image 20240912125537.png]]
### **HtDF Recipe**
- Pros: Breaks down larger problems into small ones 
- Cons: Makes easy functions harder to design
- Code coverage:
	- If code is highlighted, indicates we have poor coverage (code wasn't evaluated) which can tell us that we haven't tested all scenarios
- Recipe:
	1. Signature, purpose and stub
		- Signature: type(s) of data the function consumes and produces 
			- Input and output parameter types:
				- Number (+ and - integers), Natural (0 and + integers) String, Image, Boolean
			- E.g. `(@signature Image Image -> Boolean)`
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
		- Thorough tests (at least 2) show cases using all types of inputs for bugs
			- If using built-in data types as input (e.g. string), need to test above, at, and below the boundaries
				- E.g. `(= (image-height i1)(image-height i2)) i1)` 
						- If 2 images are same height, output first image (design choice)
					 `(> (image-height i1)(image-height i2)) i1)` 
					 `(< (image-height i1)(image-height i2)) i2)` 
			- If using own-built data types as input (e.g. SeatNum), only need to test mid-point for non-distinct (e.g. 5 i)
	3. Template and inventory 
		- `(@template-origin ...)` tag
			- Where ... is name of DD where template came from
		- Template: body of the template is the outline of the function
			- E.g. 
			  `(define (double n)(... n))`
	1. Code the function body 
		- Code body: shows why the template makes the function work (stepper)
				`(define (double n)(* 2 n))`
		- Decide on what to do in weird cases 
			- E.g. `(= (image-height i1)(image-height i2)) i1)` 
				- If 2 images are same height, output first image (design choice)
		  
- E.g. Design a function, called image>?, that takes two images and determines whether the first is larger than the second.`
```
	(@htdf image>?)                           ;HTDF tag
	
	(@signature Image Image -> Boolean)       ;Signature
	
	;; Produces true if image is larger, otherwise false 
	
	;(define (image>? i1 i2) false)           ;;Stub - used to test here and now if the function works, comment out later 
	
	(check-expect (image>?                     ;;rectangle vs rectangle i1>i2
		 (rectangle 10 30 "solid" "red")
		 (rectangle 29 10 "solid" "red")) true)
	(check-expect (image>?                     ;;rectangle vs rectangle i1<i2
		 (rectangle 10 29 "solid" "red")
		 (rectangle 30 10 "solid" "red")) false)
	(check-expect (image>?                    ;;rectangle vs rectangle i1=i2
		 (rectangle 10 30 "solid" "red")
		 (rectangle 30 10 "solid" "red")) false)
	(check-expect (image>?                   ;;circle vs circle
		(circle 20 "solid" "red")
		(circle 19 "solid" "red")) true)
			
	(@template-origin Image)                ;;Template tag
		
	(@template                              ;Template
		(define (image>? i1 i2)
		 (... i1 i2)))
		
	(define (image>? i1 i2)                ;;Code
		(> (* (image-width i1) (image-height i1))
		 (* (image-width i2) (image-height i2))))```
```

### **HtDD Recipe**
- Used to define our own data types
- Typically, we have multiple functions using the same data definition 
- Tells us:
	- How we are representing information in the problem domain (e.g. a light is red) using data in the program (e.g. 0)
	- How we interpret data in the program (e.g. 0) using information in the program domain
				  a light is red <--  --> 0 
- Gives us exactly which inputs and outputs will be accepted by the function
- Includes:
	1. Tags
		- `(@htdd ...)` where ... is Data Type Definition (e.g. GradeStanding)
		- `(@dd-template-rules ...)` 
			- Where `...` is a Data Definition followed by specific data types for all cases
	2. A possible structure definition (not until compound data) 
	3. A type comment that defines type name and describes how to form data 
	      - E.g. `;;CityName is String`
		      - Which means "CityName is a new form of data is String (type)
	4. An interpretation to describe correspondence between information and data
		- Constraints: meant to tell other user to not pass invalid values into code, so we don't need to make code bullet proof
		- E.g. `interp. the name of a city`
	1. One or more examples of the data
		- Need as many examples as there are cases
		- Purpose is to assist reader of the code
			- E.g. `;;CarSpeed is Number [0, 200]`
				- 3 data examples needed: 
				  `(define CS1 0)`
				  `(define CS2 100)`
				  `(define CS3 200)`
		- E.g. `(define CN1 "Tokyo")`
	6. A template for a 1 argument function operating on data of this type
		- `(@template (define (fn-for-<something> x)())) ` 
		- If the template is a cond, from a one-of type you MUST NOT:
			- Delete the cond
			- Reorder the QA pairs (e.g. swap "minor" and "adult" order)
			- Edit the questions (check-expect)
			- Delete any QA pair
			- Add any QA pair
		- Basically just edit the (...) in the template and nothing else

- Data Definitions (the data allowed to pass to our function):
	- `atomic-non-distinct` : type predicate 
		- If not specific match: String, Number, Boolean, and Image
			- Everyone is allowed through, even if we have stricter criteria 
		- Intervals 
			- Fixed numbers or naturals within a range
			- `[` indicates the number is included, whereas `(` means the number is not included
				- E.g. `atomic-non-distinct is Natural (1, 20]` includes: 2, 3, 4... 19
			- `Natural` indicates numbers are positive and full integer, whereas `Number` can be negative with decimal places
				- E.g. `atomic-non-distinct is Number [1, 20]` includes: 1, 1.1, 1.2... 20
		- E.g. `(string=? x)(... x)`
	- `atomic-distinct`: equality predicate with guard 
		- Is this specific String, Number, Boolean, Image?
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
	- Itemization and Enumeration: 
		- Itemization:
			- Used to reference $\geq{2}$ subclasses (e.g. , at least one of which is NOT a distinct data item 
			- Use cond statement for each data type
				- E.g. 
					`(@template-origin Balloon) ;template`
					`(@template (define (tick b)` 
					  `(cond [(number? b) (... b)]`
					        `[else (...)])))`
					
					`(define (tick b)`
					  `(cond [(number? b)`
					         `(if (>= MAX-SIZE (+ b SPEED))`
					             `(+ b SPEED) #false)]`
					        `[else #false]))`
			- E.g. 0-100, 120-150, and "H", "P"
			- If given subtype is the last category listed, we don't need a guard 
				- Not necessary though
			- Requires:
				- Examples (e.g. `(define GN1 100)`, etc)
				- The use of a guard for cond statements (e.g. `(string?)` or `(number?`) to prevent strings from being exposed to `<=` predicates, for example
				  ![[Pasted image 20240917173225.png]]
		- Enumeration:
			- Used to reference $\geq{2}$ subclasses 
			- E.g. "H", "P", "T", "F"
			- Does not require examples as its implicit 
		- `(one-of <subclass> <subclass>)`
			- Where enumeration has at least 1 non-distinct data item 
			
- E.g. Number, String (non-atomic-distinct, atomic distinct, and atomic-distinct)
```
(@htdd Altitude) ; htdd tag
;; Altitude is one of:
;;  - "pre-launch"
;;  - Number
;;  - "post-flight"
;; interp. Altitude of rocket. Before launch, in meters above launch
;;         pad, after flight has ended.
;; CONSTRAINT: when a number is > 0

;; DD Examples (doesn't constrain shit)
(define A0 "pre-launch")
(define A1 37.5)
(define A2 "post-flight")

(@dd-template-rules one-of ; data types
                    atomic-distinct ; "pre-launch"
                    atomic-non-distinct ; any n > 0
                    atomic-distinct) ; "post-flight"

(define (fn-for-altitude a) ; data template
  (cond [(and (string? a)(string=? a "pre-launch")) (...)]
        [(number? a) (... a)]
        [else (...)]))


(@htdf inflight?) ; htdf tag
(@signature Altitude -> Boolean) ; signature
(@template-origin Altitude) ; template origin tag

;; Consume Altitude and produce true if rocket in flight

; (define (inflight? a) false) ; stub

(check-expect (inflight? "pre-launch") false)
(check-expect (inflight? "post-flight") false)
(check-expect (inflight? 37.5) true)

(@template (define (fn-for-altitude a) ; fx template
  (cond [(and (string? a)(string=? a "pre-launch")) (...)]
        [(number? a) (... a)]
        [else (...)])))

;; We are not restraining our fx in a way that makes our program bulletproof, we put constraints in DD assuming user won't even try
(define (inflight? a) ; fx
  (cond [(and (string? a)(string=? a "pre-launch")) false]
        [(number? a) true]
        [else false]))

```

- E.g. String (atomic-distinct)
```
(require spd/tags) 
(@htdd LetterGrade) ;;htdd tag

;;Type comment, interp., examples:
;;Domain information - LetterGrade is one of (3 subclasses):
;;   -A
;;   -B
;;   -C
;;interp. the letter grade in a course
;;<enumeration examples redundant>

;;Template rules used:
;;-one of: 3 cases
;;   -atomic distinct value: "A"
;;   -atomic distinct value: "B"
;;   -atomic distinct value: "C"

  (@dd-template-rules one-of ;; dd template
                      atomic-distinct
                      atomic-distinct
                      atomic-distinct)
  
  (define (fn-for-letter-grade lg) ;;data template (3 cases w/ accepted values)
    (cond [(string=? lg "A") (...)] ;will always be string "A" so no lg
          [(string=? lg "B") (...)] ;will always be string "B" so no lg 
          [(string=? lg "C") (...)])) ;will always be string "C" so no lg
```
		
- E.g. String and Natural (atomic distinct and non-distinct)
```
;DATA TYPE "GRADESTANDING" DEFINITION
(@htdd GradeStanding)

;Interp. GradeStanding is a percentage grade or a standing 
;Constraint: If Natural then is in range [0, 100]
;Examples, where GS named based on dd name:
(define GS1 50) 
(define GS2 "P")  

(@dd-template-rules one-of
                    atomic-non-distinct ;Handle Natural case
                    atomic-distinct     ;Handle "H" case
                    atomic-distinct     ;Handle "P" case
                    atomic-distinct     ;Handle "F" case
                    atomic-distinct)    ;Handle "T" case

(define (fn-for-grade-standing gs) ;dd template, takes 1 parameter (gs)
  (cond [(number? gs)(... gs)]                 ;Handle Natural
        [(and (string? gs)(string=? gs "H"))(...)] ;Handle "H"
        [(and (string? gs)(string=? gs "P"))(...)] ;Handle "P" 
        [(and (string? gs)(string=? gs "F"))(...)] ;Handle "F" 
        [else (...)]))                             ;Handle "T"


;FUNCTION "EXCELLENT?" DEFINITION
(@htdf excellent?) ;HDTF tag
(@signature GradeStanding -> Boolean) ;Signature
;Purpose: produces true if the grade/standing is >= 90

;Stub where..
     ;"gs" is input data
     ;"true" is example of an output
     ;To be commented out at a later time
;(define (excellent? gs) true) 

;Check-Expects
(check-expect (excellent? 89) false)  ;<boundary
(check-expect (excellent? 90) true)   ;=boundary for Natural
(check-expect (excellent? 91) true)   ;>boundary for Natural
(check-expect (excellent? "H") false) ;for "H"
(check-expect (excellent? "H") false) ;for "P"
(check-expect (excellent? "H") false) ;for "F"
(check-expect (excellent? "H") false) ;for "T"

(@template-origin GradeStanding) ;Template origin tag

(@template          ;HTDF template, takes 1 parameter (gs)
 (define (excellent? gs) 
   (cond [(number? gs)(... gs)]                 
         [(and (string? gs)(string=? gs "H"))(...)]
         [(and (string? gs)(string=? gs "P"))(...)] 
         [(and (string? gs)(string=? gs "F"))(...)]
         [else (...)])))                                  

(define (excellent? gs)      ;Fx, should only edit the (...)
  (cond [(number? gs)(>= gs 90)]                ;Handle Natural
        [(and (string? gs)(string=? gs "H"))false] ;Handle "H"
        [(and (string? gs)(string=? gs "P"))false] ;Handle "P" 
        [(and (string? gs)(string=? gs "F"))false] ;Handle "F" 
        [else false]))                             ;Handle "T"
```

### Big Bang Mechanism
- Primitive that complex structure by integrating and coordinating many functionalities together 
- Polymorphic: works for any type of world state but all x have to be the same type
- State true shows you data computation in real time 
- E.g. 
	`(@htdf main)`
	`(@signature WS -> WS)`
	`(@template-origin htdw-main)`

	`(define (main ws)`
	  `(big-bang ws        ; WS`
		`(on-tick   tock)   ; WS -> WS`
		`(to-draw   render) ; WS -> Image`
		`(on-mouse  ...)    ; WS Integer MouseEvent -> WS`
		`(on-key    ...)))  ; WS KeyEvent -> WS`

- Interactive programs:
	- `on-tick`
		- Progresses and saves world state
		- Measured in ticks per second 
		- Arguments: world state
	- `to-draw`
		- Display changes
		- Arguments: world state
	- `on-key` and `on-mouse`
		- Keyboard or mouse affects behaviour
		- Arguments: 
			- Keyboard: world state, key event
			- Mouse: world state, mouse x-coor and y-coor, mouse event
		- ![[Pasted image 20240921121319.png]]
	- `stop-when`
		- Stop automatically
		
- Framework
	- Includes:
		- Drawing of behaviour
		- Constants (unchanging)
		- Variables (changing)
		- Primitives to use

- E.g. 
```
(require spd/tags)
(require 2htdp/image)
(require 2htdp/universe)

![[Pasted image 20240920145114.png|300]]

;; =================
;; Constants:

(define WIDTH 400) ;scene width
(define HEIGHT 200) ;scene height
(define MTS (empty-scene WIDTH HEIGHT)) ;empty

(define RCOW .)
(define LCOW .)
(define CTR-Y (/ HEIGHT 2)) ;center position 

;; =================
;; Data definitions:

(@htdd Cow)

;; Cow is (make-cow Natural[0, WIDTH] Integer)
;; Interp. (make-cow x dx) is a cow with x-coordinate (x) and x-velocity (dx)
;;      x is center of the cow
;;      to stay visible in screen, x is between 0 and WIDTH 
;;      dx is in pixels per tick

(define-struct cow (x dx)) ;define-struct

;; Examples:
(define C1 (make-cow 10 3))  ;at 10, moving left -> right
(define C2 (make-cow 20 -4)) ;at 20, moving left <- right

(@dd-template-rules compound) ;data type
(@template (define (fn-for-cow c)
             (... (cow-x c) ;Natural [0, WIDTH]
                  (cow-dx c)))) ;Integer

;; =================
;; Functions:

(@htdf main)
(@signature Cow -> Cow)
;; Makes cow walk, right and left across the screen 
;; Start the world with (main 0)

(define (main c) ;main fx
  (big-bang c                ;World state
    (on-tick   next-cow)     ;Cow -> Cow 
    (to-draw   render-cow)   ;Cow -> Image
    (on-key    handle-key))) ;Cow KeyEvent -> Cow


(@htdf next-cow)
(@signature Cow -> Cow)
;; Increase Cow by dx, bounce off edge
;; Example: cow is at 20 pixels, moving at 3 velocity
;; At next tick, cow should be at (+ 20 3), moving at 3 velocity

;(define (next-cow c) c) ;stub

;; Cases: cow continues, cow reaches edge, cow bounces off edge
(check-expect (next-cow (make-cow 100 3)) ;center right -> left
              (make-cow (+ 100 3) 3))
#;(check-expect (next-cow (make-cow 100 -3)) ;center left -> right
              (make-cow (- 100 3) -3))
(check-expect (next-cow (make-cow (- WIDTH 3) 3)) ;right edge
              (make-cow WIDTH 3))
#;(check-expect (next-cow (make-cow 3 -3)) ;left edge
              (make-cow 0 -3))
(check-expect (next-cow (make-cow (- WIDTH 2) 3)) ;passes right edge
              (make-cow WIDTH -3))  
#;(check-expect (next-cow (make-cow 2 -3)) ;passes left edge
              (make-cow 0 3))

(@template-origin Cow) ;to tag
(@template (define (next-cow c) ;fx template
             (... (cow-x c) ;Natural [0, WIDTH]
                  (cow-dx c)))) ;Integer

(define (next-cow c) ;sign change on velocity
             (cond [(> (+ (cow-x c)(cow-dx c)) ;cow tries to leave right
                       WIDTH) 
                    (make-cow WIDTH (- (cow-dx c)))] 
                   [(< (+ (cow-x c)(cow-dx c)) ;cow tries to leave left
                       0) 
                    (make-cow 0 (- (cow-dx c)))]
                   [else                       ;cow continues
                    (make-cow (+ (cow-x c)(cow-dx c)) (cow-dx c))]))


(@htdf render-cow)
(@signature Cow -> Image)
;; Place appropriate cow image on MTS at (cow-x c) and CTR-Y
;;    Asking too much from this function, therefore we need to make another
;;    This function will decide which image needs to be chosen

;(define (render-cow c) MTS) ;stub

(check-expect (render-cow (make-cow 99 3)) ;middle scene (right -> left)
                          (place-image RCOW 99 CTR-Y MTS))  
(check-expect (render-cow (make-cow 33 -3)) ;middle scene (right -> left)
                          (place-image LCOW 33 CTR-Y MTS)) 

(@template-origin Cow) ;to tag
(@template (define (render-cow c) ;fx template
             (... (cow-x c) ;Natural [0, WIDTH]
                  (cow-dx c)))) ;Integer

(define (render-cow c) ;fx using choose-image fx
   (place-image (choose-image c) (cow-x c) CTR-Y MTS)) 


(@htdf choose-image)
(@signature Cow -> Image)
;; Produce RCOW or LCOW depending on direction cow is going
;; Helper function for render-cow
;; Constraint: LCOW if dx = 0

;(define (choose-image c) RCOW) ;stub, RCOW chosen arbitrarily 

(check-expect (choose-image (make-cow 10 3)) RCOW) ;right -> left
(check-expect (choose-image (make-cow 11 -3)) LCOW) ;left -> right
(check-expect (choose-image (make-cow 11 0)) LCOW) ;dx = 0

(@template-origin Cow) ;to tag
(@template (define (choose-image c) ;fx template
             (... (cow-x c) ;Natural [0, WIDTH]
                  (cow-dx c)))) ;Integer

(define (choose-image c) ;fx
  (if (> (cow-dx c) 0) ;right-travel as +dx right and -dx left
     RCOW
     LCOW))


(@htdf handle-key)
(@signature KeyEvent -> Cow)
;; Change direction of cow travel when space bar pressed

;(define (handle-key c ke) c) ;stub

(check-expect (handle-key (make-cow 99 3) " ") (make-cow 99 -3)) ;right -> left
(check-expect (handle-key (make-cow 33 -3) " ") (make-cow 33 3)) ;left -> right
(check-expect (handle-key (make-cow 99 3) "a") (make-cow 99 3)) ;wrong-key
(check-expect (handle-key (make-cow WIDTH 3) " ")(make-cow WIDTH -3)) ;boundary

(@template-origin Cow) ;to tag
(@template (define (handle-key c ke) ;fx template
             (... (cow-x c) ;Natural [0, WIDTH]
                  (cow-dx c)))) ;Integer

(define (handle-key c ke) ;fx
             (if (key=? ke " ")
                 (make-cow (cow-x c) (- (cow-dx c)))
                 (make-cow (cow-x c) (cow-dx c))))
```

### Compound Data
-  $\geq2$ items of information that naturally belong together
	- E.g. first and last name, x-coor and y-coor
	- E.g.    `;; Player is (make-player String String)
			`;; Interp. (make-player fn ln) is a hockey player
			`;;     fn is first name`
			`;;     ln is last name``
			
			`(@dd-template-rules compound) ;data types`
			`(define (fn-for-player p) ;dd template`
			  `(... (player-fn p) ;string`
			       `(player-ln p))) ;string`
			       
- Define-struc expression: `(define-<struct> (x y))`
		- `<struct>`: define-struct name 
		- `x`: x-field
		- `y`: y-field
		- Declares definition
	- E.g. `(define-struct player (fn ln))`
	
- Constructor: `(define <constr> (make-<struct> x y))` 
		- `<constr>`: constructor name
		- `<struct>`: define-struct name
		- `x`: x-field
		- `y`: y-field
		- Declares definition
	- E.g.  `(define P1 (make-player "Bobby" "Orr"))` 
	      `(define P2 (make-player "Wayne" "Gretzky"))`
	
- Selectors: `(<struct>-x <constr>)` and `(<struct>-y <constr>)`
		-  `<struct>`: define-struct name
		- `<constr>`: constructor name
		- Calls x-field or y-field 
	- E.g. `(player-fn P1) ;returns Bobby`
		 `(player-ln P2) ;returns Gretzky`

- Predicate: `(<struct>? ...)`
		- `<struct>`: define-struct name
		- ...: argument (e.g. "hello")
		- Compares define-structure definition to argument given  
	- E.g. `(player? P1) ;returns true`
		 `(player? "Dough") ;returns false`

### Lists
- Constructor:
	- `(define <list name> (cons <element> empty))`
		- `<element>`: string, number, expression (e.g. string-append), etc
		- Used to define list
		- E.g. `(define L1 (cons "apple" (cons 2 empty))`
			- List with 2 elements "apple" and "2"
	- `(cons <value or expression> <list name>)`
		- Adds element to the front of the list
		- E.g. `(define L1 (cons "apple" empty))`
			- Running `(cons "orange" L1)` 
				- Returns `(cons "orange" (cons "apple" empty))`
 
- Selectors: `(first <list name>)` and `(rest <list name>)`
	- First: returns first element in the list as a string
	- Rest: returns all other elements in the list after first, as a list 
	- E.g. to get second element
		`(first (rest <list name>))`
		`(rest (rest <list name>))
	- E.g. `(cons "Flames" empty)`
		- List with 1 element 
		- Prints `(cons "Flames" empty)`

- Predicate: `(empty? <list name>)`
	- Returns true or false

![](Pasted%20image%2020240929200731.png)

### Self-Reference and Natural Recursion 
- Isn't exclusive to lists, can also include other data definition types, e.g. naturals
- Self-reference calls used to address lists/data of arbitrary (unknown) size  (e.g. number of students in a class)
- When creating a data definition using a list:
	- E.g. `;; Mystery is one of:
		 `;;   -(cons 1 empty)`
		 `;;   -(cons Natural Mystery)`
			- Type comment contains a recursion
		- Meaning to be of type Mystery, a list must have either:
			- 1 and empty
				- E.g. `(cons 1 empty)`
			- Natural and Mystery
				- E.g. `(cons 5 (cons 4 (cons 1 empty)))` 
					- `(cons 5` is Natural and `(cons 4 (cons 1 empty)` is Mystery
					- `(cons 4` is Natural and `(cons 1 empty)` is Mystery

- Well-formed Self-references requirements
	- At least one base case 
		- Contains no self-reference
		- One example needed only, list first
    - At least one self-reference case
	    - One example needed for each
	- Type comment example of a well-formed self-reference:
		`NonEmptyListOfNumber is one of:`
		  `(cons Number empty)`
		  `(cons Number NonEmptyListOfNumber)`
- Helper functions:
	- When def refers to another non-primitive data def (e.g. Egg)
	- When sub-task requires operating on arb. sized data
	- Two or more distinct functions
	
```
(require spd/tags)

(@htdd ListOfString)
;; ListOfString is one of:
;;  - empty
;;       -ListOfString list with nothing in it
;;       -need to start with an empty list to have something to build on
;;  - (cons String ListOfString)
;;       -where ListOfString references itself (self-ref)
;;       -list of one longer than empty
;;       -add one item at a time
;;       -can be arbitrarily long list 
;; interp. a list of strings

(define LOS1 empty)
;   -someone doesn't like hockey
;   -empty) matches empty
(define LOS2 (cons "Canucks" empty))
;   -someone only likes 1 team
;   -matches (cons String ListOfString)
;       -(cons "Canucks" matches (cons String
;       -empty) matches empty
(define LOS3 (cons "Leafs" (cons "Canucks" empty)))
;   -someone likes 2 teams
;   -matches (cons String ListOfString)
;       -(cons "Leaf" matches (cons String
;       -(cons "Canucks" matches (cons String
;       -empty) matches empty
(define LOS4 (cons "Oilers" LOS3))
;   -added 1 team to list

(@dd-template-rules one-of             ;2 cases
                    atomic-distinct    ;empty
                    compound           ;(cons String ListOfString)
                    self-ref)          ;(rest los) is ListOfString

;lists are compound data:
;   -(cons takes (cons "Canucks" empty) list and adds "Leafs"
;   -can be retrieved later

;using this template because itemization
;   -(define (fn-for-los los)
;       (cond [(empty? los) (...)]
;             [else
;               (...)]))
;   -2 or more subclasses.. 1 of which is atomic-non-distinct

(define (fn-for-los los)
  (cond [(empty? los) (...)] ;empty case - atomic distinct
        [else 
         (... (first los) ;compound case (selector 1)
              (fn-for-los (rest los)))])) ;compound case (selector 2)

;(first los) will be string, e.g. "Leafs"
;(rest los) will be ListOfString, e.g. (cons "Canucks" empty) 



;Design a function that determines whether "Canucks" appears in a list.

(@htdf contains-canucks?)
(@signature ListOfString -> Boolean)
;; produce true if list contains "Canucks"

;(define (contains-canucks? los) false) ;stub

(check-expect (contains-canucks? empty) false)
(check-expect (contains-canucks? (cons "Canucks" empty)) true)
(check-expect (contains-canucks? (cons "Leafs"
                                       (cons "Canucks"
                                             empty)))
              true)
(check-expect (contains-canucks? (cons "Leafs"
                                       (cons "Oilers"
                                             empty)))
              false)

(@template-origin ListOfString)

(@template (define (contains-canucks? los)
             (cond [(empty? los) (...)] ;(...) is base case result
                   [else 
                    (... (first los) ;... is combination
                         (contains-canucks? (rest los)))]))) ;natural recursion
;if (...) and ... are correct, we can always trust the natural recursion 
           
(define (contains-canucks? los)
  (cond [(empty? los) false] 
        [else 
         (if (string=? (first los) "Canucks") ;sometimes first in list (first los)
             true
             (contains-canucks? (rest los)))])) ;sometimes not first in list
;natural recursion asks "is Canucks in rest of list?" (rest los)
```

### Reference and Helper Functions 
- Reference rule:
	- Any time one data type refers to non-primitive type, wrap it in a call to that data type's template function
- If we need to do something complicated with the referred to type
	- E.g. if a function needs to call back to a data definition several times (e.g. retrieving student name and id 4 times) 
- Therefore we need to use another helper function (so made make-bar)


- E.g. Using compound, references, self-references data types
```
(require 2htdp/image)
(require 2htdp/universe)
(require spd/tags)
;Each egg has own constant of x-coordinate so we treat x as changing 

(@htdw ListOfEgg)
;List of non-primitive type (vs ListOfNumber for example)

;; Constants:
(@problem 1)
(define WIDTH 400)
(define HEIGHT 600)

(define MARIO
  (bitmap/url "https://cs110.students.cs.ubc.ca/lectures/m04-mario.png"))

(define MTS
  (place-image MARIO
               (/ WIDTH 2)
               (- HEIGHT (/ (image-height MARIO) 2) 5)
               (empty-scene WIDTH HEIGHT)))

(define YOSHI-EGG 
  (bitmap/url "https://cs110.students.cs.ubc.ca/lectures/m04-egg.png"))

(define FALL-SPEED 5) ;pixels  per tick
(define SPIN-SPEED 5) ;degrees per tick

;;===================================================
;; Data Definitions:

(@htdd Egg)
; set egg as compound data as we have x-coor, y-coor, and rot changing for egg

(define-struct egg (x y r))
;; Egg is (make-egg Number Number Number)
;; interp. the x, y position of an egg in screen coordinates (pixels),
;;         and rotation angle in degrees

(define E1 (make-egg 100 50 23))
(define E2 (make-egg 20 30 50))

(@dd-template-rules compound) ;3 fields


(define (fn-for-egg e)
  (... (egg-x e)    ;Number (need to allow for decimals)
       (egg-y e)    ;Number
       (egg-r e)))  ;Number


(@htdd ListOfEgg)
;creaing because we have an arb. list of eggs

;; ListOfEgg is one of:
;; - empty
;; - (cons Egg ListOfEgg)
;       -where Egg is a non-primitive type
;       -refers to another function besides itself
;; interp. a list of eggs

(define LOE1 empty)
(define LOE2 (cons E1 empty))
(define LOE3 (cons E1 (cons E2 empty)))

(@dd-template-rules one-of           ;2 cases
                    atomic-distinct  ;empty
                    compound         ;cons
                    ref              ;(first loe) is Egg
                    self-ref)        ;(rest loe) is ListOfEgg

(define (fn-for-loe loe)
  (cond [(empty? loe) (...)]
        [else
         (... (fn-for-egg (first loe)) ;ref (natural helper)
              (fn-for-loe (rest loe)))])) ;self-ref (natural recursion)
;natural helper implies we need to create a separate function


;;===================================================
;; Functions:

(@htdf main)
(@signature ListOfEgg -> ListOfEgg)
;; start the world with (main empty)

(@template-origin htdw-main)

(define (main loe)
  (big-bang loe             ;ListOfEgg
    ;(state    true)
    (on-tick  next-eggs)    ;ListOfEgg -> ListOfEgg
    (to-draw  render-eggs)  ;ListOfEgg -> Image
    (on-mouse handle-mouse) ;ListOfEgg Integer Integer MouseEvent -> ListOfEgg
    (on-key   handle-key))) ;ListOfEgg KeyEvent -> ListOfEgg

;;=====================
(@htdf next-eggs)
(@signature ListOfEgg -> ListOfEgg)
;; produce the next eggs at appropriate locations and angles
(check-expect (next-eggs empty) empty) ;empty case
(check-expect (next-eggs (cons (make-egg 10 20 30)  ;1 item case, x y r
                               empty))
              (cons (make-egg 10 (+ 20 FALL-SPEED) (+ 30 SPIN-SPEED)) empty))
(check-expect (next-eggs (cons (make-egg 2 60 20) ;2 item case
                               (cons (make-egg 10 20 30)
                                     empty))) 
              (cons (make-egg 2 (+ 60 FALL-SPEED) (+ 20 SPIN-SPEED))
                    (cons (make-egg 10 (+ 20 FALL-SPEED) (+ 30 SPIN-SPEED))
                          empty)))
;we're not actually doing the additions to fall & spin speed in this function
;produce list so we use (cons for our result
;   -carries over into our function

;(define (next-eggs loe) empty) ;stub

(@template-origin ListOfEgg)

(@template (define (next-eggs loe)
             (cond [(empty? loe) (...)]
                   [else
                    (... (next-egg (first loe))
                         (next-eggs (rest loe)))])))

(define (next-eggs loe)
  (cond [(empty? loe) empty] ;get back an empty list
        [else
         (cons (next-egg (first loe)) ;ref, going to make new egg
               (next-eggs (rest loe)))])) ;self-ref

;since (first loe) refers to the new (first) egg's x,y-coor, fall & spin speed
;   -we need to make a helper function
;   -not as easy as assessing just string or number
;   -can't call multiple selectors here
;   -need single helper function that consumes egg


;;=====================
(@htdf next-egg)
(@signature Egg -> Egg)
;; produces new egg by adding FALL-SPEED to y and SPIN-SPEED to r

;(define (next-egg e) e) ;stub

(check-expect (next-egg (make-egg 2 60 20)) ;first egg (from next-eggs)
              (make-egg 2 (+ 60 FALL-SPEED) (+ 20 SPIN-SPEED)))
(check-expect (next-egg (make-egg 10 20 30)) ;second egg (from next-eggs)
              (make-egg 10 (+ 20 FALL-SPEED) (+ 30 SPIN-SPEED)))

(@template-origin Egg)

(@template
 (define (fn-for-egg e)
   (... (egg-x e)    
        (egg-y e)    
        (egg-r e))))

(define (next-egg e)
  (make-egg (egg-x e)    
            (+ (egg-y e) FALL-SPEED)   
            (+ (egg-r e) SPIN-SPEED)))


;;=====================
(@htdf render-eggs)
(@signature ListOfEgg -> Image)
;; Place YOSHI-EGG img at appropriate location/rotation on MTS for each egg

;(define (render-eggs loe) MTS) ;stub

(check-expect (render-eggs empty) MTS) ;MTS because we're producing an image
(check-expect (render-eggs (cons (make-egg 10 20 30) ;1 item
                                 empty))
              (place-image (rotate 30 YOSHI-EGG) 10 20 MTS))  
(check-expect (render-eggs (cons (make-egg 110 120 130) ;2 items
                                 (cons (make-egg 10 20 30)
                                       empty)))
              (place-image (rotate 130 YOSHI-EGG) 110 120
                           (place-image (rotate 30 YOSHI-EGG) 10 20 MTS)))
;places 1 egg in MTS, then places next egg onto that combined image
;we're not actually placing the egg's x, y-coor, rotation in this function

(@template-origin ListOfEgg)

(@template (define (render-eggs loe)
             (cond [(empty? loe) (...)]
                   [else
                    (... (place-egg (first loe))
                         (render-eggs (rest loe)))])))

(define (render-eggs loe)
  (cond [(empty? loe) MTS]
        [else
         (place-egg (first loe) ;Egg
                    (render-eggs (rest loe)))])) ;Image
;need a helper function because we're calling on more than 1 selector


;;=====================
(@htdf place-egg)
(@signature Egg Image -> Image)
;; place YOSHI-EGG on empty-image at Egg's x, y-coor 
(check-expect (place-egg (make-egg 10 20 30) MTS)
              (place-image (rotate  30 YOSHI-EGG) 10 20 MTS))
(check-expect (place-egg (make-egg 110 120 130) empty-image) 
              (place-image (rotate  130 YOSHI-EGG) 110 120 empty-image))

;(define (place-egg e img) img)

(@template-origin Egg)

(@template
 (define (place-egg e img)
   (... (egg-x e)
        (egg-y e)
        (egg-r e)
        img)))
;for additional parameters with atomic type, add parameter everywhere after ...

(define (place-egg e img)
  (place-image (rotate  (egg-r e) YOSHI-EGG)
               (egg-x e)
               (egg-y e)
               img))


;;=====================
(@htdf handle-mouse)
(@signature ListOfEgg Integer Integer MouseEvent -> ListOfEgg)
;; add and egg at x, y with rotation 0 when the mouse is clicked
(check-expect (handle-mouse empty 10 40 "button-down")
              (cons (make-egg 10 40 0) empty))
(check-expect (handle-mouse (cons (make-egg 3 4 5) empty) 90 100 "drag")
              (cons (make-egg 3 4 5) empty))

;(define (handle-mouse loe x y me) loe) ;stub

(@template-origin MouseEvent)

(@template
 (define (handle-mouse loe x y me)
   (cond [(mouse=? me "button-down") (... loe x y)]
         [else    
          (... loe x y)])))

(define (handle-mouse loe x y me)
  (cond [(mouse=? me "button-down") (cons (make-egg x y 0) loe)] 
        [else loe]))


;;=====================
(@htdf handle-key)
(@signature ListOfEgg KeyEvent -> ListOfEgg)
;; on space reset to zero eggs
(check-expect (handle-key (cons E1 (cons E2 empty)) " ") empty)
(check-expect (handle-key (cons E1 empty) "a") (cons E1 empty))

;(define (handle-key loe ke) loe) ;stub

(@template-origin KeyEvent)

(@template   
 (define (handle-key loe ke)
   (cond [(key=? ke " ") (... loe)]
         [else  
          (... loe)])))

(define (handle-key loe ke)
  (cond [(key=? ke " ") empty]   
        [else loe]))
```


```
;; Program that will help visualize costs at differen schools
;;    -Names of schools
;;    -International student tuition costs

;; dd that represents name of schools and international tuition costs
;; fx that consumes dd and produces bar chart
;; fx that consumes dd and produces lowest cost option

(require spd/tags)
(require 2htdp/image)

;; ============================================
;; Constants

(define TEXT-COLOUR "black")
(define TEXT-SIZE 24)

(define Y-SCALE 1/200)
(define BAR-WIDTH 30)
(define BAR-COLOUR "lightblue")

;; ============================================
;; Data Definitions

(@htdd School)
;; School is (make-school String Natural)
;; Interp. string is name of school and natural is tuition cost in $USD
(define-struct school (name tuition))

(define S1 (make-school "School1" 25533))
(define S2 (make-school "School2" 31363))
(define S3 (make-school "School3" 54233))

(@dd-template-rules compound) ;name and tuition

(define (fn-for-school s) ;data template
  (... (school-name s)
       (school-tuition s)))


(@htdd ListOfSchools)
;; ListOfSchools is one of:
;;   -Empty
;;   -(cons School ListOfSchools) where School is a ref
;; Interp. list of schools and their tuition cost

(define LOS1 empty) ;base
(define LOS2 (cons S1 (cons S2 empty))) ;ref and self-ref

(@dd-template-rules one-of
                    atomic-distinct ;empty
                    compound        ;(cons School ListOfSchools)
                    ref             ;(fn-for-school (first los)) ;natural helper
                    self-ref)       ;(fn-for-los (rest los)) ;natural recursion

(define (fn-for-los los)
  (cond [(empty? los) (...)];base case
        [else
         (... (fn-for-school (first los)) ;ref
              (fn-for-los (rest los)))])) ;self-ref

;; ============================================
;; Functions

(@htdf chart)
(@signature ListOfSchools -> Image)
;; Consumes schools and their tuitions (ListOfSchools) and produces bar chart
; (define (chart los) (square 0 "solid" "white")) ;stub

;; To get:
;;   -a bar with a black outline and light blue interior
;;      --> (rectangle width height mode colour)
;;      --> (rectangle width height mode colour)
;;   -vertical text with school name overlaying the text
;;      --> (rotate 90 (text "school" size colour)) 
;;   -all components oriented to the bottom center so that they overlap
;;      --> (overlay/align "center" "bottom"
;;               (rotated text)
;;               (rectangle outline)
;;               (rectangle interior)
;;   -because list, we have to also include empty
;;      --> (beside/align "bottom"
;;                (overlayed text, bar outline, and bar interior)
;;                (square 0 "solid" "white") from stub

(check-expect (chart empty) (square 0 "solid" "white"))    ;base case
(check-expect (chart (cons (make-school "S1" 8000) ;1 school
                           empty))  
              (beside/align
               "bottom"
               (overlay/align ;S1
                "center" "bottom"
                (rotate 90 (text "S1" TEXT-SIZE TEXT-COLOUR))
                (rectangle BAR-WIDTH (* 8000 Y-SCALE) "outline" "black")
                (rectangle BAR-WIDTH (* 8000 Y-SCALE) "solid" BAR-COLOUR))
               (square 0 "solid" "white"))) ;empty
(check-expect (chart (cons (make-school "S1" 8000) ;2 schools
                           (cons (make-school "S2" 12000) empty)))  
              (beside/align
               "bottom"
               (overlay/align ;S1
                "center" "bottom"
                (rotate 90 (text "S1" TEXT-SIZE TEXT-COLOUR))
                (rectangle BAR-WIDTH (* 8000 Y-SCALE) "outline" "black")
                (rectangle BAR-WIDTH (* 8000 Y-SCALE) "solid" BAR-COLOUR))
               (overlay/align ;S2
                "center" "bottom"
                (rotate 90 (text "S2" TEXT-SIZE TEXT-COLOUR))
                (rectangle BAR-WIDTH (* 12000 Y-SCALE) "outline" "black")
                (rectangle BAR-WIDTH (* 12000 Y-SCALE) "solid" BAR-COLOUR))
               (square 0 "solid" "white"))) ;empty
 
(@template-origin ListOfSchools) ;template
(@template (define (chart los)
             (cond [(empty? los) (...)]
                   [else
                    (... (fn-for-school (first los))
                         (fn-for-los (rest los)))])))

;; Since we need to do something complicated with the referred to type..
;; i.e. because LOS refers to School (reference) and chart refers to School)
;; Therefore we need to use another helper function (so made make-bar)

(define (chart los)
  (cond [(empty? los) (square 0 "solid" "white")]
        [else
         (beside/align "bottom"
                       (make-bar (first los))
                       (chart (rest los)))]))


(@htdf make-bar)
(@signature School -> Image)
;; Hands school and produce bar image for a single school in the chart
; (define (make-bar s) (square 0 "solid" "white")) ;stub

(check-expect (make-bar (make-school "S1" 8000))
              (overlay/align 
               "center" "bottom"
               (rotate 90 (text "S1" TEXT-SIZE TEXT-COLOUR))
               (rectangle BAR-WIDTH (* 8000 Y-SCALE) "outline" "black")
               (rectangle BAR-WIDTH (* 8000 Y-SCALE) "solid" BAR-COLOUR)))

(@template-origin School) ;template
(@template (define (make-bar s)
             (... (school-name s)
                  (school-tuition s))))

(define (make-bar s)
  (overlay/align "center" "bottom"
                 (rotate 90 (text (school-name s) TEXT-SIZE TEXT-COLOUR))
                 (rectangle BAR-WIDTH (* (school-tuition s) Y-SCALE)
                            "outline" "black")
                 (rectangle BAR-WIDTH (* (school-tuition s) Y-SCALE)
                            "solid" BAR-COLOUR)))
```


### Naturals
- Naturals are a self-ref data definition because there'a an arbitrary number of natural numbers
	- We also don't know which numbers users will input
- `(add1 )` 
	- Produces a natural 1 bigger 
	- E.g. `(add 1 0)` returns 1       while      `(add 1 (add1 0))` returns 2
- `(sub1 )` 
	- Produces a natural 1 smaller 
- Factorial 
	- Computing n* n-1 * n-2 ... 
	- `(define (fact n)`
		 `(cond [(zero? n) ((1) 1)]`
				`[else`
				`((2) * n (fact (sub1 n)))]))`
	- When n - a is zero (e.g. `(list-from-to 5 5)`, should return `(cons 5 empty)`
	- E.g. `(check-expect (fact 0))`
		- Output is 1
	- E.g. `(check-expect (fact 3))`
		- Computation: (* (* 3 2) 1)
		- Output is 6