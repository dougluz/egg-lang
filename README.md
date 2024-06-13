## What is this?

Egg is a programming language where everything is a expression. This project was built based on the egg language on the [Eloquent Javascript book.](eloquentjavascript.net)

## Why I build this?

Just to learn more about how programming languages work and have some fun.

## Examples of code

```
  do(define(x, 10),
   if(>(x, 5),
      print("large"),
      print("small")))
```

```javascript
run(`
do(define(total, 0),
   define(count, 1),
   while(<(count, 11),
         do(define(total, +(total, count)),
            define(count, +(count, 1)))),
   print(total))
`);
// → 55
```
