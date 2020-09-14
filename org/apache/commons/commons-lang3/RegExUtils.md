# RegExUtils

> 正则表达式处理字符串的工具类
>
> 版本： 3.3+

## 类定义

~~~java
public class RegExUtils
~~~

## 构造函数

~~~java
// 默认构造函数不建议使用，直接按静态函数方式调用
public RegExUtils()
~~~

## 函数方法

### removeAll^1

> 移除text中所有匹配指定正则表达式regex的部分

~~~java
// 声明
public static String removeAll(final String text, final Pattern regex)

// 示例
StringUtils.removeAll(null, *)                                                                      // null
StringUtils.removeAll("any", (Pattern) null)                                                        // "any"
StringUtils.removeAll("any", Pattern.compile(""))                                                   // "any"
StringUtils.removeAll("any", Pattern.compile(".*"))                                                 // ""
StringUtils.removeAll("any", Pattern.compile(".+"))                                                 // ""
StringUtils.removeAll("abc", Pattern.compile(".?"))                                                 // ""
StringUtils.removeAll("A&lt;__&gt;\n&lt;__&gt;B", Pattern.compile("&lt;.*&gt;"))                    // "A\nB"
StringUtils.removeAll("A&lt;__&gt;\n&lt;__&gt;B", Pattern.compile("(?s)&lt;.*&gt;"))                // "AB"
StringUtils.removeAll("A&lt;__&gt;\n&lt;__&gt;B", Pattern.compile("&lt;.*&gt;", Pattern.DOTALL))    // "AB"
StringUtils.removeAll("ABCabc123abc", Pattern.compile("[a-z]"))                                     // "ABC123"
~~~

### removeAll^2

> 移除text中所有匹配指定正则表达式regex的部分

~~~java
// 声明
public static String removeAll(final String text, final String regex)

// 示例
StringUtils.removeAll(null, *)                                          // null
StringUtils.removeAll("any", (String) null)                             // "any"
StringUtils.removeAll("any", "")                                        // "any"
StringUtils.removeAll("any", ".*")                                      // ""
StringUtils.removeAll("any", ".+")                                      // ""
StringUtils.removeAll("abc", ".?")                                      // ""
StringUtils.removeAll("A&lt;__&gt;\n&lt;__&gt;B", "&lt;.*&gt;")         // "A\nB"
StringUtils.removeAll("A&lt;__&gt;\n&lt;__&gt;B", "(?s)&lt;.*&gt;")     // "AB"
StringUtils.removeAll("ABCabc123abc", "[a-z]")                          // "ABC123"
~~~

### removeFirst^1

> 移除text中首次（自左向右）匹配指定正则表达式regex的部分

~~~java
// 声明
public static String removeFirst(final String text, final Pattern regex)

// 示例
StringUtils.removeFirst(null, *)                                                        // null
StringUtils.removeFirst("any", (Pattern) null)                                          // "any"
StringUtils.removeFirst("any", Pattern.compile(""))                                     // "any"
StringUtils.removeFirst("any", Pattern.compile(".*"))                                   // ""
StringUtils.removeFirst("any", Pattern.compile(".+"))                                   // ""
StringUtils.removeFirst("abc", Pattern.compile(".?"))                                   // "bc"
StringUtils.removeFirst("A&lt;__&gt;\n&lt;__&gt;B", Pattern.compile("&lt;.*&gt;"))      // "A\n&lt;__&gt;B"
StringUtils.removeFirst("A&lt;__&gt;\n&lt;__&gt;B", Pattern.compile("(?s)&lt;.*&gt;"))  // "AB"
StringUtils.removeFirst("ABCabc123", Pattern.compile("[a-z]"))                          // "ABCbc123"
StringUtils.removeFirst("ABCabc123abc", Pattern.compile("[a-z]+"))                      // "ABC123abc"
~~~

### removeFirst^2

> 移除text中首次（自左向右）匹配指定正则表达式regex的部分

~~~java
// 声明
public static String removeFirst(final String text, final String regex)

// 示例
StringUtils.removeFirst(null, *)                                        // null
StringUtils.removeFirst("any", (String) null)                           // "any"
StringUtils.removeFirst("any", "")                                      // "any"
StringUtils.removeFirst("any", ".*")                                    // ""
StringUtils.removeFirst("any", ".+")                                    // ""
StringUtils.removeFirst("abc", ".?")                                    // "bc"
StringUtils.removeFirst("A&lt;__&gt;\n&lt;__&gt;B", "&lt;.*&gt;")       // "A\n&lt;__&gt;B"
StringUtils.removeFirst("A&lt;__&gt;\n&lt;__&gt;B", "(?s)&lt;.*&gt;")   // "AB"
StringUtils.removeFirst("ABCabc123", "[a-z]")                           // "ABCbc123"
StringUtils.removeFirst("ABCabc123abc", "[a-z]+")                       // "ABC123abc"
~~~

