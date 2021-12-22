# 检查两个值元组<t1>在 C#中是否相等</t1>

> 原文:[https://www . geesforgeks . org/checking-two-value tuple-8-in-c-sharp 是否相等/](https://www.geeksforgeeks.org/checking-if-two-valuetuple-8-are-equal-or-not-in-c-sharp/)

[ValueTuple](https://www.geeksforgeeks.org/valuetuple-in-c-sharp/) 是 C# 7.0 中引入的一个结构，代表值类型 Tuple。它已经包含在中。. NET Framework 4.7 或更高版本。它允许您存储包含多个值的数据集，这些值可能彼此相关，也可能彼此不相关。

在[值元组< T1、T2、T3、T4、T5、T6、T7、TRest>T1 中，可以使用 Equals 方法检查两个值元组是否相同。或者换句话说，我们可以说这个方法将返回一个值，该值指示给定的 ValueTuple < T1、T2、T3、T4、T5、T6、T7、TRest >实例是否等于指定的对象。如果给定值元组相等，它将返回 true，否则返回 false。该方法可以通过两种不同的方式重载:](https://www.geeksforgeeks.org/c-sharp-valuetuple-8-struct/)

1.  **[等于(ValueTuple < T1、T2、T3、T4、T5、T6、T7、TRest >)方法](#Equals(ValueTuple<T1, T2, T3, T4, T5, T6, T7, TRest >) Method)**
2.  **[等于(对象)法](#Equals(Object) Method)**

### 1.等于(值元组< T1、T2、T3、T4、T5、T6、T7、TRest >)方法

Equals(ValueTuple <t1 t2="" t3="" t4="" t5="" t6="" t7="" trest="">)方法用于检查两个 ValueTuple <t1 t2="" t3="" t4="" t5="" t6="" t7="" trest="">实例是否相等。它总是返回真。这种方法的返回类型是*系统。布尔*。在 Equals(ValueTuple < T1、T2、T3、T4、T5、T6、T7、TRest >方法中，在以下条件下，其他参数被认为等于当前实例:</t1></t1>

*   组件的类型与当前实例的类型相同。
*   元素等于当前实例的元素，每个元素的相等性由默认的相等性比较器确定。

**语法:**

```
public bool Equals (ValueTuple<T1, T2, T3, T4, T5, T6, T7, TRest> other);
```

这里，另一个是与当前实例进行比较的值元组。

**返回类型:**该方法的返回类型为*系统。布尔*。如果给定实例等于指定实例，则返回 true。否则，它返回 false。

**示例:**

```
// C# program to illustrate the use of
// Equals(ValueTuple<T1, T2, T3, T4,
// T5, T6, T7, TRest>) Method
using System;

namespace exampleofvaluetuple {

class GFG {

    // Main Method
    static void Main(string[] args)
    {
        // 8-ValueTuple
        var u1 = ValueTuple.Create(4, 3, 5, 3, 9, 98, 1, 78);
        var u2 = ValueTuple.Create(4, 3, 5, 3, 9, 76, 98, 100);
        Console.WriteLine("Result 1: {0}", u1.Equals(u2));

        // 10-ValueTuple
        var y1 = ValueTuple.Create(4, 3, 5, 3, 9, 98, 1, (1, 2, 3));
        var y2 = ValueTuple.Create(4, 3, 5, 3, 9, 98, 1, (1, 2, 3));
        Console.WriteLine("Result 2: {0}", y1.Equals(y2));

        // 13-ValueTuple
        var a1 = ValueTuple.Create(4, 3, 5, 3, 9, 98, 1, (1, 2, 3, 7, 8, 9));
        var a2 = ValueTuple.Create(4, 3, 5, 3, 9, 98, 1, (1, 2, 3, 7, 8, 30));
        Console.WriteLine("Result 3: {0}", a1.Equals(a2));
    }
}
}
```

**Output:**

```
Result 1: False
Result 2: True
Result 3: False

```

### 2.等于(对象)方法

在 [ValueTuple < T1、T2、T3、T4、T5、T6、T7、TRest >](https://www.geeksforgeeks.org/c-sharp-valuetuple-8-struct/) 中，Equals(Object)方法用于返回一个值，该值显示当前实例等于指定的对象。在 Equals(Object)方法中，在以下条件下，obj 被认为等于当前实例:

*   它是一个 ValueTuple 值类型。
*   组件的类型与当前实例的类型相同。
*   元素等于当前实例的元素，每个元素的相等性由默认的相等性比较器确定。

**语法:**

```
public override bool Equals (object obj);
```

这里，obj 是要与此实例进行比较的对象。

**返回类型:**该方法的返回类型为*系统。布尔*。如果给定实例等于指定对象，则返回 true。否则，返回 false。

**示例:**

```
// C# program to illustrate the 
// use of Equals(Object) method
using System;

namespace exampleofvaluetuple {

class GFG {

    // Main Method
    static void Main(string[] args)
    {
        // 8-ValueTuple
        var u1 = ValueTuple.Create(4, 3, 5, 3, 9, 98, 1, 78);
        var u2 = ValueTuple.Create(4, 3, 5, 3, 9, 98, 1, 78);

        // Checking the given value
        // tuples are equal or not
        // Using Equal() Method
        if (u1.Equals(u2) == true) {

            Console.WriteLine("Both value tuples are equal");
        }
        else {
            Console.WriteLine("Both value tuples are not equal");
        }
    }
}
}
```

**Output:**

```
Both value tuples are equal

```