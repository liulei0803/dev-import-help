# ArrayUtils

> 为数组操作及数组封装提供一系列简便操作
> 
> 版本： 2.0+

## 类定义

~~~java
public class ArrayUtils
~~~

## 构造函数

>编程过程中不要去构建实例，此默认构造方法为需要提供JavaBean实例的工具使用

~~~java
public ArrayUtils()
~~~

## 静态属性

~~~java
// 空的不可修改的boolean数组
public static final boolean[] EMPTY_BOOLEAN_ARRAY = new boolean[0];

// 空的不可修改的Boolean数组
public static final Boolean[] EMPTY_BOOLEAN_OBJECT_ARRAY = new Boolean[0];

// 空的不可修改的byte数组
public static final byte[] EMPTY_BYTE_ARRAY = new byte[0];

// 空的不可修改的Byte数组
public static final Byte[] EMPTY_BYTE_OBJECT_ARRAY = new Byte[0];

// 空的不可修改的char数组
public static final char[] EMPTY_CHAR_ARRAY = new char[0];

// 空的不可修改的Character数组
public static final Character[] EMPTY_CHARACTER_OBJECT_ARRAY = new Character[0];

// 空的不可修改的Class数组
public static final Class<?>[] EMPTY_CLASS_ARRAY = new Class[0];

// 空的不可修改的double数组
public static final double[] EMPTY_DOUBLE_ARRAY = new double[0];

// 空的不可修改的Double数组
public static final Double[] EMPTY_DOUBLE_OBJECT_ARRAY = new Double[0];

// 空的不可修改的Field数组
// 版本： 3.10+
public static final Field[] EMPTY_FIELD_ARRAY = new Field[0];

// 空的不可修改的float数组
public static final float[] EMPTY_FLOAT_ARRAY = new float[0];

// 空的不可修改的Float数组
public static final Float[] EMPTY_FLOAT_OBJECT_ARRAY = new Float[0];

// 空的不可修改的int数组
public static final int[] EMPTY_INT_ARRAY = new int[0];

// 空的不可修改的Integer数组
public static final Integer[] EMPTY_INTEGER_OBJECT_ARRAY = new Integer[0];

// 空的不可修改的long数组
public static final long[] EMPTY_LONG_ARRAY = new long[0];

// 空的不可修改的Long数组
public static final Long[] EMPTY_LONG_OBJECT_ARRAY = new Long[0];

// 空的不可修改的Method数组
// 版本： 3.10+
public static final Method[] EMPTY_METHOD_ARRAY = new Method[0];

// 空的不可修改的Object数组
public static final Object[] EMPTY_OBJECT_ARRAY = new Object[0];

// 空的不可修改的short数组
public static final short[] EMPTY_SHORT_ARRAY = new short[0];

// 空的不可修改的Short数组
public static final Short[] EMPTY_SHORT_OBJECT_ARRAY = new Short[0];

// 空的不可修改的String数组
public static final String[] EMPTY_STRING_ARRAY = new String[0];

// 空的不可修改的Throwable数组
// 版本： 3.10+
public static final Throwable[] EMPTY_THROWABLE_ARRAY = new Throwable[0];

// 空的不可修改的Type数组
// 版本： 3.10+
public static final Type[] EMPTY_TYPE_ARRAY = new Type[0];

// 当目标元素在数组中不存在时返回的索引值
public static final int INDEX_NOT_FOUND = -1;
~~~

## 函数方法

### add^1

> 添加一个boolean元素element到一个boolean数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static boolean[] add(final boolean[] array, final boolean element)

// 示例
boolean[] array = new boolean[]{true, false};
ArrayUtils.add(null, true);          // [true]
ArrayUtils.add(array, true);         // [true, false, true]
~~~

### add^2

> 添加一个byte元素element到一个byte数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static byte[] add(final byte[] array, final byte element)

// 示例
byte[] array = new byte[]{1, 2};
ArrayUtils.add(null, (byte)3);     // [0]
ArrayUtils.add(array, (byte)3);    // [1, 2, 3]
~~~

### add^3

> 添加一个char元素element到一个char数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static char[] add(final char[] array, final char element)

// 示例
char[] array = new char[]{'a', 'b'};
ArrayUtils.add(null, 'c');       // ['c']
ArrayUtils.add(array, 'c');      // ['a', 'b', 'c']
~~~

