# ArchUtils

> 此工具类为获取系统对应的微处理器([Processor](arch/Processor.md))信息
>
> 版本: 3.0+

## 类定义

~~~java
public class ArchUtils
~~~

## 普通函数

### getProcessor^1

> 获取当前JVM进程对象

~~~java
// 声明
public static Processor getProcessor()

// 示例
Processor processor = ArchUtils.getProcessor();
processor.getType();    // X86      处理器体系结构
processor.isX86();      // true     是否X86架构的处理器
processor.isIA64();     // false    是否是英特尔安腾处理器
processor.isPPC();      // false    是否为Apple–IBM–Motorola体系结构
processor.getArch();    // BIT_64   微处理器位值
processor.is32Bit();    // false    是否32位微处理器
processor.is64Bit();    // true     是否64位微处理器
~~~

### getProcessor^2

> 获取指定系统的当前JVM进程对象

~~~java
// 声明
public static Processor getProcessor(final String value)

// 示例
Processor processor = ArchUtils.getProcessor(SystemUtils.OS_ARCH);
processor.getType();    // X86      处理器体系结构
processor.isX86();      // true     是否X86架构的处理器
processor.isIA64();     // false    是否是英特尔安腾处理器
processor.isPPC();      // false    是否为Apple–IBM–Motorola体系结构
processor.getArch();    // BIT_64   微处理器位值
processor.is32Bit();    // false    是否32位微处理器
processor.is64Bit();    // true     是否64位微处理器
~~~
