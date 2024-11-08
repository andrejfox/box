**Verjetnost** je področje matematike, ki se ukvarja s preučevanjem naključnih dogodkov.

[[Šola/Mat/Verjetnost/Vaje|Vaje]]
[[Vzorčni prostor dogodkov]]
[[Računanje verjetnosti]]
[[Verjetnost Produkta in Pogojna Verjetnost]]
[[Zaporedje poskusov]]

**Poskus** je aktivnost, ki jo izvedemo vedno na enak način in pri enakih pogojih. 

**Dogodek** je pojav, ki se pri danem poskusu lahko zgodi ali pa ne. 
Dogodke delimo na:
- <font color="#00ff00">gotove (G)</font>   npr. Bel list papirja pade na belo stran
- <font color="#ff0000">nemogoče(N) </font>  npr. Na kocki pade 0 pik
- <font color="#ffff00">slučajne(A,B,...)</font> npr. Na kocki pade 5, Kovanec na cifro, ...

V množici dogodkov imamo <u>3 relacije</u>

| RELACIJA                  | OPIS                                                          | ZAPIS        |
| ------------------------- | ------------------------------------------------------------- | ------------ |
| biti združljiv z dogodkom | A je združljiv z B, ko se **lahko** zgodita hkrati            |              |
| biti način dogodka        | A je način B, če se **vsakokrat**, ko se zgodi A zgodi tudi B | $A\subset B$ |
| biti enak dogodku         | A je enak B, če se vsakokrat zgodita **samo** hkrati          | $A = B$      |


S temi dogodki lahko tudi računamo. Računanske operacije ustrezajo računanju z množicami:

| Zapis                                   | Operacija         | Branje    | Opis                                                                   |
| --------------------------------------- | ----------------- | --------- | ---------------------------------------------------------------------- |
| $A'$                                    | nasprotni dogodek | ne A      | Nasprotni dogodek se zgodi, če se A ne zgodi                           |
| $A \cup B$                              | vsota dogodkov    | A ali B   | Dogodek $A \cup B$ se zgodi, če se zgodi prvi ali drugi                |
| $A \setminus B$ ali $A\smallsetminus B$ | razlika dogodkov  | A in ne B | Dogodek $A \setminus B$ se zgodi, če se zgodi prvi in ne drugi dogodek |
| $A \cap B$                              | produkt dogodkov  | A in B    | Dogodek $A \cap B$ se zgodi, če se zgodita prvi in drugi hkrati        |
Nekateri dogodki imajo le 1 možnost, nekatere pa si lahko razlagamo kot vsoto večih dogodkov.

*Primer: Sodo število pri metu kocke je vsota dogodkov: 2,4,6*

Dogodki, ki se zgodijo na en sam način imenujemo <font color="#b004a0">Elementarni</font> ali $E$
Ti dogodki so med seboj nezdružljivi. Iz njih z operatorji tvorimo <font color="#c06000">Sestavljene</font> ali $A, B, \dots$

*Primer: met kocke*
elementarni: $E_1, E_2, E_3, E_4, E_5, E_6$
sestavljeni: 
$A = E_1 \cup E_2 \cup E_3$
$B=E_2\cup E_4 \cup E_6$


```handdrawn-ink
{
"versionAtEmbed": "0.2.6",
"filepath": "Ink/Drawing/2024.10.22 - 13.41pm.drawing"
}
```


Množico vseh izidov danega poskusa imenujemo **vzorčni prostor poskusa**. Vsak dogodek danega poskusa lahko prikažemo kot podmnožico vzorčnega prostora. Če sta podmnožici <u>diskunktni</u>, sta pripadajoča dogodka nezdružljiva.

#### Elementarni dogodki
- Se zgodijo na en sam način
- So med seboj paroma nezdružljivi
- Vzorčni prostor je množica vseh elementarnih dogodkov danega poskusa
- Če je število elementarnih dogodkov končno, ga označimo z $n$.

#### Sestavljeni dogodki
- Se zgodijo na več načinov
- Vsak sestavljeni dogodek lahko zapišemo kot vsoto elementarnih dogodkov
- Gotovi dogodek je sestavljeni dogodek. Enak je vsoti vseh elementarnih dogodkov.
- Vsota različnih dogodkov je vedno sestavljeni dogodek. 


**Popolni sistem dogodkov** je taka množica dogodkov pri danem poskusu, da se ob vsaki ponovitvi poskusa zgodi natanko eden izmed njih. V to množico ne dajemo nemogočega in gotovega dogodka (ker ni smiselno.)