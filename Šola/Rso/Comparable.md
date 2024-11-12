```java
package Testing;  

import java.util.Arrays;  
  
class Test {  
    public static void main(String[] args) {  
        B b = new B();  
        b.sort();  
        System.out.println(b);  
    }  
}  
  
class A implements Comparable {  
    public int x;  
    public int y;  
  
    public int compareTo(Object o) {  
        A sa = (A) o;  
        if (x < sa.x) return -1;  
        if (x > sa.y) return 1;  
        return 0;  
    }  
  
    public A(int x, int y) {  
        this.x = x;  
        this.y = y;  
    }  
      
    public String toString() {  
        return "(" + x + ", " + y + ")";  
    }  
}  
  
class B {  
    public A[] arr;  
  
    public B() {  
        A[] arr = new A[10];  
        for (int i = 0; i < 10; i++) {  
            arr[i] = new A((int) (Math.random() * 6), (int) (Math.random() * 6));  
        }  
        this.arr = arr;  
    }  
  
    public B(A[] arr) {  
        this.arr = arr;  
    }  
  
    public void sort() {  
        Arrays.sort(arr);  
    }  
  
    public String toString() {  
        StringBuilder ret = new StringBuilder();  
        for (A a : arr) {  
            ret.append(a).append(", ");  
        }  
        return "[ " + ret + " ]";  
    }  
}
```

```java
import java.util.Arrays;  
import java.util.Collections;  
import java.util.Comparator;  
  
class Test {  
    public static void main(String[] args) {  
        Integer[] arr = {1, 3, 12, 5, 7, 6, 6};  
        Arrays.sort(arr, Collections.reverseOrder());  
        System.out.println(Arrays.toString(arr));  
        Arrays.sort(arr, (a, b) -> {  
            if (a % 2 != 0 && b % 2 == 0) return -1;  
            return 1;  
        });  
        System.out.println(Arrays.toString(arr));  
        Arrays.sort(arr, new C());  
        System.out.println(Arrays.toString(arr));  
    }  
}  
  
class C implements Comparator<Integer> {  
    public int compare(Integer a, Integer b) {  
        if (a % 2 != 0 && b % 2 == 0) return 1;  
        return -1;  
    }  
}
```