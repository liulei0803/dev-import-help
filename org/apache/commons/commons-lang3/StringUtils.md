# StringUtils

- 3.11

## 类定义

~~~java
/**
  * 字符串工具类
  * 版本: 1.0+
  */
public class StringUtils
~~~

## 静态属性

~~~java

// 空格字符
public static final String SPACE = " ";

// 空的字符串
public static final String EMPTY = "";

// 换行
public static final String LF = "\n";

// 回车
public static final String CR = "\r";

// 当在一个字符串中搜索不到指定字符时返回的索引值
public static final int INDEX_NOT_FOUND = -1;

~~~

## 函数方法

### abbreviate^1

> 字符串缩略形式

~~~java
// str          待处理字符串
// maxWidth     缩略形式的最大宽度，最小4
// 异常         缩略长度过小时IllegalArgumentException
// 版本         2.0+
public static String abbreviate(final String str, final int maxWidth)

// 示例
StringUtils.abbreviate(null, *)      // null
StringUtils.abbreviate("", 4)        // ""
StringUtils.abbreviate("abcdefg", 6) // "abc..."
StringUtils.abbreviate("abcdefg", 7) // "abcdefg"
StringUtils.abbreviate("abcdefg", 8) // "abcdefg"
StringUtils.abbreviate("abcdefg", 4) // "a..."
StringUtils.abbreviate("abcdefg", 3) // IllegalArgumentException

~~~

### abbreviate^2

> 字符串缩略形式

~~~java
// str          待处理字符串
// offset       偏移量，从0开始
// maxWidth     缩略形式的最大宽度，最小4
// 异常         缩略长度过小时IllegalArgumentException
// 版本         2.0+
public static String abbreviate(final String str, final int offset, final int maxWidth)

// 示例
StringUtils.abbreviate(null, *, *)                // null
StringUtils.abbreviate("", 0, 4)                  // ""
StringUtils.abbreviate("abcdefghijklmno", -1, 10) // "abcdefg..."
StringUtils.abbreviate("abcdefghijklmno", 0, 10)  // "abcdefg..."
StringUtils.abbreviate("abcdefghijklmno", 1, 10)  // "abcdefg..."
StringUtils.abbreviate("abcdefghijklmno", 4, 10)  // "abcdefg..."
StringUtils.abbreviate("abcdefghijklmno", 5, 10)  // "...fghi..."
StringUtils.abbreviate("abcdefghijklmno", 6, 10)  // "...ghij..."
StringUtils.abbreviate("abcdefghijklmno", 8, 10)  // "...ijklmno"
StringUtils.abbreviate("abcdefghijklmno", 10, 10) // "...ijklmno"
StringUtils.abbreviate("abcdefghijklmno", 12, 10) // "...ijklmno"
StringUtils.abbreviate("abcdefghij", 0, 3)        // IllegalArgumentException
StringUtils.abbreviate("abcdefghij", 5, 6)        // IllegalArgumentException
~~~

### abbreviate^3

> 字符串缩略形式

~~~java
// str          待处理字符串
// abbrevMarker 指定省略部分替代所使用的字符串
// maxWidth     缩略形式的最大宽度，最小4
// 异常         缩略长度过小时IllegalArgumentException
// 版本         3.6+
public static String abbreviate(final String str, final String abbrevMarker, final int maxWidth)

// 示例
StringUtils.abbreviate(null, "...", *)      // null
StringUtils.abbreviate("abcdefg", null, *)  // "abcdefg"
StringUtils.abbreviate("", "...", 4)        // ""
StringUtils.abbreviate("abcdefg", ".", 5)   // "abcd."
StringUtils.abbreviate("abcdefg", ".", 7)   // "abcdefg"
StringUtils.abbreviate("abcdefg", ".", 8)   // "abcdefg"
StringUtils.abbreviate("abcdefg", "..", 4)  // "ab.."
StringUtils.abbreviate("abcdefg", "..", 3)  // "a.."
StringUtils.abbreviate("abcdefg", "..", 2)  // IllegalArgumentException
StringUtils.abbreviate("abcdefg", "...", 3) // IllegalArgumentException
~~~

### abbreviate^4

> 字符串缩略形式

