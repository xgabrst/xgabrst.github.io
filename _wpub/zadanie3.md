---
title: "XML Prezentácia"
href: "zadanie3"
menu_title: "Zadanie 3"
active: "first"
---
#### Zadanie:
Vytvorenie prezentácie v jazyku XML a návrh elementov v XML Schema. Konverzia prezentácie z XML do XHTML+CSS a do PDF.

#### Opis typu dokumentu:
Na opis typu dokumentu som použil XML Schema. V súbore schema.xsd som nadefinoval celú štruktúru prezentácie. Schéma je jednoznačná a neobsahuje redundancie. Časti prezentácie, ktoré môžu byť generované automaticky boli navrhnuté tak, aby to bolo možné a neduplikovali sa informácie v prezentácií.

Prezentácia sa skladá z metadát a slajdov, pričom slajdy môžu byť generované automaticky (úvod, obsah a zdroje) alebo môžu obsahovať nejaký obsah. Pri slajdoch s obsahom je umožnený výber jedného zo štyroch rozložení a môže sa skladať z textu, odrážok (číslovaných alebo nečíslovaných), obrázku alebo podnadpisu.

V súbore sa nachádzajú komentáre s vysvetlením jednotlivých elementov.

#### Vytvorenie ukážkovej XML prezentácie:
Vytvoril som ukážkovú prezentáciu, ktorá je zameraná na MS 2010 vo futbale. V prezentácií som použil všetky typy rozloženia aj obsahu. XML súbor je validný voči definovanej schéme.

#### Parametrizácia transformácií:
Vytvoril som súbor, v ktorom je umožnené nastaviť niekoľko parametrov.

Nastavenie veľkosti prezentácie je možné dvomi spôsobmi. Prvým z nich je zvolenie niektorej z definovaných možností (small, medium, big). Druhým spôsobom je nastavenie vlastnej výšky a širky v pixeloch. Vyššiu prioritu má nastavenie vlastných hodnôt. V prípade, že nie je nastavený ani jeden z parametrov, použije sa hodnota medium.

Ďalšou možnosťou parametrizácie je nastavenie farieb. Predvolenou hodnotou je čisto biela prezentácia s čiernym textom. Ponúkané sú však 4 farebné témy (red, blue, black, white). Vyššiu prioritu ako predvolené témy má možnosť, pri ktorej používateľ nastaví vlastnú farbu v hexadecimálnom kóde alebo slovne po anglicky. Okrem nastavenia vlastnej farby musí v tomto prípade nastaviť aj farbu písma. Pre použitie vlastných farieb musia byť nastavené obe hodnoty. Pri transformácií do PDF je podporované len definovanie vlastných farieb.

Používateľ má taktiež možnosť zvoliť, či na slajde so zdrojmi majú odkazy aj odkazovať na ich zdroj alebo byť zobrazené ako bežný text. Táto možnosť je podporovaná len v HTML verzií.

Poslednou možnosťou parametrizácie je možnosť nastaviť, či majú byť vložené čísla slajdov. Pri HTML verzií sa tieto čísla zobrazujú nad slajdom spolu s tlačidlami pre presun na predchádzajúci alebo nasledujúci slajd. Pri PDF sa tieto čísla zobrazujú v spodnej časti slajdu,

#### Konverzia do HTML+CSS:
Pri konverzií do HTML som vytvoril pre každý slajd samostatný súbor. Medzi súbormi je možné sa preklikávať. Pre definovanie vzhľadu som vytvoril CSS súbor, na ktorý sa odkazujú jednotlivé HTML stránky.

#### Konverzia do PDF:
Pri konverzií do PDF som na základe slajdov vytvoril jednotlivé stránky PDF súboru. Všetky podporované rozloženia slajdov a obsahu sa zobrazujú správne. Navrhnuté parametrizovanie funguje všade tam, kde bolo navrhnuté. Rozloženia s viacerými stĺpcami sú vytvorené pomocou tabuľky.