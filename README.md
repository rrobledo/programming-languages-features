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
Not supported
```

Python
```python
foo = lambda x : x * x
print(x(10))
```

JavaScript
```javascript
var foo = (x) => {return x * x} 

console.log(foo(10))
```

## Closures
A closure is a persistent scope which holds on to local variables even after the code execution has moved out of that block. 
A Closure is a function object that remembers values in enclosing scopes regardless of whether those scopes are still present in memory.

Scala
```scala
val add = {
  var counter = 0
  () => { counter += 1; counter}
}

println(add())
println(add())
println(add())
```

Golang
```golang
add := func() func() int {
    counter := 0
    return func() int {
        counter++
        return counter
    }
}()

fmt.Println(add())
fmt.Println(add())
fmt.Println(add())
```

Java
```java
BiFunction<Int, Int> foo = x -> { x * x }

System.out.println(foo(10))
```

Python
```python
foo = lambda x : x * x
print(x(10))
```

JavaScript
```javascript
var add = (function () {
  var counter = 0;
  return function () {counter += 1; return counter}
})();

console.log(add());
console.log(add());
console.log(add());
```


## Collection

## Pattern Matching

## Async/Away



## References
