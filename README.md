# Akvárium - Správa ryb a výpočet objemu

## Popis aplikace

Tato React aplikace slouží pro správu akvária a ryb. Umožňuje uživatelům spravovat seznam ryb, počítat potřebný objem vody a validovat rozměry akvária.

### Hlavní funkce

#### 1. Správa ryb (Rybicky)
- **Zobrazení seznamu ryb** - tabulka s ID, jménem a velikostí každé ryby
- **Přidávání nových ryb** - formulář pro zadání jména a výběr velikosti (malá/velká)
- **Mazání ryb** - možnost odstranit rybu ze seznamu
- **Validace formuláře** - kontrola, že jsou vyplněna všechna povinná pole

#### 2. Výpočet požadovaného objemu
- **Automatický výpočet** - aplikace automaticky počítá potřebný objem vody
- **Vzorec pro výpočet**:
  - Malé ryby: 10 litrů na rybu
  - Velké ryby: 20 litrů na rybu
- **Real-time aktualizace** - objem se přepočítává při každé změně seznamu ryb

#### 3. Validace akvária (Akvarium)
- **Zadání rozměrů** - formulář pro šířku, délku a výšku akvária
- **Výpočet objemu** - automatický výpočet objemu zadaných rozměrů
- **Validace** - porovnání dostupného objemu s požadovaným objemem
- **Vizuální zpětná vazba** - tlačítko se mění na zelené/červené podle validity

### Technické detaily

- **Frontend framework**: React 19.0.0
- **Bundler**: Vite 6.1.0
- **Styling**: Bootstrap 5.3.3
- **Struktura**: Komponentový přístup s useState a useEffect hooks
- **Data**: Lokální JSON soubor s výchozími rybami

### Struktura projektu

```
src/
├── components/
│   ├── Rybicky.jsx      # Komponenta pro správu ryb
│   ├── Akvarium.jsx     # Komponenta pro validaci akvária
│   └── *.css            # Styly komponent
├── App.jsx              # Hlavní aplikace
├── rawData.json         # Výchozí data ryb
└── main.jsx             # Vstupní bod aplikace
```

### Jak aplikace funguje

1. **Počáteční stav**: Aplikace načte výchozí seznam ryb z `rawData.json`
2. **Správa ryb**: Uživatel může přidávat nové ryby nebo mazat existující
3. **Výpočet objemu**: Při každé změně se automaticky přepočítá požadovaný objem
4. **Validace akvária**: Uživatel zadá rozměry akvária a aplikace ověří, zda je objem dostatečný

### Spuštění aplikace

```bash
# Instalace závislostí
npm install

# Spuštění vývojového serveru
npm run dev

# Sestavení pro produkci
npm run build
```

---

**Autor**: Robin Lassak  
**Vytvořeno**: Jako školní celodenní cvičení v limitu 6 hodin  
**Technologie**: React, Vite, Bootstrap  
**Datum**: 2025
