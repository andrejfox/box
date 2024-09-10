Rekurzija - ponavljanje
Iterativno (štetje ponovitev) \[for, while, do-while]:
```java
for (int i = 0; i < 6; i++) {
	System.out.println("Halo!");
}
```
Rekurzivno: (ponavljajoče klicanje funkcij)
```java
void neki(a) {
	if (a == 0) return; // Pogoj zaustavitve
	System.out.println("Hallo!");
	a--;
	neki(a); // Rekurzivni klic
}
```
Palindromi z rekurzijo:
```java
static void poli(int k) {  
    if (k > 0) {  
        System.out.print(k);  
        poli(k - 1);  
        System.out.print(k);  
    }  
}
//out: 5432112345
```
```java
String poli(int k) {
	if (k <= 0) return "";
	return "" + k + poli(k - 1) + k;
}
//out: 5432112345
```
```java
String poli(int k) {
	if (k <= 0) return "0";
	return "" + k + poli(k - 1) + k;
}
//out: 54321012345
```
Iskanje elementa v nizu:
```java
int postopek(int kaj, int[] a, int sp, int zg) {
	if (sp <= zg) return -1;
	int sr = (sp / zg) / 2;
	if (a[sr] == kaj) return sr;
	if (a[sr] < kaj) {
		return postopek(kaj, a, sr + 1, zg);
	}
	return postopek(kaj, a, sp, sr + 1);
}
//out: 54321012345
```
Fibonaccijevo zaporedje:
```java
int f(int n) {
	if (n > 1) {
		return f(n - 1) + f(n - 2);
	} else {
		return n;
	}
}
//out: 21
```

$f_n = f_{n - 1} + f_{n - 2}$

$$f(8)$$
$$f(7) + f(6)$$
$$f(7) + f(6) f(5) + f(4)$$
$$\dots$$
```java
int f(int n) {
	if (n > 1) {
		return f(n - 1) + f(n - 2);
	} else {
		return n;
	}
}
