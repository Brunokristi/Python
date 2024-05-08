# Program 01
## Vytvoríme si jednoduchú kalkulačku 

``` python
print("Vitaj v mojej jednoduchej kalkulačke")

while True:
    a = input("Zadaj 1. číslo: ")
    b = input("Zadaj 2. číslo: ")

    operacia = input("Zadaj operáciu (+, -, *, /): ")

    if operacia == "+":
        print("Výsledok je: ", int(a) + int(b))
    elif operacia == "-":
        print("Výsledok je: ", int(a) - int(b))
    elif operacia == "*":
        print("Výsledok je: ", int(a) * int(b))
    elif operacia == "/":
        print("Výsledok je: ", int(a) / int(b))
    else:
        print("Neznáma operácia")
```


### Otázky ❓:
1. Vysvetlite ako funguje daný kód.

2. Čo sa stane ak namiesto čísla zadáme do kalkulačky iný znak?

### Úlohy 💡:
1. Chceme obmedziť vstup iba na čísla

    #### Hint🔍 `input numbers python`

2. Pri každom novom príklade chceme, aby sa nám zobrazil text: “Nový príklad”

3. Prerobte program aby bral na vstup 3 čísla a vedel iba oparácie + a -



### Riešenia ✅:
1. 
``` python
print("Vitaj v mojej jednoduchej kalkulačke")

while True:
    a = int(input("Zadaj 1. číslo: "))
    b = int(input("Zadaj 2. číslo: "))

    operacia = input("Zadaj operáciu (+, -, *, /): ")

    if operacia == "+":
        print("Výsledok je: ", int(a) + int(b))
    elif operacia == "-":
        print("Výsledok je: ", int(a) - int(b))
    elif operacia == "*":
        print("Výsledok je: ", int(a) * int(b))
    elif operacia == "/":
        print("Výsledok je: ", int(a) / int(b))
    else:
        print("Neznáma operácia")
```
 
2. 
``` python
print("Vitaj v mojej jednoduchej kalkulačke")

while True:
    print(“Nový príklad”)
    a = int(input("Zadaj 1. číslo: "))
    b = int(input("Zadaj 2. číslo: "))

    operacia = input("Zadaj operáciu (+, -, *, /): ")

    if operacia == "+":
        print("Výsledok je: ", int(a) + int(b))
    elif operacia == "-":
        print("Výsledok je: ", int(a) - int(b))
    elif operacia == "*":
        print("Výsledok je: ", int(a) * int(b))
    elif operacia == "/":
        print("Výsledok je: ", int(a) / int(b))
    else:
        print("Neznáma operácia")
```
 
3. 
``` python
print("Vitaj v mojej jednoduchej kalkulačke")

while True:
    print(“Nový príklad”)
    a = int(input("Zadaj 1. číslo: "))
    b = int(input("Zadaj 2. číslo: "))
    c = int(input("Zadaj 3. číslo: "))

    operacia_1 = input("Zadaj 1. operáciu (+, -): ")
    operacia_2 = input("Zadaj 2. operáciu (+, -): ")

    if operacia_1 == "+":
        medzivysledok = a + b
    elif operacia_1 == "-":
        medzivysledok = a - b
    
    if operacia_2 == "+":
        vysledok = medzivysledok + c
    elif operacia_2 == "-":
        vysledok = medzivysledok - c

    print("Výsledok : ", vysledok)
```

> **Bonusové úlohy**  ➕

> Upravte kalkulačku tak, aby brala aj * a /.







