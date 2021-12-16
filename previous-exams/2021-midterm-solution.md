# 2021 Midterm, Solutions

## Exercise 1

```scala
trait Tree[T]:
    def height: Int = this match
        case EmptyTree(_) => 0
        case Node(left, _, right, _) => Math.max(left.height, right.height) + 1
    
    def isBalanced: Boolean = this match
        case EmptyTree(_) => true
        case Node(left, _, right, _) => left.isBalanced && right.isBalanced && Math.abs(left.height - right.height) <= 1

case class EmptyTree[T](leq: (T, T) => Boolean) extends Tree[T]
case class Node[T](left: Tree[T], elem: T, right: Tree[T], leq: (T, T) => Boolean)
extends Tree[T]
```

<details>

<summary>Tests</summary>

```scala
def intLeq(a: Int, b: Int) = a <= b

val exTree1 = Node(
    Node(
        Node(EmptyTree(intLeq), 1, EmptyTree(intLeq), intLeq),
        2,
        Node(EmptyTree(intLeq), 3, EmptyTree(intLeq), intLeq),
        intLeq
    ),
    5,
    Node(
        Node(EmptyTree(intLeq), 7, EmptyTree(intLeq), intLeq),
        9,
        Node(
            Node(EmptyTree(intLeq), 10, EmptyTree(intLeq), intLeq),
            15,
            Node(EmptyTree(intLeq), 25, EmptyTree(intLeq), intLeq),
            intLeq
        ),
        intLeq
    ),
    intLeq
)
// exTree1: Node[Int] = Node(
//   Node(
//     Node(
//       EmptyTree(repl.MdocSession$App$$Lambda$26768/0x0000000802a74000@96de2cb),
//       1,
//       EmptyTree(repl.MdocSession$App$$Lambda$26769/0x0000000802a745d0@7b8c0297),
//       repl.MdocSession$App$$Lambda$26770/0x0000000802a74ba0@b9d9006
//     ),
//     2,
//     Node(
//       EmptyTree(repl.MdocSession$App$$Lambda$26771/0x0000000802a754c0@76af1792),
//       3,
//       EmptyTree(repl.MdocSession$App$$Lambda$26772/0x0000000802a68000@10b2d836),
//       repl.MdocSession$App$$Lambda$26773/0x0000000802a685d0@bb1f80d
//     ),
//     repl.MdocSession$App$$Lambda$26774/0x0000000802a68ba0@6c4b54dd
//   ),
//   5,
//   Node(
//     Node(
//       EmptyTree(repl.MdocSession$App$$Lambda$26775/0x0000000802a69170@6256cd41),
//       7,
//       EmptyTree(repl.MdocSession$App$$Lambda$26776/0x0000000802a69740@64a3da55),
//       repl.MdocSession$App$$Lambda$26777/0x0000000802a4c000@60d6275c
//     ),
//     9,
//     Node(
//       Node(
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26778/0x0000000802a4c5d0@560d6a27
//         ),
//         10,
//         EmptyTree(repl.MdocSession$App$$Lambda$26779/0x0000000802a4cba0@2e58962),
//         repl.MdocSession$App$$Lambda$26780/0x0000000802a4d170@786e8a19
//       ),
//       15,
//       Node(
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26781/0x0000000802a4d740@29d3be8f
//         ),
//         25,
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26782/0x00000008023d8000@1432a5c0
//         ),
//         repl.MdocSession$App$$Lambda$26783/0x00000008023d85d0@3ab290bd
//       ),
//       repl.MdocSession$App$$Lambda$26784/0x00000008023d8ba0@3600ebb0
//     ),
// ...

val exTree2 = Node(
    Node(
        Node(
            Node(EmptyTree(intLeq), 25, EmptyTree(intLeq), intLeq),
            15,
            Node(EmptyTree(intLeq), 10, EmptyTree(intLeq), intLeq),
            intLeq
        ),
        9,
        Node(EmptyTree(intLeq), 7, EmptyTree(intLeq), intLeq),
        intLeq
    ),
    5,
    Node(
        Node(EmptyTree(intLeq), 3, EmptyTree(intLeq), intLeq),
        2,
        Node(EmptyTree(intLeq), 1, EmptyTree(intLeq), intLeq),
        intLeq
    ),
    intLeq
)
// exTree2: Node[Int] = Node(
//   Node(
//     Node(
//       Node(
//         EmptyTree(repl.MdocSession$App$$Lambda$26787/0x0000000802af2000@38eb51e),
//         25,
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26788/0x0000000802af25d0@2d17faaa
//         ),
//         repl.MdocSession$App$$Lambda$26789/0x0000000802af2ba0@1cfbd9d3
//       ),
//       15,
//       Node(
//         EmptyTree(repl.MdocSession$App$$Lambda$26790/0x0000000802af3170@613fca1),
//         10,
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26791/0x0000000802af3740@70439f38
//         ),
//         repl.MdocSession$App$$Lambda$26792/0x0000000802a4e000@6293f930
//       ),
//       repl.MdocSession$App$$Lambda$26793/0x0000000802a4e5d0@206481f0
//     ),
//     9,
//     Node(
//       EmptyTree(repl.MdocSession$App$$Lambda$26794/0x00000008023da000@390b97a9),
//       7,
//       EmptyTree(repl.MdocSession$App$$Lambda$26795/0x00000008023da5d0@55dd75ef),
//       repl.MdocSession$App$$Lambda$26796/0x0000000802af1000@287a5c1d
//     ),
//     repl.MdocSession$App$$Lambda$26797/0x0000000802af15d0@2c9523e3
//   ),
//   5,
//   Node(
//     Node(
//       EmptyTree(repl.MdocSession$App$$Lambda$26798/0x0000000802b50000@49464f07),
//       3,
//       EmptyTree(repl.MdocSession$App$$Lambda$26799/0x0000000802b505d0@778a39cd),
//       repl.MdocSession$App$$Lambda$26800/0x0000000802b50ba0@d6a0995
//     ),
//     2,
//     Node(
//       EmptyTree(repl.MdocSession$App$$Lambda$26801/0x0000000802b51170@865a9e0),
//       1,
//       EmptyTree(repl.MdocSession$App$$Lambda$26802/0x0000000802b51740@7320e19c),
//       repl.MdocSession$App$$Lambda$26803/0x0000000802b51d10@55c2fa64
//     ),
//     repl.MdocSession$App$$Lambda$26804/0x0000000802b522e0@83967e8
// ...

val tree3 = Node(
    Node(
        Node(
            Node(EmptyTree(intLeq), 25, EmptyTree(intLeq), intLeq),
            15,
            Node(EmptyTree(intLeq), 10, EmptyTree(intLeq), intLeq),
            intLeq
        ),
        9,
        Node(EmptyTree(intLeq), 7, EmptyTree(intLeq), intLeq),
        intLeq
    ),
    5,
    EmptyTree(intLeq),
    intLeq
)
// tree3: Node[Int] = Node(
//   Node(
//     Node(
//       Node(
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26806/0x0000000802b52e80@2d36e5a6
//         ),
//         25,
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26807/0x0000000802b53450@596ecd9d
//         ),
//         repl.MdocSession$App$$Lambda$26808/0x0000000802b53a20@1bbd0d0e
//       ),
//       15,
//       Node(
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26809/0x0000000802b53ff0@58783fb6
//         ),
//         10,
//         EmptyTree(
//           repl.MdocSession$App$$Lambda$26810/0x0000000802b545c0@42f9faca
//         ),
//         repl.MdocSession$App$$Lambda$26811/0x0000000802b54b90@6dd4c52d
//       ),
//       repl.MdocSession$App$$Lambda$26812/0x0000000802b55160@1e7270e4
//     ),
//     9,
//     Node(
//       EmptyTree(repl.MdocSession$App$$Lambda$26813/0x0000000802b55730@76e6913),
//       7,
//       EmptyTree(repl.MdocSession$App$$Lambda$26814/0x0000000802b55d00@a4cec9e),
//       repl.MdocSession$App$$Lambda$26815/0x0000000802b562d0@41fabd57
//     ),
//     repl.MdocSession$App$$Lambda$26816/0x0000000802b568a0@4c0210dc
//   ),
//   5,
//   EmptyTree(repl.MdocSession$App$$Lambda$26817/0x0000000802b56e70@3850cebe),
//   repl.MdocSession$App$$Lambda$26818/0x0000000802b57440@5515fd36
// )

assert(exTree1.height == 4)
assert(exTree2.height == 4)
assert(EmptyTree(intLeq).height == 0)
assert(exTree1.isBalanced)
assert(exTree2.isBalanced)
assert(!tree3.isBalanced)
```

