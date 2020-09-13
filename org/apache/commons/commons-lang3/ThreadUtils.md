# ThreadUtils

> 线程Thread与线程组ThreadGroup工具类
>
> 版本： 3.5+

~~~java
public class ThreadUtils
~~~

## 静态成员

~~~java
// 判定结果恒定为true的线程[组]判断接口
public static final AlwaysTruePredicate ALWAYS_TRUE_PREDICATE = new AlwaysTruePredicate()
~~~

## 函数方法

### findThreadById^1

> 根据线程标识threadId在它所属的线程组threadGroup中找到对应的活的线程

~~~java
// 声明
public static Thread findThreadById(final long threadId, final ThreadGroup threadGroup)

// 示例
ThreadGroup threadGroup = new ThreadGroup("group1");
Thread thread = new Thread(threadGroup, () -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
});
thread.start();
long threadId = thread1.getId();
ThreadUtils.findThreadById(threadId, threadGroup);          //Thread[Thread-0,5,group1]
~~~

### findThreadById^2

> 根据线程标识threadId在它所属的线程组threadGroupName中找到对应的活的线程

~~~java
// 声明
public static Thread findThreadById(final long threadId, final String threadGroupName)

// 示例
ThreadGroup threadGroup = new ThreadGroup("group1");
Thread thread = new Thread(threadGroup, () -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
});
thread.start();
long threadId = thread1.getId();
ThreadUtils.findThreadById(threadId, "group1");          //Thread[Thread-0,5,group1]
~~~

### findThreadsByName^1

> 根据线程名称threadName在它所属的线程组threadGroup中找到对应的所有活的线程

~~~java
// 声明
public static Collection<Thread> findThreadsByName(final String threadName, final ThreadGroup threadGroup)

