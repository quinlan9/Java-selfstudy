in Java, Map is interface using key-value to store data. [HashMap](https://github.com/quinlan9/java/blob/main/HashMap.md)是Map接口的实现类。

不能单独使用 Map 接口来保存数据，但是我们可以创建其实现类的对象，然后使用 Map 引用来保存对象。在这里，我们使用 HashMap 类来存储数据，并使用 Map 接口来保存该类的引用。请参见下面的示例。

```java
import java.util.HashMap;
import java.util.Map;

public class SimpleTesting{
    public static void main(String[] args) {
        Map<String, Integer> mapexample = new HashMap<>();
        mapexample.put("One", 1);
        mapexample.put("Two", 2);
        mapexample.put("Three", 3);
        System.out.println(mapexample);
    }
}

output:
{One=1, Two=2, Three=3}
```
Java的HashMap类实现的是Map接口，它根据哈希函数存储键值对。这就意味着它不保证映射的顺序，特别是它不保证该顺序恒定不变。你可能看到的任何特定顺序都是偶然的，都可能随着元素的插入和删除而改变。
