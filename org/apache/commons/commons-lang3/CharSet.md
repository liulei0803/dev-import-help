# CharSet

> 字符集，实例是不可变的，但子类可以是可变的
>
> 版本： 1.0

## 类定义

~~~java
public class CharSet implements Serializable
~~~

## 静态变量

~~~java
// 定义了一个空字符集
public static final CharSet EMPTY = new CharSet((String) null);

// ASCII码大小写字母范围
public static final CharSet ASCII_ALPHA = new CharSet("a-zA-Z");

// ASCII码小写字母范围
public static final CharSet ASCII_ALPHA_LOWER = new CharSet("a-z");

// ASCII码大写字母范围
public static final CharSet ASCII_ALPHA_UPPER = new CharSet("A-Z");

// ASCII码数字范围
public static final CharSet ASCII_NUMERIC = new CharSet("0-9");
~~~

## 普通函数

### getInstance

> 获取一个字符集的实例
>
> 版本： 2.4

~~~java
// 声明
public static CharSet getInstance(final String... setStrs)

// 示例
CharSet.getInstance("^a-c").contains('a') = false
CharSet.getInstance("^a-c").contains('d') = true
CharSet.getInstance("^^a-c").contains('a') = true
CharSet.getInstance("^^a-c").contains('^') = false
CharSet.getInstance("^a-cd-f").contains('d') = true
CharSet.getInstance("a-c^").contains('^') = true
CharSet.getInstance("^", "a-c").contains('^') = true
~~~
