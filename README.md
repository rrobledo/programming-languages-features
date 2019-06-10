This Document describes a list of modern features of programming languages that you need know.

Table of contents
=================

<!--ts-->
  * [Lambda Functions](#lambda-functions)
  * [Closures](#closures)
  * [Collection Pipeline](#collection-pipeline)
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
Not supported
```

Python
```python
def makeAdd():
    counter = 0
    
    def innerAdd():
        nonlocal counter
        counter += 1
        return counter
    return innerAdd

add = makeAdd()

print(add());
print(add());
print(add());
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


## Collection Pipeline
Collection pipelines are a programming pattern where you organize some computation as a sequence of operations which compose by taking a collection as output of one operation and feeding it into the next. (Common operations are filter, map, and reduce.) This pattern is common in functional programming, and also in object-oriented languages which have lambdas

Java
```java
package tool;
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;
/**
 * 
 * A simple Java Program to demonstrate how to use map and filter method Java 8.
 * In this program, we'll convert a list of String into a list of Integer and
 * then filter all even numbers.
 */
public class Hello {
  public static void main(String[] args) {
    List<String> numbers = Arrays.asList("1", "2", "3", "4", "5", "6");
    System.out.println("original list: " + numbers);
    List<Integer> even = numbers.stream()
                                .map(s -> Integer.valueOf(s))
                                .filter(number -> number % 2 == 0)
                                .collect(Collectors.toList());
    System.out.println("processed list, only even numbers: " + even);
  }
}
Output
original list: [1, 2, 3, 4, 5, 6]
the processed list, only even numbers: [2, 4, 6]
```


## Pattern Matching

## Async/Away



## References
