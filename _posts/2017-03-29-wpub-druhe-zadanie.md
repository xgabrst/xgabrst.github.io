---
layout: post
title: "WPUB - 2. zadanie"
date: 2017-03-29
---
#### Riešenie:
Výsledok tohto zadania je môj bakalársky projekt transformovaný do formátu DocBook. Pri riešení som použil rôzne konštrukcie, ktoré sú popísané nižšie.

#### Členenie textu:
Text je členený na 4 kapitoly, 13 podkapitol, 15 podpodkapitol a 1 prílohu. Na členenie som použil konštrukcie **chapter**, **section**, **para** a **appendix**.

#### Zvýraznenie slov a členenia:
Na zvýraznenie slov som na rôznych miestach dokumentu použil element **emphasis**, najmä pri uvádzaní príkladov (napr. strana 15). Na zvýraznenie členenia textu odrážkami som použil **itemizedlist** s atribútom **mark=opencircle**, ktorý obsahoval jednotlivé elementy **listitem** (napr. strana 13).

#### Odkazy:
Odkazy na iné časti sa v mojom dokumente na rôznych miestach. Jednotlivým častiam som pridal atribút **id**, na ktorého hodnotu sa následne odvolávam na požadovanom mieste prostredníctvom **xref** s atribútom **linkend**. Odkaz na URL som použil v rámci poznámky pod čiarou na strane 21. Použil som element **ulink** s **citetitle** a atribútom **url**.

#### Poznámka pod čiarou:
Poznámka pod čiarou sa nachádza na strane 21. Použil som konštrukciu **footnote**.

#### Zoznam literatúry a citácia:
Na vygenerovanie zoznamu použitej literatúry som použil element **bibliography**, ktorý obsahuje jednotlivé elementy **bibliomixed**. Každý element bibliomixed obsahuje atribút **id**, ktorý je použitý pri odkazovaní na daný záznam, **abbrev**, ktorý je zobrazený v rámci textu, **bibliomisc** a **title**. Z týchto častí je následne vygenerovaný výsledný záznam. Pri odkazovaní na zdroje v texte som použil **xref**, ktorého atribút **linkend** obsahoval id daného záznamu.

#### Zoznamy obrázkov, tabuliek a ich použitie v texte:
Zoznam obrázkov sa nachádza na strane 6 a zoznam tabuliek na strane 7. Na vloženie obrázka som použil element **figure**, ktorý sa skladá z elementov **title** a **mediaobject**. V rámci imageobject sú definované informácie o obrázku v časti **imagedata**, prostredníctvom atribútov **fileref** (cesta k obrázku), **format** (formát obrázku) a **width** (šírka obrázku). Pri vytváraní tabuľky som použil **table**, ktorý obsahuje **title** a **tbgroup**. Pri definovaní obsahu tabuľky som použil elementy **thead**, **tbody**, **row**, **entry** a atribúty **cols**, **colwidth** a **align**.

#### Register pojmov:
Na vygenerovanie registra pojmov som použil *index**, ktorého obsah vznikne na základe použitých elementov **indexterm** v texte. Pri indexterm som použil pri definovaní štruktúry všetky tri úrovne, teda **primary**, **secondary** aj **tertiary**.

#### Úpravy XSL:
*Čísla riadkov spomenuté v tejto časti sa odkazujú na súbor thesis.xsl, ktorý bol odovzdaný v rámci úlohy. Tieto zmeny som väčšinou vykonával s cieľom priblížiť sa pôvodnému dokumentu.*

* Pridal som časť, v ktorej som nadefinoval, ako sa majú zobrazovať odkazy na iné časti dokumentu. Mojím cieľom bolo, aby sa zobrazovalo len číslo danej časti. (riadky 68-93)
* Zmenil som odsadenie odstavcov, podľa vzoru pôvodného dokumentu. (97, 101, 102, 103)
* Zmenil som hodnotu bibliography.numbered, aby zoznam literatúry nebol číslovaný (175).
* Do časti generate.toc som pre book pridal aj figure a table, aby sa do dokumentu vygenerovali zoznamy obrázkov a tabuliek. (202)
* Pridal som možnosti na zlomenie strany a riadky, ktoré som následne mohol použiť v dokumente ako **?linebreak?** a **?hard-pagebreak?**. (206-213)
* Zväčšil som odsadenie zoznamov od ľavého okraja strany. (215-223)
* Zmenšil som veľkosť medzier medzi prvkami zoznamu. (225-230)

#### Odkazy:
* [GitHub Pages](http://localhost:4000/webovepublikovanie/ "GitHub Pages")