### add^4

> 添加一个double元素element到一个double数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static double[] add(final double[] array, final double element)

// 示例
double[] array = new double[]{1.0, 2.0};
ArrayUtils.add(null, 3.0);   // [3.0]
ArrayUtils.add(array, 1.0);  // [1.0, 2.0, 3.0]
~~~

### add^5

> 添加一个float元素element到一个float数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static float[] add(final float[] array, final float element)

// 示例
float[] array = new float[]{1.0f, 2.0f};
ArrayUtils.add(null, 3.0f);     // [3.0f]
ArrayUtils.add(array, 3.0f);    // [1.0f, 2.0f, 3.0f]
~~~

### add^6

> 添加一个int元素element到一个int数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static int[] add(final int[] array, final int element)

// 示例
int[] array = new int[]{1, 2};
ArrayUtils.add(null, 0);     // [0]
ArrayUtils.add(array, 0);    // [1, 2, 0]
~~~

### add^7

> 添加一个long元素element到一个long数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static long[] add(final long[] array, final long element)

// 示例
long[] array = new long[]{1L, 2L};
ArrayUtils.add(null, 0L);     // [0L]
ArrayUtils.add(array, 3L);    // [1L, 2L, 3L]
~~~

### add^8

> 添加一个short元素element到一个short数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static short[] add(final short[] array, final short element)

// 示例
short[] array = new short[]{1, 2};
ArrayUtils.add(null, (short)0);     // [0]
ArrayUtils.add(array, (short)3);    // [1, 2, 3]
~~~

### add^9

> 添加一个类元素element到一个类数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static <T> T[] add(final T[] array, final T element)

// 示例
String[] array = new String[]{"a", "b"};
ArrayUtils.add(null, null);      // IllegalArgumentException
ArrayUtils.add(null, "a");       // ["a"]
ArrayUtils.add(array, null);     // ["a", null]
ArrayUtils.add(array, "b");      // ["a", "b"]
~~~

### addAll^1

> 添加多个boolean元素element到一个boolean数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static boolean[] addAll(final boolean[] array1, final boolean... array2)

// 示例
boolean[] array = new boolean[]{true, false};
ArrayUtils.addAll(array, null);          // [true, false]
ArrayUtils.addAll(null, array);          // [true, false]
ArrayUtils.addAll(array, false, true);   // [true, false, false, true]
~~~

### addAll^2

> 添加多个byte元素element到一个byte数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static byte[] addAll(final byte[] array1, final byte... array2)

// 示例
byte[] array = new byte[]{1, 2};
ArrayUtils.addAll(array, null);               // [1, 2]
ArrayUtils.addAll(null, array);               // [1, 2]
ArrayUtils.addAll(array, (byte)3, (byte)4);   // [1, 2, 3, 4]
~~~

### addAll^3

> 添加多个char元素element到一个char数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static char[] addAll(final char[] array1, final char... array2)

// 示例
char[] array = new char[]{'a', 'b'};
ArrayUtils.addAll(array, null);               // ['a', 'b']
ArrayUtils.addAll(null, array);               // ['a', 'b']
ArrayUtils.addAll(array, 'c', 'd');           // ['a', 'b', 'c', 'd']
~~~

### addAll^4

> 添加多个double元素element到一个double数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static double[] addAll(final double[] array1, final double... array2)

// 示例
double[] array = new double[]{1.0, 2.0};
ArrayUtils.addAll(array, null);               // [1.0, 2.0]
ArrayUtils.addAll(null, array);               // [1.0, 2.0]
ArrayUtils.addAll(array, 3.0, 4.0);           // [1.0, 2.0, 3.0, 4.0]
~~~

### addAll^5

> 添加多个float元素element到一个float数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static float[] addAll(final float[] array1, final float... array2)

// 示例
float[] array = new float[]{1.0f, 2.0f};
ArrayUtils.addAll(array, null);               // [1.0, 2.0]
ArrayUtils.addAll(null, array);               // [1.0, 2.0]
ArrayUtils.addAll(array, 3.0f, 4.0f);           // [1.0, 2.0, 3.0, 4.0]
~~~

### addAll^6

> 添加多个int元素element到一个int数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static int[] addAll(final int[] array1, final int... array2)

