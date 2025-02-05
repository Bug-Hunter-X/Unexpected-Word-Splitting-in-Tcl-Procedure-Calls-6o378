# Unexpected Word Splitting in Tcl Procedure Calls

This repository demonstrates a common, yet subtle, error in Tcl related to word splitting when passing arguments to procedures.  The `bug.tcl` file contains code that highlights the problem, while `bugSolution.tcl` shows the corrected version.

## The Problem

In Tcl, when you call a procedure without explicitly using curly braces `{}` to group arguments, Tcl performs word splitting.  This means that the arguments are split into individual words.  If your procedure isn't designed to handle multiple words as a single argument, unexpected behavior will result. 

## The Solution

Always use curly braces `{}` to group arguments passed to a procedure if you intend for them to be treated as a single entity, even if the argument itself does not contain spaces.

## How to Reproduce

1. Clone this repository.
2. Run the `bug.tcl` script using a Tcl interpreter. Observe the error. 
3. Run the `bugSolution.tcl` script for the corrected behavior.

## Note

This type of error can be difficult to debug, especially in larger scripts. Paying close attention to how arguments are passed and using curly braces proactively can help avoid this pitfall.