</details>

## Exercise 2

```scala
enum Expr:
  case Var(name: String)
  case Op(name: String, args: List[Expr])

import Expr._

final case class UnknownVarException(name: String) extends Exception
final case class UnknownOpException(name: String) extends Exception
```

There was multiple correct solutions. Here two possible solutions:

```scala
def eval1(e: Expr, context: Map[Var, Int]): Int = e match 
    case Var(name) => context.get(Var(name)) match
        case Some(n) => n
        case _ => throw UnknownVarException(name)
    case Op(name, args) =>
        val nargs = args.map(eval1(_, context))
        name match
            case "*" => nargs.foldLeft(1)(_ * _)
            case "+" => nargs.foldLeft(0)(_ + _)
            case _ => throw UnknownOpException(name)

def eval2(e: Expr, context: Map[Var, Int]): Int = e match 
    case sym: Var if context.contains(sym) => context(sym)
    case sym: Var => throw UnknownVarException(sym.name)
    case Op("*", args) => args.foldLeft(1)(_ * eval2(_, context))
    case Op("+", args) => args.foldLeft(0)(_ + eval2(_, context))
    case Op(name, _) => throw UnknownOpException(name)
```

<details>

<summary>Tests</summary>

```scala
for eval <- Seq(eval1, eval2) do
    assert(eval(Op("+", List()), Map()) == 0)
    assert(eval(Op("+", List(Var("x"))), Map(Var("x") -> 2)) == 2)
    assert(eval(Op("+", List(Var("x"), Var("y"))), Map(Var("x") -> 2, Var("y") -> 3)) == 5)
    assert(eval(Op("*", List()), Map()) == 1)
    assert(eval(Op("*", List(Var("x"))), Map(Var("x") -> 2)) == 2)
    assert(eval(Op("*", List(Var("x"), Var("y"))), Map(Var("x") -> 2, Var("y") -> 3)) == 6)
    assert(eval(Op("*", List(Op("+", List(Var("x"), Var("x"))), Var("y"))), Map(Var("x") -> 2, Var("y") -> 3)) == 12)
```

