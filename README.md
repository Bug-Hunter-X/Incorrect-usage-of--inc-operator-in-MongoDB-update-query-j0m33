# Incorrect usage of $inc operator in MongoDB update query
This example demonstrates an incorrect usage of the `$inc` operator in a MongoDB update query.  The `$inc` operator is used to increment a numeric field by a specified value.  However, using a string instead of a number will result in an error.

## Bug
The bug is caused by providing a string ('1') instead of a number (1) as the increment value to the `$inc` operator. MongoDB expects a numeric value for this operation. This will lead to an error similar to:

```
MongoError: $inc needs a number
```

## Solution
The solution is to provide a numerical value to the `$inc` operator instead of a string.  Modify the query to use a number as shown in `bugSolution.js`.