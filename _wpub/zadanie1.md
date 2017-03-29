---
title: "Osobná webová prezentácia na GitHub Pages"
href: "zadanie1"
menu_title: "Zadanie 1"
active: "enabled"
---
#### Zadanie:
Vytvorte webovú prezentáciu (webové sídlo) o sebe. Zamerajte sa jednak na vaše profesné záujmy (napr. projekty, ktoré riešite/riešili ste, čo vás v informatike najviac baví, fascinuje = váš developerský profil) a jednak vaše osobné záujmy, hobby.V rámci developerského profilu vytvorte sekciu Webové publikovanie, kde budete publikovať všetky tri vaše vypracované zadania z predmetu.Využite pritom technológie Git + GitHub Pages + Jekyll + Markdown. Využite potenciál statického generátora Jekyll a jeho templatovacích možností.

#### Riešenie:
Výsledkom tohto zadania je internetová stránka, na ktorej sa práve nachádzate. Pri riešení som použil technológie **Git**, **GitHub Pages**, **Jekyll** a **Markdown**. Pri dizajne stránky som použil **Bootstrap**, ktorý som následne upravil podľa svojej potreby. Pri tvorbe stránky som sa snažil vhodne použiť možnosti Jekyllu a naplniť stránku zmysluplným obsahom.

Pri použití šablóny **Bootstrap** som vychádzal z dokumentácie a preto je použitá takým spôsobom ako je odporúčané. Okrem základnej šablóny som pri dizajne stránky používal vlastný súbor **main.css**, v ktorom som upravoval šablónu pre časti, kde to bolo potrebné. Najčastejšie som pre svoje potreby musel upraviť odsadenia niektorých blokov alebo farby. Zložitejšie štruktúry som použil pri tvorbe responzívneho footeru, ktorý je neustále na spodnej časti obrazovky (aj v prípade, že obsah stránky je krátky). Pre tento účel som použil možnosť **media-query** a jednotlivé intervaly sú konzistentné so základmi Bootstrapu.

#### Podstránky:
* **Úvod** - Úvodná stránka, obsahuje uvítaciu správu, 3 najnovšie príspevky, rýchle informácie a odkazy ohľadom bakalárskeho projektu a webového publikovania.
* **O mne** - Stránka obsahuje informácie o tom odkiaľ pochádzam a aké sú moje hobby.
* **Práca** - Informácie o mojej práci a bakalárskom projekte.
* **Blog** - Zoznam článkov s krátkym náhľadom ku každému článku.
* **Webové publikovanie** - Sekcia obsahuje informácie o jednotlivých zadaniach v rámci predmetu Webové publikovanie.
* **Kontakt** - Stránka s kontaktami a užitočnými odkazmi.
* (**Informácie o filme** - Podstránka vytvorená pre každý film z kolekcie filmov obsahuje základné informácie a obsah filmu.)

#### Šablóny:
* **default** - Základná šablóna, od ktorej následne dedia všetky zvyšné šablóny. Obsahuje štruktúru HTML stránky, všetky metadáta, rovnako ako include hlavičky, horného menu a footeru.
* **page_with_header** - Šablóna pre stránku s veľkým obrázkom v hornej časti. V projekte použitá pri stránke *Úvod*.
* **basic** - Šablóna pre stránky s jednoduchou štruktúrou. Obsahuje titulok stránky pod hlavným menu. Šablónu používajú stránky *O mne*, *Blog* a *Kontakt*. Od šablóny ďalej dedia šablóny *left_menu*, *top_menu*, *post* a *movie*.
* **left_menu** - Šablóna dedí od *basic* a slúži na zobrazenie kolekcie so zoznamom prvkov v ľavej časti stránky. Po načítaní stránky je najskôr zobrazený prvý prvok kolekcie. Použítá pri stránke *Práca*.
* **top_menu** - Šablóna dedí od *basic* a slúži na zobrazenie kolekcie so zoznamom prvkov v hornej časti stránky. Po načítani stránky je najskôr zobrazený prvok kolekcie, ktorý má v premennej *active* hodnotu *first*. Použitá pri stránke *Webové publikovanie*.
* **movie** - Šablóna dedí od *basic. Je použitá pri kolekcií *movies* pre zobrazenie jednotlivých filmov.
* **post** - Šablóna dedí od *basic*. Je použitá pre zobzrazenie jednotlivých príspevkov. Pod nadpisom článku sú zobrazené informácie o článku, dátum, počet slov a odhadovaný čas čítania. Pod obsahom článku sa nachádzajú tlačidlá na rýchly presun na nasledujúci/predchádzajúci článok (ak existuje).

