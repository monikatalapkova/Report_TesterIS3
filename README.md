# Report_TesterIS3
Bug reports and documentation for app TesterIS3.
# Základné informácie

Mojou úlohou bolo otestovať funkčnosť programu **TesteriS3.exe** a zabezpečiť, že funguje správne a spĺňa všetky stanovené požiadavky. Testovanie prebiehalo na základe testovacieho scenára, ktorý som vypracovala na základe zadaných pokynov.  
Na testovanie bol použitý operačný systém **Ubuntu 24.04.1 LTS**.

# Metodika testovania

Testovanie aplikácie zahŕňalo manuálne testovanie, testovanie hraničných prípadov a negatívne testovanie, ktoré sa riadilo predpísaným testovacím scenárom. Tento scenár bol vytvorený na základe funkčnej špecifikácie a požiadaviek.  

Okrem overovania funkčnosti som sa zamerala aj na to, aby bol formulár intuitívny a používateľsky prívetivý. V rámci testovania som zohľadnila aj hraničné prípady, ako sú minimálne a maximálne hodnoty pre vstupy, a vykonala negatívne testy na overenie správania aplikácie pri neplatných vstupoch.  

Prehľadný záznam o chybách bol dokumentovaný aj v Excel súbore, ktorý je súčasťou prílohy.
# Testovací scenár

**Cieľ:** Otestovať funkčnosť formulára zdravotnej karty pacienta a zabezpečiť, že splňuje všetky požiadavky.

### 1. Vytvorenie formulára
- Otestovať možnosť vytvoriť formulár.

### 2. Vkladanie pacientov
- Vloženie základných povinných údajov:  
  Otestujte zadanie mena, priezviska, dátumu narodenia a poisťovne.
- Skontrolujte, či sú všetky údaje povinné a aký môže byť ich formát.
- Overte, či aplikácia poskytuje jasné a používateľsky zrozumiteľné chybové hlásenia pri nesprávnych údajoch.

### 3. Vloženie nepovinných údajov
- Otestujte zadanie pohlavia, výšky, váhy, krvnej skupiny a pracovnej pozície.
- Vyskúšajte zadať extrémne hodnoty (napr. 0 a iné).
- Otestujte, či môžete do poľa pre text vložiť číslo a naopak.
- Skontrolujte, či je možné vybrať viacero pohlaví, ani jedno alebo jedno.
- Overte, či aplikácia poskytuje jasné chybové hlásenia pri nesprávnych údajoch.

### 4. Výpočet veku
- Otestujte správny výpočet veku na základe roku narodenia:
  - Zadajte rôzne roky narodenia (minulosť, súčasnosť a budúcnosť).
  - Skontrolujte, či aplikácia zobrazuje upozornenia, ak rok narodenia nie je v správnom formáte.

### 5. Výpočet BMI
- Otestujte správny výpočet BMI na základe výšky a váhy.
- Skontrolujte, čo sa stane, ak jeden parameter vynecháte.
- Otestujte zadanie údajov v rôznych jednotkách (napr. kg/g, cm/m).
- Vyskúšajte zadať extrémne hodnoty.
- Overte, či aplikácia poskytuje jasné chybové hlásenia pri nesprávnych údajoch.

### 6. Údaje o anamnéze
- Overte, či môžete zadať anamnézu predošlých chorôb a pretrvávajúcich ťažkostí.
- Testujte operácie insert, update a delete.
- Overte, či je možné vybrať viac možností, všetky alebo jednu z ponuky chorôb a ťažkostí.
- Overte chybové hlásenia pri nesprávnych údajoch.

### 7. Zoznam pravidelne užívaných liekov
- Skontrolujte, či ide o zoznam a či môžete lieky pridávať alebo odoberať.
- Overte chybové hlásenia pri nesprávnych údajoch.

### 8. Prehľad očkovania
- Otestujte, či sú v prehľade uvedené očkovania proti tetanu, žltačke a chrípke.
- Môžete pridať alebo meniť existujúce očkovania.
- Kontrolujte správnosť dátumov očkovaní.
- Overte chybové hlásenia pri nesprávnych údajoch.

### 9. Zľavy na okuliare
- Otestujte zľavy pre pacientov od 30 rokov (20%), 50 rokov (30%) a 70 rokov (50%).
- Otestujte hraničné a extrémne hodnoty.
- Skontrolujte, či sú zľavy správne priradené vzhľadom k veku.

### 10. Očkovanie proti chrípke
- Overte, či muži vo veku 25-50 rokov a ženy vo veku 25-60 rokov môžu získať prvé očkovanie proti chrípke zdarma.
- Otestujte rôzne vekové kategórie pre mužov a ženy a či je spomínaná zľava správne priradená.

### 11. Formulár na recept
- Overte, či formulár obsahuje všetky povinné údaje ako meno, priezvisko, dátum narodenia a poisťovňu.
- Môžete lieky pridávať manuálne alebo zo zoznamu?
- Testujte operácie insert, update a delete.

### 12. Uloženie a načítanie karty
- Otestujte možnosť uložiť kartu pacienta a následne ju načítať späť do programu.
- Skontrolujte, či načítanie hodnôt je správne a či sa zobrazia všetky hodnoty.

### 13. Export do textového súboru
- Skontrolujte, či export funguje a aké údaje obsahuje:
  - Obsahuje textový súbor všetky povinné údaje a formát údajov je správny.
  - Skontrolujte, či po opätovnom načítaní ostali hodnoty nemenné a žiadna nepribudla ani neubudla.
