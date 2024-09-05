Rekurzija - ponavljanje
iterativno (štetje ponovitev) \[for, while, do-while]:
```java
for (int i = 0; i < 6; i++) {
	System.out.println("Halo!");
}
```
rekurzivno: (ponavljajoče klicanje funkcij)
```java
void neki(a) {
	if (a == 0) return; // Pogoj zaustavitve
	System.out.println("Hallo!");
	a--;
	neki(a); // Rekurzivni klic
}
```