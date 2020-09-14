# AnnotationUtils

> 注解工具类，这个类所包含的实用方法使得注解使用起来更加方便
>
> 版本: 3.0+

## 类定义

~~~java
public class AnnotationUtils
~~~

## 构造函数

~~~java
// 编程过程中不要去构建实例，此默认构造方法为需要提供JavaBean实例的工具使用
public AnnotationUtils()
~~~

## 函数方法

### equals

> 校验两个注解是否相等;
>
> 深度比较;
>
> 都为null时返回true;

~~~java
// 声明
public static boolean equals(final Annotation a1, final Annotation a2);

// 示例
a1 => @Table("t_user");
a2 => @Table("t_job");
boolean r = AnnotationUtils.equals(a1, a2); // r = false
~~~

### toString

> 生成指定注解的字符串描述

~~~java
// 声明
public static String toString(final Annotation a);

// 示例
a => @Table("t_user");
String str = AnnotationUtils.toString(a); // str = @com.test.Table(value = "t_user")
~~~

### hashCode

> 生成给定注解的哈希值

~~~java
// 声明
public static int hashCode(final Annotation a);

// 示例
a => @Table("t_user");
int h = AnnotationUtils.hashCode(a); // h = -123452
~~~

### isValidAnnotationMemberType

> 检查指定类型是否为一 个注解

~~~java
// 声明
public static boolean isValidAnnotationMemberType(Class<?> type);

// 示例
boolean is = AnnotationUtils.isValidAnnotationMemberType(Table.class);   // is = true
boolean is = AnnotationUtils.isValidAnnotationMemberType(HashMap.class); // is = false
~~~