// 示例
int[] array = new int[]{1, 2};
ArrayUtils.addAll(array, null);               // [1, 2]
ArrayUtils.addAll(null, array);               // [1, 2]
ArrayUtils.addAll(array, 3, 4);               // [1, 2, 3, 4]
~~~

### addAll^7

> 添加多个long元素element到一个long数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static long[] addAll(final long[] array1, final long... array2)

// 示例
long[] array = new long[]{1L, 2L};
ArrayUtils.addAll(array, null);                 // [1, 2]
ArrayUtils.addAll(null, array);                 // [1, 2]
ArrayUtils.addAll(array, 3L, 4L);               // [1, 2, 3, 4]
~~~

### addAll^8

> 添加多个short元素element到一个short数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static short[] addAll(final short[] array1, final short... array2)

// 示例
short[] array = new short[]{1, 2};
ArrayUtils.addAll(array, null);                 // [1, 2]
ArrayUtils.addAll(null, array);                 // [1, 2]
ArrayUtils.addAll(array, (short)3, (short)4);   // [1, 2, 3, 4]
~~~

### addAll^9

> 添加多个类元素element到一个类数组array的末尾，并返回一个新数组。

~~~java
// 声明
// 版本： 2.1+
public static <T> T[] addAll(final T[] array1, @SuppressWarnings("unchecked") final T... array2)

// 示例
String[] array = new String[]{"a", "b"};
ArrayUtils.addAll(array, null);                 // ["a", "b"]
ArrayUtils.addAll(null, array);                 // ["a", "b"]
ArrayUtils.addAll(array, "c", "d");             // ["a", "b", "c", "d"]
~~~

### addFirst^1

> 添加一个boolean元素element到一个boolean数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static boolean[] addFirst(final boolean[] array, final boolean element)

// 示例
boolean[] array = new boolean[]{true, false};
ArrayUtils.addFirst(null, true);              // [true]
ArrayUtils.addFirst(array, false);            // [false, true, false]
~~~

### addFirst^2

> 添加一个byte元素element到一个byte数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static byte[] addFirst(final byte[] array, final byte element)

// 示例
byte[] array = new byte[]{1, 2};
ArrayUtils.addFirst(null, (byte)1);             // [1]
ArrayUtils.addFirst(array, (byte)3);            // [3, 1, 2]
~~~

### addFirst^3

> 添加一个char元素element到一个char数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static char[] addFirst(final char[] array, final char element)

// 示例
char[] array = new char[]{'a', 'b'};
ArrayUtils.addFirst(null, 'a');             // ['a']
ArrayUtils.addFirst(array, 'c');            // ['c', 'a', 'b']
~~~

### addFirst^4

> 添加一个double元素element到一个double数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static double[] addFirst(final double[] array, final double element)

// 示例
double[] array = new double[]{1.0, 2.0};
ArrayUtils.addFirst(null, 1.0);             // [1.0]
ArrayUtils.addFirst(array, 3.0);            // [3.0, 1.0, 2.0]
~~~

### addFirst^5

> 添加一个float元素element到一个float数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static float[] addFirst(final float[] array, final float element)

// 示例
float[] array = new float[]{1.0f, 2.0f};
ArrayUtils.addFirst(null, 1.0f);             // [1.0]
ArrayUtils.addFirst(array, 3.0f);            // [3.0, 1.0, 2.0]
~~~

### addFirst^6

> 添加一个int元素element到一个int数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static int[] addFirst(final int[] array, final int element)

// 示例
int[] array = new int[]{1, 2};
ArrayUtils.addFirst(null, 1);             // [1]
ArrayUtils.addFirst(array, 3);            // [3, 1, 2]
~~~

### addFirst^7

> 添加一个long元素element到一个long数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static long[] addFirst(final long[] array, final long element)

// 示例
long[] array = new long[]{1L, 2L};
ArrayUtils.addFirst(null, 1L);             // [1]
ArrayUtils.addFirst(array, 3L);            // [3, 1, 2]
~~~

### addFirst^8

> 添加一个short元素element到一个short数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static short[] addFirst(final short[] array, final short element)

// 示例
short[] array = new short[]{1, 2};
ArrayUtils.addFirst(null, (short)1);             // [1]
ArrayUtils.addFirst(array, (short)3);            // [3, 1, 2]
~~~

### addFirst^9

> 添加一个类元素element到一个类数组array的头部，并返回一个新数组。

