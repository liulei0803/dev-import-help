# CharSetUtils

## 类定义

> 字符集合(CharSet)工具类
>
> 版本： 1.0+

~~~java
public class CharSetUtils
~~~

## 静态方法

### containsAny

> 检查一个字符串str是否包含指定字符集合set内的字符
>
> 版本： 3.2+

~~~java
// 声明
public static boolean containsAny(final String str, final String... set)

// 示例
// *表示取对应类型的任意值， 不可以直接出现在代码中
CharSetUtils.containsAny(null, *)        // false
CharSetUtils.containsAny("", *)          // false
CharSetUtils.containsAny(*, null)        // false
CharSetUtils.containsAny(*, "")          // false
CharSetUtils.containsAny("hello", "k-p") // true
CharSetUtils.containsAny("hello", "a-d") // false
~~~

### count

> 检查一个字符串str中指定字符集合set内字符出现的数量

~~~java
// 声明
public static int count(final String str, final String... set)

// 示例
// *表示取对应类型的任意值， 不可以直接出现在代码中
CharSetUtils.count(null, *)        // 0
CharSetUtils.count("", *)          // 0
CharSetUtils.count(*, null)        // 0
CharSetUtils.count(*, "")          // 0
CharSetUtils.count("hello", "k-p") // 3
CharSetUtils.count("hello", "a-e") // 1
~~~

### delete

> 删除一个字符串str中出现的指定字符集合set内的字符

~~~java
// 声明
public static String delete(final String str, final String... set)

// 示例
// *表示取对应类型的任意值， 不可以直接出现在代码中
CharSetUtils.delete(null, *)        // null
CharSetUtils.delete("", *)          // ""
CharSetUtils.delete(*, null)        // *
CharSetUtils.delete(*, "")          // *
CharSetUtils.delete("hello", "hl")  // "eo"
CharSetUtils.delete("hello", "le")  // "ho"
~~~

### keep

> 保留一个字符串str中出现的指定字符集合set内的字符，删除其它字符
>
> 版本： 2.0+

~~~java
// 声明
public static String keep(final String str, final String... set)

// 示例
// *表示取对应类型的任意值， 不可以直接出现在代码中
CharSetUtils.keep(null, *)        // null
CharSetUtils.keep("", *)          // ""
CharSetUtils.keep(*, null)        // ""
CharSetUtils.keep(*, "")          // ""
CharSetUtils.keep("hello", "hl")  // "hll"
CharSetUtils.keep("hello", "le")  // "ell"
~~~

### squeeze

> 合并一个字符串str中出现的指定字符集合set内的字符，只合并相邻且重复的字符

~~~java
// 声明
public static String squeeze(final String str, final String... set)

// 示例
// *表示取对应类型的任意值， 不可以直接出现在代码中
CharSetUtils.squeeze(null, *)        // null
CharSetUtils.squeeze("", *)          // ""
CharSetUtils.squeeze(*, null)        // *
CharSetUtils.squeeze(*, "")          // *
CharSetUtils.squeeze("hello", "k-p") // "helo"
CharSetUtils.squeeze("hello", "a-e") // "hello"
~~~
