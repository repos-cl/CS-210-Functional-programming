# Exercise Session 9, Solutions

## Question 1

```scala mdoc
def groupBy[T, S](f: T => S)(xs: List[T]): Map[S, List[T]] =
    var result = Map[S, List[T]]()
    xs.reverse.foreach(el =>
        val key = f(el)
        val prevValue = result.getOrElse(key, List())
        result = result.updated(key, el :: prevValue)
    )
    result
```

```scala mdoc
def groupBy2[T, S](f: T => S)(xs: List[T]): Map[S, List[T]] =
    xs.foldRight(Map[S, List[T]]())((el: T, acc: Map[S, List[T]]) =>
        val key = f(el)
        val prevValue = acc.getOrElse(key, List())
        acc.updated(key, el :: prevValue)
    )
```

Example run:

```scala mdoc
groupBy[Int, Int](_ % 3)((0 to 10).toList)
```

## Question 2

### Question 2.1

```scala mdoc:invisible
trait Logger:
    def log(message: String): Unit
```

```scala mdoc
class LoggerBuffered extends Logger:
    private var output: String = ""
    def log(message: String): Unit = output = output + message + "\n"
    def getOutput(): String = output
```

### Question 2.2

```scala mdoc:invisible
enum Expr:
  case Var(name: String)
  case Op(name: String, args: List[Expr])

import Expr._

final case class UnknownVarException(name: String) extends Exception
final case class UnknownOpException(name: String) extends Exception

def eval(e: Expr, context: Map[Var, Int]): Int = e match 
    case sym: Var if context.contains(sym) => context(sym)
    case sym: Var => throw UnknownVarException(sym.name)
    case Op("*", args) => args.map(eval(_, context)).foldLeft(1)(_ * _)
    case Op("+", args) => args.map(eval(_, context)).foldLeft(0)(_ + _)
    case Op(name, _) => throw UnknownOpException(name)
```

```scala mdoc
def evalTracing(e: Expr, context: Map[Var, Int])(using logger: Logger): Int = e match 
    case sym: Var if context.contains(sym) =>
        val value = context(sym)
        logger.log(f"Get var ${sym.name} = ${value} from the context.\n")
        value
    case sym: Var => throw UnknownVarException(sym.name)
    case Op(name, args) =>
        val evaluatedArgs= args.map(evalTracing(_, context))
        logger.log(f"Apply operation ${name} to arguments ${evaluatedArgs.mkString(",")}")
        name match
            case "*" => evaluatedArgs.foldLeft(1)(_ * _)
            case "+" => evaluatedArgs.foldLeft(0)(_ + _)
            case _   => throw UnknownOpException(name)
```