~~~java
// 声明
// 版本： 3.10+
public static <T> T[] addFirst(final T[] array, final T element)

// 示例
String[] array = new String[]{"a", "b"};
ArrayUtils.addFirst(null, "c");             // ["c"]
ArrayUtils.addFirst(array, "c");            // ["c", "a", "b"]
~~~

### clone^1

> 克隆一个boolean数组array。

~~~java
// 声明
public static boolean[] clone(final boolean[] array)

// 示例
Object[] nil = null;
boolean[] array = new boolean[]{true, false};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // [true, false]
~~~

### clone^2

> 克隆一个byte数组array。

~~~java
// 声明
public static byte[] clone(final byte[] array)

// 示例
Object[] nil = null;
byte[] array = new byte[]{1, 2};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // [1, 2]
~~~

### clone^3

> 克隆一个char数组array。

~~~java
// 声明
public static char[] clone(final char[] array)

// 示例
Object[] nil = null;
char[] array = new char[]{'a', 'b'};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // ['a', 'b']
~~~

### clone^4

> 克隆一个double数组array。

~~~java
// 声明
public static double[] clone(final double[] array)

// 示例
Object[] nil = null;
double[] array = new double[]{1.0, 2.0};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // [1.0, 2.0]
~~~

### clone^5

> 克隆一个float数组array。

~~~java
// 声明
public static float[] clone(final float[] array)

// 示例
Object[] nil = null;
float[] array = new float[]{1.0f, 2.0f};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // [1.0, 2.0]
~~~

### clone^6

> 克隆一个float数组array。

~~~java
// 声明
public static int[] clone(final int[] array)

// 示例
Object[] nil = null;
int[] array = new int[]{1, 2};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // [1, 2]
~~~

### clone^7

> 克隆一个long数组array。

~~~java
// 声明
public static long[] clone(final long[] array)

// 示例
Object[] nil = null;
long[] array = new long[]{1L, 2L};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // [1, 2]
~~~

### clone^8

> 克隆一个short数组array。

~~~java
// 声明
public static short[] clone(final short[] array)

// 示例
Object[] nil = null;
short[] array = new short[]{1, 2};
ArrayUtils.clone(nil);               // null
ArrayUtils.clone(array);             // [1, 2]
~~~

### clone^9

> 克隆一个类数组array, 返回一个新数组，数组中的元素还是原来的元素

~~~java
// 声明
public static <T> T[] clone(final T[] array)

// 示例
Object[] nil = null;
Object obj1 = new Object();
Object obj2 = new Object();
Object[] array = new Object[]{obj1, obj2};
ArrayUtils.clone(nil);                          // null
Object[] array2 = ArrayUtils.clone(array);      // [obj1, obj2]
array == array2;                                // false
array[0] == array2[0];                          // true
array[1] == array2[1];                          // true
~~~

### contains^1

> 检查一个boolean数组array中是否包含指定boolean元素valueToFind

~~~java
// 声明
public static boolean contains(final boolean[] array, final boolean valueToFind)

// 示例
boolean[] nil = null;
boolean[] array = new boolean[]{true};
ArrayUtils.contains(nil, false);           // false
ArrayUtils.contains(array, true);          // true
ArrayUtils.contains(array, false);         // false
~~~

### contains^2

> 检查一个byte数组array中是否包含指定byte元素valueToFind

~~~java
// 声明
public static boolean contains(final byte[] array, final byte valueToFind)

// 示例
byte[] nil = null;
byte[] array = new byte[]{1, 2};
ArrayUtils.contains(nil, 1);           // false
ArrayUtils.contains(array, 1);         // true
ArrayUtils.contains(array, 3);         // false
~~~

### contains^3

> 检查一个char数组array中是否包含指定char元素valueToFind

~~~java
// 声明
public static boolean contains(final char[] array, final char valueToFind)

// 示例
char[] nil = null;
char[] array = new char[]{'a', 'b'};
ArrayUtils.contains(nil, 'a');           // false
ArrayUtils.contains(array, 'a');         // true
ArrayUtils.contains(array, 'c');         // false
~~~

### contains^4

> 检查一个double数组array中是否包含指定double元素valueToFind

~~~java
// 声明
public static boolean contains(final double[] array, final double valueToFind)

