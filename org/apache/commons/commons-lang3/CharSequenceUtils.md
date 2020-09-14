# CharSequenceUtils

> 字符串序列工具
>
> 版本： 3.0+

## 类定义

~~~java
public class CharSequenceUtils
~~~

## 构造函数

~~~java
// 不建议通过构造函数生成实例对方法属性进行访问
public CharSequenceUtils()
~~~

## 函数方法

### subSequence

> 从指定索引位置start开始截取子字符串

~~~java
// 声明
public static CharSequence subSequence(final CharSequence cs, final int start)

// 示例
CharSequenceUtils.subSequence("abcdefg", 2) // cdefg
~~~

### toCharArray

> 将一个字符串转换成字符数组

~~~java
// 声明
public static char[] toCharArray(final CharSequence source)

// 示例
CharSequenceUtils.toCharArray("abcd")   // [a, b, c, d]
~~~
