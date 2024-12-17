# MongoDB $inc operator error with non-numeric value
This example demonstrates an error that can occur when using the `$inc` operator in a MongoDB update query with a non-numeric value. The `$inc` operator is used to increment a numerical field by a given value. Attempting to increment a field by a non-numeric value will result in an error.

## Bug
The bug is caused by passing a string value ('abc') as the increment value to the `$inc` operator. MongoDB expects a numerical value for the `$inc` operator, and attempting to use a non-numeric value results in an error.

## Solution
The solution is to ensure that the value passed to the `$inc` operator is a number. In this case, the string 'abc' should be replaced with a numeric value, such as 1.