~~~java
// str          待处理字符串
// offset       偏移量，从0开始
// abbrevMarker 指定省略部分替代所使用的字符串
// maxWidth     缩略形式的最大宽度，最小4
// 异常         缩略长度过小时IllegalArgumentException
// 版本         3.6+
public static String abbreviate(final String str, final String abbrevMarker, int offset, final int maxWidth)

// 示例
StringUtils.abbreviate(null, null, *, *)                 // null
StringUtils.abbreviate("abcdefghijklmno", null, *, *)    // "abcdefghijklmno"
StringUtils.abbreviate("", "...", 0, 4)                  // ""
StringUtils.abbreviate("abcdefghijklmno", "---", -1, 10) // "abcdefg---"
StringUtils.abbreviate("abcdefghijklmno", ",", 0, 10)    // "abcdefghi,"
StringUtils.abbreviate("abcdefghijklmno", ",", 1, 10)    // "abcdefghi,"
StringUtils.abbreviate("abcdefghijklmno", ",", 2, 10)    // "abcdefghi,"
StringUtils.abbreviate("abcdefghijklmno", "::", 4, 10)   // "::efghij::"
StringUtils.abbreviate("abcdefghijklmno", "...", 6, 10)  // "...ghij..."
StringUtils.abbreviate("abcdefghijklmno", "*", 9, 10)    // "*ghijklmno"
StringUtils.abbreviate("abcdefghijklmno", "'", 10, 10)   // "'ghijklmno"
StringUtils.abbreviate("abcdefghijklmno", "!", 12, 10)   // "!ghijklmno"
StringUtils.abbreviate("abcdefghij", "abra", 0, 4)       // IllegalArgumentException
StringUtils.abbreviate("abcdefghij", "...", 5, 6)        // IllegalArgumentException
~~~

### abbreviateMiddle

> 缩略掉字符串中间一部分的字符

~~~java
// str          待处理字符串
// middle       指定省略部分替代所使用的字符串
// length       缩略形式的最大宽度，最小4
// 版本         2.5+
public static String abbreviateMiddle(final String str, final String middle, final int length)
~~~

### appendIfMissing

> 如果一个字符串不以指定字符串结尾，则补之

~~~java
// str          待处理字符串
// suffix       要添加到尾部的字符串
// suffixes     校验字符串是否以指定字符串结尾
// 版本         3.2+
public static String appendIfMissing(final String str, final CharSequence suffix, final CharSequence... suffixes)

// 示例
StringUtils.appendIfMissing(null, null, null)       // null
StringUtils.appendIfMissing("abc", null, null)      // "abc"
StringUtils.appendIfMissing("", "xyz", null)        // "xyz"
StringUtils.appendIfMissing("abc", "xyz", new CharSequence[]{null}) // "abcx
StringUtils.appendIfMissing("abc", "xyz", "")       // "abc"
StringUtils.appendIfMissing("abc", "xyz", "mno")    // "abcxyz"
StringUtils.appendIfMissing("abcxyz", "xyz", "mno") // "abcxyz"
StringUtils.appendIfMissing("abcmno", "xyz", "mno") // "abcmno"
StringUtils.appendIfMissing("abcXYZ", "xyz", "mno") // "abcXYZxyz"
StringUtils.appendIfMissing("abcMNO", "xyz", "mno") // "abcMNOxyz"
~~~

### appendIfMissingIgnoreCase

> 如果一个字符串不以指定字符串结尾，则补之，忽略大小写

~~~java
// str          待处理字符串
// suffix       要添加到尾部的字符串
// suffixes     校验字符串是否以指定字符串结尾
// 版本         3.2+
public static String appendIfMissingIgnoreCase(final String str, final CharSequence suffix, final CharSequence... suffixes)

// 示例
StringUtils.appendIfMissingIgnoreCase(null, null, null)       // null
StringUtils.appendIfMissingIgnoreCase("abc", null, null)      // "abc"
StringUtils.appendIfMissingIgnoreCase("", "xyz", null)        // "xyz"
StringUtils.appendIfMissingIgnoreCase("abc", "xyz", new CharSequence[]{null}) // "abcxyz"
StringUtils.appendIfMissingIgnoreCase("abc", "xyz", "")       // "abc"
StringUtils.appendIfMissingIgnoreCase("abc", "xyz", "mno")    // "abcxyz"
StringUtils.appendIfMissingIgnoreCase("abcxyz", "xyz", "mno") // "abcxyz"
StringUtils.appendIfMissingIgnoreCase("abcmno", "xyz", "mno") // "abcmno"
StringUtils.appendIfMissingIgnoreCase("abcXYZ", "xyz", "mno") // "abcXYZ"
StringUtils.appendIfMissingIgnoreCase("abcMNO", "xyz", "mno") // "abcMNO"
~~~