// 示例
double[] nil = null;
double[] array = new double[]{1.0, 2.0};
ArrayUtils.contains(nil, 1.0);           // false
ArrayUtils.contains(array, 1.0);         // true
ArrayUtils.contains(array, 3.0);         // false
~~~

### contains^5

> 检查一个double数组array中是否包含指定double元素valueToFind，并且可以接受一个误差范围tolerance

~~~java
// 声明
public static boolean contains(final double[] array, final double valueToFind, final double tolerance)

// 示例
double[] nil = null;
double[] array = new double[]{1.0, 2.0};
ArrayUtils.contains(nil, 1.0, 1.0);           // false
ArrayUtils.contains(array, 1.0, 1.0);         // true
ArrayUtils.contains(array, 3.0, 2.0);         // true
ArrayUtils.contains(array, 5.0, 2.0);         // false
~~~

### contains^6

> 检查一个float数组array中是否包含指定float元素valueToFind

~~~java
// 声明
public static boolean contains(final float[] array, final float valueToFind)

// 示例
float[] nil = null;
float[] array = new float[]{1.0f, 2.0f};
ArrayUtils.contains(nil, 1.0f);           // false
ArrayUtils.contains(array, 1.0f);         // true
ArrayUtils.contains(array, 3.0f);         // false
~~~

### contains^7

> 检查一个int数组array中是否包含指定int元素valueToFind

~~~java
// 声明
public static boolean contains(final int[] array, final int valueToFind)

// 示例
int[] nil = null;
int[] array = new int[]{1, 2};
ArrayUtils.contains(nil, 1);           // false
ArrayUtils.contains(array, 1);         // true
ArrayUtils.contains(array, 3);         // false
~~~

### contains^8

> 检查一个long数组array中是否包含指定long元素valueToFind

~~~java
// 声明
public static boolean contains(final long[] array, final long valueToFind)

// 示例
long[] nil = null;
long[] array = new long[]{1L, 2L};
ArrayUtils.contains(nil, 1L);           // false
ArrayUtils.contains(array, 1L);         // true
ArrayUtils.contains(array, 3L);         // false
~~~

### contains^9

> 检查一个short数组array中是否包含指定short元素valueToFind

~~~java
// 声明
public static boolean contains(final short[] array, final short valueToFind)

// 示例
short[] nil = null;
short[] array = new short[]{1, 2};
ArrayUtils.contains(nil, (short)1);           // false
ArrayUtils.contains(array, (short)1);         // true
ArrayUtils.contains(array, (short)3);         // false
~~~

### get^1

> 获取类数组array中指定索引index位置的元素
>
> 版本： 3.11

~~~java
// 声明
public static <T> T get(final T[] array, final int index)

// 示例
String[] nil = null;
String[] array = new String[]{"abc", "def"};
ArrayUtils.get(nil, 1);           // null
ArrayUtils.get(array, 1);         // def
ArrayUtils.get(array, 3);         // null
~~~

### get^2

> 获取类数组array中指定索引index位置的元素，找不到时返回一个指定的默认值defaultValue
>
> 版本： 3.11

~~~java
// 声明
public static <T> T get(final T[] array, final int index, final T defaultValue)

// 示例
String[] nil = null;
String[] array = new String[]{"abc", "def"};
ArrayUtils.get(nil, 1, "zzz");           // zzz
ArrayUtils.get(array, 1, "zzz");         // def
ArrayUtils.get(array, 3, "zzz");         // zzz
~~~

### getLength

> 获取数组array的元素个数
>
> 版本： 2.1

~~~java
// 声明
public static int getLength(final Object array)

// 示例
String[] nil = null;
String[] array = new String[]{"abc", "def"};
ArrayUtils.getLength(nil);           // 0
ArrayUtils.getLength(array);         // 0
~~~

### hashCode

> 计算数组array的哈希值

~~~java
// 声明
public static int hashCode(final Object array)

// 示例
String[] nil = null;
String[] array = new String[]{"abc", "def"};
ArrayUtils.hashCode(nil);           // 629
ArrayUtils.hashCode(array);         // 3687704
~~~

### indexesOf^1

> 查找boolean数组array中指定boolean元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final boolean[] array, final boolean valueToFind)

// 示例
boolean[] nil = null;
boolean[] array = new boolean[]{true, false, false, true};
ArrayUtils.indexesOf(nil, true);             // {}
ArrayUtils.indexesOf(array, true);           // {0, 3}
ArrayUtils.indexesOf(array, false);          // {1, 2}
~~~