</details>

## Exercise 3

### Exercise 3.1

- Type parameter `A` in `map`
- `def map[B >: A](f: B => C): Transform[B, C]`

### Exercise 3.2

```
Is the following subtype assertion true?                yes    no

List[Triangle]            <:  List[AnyRef]              [X]    [ ]
List[Shape]               <:  List[AnyVal]              [ ]    [X]
List[String]              <:  List[Shape]               [ ]    [X]
Transform[Point, Circle]  <:  Transform[Point, Any]     [X]    [ ]
Transform[Point, Shape]   <:  Transform[Shape, Point]   [ ]    [X]
Transform[Shape, Point]   <:  Transform[Point, Shape]   [X]    [ ]
```

## Exercise 4

Axioms:

```
(1) Nil.reverse === Nil

(2) (x::xs).reverse === xs.reverse ++ (x::Nil)

(3) (xs++ys)++zs === xs++(ys++zs)

(4) Nil map f === Nil

(5) (x::xs) map f === f(x) :: (xs map f)

(6) Nil ++ ys === ys

(7) xs ++ Nil === xs

(8) x::xs ++ ys === x::(xs ++ ys)

(9) (l1 ++ l2).map(f) === l1.map(f) ++ l2.map(f)
```

### Exercise 4.1


```
We must prove:

(10) (l1 ++ l2).reverse === l2.reverse ++ l1.reverse


By induction on l1:

- l1 is Nil:

        (Nil ++ l2).reverse ===
    (6) l2.reverse

        l2.reverse ++ Nil.reverse ===
    (1) l2.reverse ++ Nil ===
    (7) l2.reverse

- l1 is x::xs

    IH: (xs ++ l2).reverse === l2.reverse ++ xs.reverse

         (x::xs ++ l2).reverse ===
    (8)  (x::(xs ++ l2)).reverse ===
    (2)  (xs ++ l2).reverse ++ (x::Nil) ===
    (IH) l2.reverse ++ xs.reverse ++ x::Nil ===
    (3)  l2.reverse ++ (xs.reverse ++ x::Nil) ===
    (2)  l2.reverse ++ (x::xs).reverse ===
         l2.reverse ++ l1.reverse
```