### capitalize

> 将一个字符串的首字母转换成大写

~~~java
// str          待处理字符串
// 版本         2.0+
public static String capitalize(final String str)

// 示例
StringUtils.capitalize(null)    // null
StringUtils.capitalize("")      // ""
StringUtils.capitalize("cat")   // "Cat"
StringUtils.capitalize("cAt")   // "CAt"
StringUtils.capitalize("'cat'") // "'cat'"
~~~

### center^1

> 将一个字符串按照指定宽度置于中间位置

~~~java
// str          待处理字符串
// size         指定宽度
// 版本         2.0+
public static String center(final String str, final int size)

// 示例
StringUtils.center(null, *)   // null
StringUtils.center("", 4)     // "    "
StringUtils.center("ab", -1)  // "ab"
StringUtils.center("ab", 4)   // " ab "
StringUtils.center("abcd", 2) // "abcd"
StringUtils.center("a", 4)    // " a  "
~~~

### center^2

> 将一个字符串按照指定宽度置于中间位置

~~~java
// str          待处理字符串
// size         指定宽度
// padChar      指定填充字符
// 版本         2.0+
public static String center(final String str, final int size, final char padChar)

// 示例
StringUtils.center(null, *, *)     // null
StringUtils.center("", 4, ' ')     // "    "
StringUtils.center("ab", -1, ' ')  // "ab"
StringUtils.center("ab", 4, ' ')   // " ab "
StringUtils.center("abcd", 2, ' ') // "abcd"
StringUtils.center("a", 4, ' ')    // " a  "
StringUtils.center("a", 4, 'y')    // "yayy"
~~~

### center^3

> 将一个字符串按照指定宽度置于中间位置

~~~java
// str          待处理字符串
// size         指定宽度
// padChar      指定填充字符串
// 版本         2.0+
public static String center(final String str, final int size, String padChar)

// 示例
StringUtils.center(null, *, *)     // null
StringUtils.center("", 4, " ")     // "    "
StringUtils.center("ab", -1, " ")  // "ab"
StringUtils.center("ab", 4, " ")   // " ab "
StringUtils.center("abcd", 2, " ") // "abcd"
StringUtils.center("a", 4, " ")    // " a  "
StringUtils.center("a", 4, "yz")   // "yayz"
StringUtils.center("abc", 7, null) // "  abc  "
StringUtils.center("abc", 7, "")   // "  abc  "
~~~

### chomp^1

> 移除指定字符串后的一个新行

~~~java
// str          待处理字符串
// 版本         2.0+
public static String chomp(final String str)

// 示例
StringUtils.chomp(null)          // null
StringUtils.chomp("")            // ""
StringUtils.chomp("abc \r")      // "abc "
StringUtils.chomp("abc\n")       // "abc"
StringUtils.chomp("abc\r\n")     // "abc"
StringUtils.chomp("abc\r\n\r\n") // "abc\r\n"
StringUtils.chomp("abc\n\r")     // "abc\n"
StringUtils.chomp("abc\n\rabc")  // "abc\n\rabc"
StringUtils.chomp("\r")          // ""
StringUtils.chomp("\n")          // ""
StringUtils.chomp("\r\n")        // ""
~~~

### chomp^2

> 移除指定字符串后的一个新行

~~~java
// str          待处理字符串
// separator    指定结尾字符串
// 版本         2.0+
@Deprecated
public static String chomp(final String str, final String separator)

// 示例
StringUtils.chomp(null, *)         // null
StringUtils.chomp("", *)           // ""
StringUtils.chomp("foobar", "bar") // "foo"
StringUtils.chomp("foobar", "baz") // "foobar
StringUtils.chomp("foo", "foo")    // ""
StringUtils.chomp("foo ", "foo")   // "foo "
StringUtils.chomp(" foo", "foo")   // " "
StringUtils.chomp("foo", "foooo")  // "foo"
StringUtils.chomp("foo", "")       // "foo"
StringUtils.chomp("foo", null)     // "foo"
~~~

### chop

