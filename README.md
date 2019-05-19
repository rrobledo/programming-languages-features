This Document describes a list of modern features of programming languages that you need know.

Table of contents
=================

<!--ts-->
  * [Lambda Functions](#lambda-functions)
  * [Closures](#closures)
  * [Collections](#collection)
  * [Pattern Marching](#pattern-matching)
  * [Promises](#promices)
  * [Async/Away](#async/away)

  * [References](#references)
<!--te-->


## Lambda Functions
Lambda comes from the Lambda Calculus and refers to anonymous functions in programming. 
Why is this cool? It allows you to write quick throw away functions without naming them. It also provides a nice way to write closures. With that power you can do things like this.

Scala
```scala
val foo = (x: Int) : Int => x * x

println(foo(10))
```

Golang
```golang
foo := func(x int) int {
 return x * x
}

fmt.Println(foo(10))
```

Java
```java
BiFunction<Int, Int> foo = x -> { x * x }

System.out.println(foo(10))
```

Python
```
```

JavaScript
```
```



## Closures

## Collection

## Pattern Matching

## Async/Away



## References
