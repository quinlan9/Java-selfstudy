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

## Map.getOrDefault()
Map中会存储一一对应的key和value。  
如果 在Map中存在key，则返回key所对应的的value。  
如果 在Map中不存在key，则返回默认值。  
```java
public class Demo {
    public static void main(String[] args) {
        Map<String, Integer> map = new HashMap<>();
        map.put("张三", 23);
        map.put("赵四", 24);
        map.put("王五", 25);
        String age= map.getOrDefault("赵四", 30);
        System.out.println(age);// 24，map中存在"赵四",使用其对应值24
        String age = map.getOrDefault("刘能", 30);
        System.out.println(age);// 30，map中不存在"刘能",使用默认值30
    }
}
```
第一个输出为24，因为已经输入了（’'赵四"，24）的数据，所以返回其value值（24）；  
第二个输出为30，因为在Map中不存在"刘能"这个key值，所以返回getOrDefault()方法中的默认值。
