# map简单应用

## 描述

现在有一个`map`集合如下：
```java
  Map<Integer,String> map = new HashMap<Integer, String>();
  map.put(1, "Amy");
  map.put(2, "Joe");
  map.put(3, "Tom");
  map.put(4, "Susan");
```

  要求：
       1. 遍历集合，并将序号与对应人名打印。
       2. 向该`map`集合中插入一个编码为`5`姓名为控制台输入的人名的信息
       3. 移除该`map`中的编号为`4`的信息
       4. 将`map`集合中编号为`3`的姓名信息修改为"`Tommy`"
       5. 再次遍历经过上述操作后的集合，并将序号与对应人名打印。(注：第一次输出和第二次输出需用空行隔开)

### 输入描述：

`String`类型人名

### 输出描述：

先将题中给定的集合遍历输出，完成题中要求之后再遍历输出一次（输出格式为key+":"+value，第一次输出和第二次输出用空行隔开）

## 示例1

输入：

```
David
```

输出：

```
1:Amy
2:Joe
3:Tom
4:Susan

1:Amy
2:Joe
3:Tommy
5:David
```

## 代码

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scanner  = new Scanner(System.in);
        String name = scanner.next();
        Map<Integer, String> map = new HashMap<Integer, String>();
        map.put(1, "Amy");
        map.put(2, "Joe");
        map.put(3, "Tom");
        map.put(4, "Susan");

        //write your code here......       
    }
}
```



---



## 解题

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String name = scanner.next();
        Map<Integer, String> map = new HashMap<Integer, String>();
        map.put(1, "Amy");
        map.put(2, "Joe");
        map.put(3, "Tom");
        map.put(4, "Susan");

        // 遍历并打印集合中的内容
        for (Map.Entry<Integer, String> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ":" + entry.getValue());
        }

        // 向集合中插入新信息
        map.put(5, name);

        // 移除编号为4的信息
        map.remove(4);

        // 修改编号为3的姓名信息
        map.put(3, "Tommy");

        // 再次遍历并打印集合中的内容
        System.out.println();
        for (Map.Entry<Integer, String> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ":" + entry.getValue());
        }
    }
}
```