### indexesOf^2

> 从指定位置startIndex开始查找boolean数组array中指定boolean元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final boolean[] array, final boolean valueToFind, int startIndex)

// 示例
boolean[] nil = null;
boolean[] array = new boolean[]{true, false, false, true};
ArrayUtils.indexesOf(nil, true, 1);             // {}
ArrayUtils.indexesOf(array, true, 1);           // {3}
ArrayUtils.indexesOf(array, false, 1);          // {1, 2}
~~~

### indexesOf^3

> 查找byte数组array中指定byte元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final byte[] array, final byte valueToFind)

// 示例
byte[] nil = null;
byte[] array = new byte[]{1, 2, 3, 1, 2};
ArrayUtils.indexesOf(nil, (byte)1);            // {}
ArrayUtils.indexesOf(array, (byte)1);          // {0, 3}
ArrayUtils.indexesOf(array, (byte)2);          // {1, 4}
~~~

### indexesOf^4

> 从指定位置startIndex开始查找byte数组array中指定byte元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final byte[] array, final byte valueToFind, int startIndex)

// 示例
byte[] nil = null;
byte[] array = new byte[]{1, 2, 3, 1, 2};
ArrayUtils.indexesOf(nil, (byte)1, 1);            // {}
ArrayUtils.indexesOf(array, (byte)1, 1);          // {3}
ArrayUtils.indexesOf(array, (byte)2, 1);          // {1, 4}
~~~

### indexesOf^5

> 查找char数组array中指定char元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final char[] array, final char valueToFind)

// 示例
char[] nil = null;
char[] array = new char[]{'a', 'b', 'c', 'a', 'c'};
ArrayUtils.indexesOf(nil, 'a');            // {}
ArrayUtils.indexesOf(array, 'a');          // {0, 3}
ArrayUtils.indexesOf(array, 'b');          // {1}
~~~

### indexesOf^6

> 从指定位置startIndex开始查找char数组array中指定char元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final char[] array, final char valueToFind, int startIndex)

// 示例
char[] nil = null;
char[] array = new char[]{'a', 'b', 'c', 'a', 'c'};
ArrayUtils.indexesOf(nil, 'a', 1);            // {}
ArrayUtils.indexesOf(array, 'a', 1);          // {3}
ArrayUtils.indexesOf(array, 'b', 1);          // {1}
~~~

### indexesOf^7

> 查找double数组array中指定double元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final double[] array, final double valueToFind)

// 示例
double[] nil = null;
double[] array = new double[]{1.1, 2.2, 3.3, 1.1, 2.2, 3.3};
ArrayUtils.indexesOf(nil, 1.1);            // {}
ArrayUtils.indexesOf(array, 1.1);          // {0, 3}
ArrayUtils.indexesOf(array, 3.3);          // {2, 5}
~~~

### indexesOf^8

> 查找double数组array中指定double元素valueToFind的索引位集，允许一定的精度误差tolerance

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final double[] array, final double valueToFind, final double tolerance)

// 示例
double[] nil = null;
double[] array = new double[]{1.1, 2.2, 3.3, 1.1, 2.2, 3.3};
ArrayUtils.indexesOf(nil, 1.1, 0.1);            // {}
ArrayUtils.indexesOf(array, 1.2, 0.1);          // {0, 3}
ArrayUtils.indexesOf(array, 3.6, 0.1);          // {}
~~~

### indexesOf^9

> 从指定位置startIndex开始查找double数组array中指定double元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final double[] array, final double valueToFind, int startIndex)

// 示例
double[] nil = null;
double[] array = new double[]{1.1, 2.2, 3.3, 1.1, 2.2, 3.3};
ArrayUtils.indexesOf(nil, 1.1, 0);            // {}
ArrayUtils.indexesOf(array, 1.1, 0);          // {0, 3}
ArrayUtils.indexesOf(array, 3.3, 3);          // {5}
~~~

### indexesOf^10

> 从指定位置startIndex开始查找double数组array中指定double元素valueToFind的索引位集，允许一定的精度误差tolerance

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final double[] array, final double valueToFind, int startIndex, final double tolerance)

