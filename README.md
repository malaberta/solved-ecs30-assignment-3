Download Link: https://assignmentchef.com/product/solved-ecs30-assignment-3
<br>
Problem 1: squareroot.c

In this program you will approximate the square root of a number <em>n </em>using the <em>Babylonian method</em>. This method starts with an initial guess <em>x</em><sub>0 </sub>close to √√<em>n</em>, and at the <em>n</em><sup>th </sup>step calculates . As <em>n </em>gets larger an larger, <em>x<sub>n </sub></em>≈ <em>n</em>. Your program must take the number <em>n</em>, initial guess <em>x</em><sub>0</sub>, and number of steps <em>m </em>and print <em>x<sub>m </sub></em>with exactly 5 decimal places.

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="deacadb9a7adbbb29eaebdefe9">[email protected]</a> <sup>˜</sup>]$ ./squareroot

Enter the integer you wish to find the square root of: 2

Enter your first guess and number of steps: 1 1000

The square root of 2 is approximately 1.41421

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="403233273933252c0030237177">[email protected]</a> <sup>˜</sup>]$ ./squareroot

Enter the integer you wish to find the square root of: 2

Enter your first guess and number of steps: 1 1

The square root of 2 is approximately 1.50000

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="82f0f1e5fbf1e7eec2f2e1b3b5">[email protected]</a> <sup>˜</sup>]$ ./squareroot

Enter the integer you wish to find the square root of: 5

Enter your first guess and number of steps: 2 100

The square root of 2 is approximately 2.23607

Problem 2: guessyournumber.c (70 points, 7 per test case)

Write a program that will guess an integer that the user has picked. Imagine that the user will write down a positive integer <em>x </em>on a piece of paper and your program will repeatedly ask questions in order to guess what <em>x </em>is, and the user replies honestly. Your program will start by asking for an int<em>n</em>, and you must have 1 ≤<em>x</em>≤<em>n</em>. After that, the program will successively guess what <em>x </em>is, and the user must tell the computer if <em>x </em>is equal to the guess (entering ’e’), larger than the guess (entering ’l’), or smaller than the guess (entering ’s’).

Your program will guess by maintaining a lower bound (initially 1) and upper bound (initially <em>n</em>) and pick the largest integer equal to or smaller than<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> the midpoint of the lower bound and upper bound. If the user responds with ’l’ indicating that <em>x </em>is larger, the guess becomes the new lower bound plus one. If the user responds with ’s’ indicating that <em>x </em>is smaller, the guess becomes the new upper bound minus one. If the user responds with ’e’ indicating that <em>x </em>is the guess, your program will report the number of guesses made and terminate execution:

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4c3e3f2b353f29200c3c2f7d7b">[email protected]</a> <sup>˜</sup>]$ ./guessyournumber

Enter n: 50

Is your number 25? l

Is your number 38? l

Is your number 44? s

Is your number 41? e

Your number must be 41. I used 4 guesses.

If the user responds in a way that is not feasible (no such <em>x </em>can exist), print an error and quit:

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2a58594d53594f466a5a491b1d">[email protected]</a> <sup>˜</sup>]$ ./guessyournumber

Enter n: 9

Is your number 5? s

Is your number 3? s

Is your number 2? l

Error: that’s not possible.

If only one number is still possible, your program should conclude what it is and report the number of guesses:

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="562425312f25333a1626356761">[email protected]</a> <sup>˜</sup>]$ ./guessyournumber

Enter n: 50

Is your number 25? l

Is your number 38? l

Is your number 44? s

Is your number 41? s

Is your number 39? l

Your number must be 40. I used 4 guesses.

Report invalid input as follows:

[<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="addfdecad4dec8c1edddce9c9a">[email protected]</a> <sup>˜</sup>]$ ./guessyournumber

Enter n: -2

Error: n must be positive.

Enter n: a

Error: invalid input.

Enter n: 9

Is your number 5? m Error: invalid input.

<a href="#_ftnref1" name="_ftn1">[1]</a> This is called the <em>floor </em>of a number.