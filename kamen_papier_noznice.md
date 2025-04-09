
# Program 03  
## Vytvoríme si jednoduchú hru **Kameň – Papier – Nožnice** ✊📄✂️

```python
import random

moznosti = ["kamen", "papier", "noznice"]
pocitac = random.choice(moznosti)
hrac = input("Vyber si: kamen, papier alebo noznice: ").lower()

print(f"👤 Hráč si vybral: {hrac}")
print(f"💻 Počítač si vybral: {pocitac}")

if hrac == pocitac:
    print("🤝 Remíza!")
elif (hrac == "kamen" and pocitac == "noznice") or      (hrac == "papier" and pocitac == "kamen") or      (hrac == "noznice" and pocitac == "papier"):
    print("🎉 Vyhrávaš!")
else:
    print("💻 Vyhráva počítač!")
```

---

### Otázky ❓
1. Aké sú možnosti výhry hráča?
2. Čo sa stane, ak hráč zadá nesprávny vstup (napr. „strom“)?

---

### Úlohy 💡
1. Pridaj kontrolu neplatného vstupu a upozorni hráča.
2. Nech sa hra opakuje, kým hráč nenapíše „koniec“.
3. Po každom kole zobraz aktuálne skóre (hráč vs. počítač).

---

### Riešenia ✅

#### 1. Kontrola vstupu
```python
if hrac not in moznosti:
    print("❌ Neplatná voľba. Skús to znova.")
    exit()
```

#### 2. Opakovanie hry
```python
import random

moznosti = ["kamen", "papier", "noznice"]
skore_hrac = 0
skore_pocitac = 0

while True:
    hrac = input("Vyber si: kamen, papier, noznice (alebo napis 'koniec'): ").lower()
    
    if hrac == "koniec":
        print("👋 Koniec hry.")
        break

    if hrac not in moznosti:
        print("❌ Neplatná voľba.")
        continue

    pocitac = random.choice(moznosti)
    print(f"👤 Hráč: {hrac} | 💻 Počítač: {pocitac}")

    if hrac == pocitac:
        print("🤝 Remíza!")
    elif (hrac == "kamen" and pocitac == "noznice") or          (hrac == "papier" and pocitac == "kamen") or          (hrac == "noznice" and pocitac == "papier"):
        print("🎉 Vyhrávaš!")
        skore_hrac += 1
    else:
        print("💻 Vyhráva počítač!")
        skore_pocitac += 1

    print(f"📊 Skóre – Hráč: {skore_hrac} | Počítač: {skore_pocitac}")
```