// 示例
ThreadGroup threadGroup = new ThreadGroup("group1");
Thread thread1 = new Thread(threadGroup, () -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread");
thread1.start();
Thread thread2 = new Thread(threadGroup, () -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread");
thread2.start();
ThreadUtils.findThreadsByName("thread", threadGroup);        // [Thread[thread,5,group1], Thread[thread,5,group1]]
~~~

### findThreadsByName^2

> 根据线程名称threadName在它所属的线程组threadGroupName中找到对应的所有活的线程

~~~java
// 声明
public static Collection<Thread> findThreadsByName(final String threadName, final String threadGroupName)

// 示例
ThreadGroup threadGroup = new ThreadGroup("group1");
Thread thread1 = new Thread(threadGroup, () -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread");
thread1.start();
Thread thread2 = new Thread(threadGroup, () -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread");
thread2.start();
ThreadUtils.findThreadsByName("thread", "group1");        // [Thread[thread,5,group1], Thread[thread,5,group1]]
~~~

### findThreadGroupsByName

> 根据线程组名称threadGroupName找到对应的所有活的线程组，无法获取到系统级线程组

~~~java
// 声明
public static Collection<ThreadGroup> findThreadGroupsByName(final String threadGroupName)

// 示例
ThreadGroup threadGroup1 = new ThreadGroup("group1");
ThreadUtils.findThreadGroupsByName("group1");           // [java.lang.ThreadGroup[name=group1,maxpri=10]]
~~~

### getAllThreadGroups

> 获取对应的所有活的线程组，不包括系统级线程组

~~~java
// 声明
public static Collection<ThreadGroup> getAllThreadGroups()

// 示例
ThreadGroup threadGroup1 = new ThreadGroup("group1");
ThreaUtils.getAllThreadGroups();                        // [java.lang.ThreadGroup[name=main,maxpri=10], java.lang.ThreadGroup[name=group1,maxpri=10]]
threadGroup1.destroy();
ThreaUtils.getAllThreadGroups();                        // [java.lang.ThreadGroup[name=main,maxpri=10]]
~~~

### getSystemThreadGroup

> 获取系统级线程组

~~~java
// 声明
public static ThreadGroup getSystemThreadGroup()

// 示例
ThreaUtils.getSystemThreadGroup();                        // java.lang.ThreadGroup[name=system,maxpri=10]
~~~

### getAllThreads

> 获取系统所有活的线程

~~~java
// 声明
public static Collection<Thread> getAllThreads()

// 示例
ThreadUtils.getAllThreads();            // [Thread[main,5,main]]
Thread thread1 = new Thread(() -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
});
thread1.start();
ThreadUtils.getAllThreads();            // [Thread[main,5,main], Thread[Thread-0,5,main]]
~~~

### findThreadsByName

> 根据线程名threadName找到所有活的线程

~~~java
// 声明
public static Collection<Thread> findThreadsByName(final String threadName)

// 示例
Thread thread1 = new Thread(() -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread");
thread1.start();
Thread thread2 = new Thread(() -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread2 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread");
thread2.start();
ThreadUtils.findThreadsByName("thread");        // [Thread[thread,5,main], Thread[thread,5,main]]
~~~

### findThreadById

> 根据线程标识threadId找到对应活的线程

~~~java
// 声明
public static Thread findThreadById(final long threadId)

// 示例
Thread thread1 = new Thread(() -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
});
thread1.start();
long thread1Id = thread1.getId();
ThreadUtils.findThreadById(thread1Id);        // Thread[Thread-0,5,main]
~~~

### findThreads^1

> 找到所有匹配线程判定接口predicate的活的线程

~~~java
// 声明
public static Collection<Thread> findThreads(final ThreadPredicate predicate)

// 示例
new Thread(() -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread").start();
ThreadUtils.findThreads(thread -> "thread".equals(thread.getName()));   // [Thread[thread,5,main]]
~~~

### findThreads^2

> 查找所有匹配线程判定接口predicate的属于指定线程组group的所有活的线程，recurse表示是否递归查询线程组group的子组

~~~java
// 声明
public static Collection<Thread> findThreads(final ThreadGroup group, final boolean recurse, final ThreadPredicate predicate)

// 示例
ThreadGroup parentGroup = new ThreadGroup("parentGroup");
ThreadGroup subThreadGroup = new ThreadGroup(parentGroup, "subGroup");
new Thread(subThreadGroup, () -> {
    for (int i = 0; i < 10; i++) {
        System.out.println("thread1 is running...");
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
        }
    }
}, "thread").start();
ThreadUtils.findThreads(parentGroup, true, thread -> "thread".equals(thread.getName()));        // [Thread[thread,5,subGroup]]
ThreadUtils.findThreads(parentGroup, false, thread -> "thread".equals(thread.getName()));        // []
~~~

### findThreadGroups^1

> 找到所有匹配线程组判定接口predicate的活的线程组

~~~java
// 声明
public static Collection<ThreadGroup> findThreadGroups(final ThreadGroupPredicate predicate)

// 示例
ThreadGroup parentGroup = new ThreadGroup("parentGroup");
ThreadGroup subThreadGroup1 = new ThreadGroup(parentGroup, "subGroup1");
ThreadGroup subThreadGroup2 = new ThreadGroup(parentGroup, "subGroup2");
ThreadGroup subThreadGroup3 = new ThreadGroup(parentGroup, "subGroup3");
ThreadUtils.findThreadGroups(threadGroup -> threadGroup.getName().contains("Group"));      // [java.lang.ThreadGroup[name=parentGroup,maxpri=10], java.lang.ThreadGroup[name=subGroup1,maxpri=10], java.lang.ThreadGroup[name=subGroup2,maxpri=10], java.lang.ThreadGroup[name=subGroup3,maxpri=10]]
ThreadUtils.findThreadGroups(threadGroup -> threadGroup.getName().startsWith("subGroup"));      // [java.lang.ThreadGroup[name=subGroup1,maxpri=10], java.lang.ThreadGroup[name=subGroup2,maxpri=10], java.lang.ThreadGroup[name=subGroup3,maxpri=10]]
~~~

### findThreadGroups^2

> 递归recurse查找所有匹配线程组判定接口predicate的指定线程组group的所有活的子线程组，recurse表示是否递归查询线程组group的子组

~~~java
// 声明
public static Collection<ThreadGroup> findThreadGroups(final ThreadGroup group, final boolean recurse, final ThreadGroupPredicate predicate)

// 示例
ThreadGroup parentGroup = new ThreadGroup("parentGroup");
ThreadGroup subThreadGroup1 = new ThreadGroup(parentGroup, "subGroup1");
ThreadGroup subThreadGroup2 = new ThreadGroup(parentGroup, "subGroup2");
ThreadGroup subThreadGroup3 = new ThreadGroup(parentGroup, "subGroup3");
ThreadUtils.findThreadGroups(parentGroup, true, threadGroup -> threadGroup.getName().contains("Group"));      // [java.lang.ThreadGroup[name=subGroup1,maxpri=10], java.lang.ThreadGroup[name=subGroup2,maxpri=10], java.lang.ThreadGroup[name=subGroup3,maxpri=10], java.lang.ThreadGroup[name=subSubGroup1,maxpri=10]]
ThreadUtils.findThreadGroups(parentGroup, false, threadGroup -> threadGroup.getName().contains("Group"));      // [java.lang.ThreadGroup[name=subGroup1,maxpri=10], java.lang.ThreadGroup[name=subGroup2,maxpri=10], java.lang.ThreadGroup[name=subGroup3,maxpri=10]]
~~~
