




# Název testu                      ← začíná nový test

? Otázka s výběrem                 ← otázka
+ správná možnost                  ← právě jedna +
- špatná možnost                   ← aspoň jedna -
"" vysvětlení správné odpovědi (pokud je to potřeba)

? Volná otázka, hodnotím se sám    ← pro psané odpovědi, kde jde odpovědět více způsoby,
                                     např. vysvětlení elektromagnetu
= Rusko, Velká Británie, USA                           ← správná odpověď (zobrazí se po odpovědi)
= Německo, Rakousko-Uhersko, Osmanská říše             ← další správná varianta, zobrazí se také
// tady vysvětlení potřeba, jinak by na začátku řádku bylo ""
? Volná otázka, kontroluje stránka
== 2*x                             ← uznána jen tato odpověď
== x*2                             ← případně další uznaná varianta
"" vysvětlení
// řádek začínající // je poznámka a ignoruje se


## Zlomky

Zlomek se zapisuje jako `(čitatel(/)jmenovatel)` a zobrazí se jako zlomek s čitatelem nad jmenovatelem.

| Zapíšeš | Zobrazí se |
|---|---|
| `(4(/)2)` | 4 nad 2 |
| `(1(/)3)` | 1 nad 3 |
| `((x+1)(/)2)` | (x+1) nad 2 |

Zlomky fungují všude, kde se zobrazuje text zadání:

- v **textu otázky** (za `?`),
- v **možnostech** u otázek s výběrem (za `+` a `-`),
- ve **správných odpovědích** u volných otázek (za `=` a `==`), které se zobrazí po odpovědi.

Příklad:

```
# Zlomky

? Kolik je (1(/)2) + (1(/)4)?
+ (3(/)4)
- (2(/)6)
- (1(/)8)
"" nejdříve převdeme oba zlomky na společného jmenovatele, to uděláme tak, že......

? Zkrať zlomek (4(/)8).
== 1/2
== 0,5
"" čitatel i jmenovatel můžeme vydělit čtyřmi......
```

Poznámky:

- V čitateli a jmenovateli může být jedna úroveň závorek, např. `((x+1)(/)2)`. Zlomek uvnitř zlomku zatím není podporovaný.
- U otázek kontrolovaných stránkou (`==`) se zapsaný zlomek `(1(/)2)` bere stejně jako `1/2`. Žák tedy může do pole napsat `1/2` i `(1(/)2)` a obojí se uzná. Jiné tvary, např. `0,5`, je potřeba uvést jako další variantu.
- Běžné závorky jako ve `f(x)` se nemění, jen zápis s `(/)` uprostřed.
- vysvětlení odpovědi funguje u všech typů úloh 
