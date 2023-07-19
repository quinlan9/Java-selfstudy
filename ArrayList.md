# ArrayList
The ArrayList class is a resizable array, which can be found in the java.util package.

The difference between a built-in array and an ArrayList in Java, is that the size of an array cannot be modified (if you want to add or remove elements to/from an array, you have to create a new one). While elements can be added and removed from an ArrayList whenever you want. The syntax is also slightly different:

## example:
create an ArrayList object called cars that will store strings:
```java
import java.util.ArrayList; // import the ArrayList class

ArrayList<String> cars = new ArrayList<String>(); // Create an ArrayList object
```

## Add items:
```java
import java.util.ArrayList;

public class Main {
  public static void main(String[] args) {
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    System.out.println(cars);
  }
}

output:
[Volvo, BMW, Ford, Mazda]
```

## Access an Item:
```java
cars.get(0);

output:
Vlovo
```

## Change an Item;
```java
cars.set(0,"Opel");

output:
[Opel, BMW, Ford, Mazda]
```

## remove an item
```java
cars.remove(0);
```

## remove all the elements in the ArrayList
```java
cars.clear();
```

## ArrayList Size
to find out how many elements an ArrayList have
```java
cars.size();

output:
4
```

# Loop through an ArrayList
```java
public class Main{
  public static void main(String[] args){
    ArrayList<String> cars = new ArrayList<String>();
    cars.add("Volvo");
    cars.add("BMW");
    cars.add("Ford");
    cars.add("Mazda");
    for(int i=0;i<cars.size();i++){
      System.out.println(cars.get(i));
    }
    //or use for-each loop:
    for(String i: cars){
      System.out.println(i);
    }
  }
}

output:
Volvo
BMW
Ford
Mazda
```
