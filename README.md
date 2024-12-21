# Ruby Accessor Assignment Bug

This repository demonstrates a common, yet subtle, error in Ruby related to how direct assignment to accessor methods interacts with instance variables.  The `bug.rb` file showcases the problem.  The solution in `bugSolution.rb` illustrates correct approaches to modifying the instance variable.

## The Problem

In many languages, a getter/setter pattern implies that assignment via the getter will update the underlying variable.  Ruby's approach is different.  Assigning directly to the result of a getter method does not change the instance variable itself; instead, the assignment creates a local variable.

## The Solution

To modify the instance variable, use either `instance_variable_set` or define a setter method.