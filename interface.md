# interface
define interface to implement comparison between 2 objects:
```java
package ...;

public interface CompareObject<object> {
    //method
    public int compareto(object o);
    //若返回值是 0 , 代表相等; 若为正数，代表当前对象大；负数代表当前对象小
}
```
define Class Circle 
```java
package ...

public class Circle {
    private double radius;
    private final double PI=3.14;

    public double findArea(){
        return PI*radius*radius;
    }

    public double getRadius() {
        return radius;
    }

    public void setRadius(double radius) {
        this.radius = radius;
    }
}
```

定义一个ComparableCircle类，继承Circle类并且实现CompareObject接口。在ComparableCircle类中给出接口中方法compareTo的实现体，用来比较两个圆的半径大小。
```java
package ...;

public class ComparableCircle extends Circle implements CompareObject<Circle> {
    @Override
    public int compareto(Circle o) {
        if(this.getRadius()==o.getRadius()){
            return 0;
        }else if(this.getRadius()<=o.getRadius()){
            return -1;
        }else {
            return 1;
        }
    }
}
```
定义一个测试类TestInterface，创建两个ComaparableCircle对象，调用compareTo方法比较两个类的半径大小。
```java
package c...;

import java.util.Scanner;

public class TestInterface {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ComparableCircle c1 = new ComparableCircle();
        ComparableCircle c2 = new ComparableCircle();
        c1.setRadius(sc.nextDouble());    //nextDouble只能输入双精度浮点数
        c2.setRadius(sc.nextDouble());
        System.out.println(c1.compareto(c2));
    }
}
```
