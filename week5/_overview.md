# Week 5

# String Theory

## What is a "string"?
A string is a string of "characters"

## What is a "character"?
A, a, 3, ^, F, ] are all characters

### String = Text
In Magick, "text" and "string" are interchangeable. "Text" usually indicates that the text editor window is involved, or a long template is used. "String" is a more general term for a string of characters: letters, numbers and symbols. Generally we try to use "text" because it's a less confusing term. However in some places, for example for sockets, "string" is used.

### String Variable
Short string of characters, edited in the inspector window

### Text Variable
Long string of characters, edited in the text editor window

### Profanity filter
Match against a list of bad words

### Combine Text
Combine two strings or more text variables, the delimiter is optional but can be useful to separate the strings
\n for newline

### Evaluate Text
(experimental)
includes, not includes, equals, not equals, starts with, not starts with, ends with, not ends with

### Replace Text
Replace some text with some other text

### Text Rule Matcher
Match a some text against a list of rules

### Text Template

### Current Time
Gives you the current time!

# Control Flow
One of the core functions of Magick is enabling you to evaluate conditions and make decisions based on those conditions. This is called "control flow" and is a core concept in programming. Magick is a visual programming language, so we use nodes to represent control flow. Magick inherits many concepts from a long line of "flow-based" programming languages, which are a type of visual programming language.

## Exclusive Gate
Take whichever input happens first (or ever) and pass it on, ignoring the rest

If a value is null or undefined, activate the TRUE path, otherwise activate the FALSE path

## Or Gate
If any trigger arrives, pass it on to the next node

## Random Gate
Trigger one of the outputs at random

## Switch
Evaluate the input text and trigger based on one of the cases

# Null
null means (nothing) or (empty) or (no value). It's not zero. It's just nothing.

## Is Null Or Undefined Node

# Booleans
Booleans are named after George Boole, for his Boolean Algebra
In programming, booleans are used to represent true or false

## Boolean Gate
Evaluate a boolean type for true or false

## Is Variable True
Evaluate a variable for "true" or "false", including strings and numbers (0 or 1)

## Wait For All
Wait for all things to execute before passing on the trigger
Useful for executing multiple asynchronous functions in parallel

## Adding commands to your agent
/example

