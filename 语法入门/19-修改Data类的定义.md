# 修改Data类的定义

## 描述

现有一个`Data`类，内部定义了属性`x`和`y`，在`main`方法中实例化了`Data`类，并计算了`data`对象中`x`和`y`的和。但是，`Data`类的定义存在错误，请你将这些错误修正过来，使得`main`方法中的求和逻辑可以正常执行。

### 输入描述：

两个整数

### 输出描述：

两个整数的和

## 示例1

输入：

```
1 2
```

输出：

```
3
```

## 代码

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        while (scanner.hasNextInt()) {
            int x = scanner.nextInt();
            int y = scanner.nextInt();
            Data data = new Data(x, y);
            System.out.println(data.getX() + data.getY());
        }
    }

}

class Data {

    private int x;
    private int y;

    private Data(int x, int y) {
        x = x;
        y = y;
    }

    private int getX() {
        return x;
    }

    private int getY() {
        return y;
    }

}
```



---



## 解题

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        while (scanner.hasNextInt()) {
            int x = scanner.nextInt();
            int y = scanner.nextInt();
            Data data = new Data(x, y);
            System.out.println(data.getX() + data.getY());
        }
    }
}

class Data {
    private int x;
    private int y;

    public Data(int x, int y) {
        this.x = x;
        this.y = y;
    }

    public int getX() {
        return x;
    }

    public int getY() {
        return y;
    }
}
```

我们将`Data`类的构造函数和属性的访问修饰符设置为公共，使得它们可以在`Main`类中正常访问。同时，修正了构造函数中参数名和属性名相同的问题，并将`getX`和`getY`方法的访问修饰符设置为公共，以便在`Main`类中调用它们。