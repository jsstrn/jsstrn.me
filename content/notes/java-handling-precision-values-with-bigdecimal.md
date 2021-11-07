---
title: "Handling precision values in Java with BigDecimal"

tags: [java]
categories: [software engineering]
---

When it comes to handling values that require precision, using data types like `float` and `double` may result in unexpected behavior.

```java
double doubleValue = 0.012;
double doubleSum = doubleValue + doubleValue + doubleValue;
```

In this example, we would expect the `sum` to be `0.036`, but instead we get `0.036000000000000004`.

This can lead to a lot of issues when we are dealing with currency conversion. For this reason, it is recommended to use `BigDecimal` instead.

We first create a new `BigDecimal` value with the `.valueOf()` static method.

```java
BigDecimal bigValue = BigDecimal.valueOf(doubleValue);
```

`bigValue` is a `BigDecimal` object which has a `.add()` instance method that can be chained.

```java
BigDecimal bigSum = bigValue.add(bigValue).add(bigValue);
```

We now get the correct result of `0.036`. If we want, we can convert this value back to `double` with the `.doubleValue()` method.

```java
double doubleSumConverted = bigSum.doubleValue();
```

## Reference

- [BigDecimal](https://docs.oracle.com/en/java/javase/16/docs/api/java.base/java/math/BigDecimal.html) – Java SE 16 & JDK 16
