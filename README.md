## What is this?

Egg is a programming language where everything is a expression. This project was built based on the egg language on the [Eloquent Javascript book.](eloquentjavascript.net)

Currently the language supports:

variables:
```javascript
   define(x, 10) -> 10
```
functions:
```javascript
   fun(sum, do(+(1,2)))
```

arrays:
```javascript
   array(1,2,3) -> [1,2,3],
   length(array) -> 3,
   element(array, 1) -> 2
```

operators:
```javascript
   +(1,2) -> 3
   -(1,2) -> 1
   /(1,2) -> 0.5
   *(1,2) -> 2
   =(1,2) -> false
   <(1,2) -> true
   >(1,2) -> false
```

while:
```javascript
   while(<(count, 10))
```

do blocks:
```javascript
   while(<(count, 11),
         do(define(total, +(total, count)),
            define(count, +(count, 1)))),
```

## Why I build this?

Just to learn more about how programming languages work and have some fun.

## Examples of code

```javascript
  do(define(x, 10),
   if(>(x, 5),
      print("large"),
      print("small")))
// -> "large"

  do(define(total, 0),
      define(count, 1),
      while(<(count, 11),
            do(define(total, +(total, count)),
               define(count, +(count, 1)))),
      print(total))
// → 55

  do(define(sum, fun(array,
       do(define(i, 0),
          define(sum, 0),
          while(<(i, length(array)),
            do(define(sum, +(sum, element(array, i))),
               define(i, +(i, 1)))),
          sum))),
     print(sum(array(1, 2, 3))))
// -> 6
```
