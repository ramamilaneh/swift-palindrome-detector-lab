# Code-Along: Palindrome Detector

## Objectives

1. Declare and define functions using proper syntax.
3. Engage a problem to be solved in code by breaking the approach down into smaller steps.
4. Solve each step sequentially in increasing levels of complexity.
5. Check your code's behavior periodically with `Print()` as you progress in your solution.
6. Call another function in the same file

 ### Optional 
7. Memorize some palindromes that you can use to impress your friends.

## Introduction

A [palindrome](https://en.wikipedia.org/wiki/Palindrome) is a word, phrase, or sentence whose letters are exactly mirrored around the center letter. Some examples include:

*racecar*  
*Bob*  
*Kanakanak*  (a city in Alaska)  
*Aibohphobia*  (the fear of palindromes)   
*never odd or even*  
*I prefer pi*  
*Flee to me, remote elf.*  
*Norma is as selfless as I am, Ron.*  
*No sir! Away! A papaya war is on.*

The qualification of a palindrome typically ignores spaces, punctuation, and capitalization, judging only the order of the letters themselves. Essentially, when a palindrome is reversed, its letters fall into the same order.

We're going to write a function that can judge whether or not a particular string qualifies as a palindrome. We're going to start with judging a single all-lowercase word, and then add complexity to allow the function to handle capitalization, spaces, and punctuation. We'll call this function `stringIsPalindrome()`.

The easiest way to judge a palindrome is simply to compare it to its reverse. However, there is no string reversal function built into the Swift language so we'll have to write this functionality ourselves. We'll accomplish this by writing another function called `stringByReversingString()` that we can call from within the `stringIsPalindrome()` function.

## Instructions

Fork and clone this lab. 

### I. Write The Functions

Open the project file and navigate to the `AppDelegate` file. 

Declare the following functions:

* `stringIsPalindrome()` which takes one `String` argument called `string` and returns a `bool`, and
* `stringByReversingString()` which takes one `String` argument names `string` and returns an `String`.


### II. Function Bodies

1. `stringByReversingString(_:)` function's goal is take whatever string variable is passed into the `string` argument (also "parameter") and return its exact reverse at the end of the method.

2. `stringIsPalindrome(_:)` should return a bool for indicating wether the submitted argument is a palidrome or not.
 * Use the function `stringByReversingString(_:)` you wrote earlier to help

### III. Check The Implementation

1. Let's use local variables and an `Print()` within the `application(didFinishLaunchingWithOptions:)` method to check that our method can handle the case of "*racecar*".

 * This should return `true`
 
2. Next try the string "*racecars*"
 * This should return `false`

 
## Adding Complexity

### IV. Ignoring Typecase

Let's improve our `stringIsPalindrome(_:)` method to allow it to handle uppercase letters in strings. Right now, evaluating the actual palindromes "*Bob*", "*Kanakanak*", and "*Aibohphobia*" will all return `false` because they contain a capital letter. Verify this by adding these checks into the `application(didFinishLaunchingWithOptions:):` method in the same style as evaluating "*racecar*":

### V. Removing Spaces

Since phrases can qualify as a palindromes, let's improve our `stringIsPalindrome(_:)` method to evaluate strings that contain spaces. 
Once you've got the logic done for that test your function with these phrases:

"*this is not a palindrome*"

"*never odd or even*"


### VI. Removing Punctuation

For our final trick, let's add the functionality to our `stringIsPalindrome(_:)` method so that can accommodate palindromes that are full sentences. (That means punctuation!) Once you have the logic done, test your function with these palindrome phrases that include punctuation:

 "*Flee to me, remote elf.*"
 
 "*Norma is as selfless as I am, Ron.*"
 
 "*No sir! Away! A papaya war is on.*":


### X. Memorize Some Palindromes (optional)

Because [palindromes are cool](https://www.youtube.com/watch?v=vPGTizdGwSc) (like bowties).
<p data-visibility='hidden'>View <a href='https://learn.co/lessons/objc-palindrome-detector' title='Code-Along: Palindrome Detector'>Code-Along: Palindrome Detector</a> on Learn.co and start learning to code for free.</p>

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/objc-palindrome-detector'>Code-Along: Palindrome Detector</a> on Learn.co and start learning to code for free.</p>
