koda - se lahko deli med programi
data - za vsak program svoj
stack - za vsak program svoj

**lahek proces \[nit]** - data in stack se delita znotraj enega procesa, ko delamo async procese.

**niti/Thread**
enkapsulacija:
```java
public void run() { //- lifetime start
					//|
					//|
}					//- lifetime end

class Test extends Thread {
	@Override
	public void run() {
		//telo niti
	}
}
```

Uporaba:
```java
class Test {  
    public static void main(String[] args) {  
        Thread tr1 = new Thread(new B());  
        Thread tr2 = new Thread(new B());  
        Thread tr3 = new Thread(new B());  
		  
        tr1.start();  
        tr2.start();  
        tr3.start(); 
		
		System.out.println("end");
    }  
}

//Runnable <- functional interface (ena sama metoda)
class B implements Runnable {  
    @Override  
    public void run() {  
        for (int i = 0; i < 9999999; i++) {  
            System.out.println(i%10+"");  
        }  
    }  
}
```

Lambda:
```java
class Test {  
    public static void main(String[] args) {  
        new Thread(new Runnable() {  
            @Override  
            public void run() {  
                for (int i = 0; i < 999999999; i++) {  
                    System.out.println("A");  
                }  
            }  
        }).start();  
    }  
}

//Lambda syntax:
class Test {  
    public static void main(String[] args) {  
        new Thread(() -> {  
            for (int i = 0; i < 999999999; i++) {  
                System.out.println("A");  
            }  
        }).start();  
    }  
}
```

```java
class Test {  
    public static void main(String[] args) {  
        MT tt = new MT();  
        tt.start();  
    }  
}

class MT extends Thread implements Runnable {  
    public void run() {  
        for (int i = 0; i < 100; i++) {  
            System.out.print("A ");  
            System.out.println();  
        }  
    }  
}
```