> 移除一个字符串的最后一个字符，回车换行(/r/n)算作一个字符

~~~java
// str          待处理字符串
public static String chop(final String str)

// 示例
StringUtils.chop(null)          // null
StringUtils.chop("")            // ""
StringUtils.chop("abc \r")      // "abc "
StringUtils.chop("abc\n")       // "abc"
StringUtils.chop("abc\r\n")     // "abc"
StringUtils.chop("abc")         // "ab"
StringUtils.chop("abc\nabc")    // "abc\nab"
StringUtils.chop("a")           // ""
StringUtils.chop("\r")          // ""
StringUtils.chop("\n")          // ""
StringUtils.chop("\r\n")        // ""
~~~

### compare^1

> 按字典顺序比较两个字符串
> null与任何非空字符串比较结果都小于0

~~~java
// str1           待比较字符串1
// str2           待比较字符串2
// 版本           3.5+
public static int compare(final String str1, final String str2)

// 示例
StringUtils.compare(null, null)   // = 0
StringUtils.compare(null , "a")   // < 0
StringUtils.compare("a", null)    // > 0
StringUtils.compare("abc", "abc") // = 0
StringUtils.compare("a", "b")     // < 0
StringUtils.compare("b", "a")     // > 0
StringUtils.compare("a", "B")     // > 0
StringUtils.compare("ab", "abc")  // < 0
~~~

### compare^2

> 按字典顺序比较两个字符串
> null与任何非空字符串比较结果都小于0

~~~java
// str1           待比较字符串1
// str2           待比较字符串2
// nullIsLess     true: null被认为最小, false: null被认为最大
// 版本           3.5+
public static int compare(final String str1, final String str2, final boolean nullIsLess)

// 示例
// *表示取值不会影响结果， 不可以直接出现在代码中
StringUtils.compare(null, null, *)     // = 0
StringUtils.compare(null , "a", true)  // < 0
StringUtils.compare(null , "a", false) // > 0
StringUtils.compare("a", null, true)   // > 0
StringUtils.compare("a", null, false)  // < 0
StringUtils.compare("abc", "abc", *)   // = 0
StringUtils.compare("a", "b", *)       // < 0
StringUtils.compare("b", "a", *)       // > 0
StringUtils.compare("a", "B", *)       // > 0
StringUtils.compare("ab", "abc", *)    // < 0
~~~

### compareIgnoreCase^1

> 按字典顺序比较两个字符串，忽略大小写
> null与任何非空字符串比较结果都小于0

~~~java
// str1           待比较字符串1
// str2           待比较字符串2
// 版本           3.5+
public static int compareIgnoreCase(final String str1, final String str2)

// 示例
StringUtils.compareIgnoreCase(null, null)   // = 0
StringUtils.compareIgnoreCase(null , "a")   // < 0
StringUtils.compareIgnoreCase("a", null)    // > 0
StringUtils.compareIgnoreCase("abc", "abc") // = 0
StringUtils.compareIgnoreCase("abc", "ABC") // = 0
StringUtils.compareIgnoreCase("a", "b")     // < 0
StringUtils.compareIgnoreCase("b", "a")     // > 0
StringUtils.compareIgnoreCase("a", "B")     // < 0
StringUtils.compareIgnoreCase("A", "b")     // < 0
StringUtils.compareIgnoreCase("ab", "ABC")  // < 0
~~~

### compareIgnoreCase^2

> 按字典顺序比较两个字符串，忽略大小写
> null与任何非空字符串比较结果都小于0

~~~java
// str1           待比较字符串1
// str2           待比较字符串2
// nullIsLess     true: null被认为最小, false: null被认为最大
// 版本           3.5+
public static int compareIgnoreCase(final String str1, final String str2, final boolean nullIsLess)

// 示例
// *表示取值不会影响结果， 不可以直接出现在代码中
StringUtils.compareIgnoreCase(null, null, *)     // = 0
StringUtils.compareIgnoreCase(null , "a", true)  // < 0
StringUtils.compareIgnoreCase(null , "a", false) // > 0
StringUtils.compareIgnoreCase("a", null, true)   // > 0
StringUtils.compareIgnoreCase("a", null, false)  // < 0
StringUtils.compareIgnoreCase("abc", "abc", *)   // = 0
StringUtils.compareIgnoreCase("abc", "ABC", *)   // = 0
StringUtils.compareIgnoreCase("a", "b", *)       // < 0
StringUtils.compareIgnoreCase("b", "a", *)       // > 0
StringUtils.compareIgnoreCase("a", "B", *)       // < 0
StringUtils.compareIgnoreCase("A", "b", *)       // < 0
StringUtils.compareIgnoreCase("ab", "abc", *)    // < 0
~~~