// 示例
double[] nil = null;
double[] array = new double[]{1.1, 2.2, 3.3, 1.1, 2.2, 3.3};
ArrayUtils.indexesOf(nil, 1.2, 0, 0.1);            // {}
ArrayUtils.indexesOf(array, 1.2, 0, 0.1);          // {0, 3}
ArrayUtils.indexesOf(array, 3.0, 3, 0.4);          // {5}
ArrayUtils.indexesOf(array, 3.6, 3, 0.2);          // {}
~~~

### indexesOf^11

> 查找float数组array中指定float元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final float[] array, final float valueToFind)

// 示例
float[] nil = null;
float[] array = new float[]{1.1f, 2.2f, 3.3f, 1.1f, 2.2f, 3.3f};
ArrayUtils.indexesOf(nil, 1.1f);            // {}
ArrayUtils.indexesOf(array, 1.1f);          // {0, 3}
ArrayUtils.indexesOf(array, 3.3f);          // {2, 5}
~~~

### indexesOf^12

> 从指定位置startIndex开始查找float数组array中指定float元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final float[] array, final float valueToFind, int startIndex)

// 示例
float[] nil = null;
float[] array = new float[]{1.1f, 2.2f, 3.3f, 1.1f, 2.2f, 3.3f};
ArrayUtils.indexesOf(nil, 1.1f, 0);            // {}
ArrayUtils.indexesOf(array, 1.1f, 0);          // {0, 3}
ArrayUtils.indexesOf(array, 3.3f, 2);          // {2, 5}
~~~

### indexesOf^13

> 查找int数组array中指定int元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final int[] array, final int valueToFind)

// 示例
int[] nil = null;
int[] array = new int[]{1, 2, 3, 1, 2, 3};
ArrayUtils.indexesOf(nil, 1);            // {}
ArrayUtils.indexesOf(array, 1);          // {0, 3}
ArrayUtils.indexesOf(array, 3);          // {2, 5}
~~~

### indexesOf^14

> 从指定位置startIndex开始查找int数组array中指定int元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final int[] array, final int valueToFind, int startIndex)

// 示例
int[] nil = null;
int[] array = new int[]{1, 2, 3, 1, 2, 3};
ArrayUtils.indexesOf(nil, 1, 0);            // {}
ArrayUtils.indexesOf(array, 1, 0);          // {0, 3}
ArrayUtils.indexesOf(array, 3, 3);          // {5}
~~~

### indexesOf^15

> 查找long数组array中指定long元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final long[] array, final long valueToFind)

// 示例
long[] nil = null;
long[] array = new long[]{1L, 2L, 3L, 1L, 2L, 3L};
ArrayUtils.indexesOf(nil, 1L);            // {}
ArrayUtils.indexesOf(array, 1L);          // {0, 3}
ArrayUtils.indexesOf(array, 3L);          // {2, 5}
~~~

### indexesOf^16

> 从指定位置startIndex开始查找long数组array中指定long元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final long[] array, final long valueToFind, int startIndex)

// 示例
long[] nil = null;
long[] array = new long[]{1L, 2L, 3L, 1L, 2L, 3L};
ArrayUtils.indexesOf(nil, 1L, 0);            // {}
ArrayUtils.indexesOf(array, 1L, 0);          // {0, 3}
ArrayUtils.indexesOf(array, 3L, 3);          // {5}
~~~

### indexesOf^17

> 查找Object数组array中指定Object元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final Object[] array, final Object valueToFind)

// 示例
Object[] nil = null;
Object[] array = new Object[]{1, "a", 3, 1, 2, "a"};
ArrayUtils.indexesOf(nil, "a");          // {}
ArrayUtils.indexesOf(nil, null);         // {}
ArrayUtils.indexesOf(array, "a");        // {}
ArrayUtils.indexesOf(array, 1);          // {0, 3}
ArrayUtils.indexesOf(array, 3);          // {2}
ArrayUtils.indexesOf(array, "a");        // {1, 5}
~~~

### indexesOf^18

> 从指定位置startIndex开始查找Object数组array中指定Object元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final Object[] array, final Object valueToFind, int startIndex)