### removePattern

> 移除text中所有匹配指定正则表达式regex的部分

~~~java
// 声明
public static String removePattern(final String text, final String regex)

// 示例
StringUtils.removePattern(null, *)                                      // null
StringUtils.removePattern("any", (String) null)                         // "any"
StringUtils.removePattern("A&lt;__&gt;\n&lt;__&gt;B", "&lt;.*&gt;")     // "AB"
StringUtils.removePattern("ABCabc123", "[a-z]")                         // "ABC123"
~~~

### replaceAll^1

> 找到text中所有匹配指定正则表达式regex的部分，替换为字符串replacement

~~~java
// 声明
public static String replaceAll(final String text, final Pattern regex, final String replacement)

// 示例
StringUtils.replaceAll(null, *, *)                                                                      // null
StringUtils.replaceAll("any", (Pattern) null, *)                                                        // "any"
StringUtils.replaceAll("any", *, null)                                                                  // "any"
StringUtils.replaceAll("", Pattern.compile(""), "zzz")                                                  // "zzz"
StringUtils.replaceAll("", Pattern.compile(".*"), "zzz")                                                // "zzz"
StringUtils.replaceAll("", Pattern.compile(".+"), "zzz")                                                // ""
StringUtils.replaceAll("abc", Pattern.compile(""), "ZZ")                                                // "ZZaZZbZZcZZ"
StringUtils.replaceAll("&lt;__&gt;\n&lt;__&gt;", Pattern.compile("&lt;.*&gt;"), "z")                    // "z\nz"
StringUtils.replaceAll("&lt;__&gt;\n&lt;__&gt;", Pattern.compile("&lt;.*&gt;", Pattern.DOTALL), "z")    // "z"
StringUtils.replaceAll("&lt;__&gt;\n&lt;__&gt;", Pattern.compile("(?s)&lt;.*&gt;"), "z")                // "z"
StringUtils.replaceAll("ABCabc123", Pattern.compile("[a-z]"), "_")                                      // "ABC___123"
StringUtils.replaceAll("ABCabc123", Pattern.compile("[^A-Z0-9]+"), "_")                                 // "ABC_123"
StringUtils.replaceAll("ABCabc123", Pattern.compile("[^A-Z0-9]+"), "")                                  // "ABC123"
StringUtils.replaceAll("Lorem ipsum  dolor   sit", Pattern.compile("( +)([a-z]+)"), "_$2")              // "Lorem_ipsum_dolor_sit"
~~~

### replaceAll^2

> 找到text中所有匹配指定正则表达式regex的部分，替换为字符串replacement

~~~java
// 声明
public static String replaceAll(final String text, final String regex, final String replacement)

// 示例
StringUtils.replaceAll(null, *, *)                                          // null
StringUtils.replaceAll("any", (String) null, *)                             // "any"
StringUtils.replaceAll("any", *, null)                                      // "any"
StringUtils.replaceAll("", "", "zzz")                                       // "zzz"
StringUtils.replaceAll("", ".*", "zzz")                                     // "zzz"
StringUtils.replaceAll("", ".+", "zzz")                                     // ""
StringUtils.replaceAll("abc", "", "ZZ")                                     // "ZZaZZbZZcZZ"
StringUtils.replaceAll("&lt;__&gt;\n&lt;__&gt;", "&lt;.*&gt;", "z")         // "z\nz"
StringUtils.replaceAll("&lt;__&gt;\n&lt;__&gt;", "(?s)&lt;.*&gt;", "z")     // "z"
StringUtils.replaceAll("ABCabc123", "[a-z]", "_")                           // "ABC___123"
StringUtils.replaceAll("ABCabc123", "[^A-Z0-9]+", "_")                      // "ABC_123"
StringUtils.replaceAll("ABCabc123", "[^A-Z0-9]+", "")                       // "ABC123"
StringUtils.replaceAll("Lorem ipsum  dolor   sit", "( +)([a-z]+)", "_$2")   // "Lorem_ipsum_dolor_sit"
~~~

### replaceFirst^1

> 找到text中首次（自左向右）匹配指定正则表达式regex的部分，替换为字符串replacement

~~~java
// 声明
public static String replaceFirst(final String text, final Pattern regex, final String replacement)