### contains^1

> 检查某个字符串是否包含另一个字符串

~~~java
// seq            待检查字符串
// searchSeq      待查找字符串
// 版本           2.0+
// 3.0版本从原来的contains(String, String)改为contains(CharSequence, CharSequence)
public static boolean contains(final CharSequence seq, final CharSequence searchSeq)

// 示例
// *表示取值不会影响结果， 不可以直接出现在代码中
StringUtils.contains(null, *)     // false
StringUtils.contains(*, null)     // false
StringUtils.contains("", "")      // true
StringUtils.contains("abc", "")   // true
StringUtils.contains("abc", "a")  // true
StringUtils.contains("abc", "z")  // false
~~~

### contains^2

> 检查某个字符串是否包含另一个字符

~~~java
// seq            待检查字符串
// searchChar     待查找字符
// 版本           2.0+
// 3.0版本从原来的contains(String, int)改为contains(CharSequence, int)
public static boolean contains(final CharSequence seq, final int searchChar)

// 示例
// *表示取值不会影响结果， 不可以直接出现在代码中
StringUtils.contains(null, *)    // false
StringUtils.contains("", *)      // false
StringUtils.contains("abc", 'a') // true
StringUtils.contains("abc", 'z') // false
~~~

### containsAny^1

> 检查某个字符串是否包含一组字符中的某个字符

~~~java
// seq            待检查字符串
// searchChars    待查找字符数组
// 版本           2.4+
// 3.0版本从原来的contains(String, char[])改为contains(CharSequence, char...)
public static boolean containsAny(final CharSequence cs, final char... searchChars)

// 示例
// *表示取值不会影响结果， 不可以直接出现在代码中
StringUtils.containsAny(null, *)                  // false
StringUtils.containsAny("", *)                    // false
StringUtils.containsAny(*, null)                  // false
StringUtils.containsAny(*, [])                    // false
StringUtils.containsAny("zzabyycdxx", 'z', 'a')   // true
StringUtils.containsAny("zzabyycdxx", 'b', 'y')   // true
StringUtils.containsAny("zzabyycdxx", 'z', 'y')   // true
StringUtils.containsAny("aba", 'z')               // false
~~~

### containsAny^2

> 检查某个字符串是否包含指定字符串中的某个字符

~~~java
// seq            待检查字符串
// searchChars    待查找字符串
// 版本           2.4+
// 3.0版本从原来的contains(String, String)改为contains(CharSequence, CharSequence)
public static boolean containsAny(final CharSequence cs, final CharSequence searchChars)

// 示例
// *表示取值不会影响结果， 不可以直接出现在代码中
StringUtils.containsAny(null, *)               // false
StringUtils.containsAny("", *)                 // false
StringUtils.containsAny(*, null)               // false
StringUtils.containsAny(*, "")                 // false
StringUtils.containsAny("zzabyycdxx", "za")    // true
StringUtils.containsAny("zzabyycdxx", "by")    // true
StringUtils.containsAny("zzabyycdxx", "zy")    // true
StringUtils.containsAny("zzabyycdxx", "\tx")   // true
StringUtils.containsAny("zzabyycdxx", "$.#yF") // true
StringUtils.containsAny("aba", "z")            // false
~~~

### containsAny^3

> 检查某个字符串是否包含指定字符串数组中的某个字符

~~~java
// seq                  待检查字符串
// searchCharSequences  待查找字符串数组
// 版本                 3.4+
public static boolean containsAny(final CharSequence cs, final CharSequence... searchCharSequences)

// 示例
// *表示取值不会影响结果， 不可以直接出现在代码中
StringUtils.containsAny(null, *)            // false
StringUtils.containsAny("", *)              // false
StringUtils.containsAny(*, null)            // false
StringUtils.containsAny(*, [])              // false
StringUtils.containsAny("abcd", "ab", null) // true
StringUtils.containsAny("abcd", "ab", "cd") // true
StringUtils.containsAny("abc", "d", "abc")  // true
~~~
