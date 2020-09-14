# RandomUtils

> 随机数工具类
>
> 版本： 3.3+

## 类定义

~~~java
public class RandomUtils
~~~

## 构造函数

~~~java
// 代码编写过程中不要构造此类的实例
public RandomUtils()
~~~

## 普通函数

### nextBoolean

> 随机生成一个布尔值
>
> 版本： 3.5+

~~~java
// 声明
public static boolean nextBoolean()

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextBoolean();   // true
~~~

### nextBytes

> 随机生成一个指定长度的字节数组

~~~java
// 声明
public static byte[] nextBytes(final int count)

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextBytes(3);   // [-24, -9, 92]
~~~

### nextInt^1

> 随机生成一个指定范围内[startInclusive, endExclusive)的整数

~~~java
// 声明
public static int nextInt(final int startInclusive, final int endExclusive)

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextInt(3, 20);   // 12
~~~

### nextInt^2

> 随机生成一个整数
>
> 版本： 3.5+

~~~java
// 声明
public static int nextInt()

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextInt();   // 598
~~~

### nextLong^1

> 随机生成一个指定范围内[startInclusive, endExclusive)的长整数

~~~java
// 声明
public static long nextLong(final long startInclusive, final long endExclusive)

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextLong(3L, 200000L);  // 6728
~~~

### nextLong^2

> 随机生成一个长整数
>
> 版本： 3.5+

~~~java
// 声明
public static long nextLong()

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextLong();   // 62347274
~~~

### nextDouble^1

> 随机生成一个指定范围内[startInclusive, endExclusive)的双精度浮点数

~~~java
// 声明
public static double nextDouble(final double startInclusive, final double endExclusive)

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextFloat(1.2, 9.3);   // 7.985642250354838
~~~

### nextDouble^2

> 随机生成一个双精度浮点数
>
> 版本： 3.5+

~~~java
// 声明
public static double nextDouble()

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextDouble();   // 8.898622522936063E306
~~~

### nextFloat^1

> 随机生成一个指定范围内[startInclusive, endExclusive)的单精度浮点数

~~~java
// 声明
public static float nextFloat(final float startInclusive, final float endExclusive)

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextFloat(1.2f, 9.3f);   // 3.1761312
~~~

### nextFloat^2

> 随机生成一个单精度浮点数
>
> 版本： 3.5+

~~~java
// 声明
public static float nextFloat()

// 示例
// 结果是随机的，此处只做示例参考
RandomUtils.nextFloat();   // 2.1035796E38
~~~
