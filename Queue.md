
  Queue是java中实现队列的接口，它总共只有6个方法，常用LinkedList 和 PriorityQueue  

  压入元素(添加): add()    offer()  
    相同：未超出容量，从队尾压入元素，返回压入的那个元素。  
    区别：在超出容量时，add()方法会对抛出异常，offer()返回false
    
  弹出元素(删除): remove()    poll()  
    相同：容量大于0的时候，删除并返回队头被删除的那个元素。  
    区别：在容量为0的时候，remove()会抛出异常，poll()返回false

  获取队头元素(不删除): element()  peek()  
    相同：容量大于0的时候，都返回队头元素。但是不删除。  
    区别：容量为0的时候，element()会抛出异常，peek()返回null。


```java
public class QueueTest{
  public static void main(String[] args){
    Queue<String> que = new LinkedList<String>();
    //添加元素
    que.offer("A");
    que.offer("B");
    que.offer("C");
    que.offer("D");
    que.offer("E");
    for(String q:que){
      System.out.println(q);
    }
    // A
    // B
    // C
    // D
    // E

    System.out.println("poll="+que.poll()); //返回第一个元素 并在队列中删除
    // poll=A
    for(String q:que){
      System.out.println(q);
    }
    // B
    // C
    // D
    // E

    System.out.println("element="+que.element()); //返回第一个元素, 不删除
    // element=B

  }
}


```