### Exercise 4.2

```
We must prove:

(l1 ++ l2).reverse.map(f) === l2.reverse.map(f) ++ l1.reverse.map(f)


Direct proof using axiom 10 proved in 4.1:

     (l1 ++ l2).reverse.map(f) =
(10) (l2.reverse ++ l1.reverse).map(f) =
(9)  l2.reverse.map(f) ++ l1.reverse.map(f)


Or without using axiom 10:

By induction on l1:

- l1 is Nil:

        ((l1 ++ l2).reverse).map(f) ===
    (6) l2.reverse.map.(f)

        l2.reverse.map(f) ++ l1.reverse.map(f) ===
    (1) l2.reverse.map(f) ++ Nil.map(f) ===
    (4) l2.reverse.map(f) ++ Nil ===
    (7) l2.reverse.map(f)


- l1 is x::xs

    IH: ((xs ++ l2).reverse).map(f) === l2.reverse.map(f) ++ xs.reverse.map(f)

         ((x::xs) ++ l2).reverse.map(f) ===
    (8)  (x::(xs ++ l2)).reverse.map(f) ===
    (2)  ((xs ++ l2).reverse ++ (x::Nil)).map(f) ===
    (9)  ((xs ++ l2).reverse.map(f)) ++ ((x::Nil).map(f)) ===
    (IH) l2.reverse.map(f) ++ xs.reverse.map(f) ++ (x::Nil).map(f) ===
    (3)  l2.reverse.map(f) ++ (xs.reverse.map(f) ++ (x::Nil).map(f)) ===
    (9)  l2.reverse.map(f) ++ (xs.reverse ++ x::Nil).map(f)) ===
    (2)  l2.reverse.map(f) ++ ((x::xs).reverse.map(f)) ===
```

## Exercise 5

### Exercise 5.1

There was multiple correct solutions:

```scala
def takeWhileStrictlyIncreasing1(list: List[Int]): List[Int] = list match
    case Nil => Nil
    case x :: Nil => list
    case x1 :: x2 :: xs => if x1 < x2 then x1 :: takeWhileStrictlyIncreasing1(x2 :: xs) else List(x1)

def takeWhileStrictlyIncreasing2(list: List[Int]): List[Int] = {
    def fun(ls: List[Int], last: Int): List[Int] = ls match
        case x :: xs if x > last => x :: fun(xs, x)
        case _ => Nil

    list match
        case x :: xs => x :: fun(xs, x)
        case Nil => Nil
}

def takeWhileStrictlyIncreasing3(list: List[Int]): List[Int] = {
    def fun(ls: List[Int], last: Option[Int]): List[Int] = (ls, last) match
        case (x :: xs, Some(last)) if x > last => x :: fun(xs, Some(x))
        case (x :: xs, None) => x :: fun(xs, Some(x))
        case _ => Nil

    fun(list, None)
}
```


**Comments**
- It was possible to write a correct implementation using foldLeft. Note that foldLeft traverses the whole list and cannot "early return" like a recursive call. This possible solution was not very clean as it required a flag or a condition to check that foldLeft should do nothing once it passed the first decreasing step. Avoid using foldLeft when you do not need to traverse the whole list every time.
- When we do not ask for a tail recursive implementation, the solution can be more readable without an accumulator. You should favor a simple and readable version.
- The solution `takeWhileStrictlyIncreasing3` uses `Option` and is elaborate. We include this solution for a good example of using `Option` but `takeWhileStrictlyIncreasing2` is simpler and more readable.

### Exercise 5.2

```scala
def increasingSequences(list: List[Int]): List[List[Int]] = list match
    case Nil => Nil
    case _ =>
        val prefix = takeWhileStrictlyIncreasing(list)
        prefix :: increasingSequences(list.drop(prefix.length))
```

**Comments**
- It is important to store `prefix` to avoid calling twice `takeWhileStrictlyIncreasing`.
- In the empty list case, some students made the confusion of returning a list containing the empty list. In this case, we have: `List[List[Int]]() == Nil != List(Nil) == List(List[Int]())`.