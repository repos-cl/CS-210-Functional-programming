# Exercise Session 9, Solutions

## Question 1

```scala
def groupBy[T, S](f: T => S)(xs: List[T]): Map[S, List[T]] =
    var result = Map[S, List[T]]()
    xs.foreach(el =>
        val key = f(el)
        val prevValue = result.getOrElse(key, List())
        result = result.updated(key, el :: prevValue)
    )
    result
```

```scala
def groupBy2[T, S](f: T => S)(xs: List[T]): Map[S, List[T]] =
    xs.foldLeft(Map[S, List[T]]())((acc: Map[S, List[T]], el: T) =>
        val key = f(el)
        val prevValue = acc.getOrElse(key, List())
        acc.updated(key, el :: prevValue)
    )
```

## Question 2

### Question 2.1


```scala
class LoggerBuffered extends Logger:
    private var output: String = ""
    def log(message: String): Unit = output = output + message + "\n"
    def getOutput(): String = output
```

### Question 2.2


```scala
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