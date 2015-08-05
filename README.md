# bench

A minimal benchmarker for statements in zepto.

# Usage

Bench exposes two endpoints, `time` and `bench`.
They are used like this:

````clojure
(bench:time '(+ 1 2))  ; will return time elapsed in nanoseconds
(bench:bench '(+ 1 2))
; will test the statement 100k times and print metrics in the format:
; Tested function 1000 times:
; 	Average duration:   7180076.0 	( 7.180076e-3 secs) 
; 	Best case:          5740000 	( 5.74e-3 secs) 
; 	Worst case:         12395000 	( 1.2395e-2 secs) 
; 	Total:              7180076000 	( 7.180076 secs)
(bench:bench '(+ 1 2) 100) ; will test the statement 100 times
```

Functions as arguments are supported too.

The test script takes somewhat long, so you might make yourself
a coffee while it runs.

<br/>

*Have fun!*
