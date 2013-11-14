# Infinite Loops

## Problem
You need to loop forever, without doing any work.

## Solution

Use an empty select block.

    select {}

## Discussion

Empty infinte loops are often used to provide blocking behaviour for part or all of an application. You may be tempted to use an infinite for loop such as:

    for {}

but this is inefficient since it wastes cpu time and cannot be pre-empted by the garbage collector. A select with zero cases is optimised by the compiler into a simple blocking statement.


## See Also

[Go Language Specification: Select statements](http://golang.org/ref/spec#Select_statements)

----
[no rights reserved](http://creativecommons.org/publicdomain/zero/1.0/)
