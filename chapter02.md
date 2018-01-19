# Chapter 2 Exercises
## 1.
```
def signum(i:Int) = {
    if (i>0) 1
    else if (i<0) -1
    0
}

def signum2(i:Int) = {
    i match {
        case i if i>0 => 1
        case i if i<0 => -1
        case _ => 0
    }
}
```

## 2.
```
var x = {}
//Unit
```

## 4.
```
for(i <- 10 to 1 by -1) println(i)
```

## 5.
```
def countdown(n:Int) = {
    for(i <- n to 0 by -1) println(i)  
}
```

## 6.
```
def product(s:String):Long = {
    var p:Long = 1;
    for(c <- s) p *= c.toLong
    p
}
```

## 7.
```
def product(s:String):Long = {
    s.foldLeft(1L)(_*_.toLong)
}
```

## 8.
// already done above

## 9.
```
def product(s:String):Long = {
    if (s.isEmpty) 1
    else product(s.tail) * s.head.toLong
}

import scala.annotation.tailrec

def product(str:String):Long = {
    @tailrec
    def innerProd(s:String, l:Long):Long = {
        s match {
            case s if s.isEmpty => l
            case _ => innerProd(s.tail, l * s.head)
        }
    }

    innerProd(str, 1)
}
```

## 10.
```
def pow(x:Double, n:Int): Double = {
    (x, n) match {
        //case (x, n) if n > 0 => x * pow(x, n-1)
        //case (x, n) if (n % 2 == 0 && n > 0) => pow(pow(x, n/2), 2)
        case (x, n) if (n % 2 == 0)&& n > 0) => pow(x, n/2) * pow(x, n/2)
        case (x, n) if (n % 2 == 1 && n > 0) => x * pow(x, n-1)
        case (x, n) if n == 0 => 1
        case (x, n) if n < 0 => 1 / pow(x, -n)
    }
}
```