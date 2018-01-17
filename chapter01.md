# Exercises
## 1.
```
3.
!=   <    >>>         doubleValue   isNaN           isValidShort   shortValue       toDouble        toShort      
%    <<   ^           floatValue    isNegInfinity   isWhole        signum           toFloat         unary_+      
&    <=   abs         floor         isPosInfinity   longValue      to               toHexString     unary_-      
*    ==   byteValue   getClass      isValidByte     max            toBinaryString   toInt           unary_~      
+    >    ceil        intValue      isValidChar     min            toByte           toLong          underlying   
-    >=   compare     isInfinite    isValidInt      round          toChar           toOctalString   until        
/    >>   compareTo   isInfinity    isValidLong     self           toDegrees        toRadians       |            
```

## 2.
```
val sqrt = math.sqrt(3)
//1.7320508075688772

val sqr = math.pow(sqrt, 2)
//2.9999999999999996
```

## 3
```
math.sqrt(3)
res0 = 1.0
// error: reassignment to val
```

## 4.
```val s = "crazy" * 3
//crazycrazycrazy
```

## 5.
```val i = 10 max 2
//Returns this if this > that or that otherwise.
```

## 6.
```
val bi = BigInt(2)
bi.pow(bi, 1024)
```

## 7.
```
import scala.util.
import scala.BigInt.probablePrime
```

## 8.
```
val rbi = BigInt(128, util.Random)
val filename = rbi.toString(36)
```

## 9.
```
filename.head 
// or
filename(0)

filename.last
filename(filename.length-1)
```

## 10.
```
filename.take(2)
filename.drop(2)
filename.takeRight(2)
filenae.dropRight(2)
```
