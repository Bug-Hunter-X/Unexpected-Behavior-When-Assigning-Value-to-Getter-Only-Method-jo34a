# Unexpected Behavior When Assigning Value to Getter-Only Method

This repository demonstrates a common, yet subtle, error in Ruby related to getter methods.  When a class defines a getter method for an instance variable but omits a setter, assigning a value through the getter method has no effect on the instance variable's value.

The `bug.rb` file showcases the issue.  The `bugSolution.rb` file shows the corrected approach.

## Bug
The primary issue lies in the expectation that `my_object.value = 20` will update `@value`.  This is not the case; the assignment is effectively ignored.

## Solution
The correct approach is to explicitly define a `setter` method if you want to allow external modification of the instance variable.