#### Premenné:
* **title** - Použitá pri každej stránke a príspevku.
* **year** - Použitá pri prvkoch kolekcie *movies*.
* **country** - Použitá pri prvkoch kolekcie *movies*.
* **minutes** - Použitá pri prvkoch kolekcie *movies*.
* **date** - Použitá pri príspevkoch do blogu.
* **href** - Použitá pri prvkoch kolekcií *work* a *wpub*. Používa sa pri preklikoch k jednotlivým prvkom.
* **menu_title** - Použitá pri prvkoch kolekcie *wpub*, označuje ako má byť prvok označený v zozname prvkov.
* **active** - Použitá pri prvkoch kolekcie *wpub*. Ak má hodnotu *disabled*, preklik na prvok nie je umožnený, ak má hodnotu *first*, zobrazí sa prvok ako prvý.
* **collection** - Použitá pri stránkach *Webové publikovanie* a *Práca*. Slúži na informáciu pre šablónu, z ktorej kolekcie má zobrazovať prvky. Šablóny následne vyhľadá potrebnú kolekciu a zobrazí dané prvky.
* **message** - Použitá na úvodnej stránke. Slúži na informáciu pre šablónu, akú správu na zobraziť pod nadpisom.
* **header_image** - Použitá na úvodnej stránke. Slúži na informáciu pre šablónu, aký obrázok má byť zobrazený pod horným menu.
* **image_folder** - Cesta k priečinku obsahujúcemu obrázky. Pre prípad, že by bolo nutné túto cestu zmeniť. Používa sa pri všetkých cestách k obrázkom.
* **css_folder** - Cesta k priečinku obsahujúcemu CSS súbory. Pre prípad, že by bolo nutné túto cestu zmeniť. Používa sa v include *head*.
* **js_folder** - Cesta k priečinku obsahujúcemu JavaScript súbory. Pre prípad, že by bolo nutné túto cestu zmeniť. Používa sa v include *head*.
* **name** - Názov stránky. Používa sa napríklad v hornom menu alebo v titulku stránky, ktorý je vytvorený z názvu stránku a titulku aktuálnej podstránky.

#### Kolekcie a dátové súbory:
* **contacts** - Dátový súbor obsahuje zoznam mojich kontaktov. Každý sa skladá z označenia typu kontaktu a daného kontaktu. Použitý pri stránke **Kontakt**.
* **pages** - Dátový súbor obsahuje zoznam podstránok s odkazmi na ne. Je použitý pri hornom menu aj v menu vo footeri.
* **quotes** - Dátový súbor obsahuje citáty a ich autorov. Pre každú podstránku je vo footeri vybratý a zobrazený náhodný prvok tohto zoznamu.
* **work** - Kolekcia obsahuje informácie o mojej práci a je zobrazená na stránke *Práca*.
* **wpub** - Kolekcia obsahuje informácie o zadaniach z predmetu Webové publikovanie a je zobrazená na stránke *Webové publikovanie*.
* **movies** - Kolekcia obsahuje informácie o mojich obľúbených filmoch. Je zobrazená na stránke *O mne* s možnosťou prekliku na detailné informácie o každom filme.

#### Filtre a tagy:
* **foreach** - Tag je použitý na veľkom počte miest, napríklad pri generovaní menu alebo pri vytváraní elementov z akéhokoľvek zoznamu. Okrem samotnej konštrukcie *for* som využil aj možnosť *limit* pri zobrazení 3 článkov na úvodnej stránke a možnosť *offset* v šablóne *left_menu* pre výber všetkých prvkov okrem prvého, ktorý bol vybraný pred samotnou iteráciou z dävodu jeho aktivovania.
* **assign** - Tag slúži na priradenie určitej hodnoty do premennej. Použitý je napríklad pri šablónach *top_menu* a *left_menu*, alebo pri výbere náhodného citátu pre *footer*.
* **include** - Tag slúži na vloženie menšej časti kódu do súboru. Pracuje so súbormi v priečinku *_include* a použitý je v šablóne *default* pri vkladaní *head*, *navbar* a *footer*.
* **if** - Tag som použil opäť na viacerých miestach, najzložitejšia konštrukcia je použitá zrejme v šablóne *top_menu* kde sa
* **sample** - Filter som použil pri výbere náhodného citátu v časti *footer*.
* **date_to_string** - Filter som použil pri zobrazení dátumu článku na stránke *Blog* aj na stránke samotného článku v šablóne *post*.
* **number_of_words** - Filter som použil pri zobrazení počtu slov článku na stránke *Blog* aj na stránke samotného článku v šablóne *post*.
* **reading_time** - Filter je vytvorený pluginom *reading_time* a je použitý pri zobrazení odhadovaného času čítania článku v šablóne *post*.
* **truncate** - Filter je použitý pri náhľade posledných článkov na stránke *Úvodná stránka* a pri náhľade článkov na stránke *Blog*.

#### Pluginy (obidva sú funkčné len na lokálnej verzií):
* **sitemap** - Plugin slúži na vygenerovanie mapy stránky. Odkaz na výsledný súbor sa nachádza vo footeri. [Zdroj](https://github.com/kinnetica/jekyll-plugins "Zdroj")
* **reading_time** - Plugin slúži na vypočítanie odhadovaného času potrebného na prečítanie článku. Vytvára filter *reading_time*, ktorý je použitý na stránke pre jednotlivé články. [Zdroj](https://github.com/bdesham/reading_time "Zdroj")

#### Odkazy:
* [GitHub Pages](https://xgabrst.github.io/ "GitHub Pages")
* [GitHub Repository](https://github.com/xgabrst/xgabrst.github.io "GitHub Repository")