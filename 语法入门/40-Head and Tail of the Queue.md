# Head and Tail of the Queue

## 描述

Students are picked from a group of students to give speeches. To be fair, the head and tail of the queue are drawn alternately. Please implement the process of leaving the queue through the program.

### 输入描述：

A group of students' names

### 输出描述：

Print the names of the students at the head and tail of the queue alternately

## 示例1

输入：

```
Tom Jim Lily Lucy Mary
```

输出：

```
Tom
Mary
Jim
Lucy
Lily
```

## 代码

```java
import java.util.ArrayDeque;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        ArrayDeque deque = new ArrayDeque();

        Scanner scanner = new Scanner(System.in);
        while (scanner.hasNext()) {
            String name = scanner.next();
            // 初始化队列中的数据
            deque.offerLast(name);
        }

        // write your code here......
        
    }

}
```



---



## 解题

```java
import java.util.ArrayDeque;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        ArrayDeque<String> deque = new ArrayDeque<>();

        Scanner scanner = new Scanner(System.in);
        while (scanner.hasNext()) {
            String name = scanner.next();
            // 初始化队列中的数据
            deque.offerLast(name);
        }

        boolean head = true; // 用于交替选择头部和尾部

        while (!deque.isEmpty()) {
            if (head) {
                System.out.println(deque.pollFirst()); // 输出头部元素
            } else {
                System.out.println(deque.pollLast()); // 输出尾部元素
            }
            head = !head; // 切换头尾标志
        }
    }
}
```

