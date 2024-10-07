$\log_2{N}$
$\log_3{N}$
[[Untitled.canvas]]
```java
class Main{
	public static void main(String[] args) {
		System.out.println("hello svit");
	}
}

class Vozu{
	int km, kv;
	Vozu L, S, D;
	public Vozu(int km) {
		this.km = km;
		Vozu L = S = D = null;
	}

	void izrisi(Vozu v) {
		if (v != null) {
			izrisi(v.L);
			System.out.println(v.km);
			izrisi(v.D);
		}
	}
	
	void izrisi2(Vozu v) {
		if (v != null) {
			izrisi2(v.L);
			System.out.println(v.km);
			izrisi2(v.S);
			System.out.println(v.kv);
			izrisi2(v.D);
		}
	}
}

