# Java HashMap  
(w3schools)  
In the ArrayList chapter, you learned that Arrays store items as an ordered collection, and you have to access them with an index number (int type). A HashMap however, store items in "key/value" pairs, and you can access them by an index of another type (e.g. a String).

One object is used as a key (index) to another object (value). It can store different types: String keys and Integer values, or the same type, like: String keys and String values:

## example:
Create a HashMap object called capitalCities that will store String keys and String values:
```java
import java.util.HashMap; // import the HashMap class
HashMap<String, String> capitalCities = new HashMap<>();
```

## add items
use put() method:
```java
// Import the HashMap class
import java.util.HashMap;

public class Main {
  public static void main(String[] args) {
    // Create a HashMap object called capitalCities
    HashMap<String, String> capitalCities = new HashMap<>();

    // Add keys and values (Country, City)
    capitalCities.put("England", "London");
    capitalCities.put("Germany", "Berlin");
    capitalCities.put("Norway", "Oslo");
    capitalCities.put("USA", "Washington DC");
    System.out.println(capitalCities);
  }
}

output:
{USA=Washington DC, Norway=Oslo, England=London, Germany=Berlin}
```
## access an item
```java
capitalCities.get("England");

output:
London
```

## remove an item
```java
capitalCities.remove("England");
```

## clear all items
```java
capitalCities.clear();
```

## entrySet()
[entrySet](https://blog.csdn.net/m0_43410048/article/details/105853164)
