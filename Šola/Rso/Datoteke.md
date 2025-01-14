Human readable / Machine readable

java5(6)+ -> `java.io (java.nio, java.nio2)`

Reader (Filereader, ObjectReader) <- {program} -> Writer (Filewriter, Objectwriter)ž
Reader -> vrne byte
`reade(<ovoj formata zapisovanja>);`
`BufferdReader`
Writer -> vzame byte
`write(<ovoj formata zapisovanja>);`
`PrintWriter` -> println() + zapis primitivov

```java
import java.io.FileWriter;  
import java.io.IOException;  
  
public class JavanskiProgram {  
    public static void main(String[] args) {  
        FileWriter writer;  
        try {  
            writer = new FileWriter("ecka.pecka", true);  
            writer.write(65);  
            writer.write('Ž');  
            writer.close();  
        } catch (IOException e) {  
            throw new RuntimeException(e);  
        }  
    }  
}
```

Ne znam brat:
![[ne znamo brat.m4a]]

Ecka pecka original!!!!
![[Ecka pecka.m4a]]