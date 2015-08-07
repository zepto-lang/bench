# bench

A minimal benchmarker for statements in zepto.

# Usage

Bench exposes two endpoints, `time` and `bench`.
They are used like this:

````clojure
(bench:time '(+ 1 2))  ; will return time elapsed in nanoseconds
(bench:bench '(+ 1 2))
; will test the statement 100k times and print metrics in the format:
; Tested function 100000 times 
; 	Average duration:   13952.31 	( 1.395231e-5 secs) 
; 	Best case:          0 	( 0.0 secs) 
; 	Worst case:         308000 	( 3.08e-4 secs) 
; 	Total:              1395231000 	( 1.395231 secs)
(bench:bench '(+ 1 2) 100) ; will test the statement 100 times
```

Functions as arguments are supported too.

<br/>

*Have fun!*
