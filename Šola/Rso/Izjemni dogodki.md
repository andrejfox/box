Exception <- (managed) moramo obravnavati 
- IOException
Runtime Exception <- (unmanaged) ni potrebno obravnavati
- indexOutOutOfRagneException
obravnava, delegiranje
 ```java
 try {
	 // testni blok
 } catch (TipIzjeme e) {
	 // obravnavanje
 }
 ```

Proženje izjem
**Definicija lastne izjeme**
Vse izjeme če jih hočemo uporabiti so izvedene iz *Exception*.
Lovljenje se izvrši glede na tip izjeme.

> [!NOTE] Kastelic quote
> Ecka pecka pošto pela, ecka pecka o pošta se prevrne.

```java
class Main {
	public static void main(String[] args) {
		proziIzjemo();
	}
	
	static void proziIzjemo() throws mojaIzjemaException {
		throw new mojaIzjemaException();
	}
}

//unmanaged
class mojaIzjemaException extends RuntimeException {}

//managed
class mojaDrugaIzjemaException extends Exception {}
```

```java

class Main {
	public static void main(String[] args) {
		try {
			for(int i = 0; i < 100; i++) {
				if (i > 55) {
					proziIzjemo();
				}
				System.out.print(i + " ");
			}
		} catch (mojaIzjemaException e) {
			System.out.println("\n" + e);
		}
	}
	static void proziIzjemo() throws mojaIzjemaException {
		throw new mojaIzjemaException();
	}
}

//unmanaged
class mojaIzjemaException extends RuntimeException {}

//managed
class mojaDrugaIzjemaException extends Exception {}
```

```java
class Main {
	public static void main(String[] args) {
		try {
			test();
		} catch (mojaIzjemaException e) {
			System.out.println("\n" + e);
		}
	}
	
	static void test() throws mojaIzjemaException {
		for(int i = 0; i < 100; i++) {
			if (i > 55) {
				proziIzjemo();
			}
			System.out.print(i + " ");
		}
	}
	
	static void proziIzjemo() throws mojaIzjemaException {
		throw new mojaIzjemaException();
	}
}

//unmanaged
class mojaIzjemaException extends RuntimeException {}

//managed
class mojaDrugaIzjemaException extends Exception {}
```