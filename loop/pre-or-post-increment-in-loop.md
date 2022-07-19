# pre or post increment in loop

It's better to use pre increment, because post increment is more costly. Pre increment directly returns the incremented value, but post increments need to copy the value in a temporary variable, increment the original and then returns the previous made copy.
