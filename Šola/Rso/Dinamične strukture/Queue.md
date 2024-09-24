Seznami:
- enosmerno povezani
- dvosmerno povezani
- realizacija:
	- s stražarjem
	- brez ?

```java
//Queue (queue):
class El1 {
	int vr;
	EL1 nasl; //naslov naslednega
}
//Double ended queue (dequeue):
class El1 {
	int vr;
	EL2 nasl; //naslov nasledneg
	EL2 pred; //naslov prejšnega
}
```
```java
class main {
	public static void main(String[] args) {
		System.out.println("Nejko smejko");
	}
}
```
```java
package Testing;  
  
import java.util.LinkedList;  
import java.util.List;  
  
class Test {  
    // add, clear, contains, get, remove, size, to array  
    static List list = new LinkedList();  
    public static void main(String[] args) {  
        System.out.println(list.size());  
  
        list.add(6);  
        System.out.println(list.size());  
  
        for (int i = 0; i < 5; i++) {  
            System.out.println(list.add((int) (Math.random() * 50)));  
        }  
        System.out.println(list.size());  
  
        for (Object o : list) {  
            System.out.print(o);  
            System.out.println(o instanceof Integer);  
        }  
    }  
}
```