// 示例
StringUtils.replaceFirst(null, *, *)                                                            // null
StringUtils.replaceFirst("any", (Pattern) null, *)                                              // "any"
StringUtils.replaceFirst("any", *, null)                                                        // "any"
StringUtils.replaceFirst("", Pattern.compile(""), "zzz")                                        // "zzz"
StringUtils.replaceFirst("", Pattern.compile(".*"), "zzz")                                      // "zzz"
StringUtils.replaceFirst("", Pattern.compile(".+"), "zzz")                                      // ""
StringUtils.replaceFirst("abc", Pattern.compile(""), "ZZ")                                      // "ZZabc"
StringUtils.replaceFirst("&lt;__&gt;\n&lt;__&gt;", Pattern.compile("&lt;.*&gt;"), "z")          // "z\n&lt;__&gt;"
StringUtils.replaceFirst("&lt;__&gt;\n&lt;__&gt;", Pattern.compile("(?s)&lt;.*&gt;"), "z")      // "z"
StringUtils.replaceFirst("ABCabc123", Pattern.compile("[a-z]"), "_")                            // "ABC_bc123"
StringUtils.replaceFirst("ABCabc123abc", Pattern.compile("[^A-Z0-9]+"), "_")                    // "ABC_123abc"
StringUtils.replaceFirst("ABCabc123abc", Pattern.compile("[^A-Z0-9]+"), "")                     // "ABC123abc"
StringUtils.replaceFirst("Lorem ipsum  dolor   sit", Pattern.compile("( +)([a-z]+)"), "_$2")    // "Lorem_ipsum  dolor   sit"
~~~

### replaceFirst^2

> 找到text中首次（自左向右）匹配指定正则表达式regex的部分，替换为字符串replacement

~~~java
// 声明
public static String replaceFirst(final String text, final String regex, final String replacement)

// 示例
StringUtils.replaceFirst(null, *, *)                                         // null
StringUtils.replaceFirst("any", (String) null, *)                            // "any"
StringUtils.replaceFirst("any", *, null)                                     // "any"
StringUtils.replaceFirst("", "", "zzz")                                      // "zzz"
StringUtils.replaceFirst("", ".*", "zzz")                                    // "zzz"
StringUtils.replaceFirst("", ".+", "zzz")                                    // ""
StringUtils.replaceFirst("abc", "", "ZZ")                                    // "ZZabc"
StringUtils.replaceFirst("&lt;__&gt;\n&lt;__&gt;", "&lt;.*&gt;", "z")        // "z\n&lt;__&gt;"
StringUtils.replaceFirst("&lt;__&gt;\n&lt;__&gt;", "(?s)&lt;.*&gt;", "z")    // "z"
StringUtils.replaceFirst("ABCabc123", "[a-z]", "_")                          // "ABC_bc123"
StringUtils.replaceFirst("ABCabc123abc", "[^A-Z0-9]+", "_")                  // "ABC_123abc"
StringUtils.replaceFirst("ABCabc123abc", "[^A-Z0-9]+", "")                   // "ABC123abc"
StringUtils.replaceFirst("Lorem ipsum  dolor   sit", "( +)([a-z]+)", "_$2")  // "Lorem_ipsum  dolor   sit"
~~~

### replacePattern

> 找到text中所有匹配指定正则表达式regex的部分，全部替换为字符串replacement

~~~java
// 声明
public static String replacePattern(final String text, final String regex, final String replacement)

// 示例
StringUtils.replacePattern(null, *, *)                                          // null
StringUtils.replacePattern("any", (String) null, *)                             // "any"
StringUtils.replacePattern("any", *, null)                                      // "any"
StringUtils.replacePattern("", "", "zzz")                                       // "zzz"
StringUtils.replacePattern("", ".*", "zzz")                                     // "zzz"
StringUtils.replacePattern("", ".+", "zzz")                                     // ""
StringUtils.replacePattern("&lt;__&gt;\n&lt;__&gt;", "&lt;.*&gt;", "z")         // "z"
StringUtils.replacePattern("ABCabc123", "[a-z]", "_")                           // "ABC___123"
StringUtils.replacePattern("ABCabc123", "[^A-Z0-9]+", "_")                      // "ABC_123"
StringUtils.replacePattern("ABCabc123", "[^A-Z0-9]+", "")                       // "ABC123"
StringUtils.replacePattern("Lorem ipsum  dolor   sit", "( +)([a-z]+)", "_$2")   // "Lorem_ipsum_dolor_sit"
~~~