// 示例
Object[] nil = null;
Object[] array = new Object[]{1, "a", 3, 1, 2, "a"};
ArrayUtils.indexesOf(nil, "a", 1);          // {}
ArrayUtils.indexesOf(nil, null, 1);         // {}
ArrayUtils.indexesOf(array, "a", 1);        // {}
ArrayUtils.indexesOf(array, 1, 1);          // {0, 3}
ArrayUtils.indexesOf(array, 3, 2);          // {2}
ArrayUtils.indexesOf(array, "a", 2);        // {5}
~~~

### indexesOf^19

> 查找short数组array中指定short元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final short[] array, final short valueToFind)

// 示例
short[] nil = null;
short[] array = new short[]{1, 2, 3, 1, 2, 3};
ArrayUtils.indexesOf(nil, (short)1);            // {}
ArrayUtils.indexesOf(array, (short)1);          // {0, 3}
ArrayUtils.indexesOf(array, (short)3);          // {2, 5}
~~~

### indexesOf^20

> 从指定位置startIndex开始查找short数组array中指定short元素valueToFind的索引位集

~~~java
// 声明
// 版本： 3.10+
public static BitSet indexesOf(final short[] array, final short valueToFind, int startIndex)

// 示例
short[] nil = null;
short[] array = new short[]{1, 2, 3, 1, 2, 3};
ArrayUtils.indexesOf(nil, (short)1, 1);            // {}
ArrayUtils.indexesOf(array, (short)1, 1);          // {3}
ArrayUtils.indexesOf(array, (short)3, 1);          // {2, 5}
~~~

### indexOf^1

> 查找boolean数组array中指定boolean元素valueToFind的索引

~~~java
// 声明
public static int indexOf(final boolean[] array, final boolean valueToFind)

// 示例
boolean[] nil = null;
boolean[] array = new boolean[]{true, false, true, false};
ArrayUtils.indexOf(nil, true);            // -1
ArrayUtils.indexOf(array, true);           // 0
ArrayUtils.indexOf(array, false);          // 1
~~~

### indexOf^2

> 从指定位置startIndex开始查找boolean数组array中指定boolean元素valueToFind的索引

~~~java
// 声明
public static int indexOf(final boolean[] array, final boolean valueToFind, int startIndex)

// 示例
boolean[] nil = null;
boolean[] array = new boolean[]{true, false, true, false};
ArrayUtils.indexOf(nil, true, 1);            // -1
ArrayUtils.indexOf(array, true, 1);           // 2
ArrayUtils.indexOf(array, false, 1);          // 1
~~~

### indexOf^3

> 查找byte数组array中指定byte元素valueToFind的索引

~~~java
// 声明
public static int indexOf(final byte[] array, final byte valueToFind)

// 示例
byte[] nil = null;
byte[] array = new byte[]{1, 2, 1, 2};
ArrayUtils.indexOf(nil, (byte)1);            // -1
ArrayUtils.indexOf(array, (byte)1);          // 0
ArrayUtils.indexOf(array, (byte)2);          // 1
~~~

### indexOf^4

> 从指定位置startIndex开始查找byte数组array中指定byte元素valueToFind的索引

~~~java
// 声明
public static int indexOf(final byte[] array, final byte valueToFind, int startIndex)

// 示例
byte[] nil = null;
byte[] array = new byte[]{1, 2, 1, 2};
ArrayUtils.indexOf(nil, (byte)1, 1);             // -1
ArrayUtils.indexOf(array, (byte)1, 1);           // 2
ArrayUtils.indexOf(array, (byte)2, 1);          // 1
~~~

### indexOf^5

> 查找char数组array中指定char元素valueToFind的索引

~~~java
// 声明
public static int indexOf(final char[] array, final char valueToFind)

// 示例
char[] nil = null;
char[] array = new char[]{'a', 'b', 'a', 'b'};
ArrayUtils.indexOf(nil, 'a');            // -1
ArrayUtils.indexOf(array, 'a');          // 0
ArrayUtils.indexOf(array, 'b');          // 1
~~~

### indexOf^6

> 从指定位置startIndex开始查找char数组array中指定char元素valueToFind的索引

~~~java
// 声明
public static int indexOf(final char[] array, final char valueToFind, int startIndex)

// 示例
char[] nil = null;
char[] array = new char[]{'a', 'b', 'a', 'b'};
ArrayUtils.indexOf(nil, 'a', 1);             // -1
ArrayUtils.indexOf(array, 'a', 1);           // 2
ArrayUtils.indexOf(array, 'b', 1);          // 1
~~~
