# Exercise Session 1, Solutions

## Question 3: Fast exponentiation

```scala
import scala.annotation.tailrec

def fastExp(base: Int, exp: Int): Int =
  require(exp >= 0)

  @tailrec
  def go(base: Int, exp: Int, acc: Int): Int =
    if exp == 0 then
      acc
    else if (exp % 2) != 0 then
      go(base, exp - 1, base * acc)
    else
      go(base * base, exp / 2, acc)

  go(base, exp, 1)
```

## Question 4: Tail recursive Fibonacci

```scala
import scala.annotation.tailrec

def fibonacci(n: Int): Int =
  require(n >= 0)

  @tailrec
  def go(k: Int, previous: Int, current: Int): Int =
    if k == n then current
    else go(k + 1, current, previous + current)

  if n == 0 then 0 else go(1, 0, 1)
```
