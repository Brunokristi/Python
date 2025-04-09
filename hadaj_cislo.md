
# Program 03  
## Vytvoríme si jednoduchú hru **Hádaj číslo** 🎯

```python
# Hra: Hádaj číslo
import random

print("🎲 Vítaj v hre: Hádaj číslo!")

tajne_cislo = random.randint(1, 100)
pokusy = 0

while True:
    tip = input("Zadaj číslo medzi 1 a 100: ")

    if not tip.isdigit():
        print("⚠️ Zadaj prosím platné celé číslo.")
        continue

    tip = int(tip)
    pokusy += 1

    if tip < tajne_cislo:
        print("🔼 Moje číslo je väčšie.")
    elif tip > tajne_cislo:
        print("🔽 Moje číslo je menšie.")
    else:
        print(f"🎉 Správne! Uhádol si číslo {tajne_cislo} na {pokusy}. pokus.")
        break
```

---

### Otázky ❓
1. Vysvetli, čo robí premenná `pokusy` a ako sa mení počas hry.
2. Čo sa stane, ak zadáme napr. slovo alebo špeciálny znak namiesto čísla?

---

### Úlohy 💡
1. Zmeň rozsah tajného čísla podľa úrovne obtiažnosti:
   - ľahká: 1–10
   - stredná: 1–100
   - ťažká: 1–1000  
   #### Hint 🔍 `input`, `if`, `elif`

2. Pridaj možnosť opakovať hru po uhádnutí čísla (spýtať sa hráča, či chce hrať znova).

---

### Riešenia ✅

#### 1. Obtiažnosti
```python
import random

print("🎯 Vítaj v hre: Hádaj číslo!")

# Výber obtiažnosti
obtiaznost = input("Vyber si obtiažnosť (lahka / stredna / tazka): ").lower()

if obtiaznost == "lahka":
    max_cislo = 10
elif obtiaznost == "tazka":
    max_cislo = 1000
else:
    max_cislo = 100

tajne_cislo = random.randint(1, max_cislo)
pokusy = 0

print(f"(🔢 Uhádni číslo medzi 1 a {max_cislo})")

while True:
    tip = input("Zadaj svoj tip: ")

    if not tip.isdigit():
        print("⚠️ Zadaj prosím platné celé číslo.")
        continue

    tip = int(tip)
    pokusy += 1

    if tip < tajne_cislo:
        print("🔼 Moje číslo je väčšie.")
    elif tip > tajne_cislo:
        print("🔽 Moje číslo je menšie.")
    else:
        print(f"🎉 Správne! Uhádol si číslo {tajne_cislo} na {pokusy}. pokus.")
        break

```

#### 2. Opakovanie hry
```python
import random

print("🎯 Vítaj v hre: Hádaj číslo!")

while True:
    # Výber obtiažnosti
    obtiaznost = input("Vyber si obtiažnosť (lahka / stredna / tazka): ").lower()

    if obtiaznost == "lahka":
        max_cislo = 10
    elif obtiaznost == "tazka":
        max_cislo = 1000
    else:
        max_cislo = 100

    tajne_cislo = random.randint(1, max_cislo)
    pokusy = 0

    print(f"(🔢 Uhádni číslo medzi 1 a {max_cislo})")

    while True:
        tip = input("Zadaj svoj tip: ")

        if not tip.isdigit():
            print("⚠️ Zadaj prosím platné celé číslo.")
            continue

        tip = int(tip)
        pokusy += 1

        if tip < tajne_cislo:
            print("🔼 Moje číslo je väčšie.")
        elif tip > tajne_cislo:
            print("🔽 Moje číslo je menšie.")
        else:
            print(f"🎉 Správne! Uhádol si číslo {tajne_cislo} na {pokusy}. pokus.")
            break

    znova = input("Chceš hrať znova? (ano/nie): ")
    if znova.lower() != "ano":
        print("👋 Ďakujeme za hranie!")
        break

```

---

> **Bonusové úlohy** ➕  
> - Pridaj obmedzený počet pokusov – ak ho hráč minie, hra končí.  

