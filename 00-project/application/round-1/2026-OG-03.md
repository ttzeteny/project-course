---
name: Tolnai-Tóth Zétény
neptun: YV4RVH
id: 2026-OG-03
---
# Drónrajok optimális útvonaltervezésének és formációváltásának vizsgálata

## A brief értelmezése

A projekt célja egy 3D szimulációs alkalmazás elkészítése, amely több drónból álló raj formációváltását modellezi és optimalizálja. A fő kihívás annak meghatározása, hogy a drónok hogyan rendelhetők hozzá a célpozíciókhoz a legoptimálisabban egy kezdeti és egy célalakzat között. A rendszernek figyelembe kell vennie a repülési időt, az útvonal hosszát, a mozgási korlátokat (pl. gyorsulás, végsebesség), és kezelnie kell az ütközéselkerülést. Kulcsfontosságú elvárás, hogy a szimulációs és optimalizálási logika architektúrálisan különüljön el a megjelenítéstől.

## Miért én lennék alkalmas erre a projektre?

A budapesti augusztus 20-i tűzijátékokat kísérő drónos vizuális show-k mindig is lenyűgöztek, és régóta érdekelt, hogy algoritmikusan hogyan lehet ennyire precízen összehangolni ilyen sok eszköz mozgását a térben. Ez a projekt tökéletes lehetőség arra, hogy a felszín alá lássak, és magam is implementáljam a mögöttes logikát. Az ehhez szükséges algoritmikus gondolkodás, a matematikai optimalizáció és a 3D-s vizualizáció mind olyan területek, amelyek motiválnak és amelyekben már szereztem előzetes tapasztalatokat.

## Releváns tapasztalat és előzmények

Saját projektjeim során már dolgoztam a 3D térértelmezés és renderelés alapjaival (pl. Javában írt 3D szoftveres renderelő készítésekor). A gépi tanulási és adatfeldolgozási feladataim (pl. hitelkockázat-becslő alkalmazás, számjegy felismerő) során megszoktam az összetett számítási és optimalizációs problémák kezelését. Ezen felül stabil alappal rendelkezem a modern webes technológiák (React, TypeScript) és a backend fejlesztés (Spring Boot, Python FastAPI) terén, ami elengedhetetlen a szimuláció és a megjelenítés szétválasztásához.
Ezek a projektek megtalálhatók GitHubon:
- Java 3D renderer: https://github.com/ttzeteny/java-software-renderer
- Credit risk predictor: https://github.com/ttzeteny/credit-risk-predictor
- Kézzel rajzolt számjegy felismerő: https://github.com/ttzeteny/digit-vision
- Full-stack web application: https://github.com/ttzeteny/gridbase

## Tervezett megközelítés

A projekt megvalósításához egy elosztott webes architektúrát építenék fel egy hagyományos asztali szoftver helyett. Ez a megközelítés több szempontból is előnyös: egyrészt a kliens-szerver modell természetes és szigorú módon kikényszeríti a szimulációs logika és a vizuális megjelenítés projektkiírásban elvárt elkülönítését. Másrészt a webes platform telepítés nélkül, azonnal bemutathatóvá teszi az eredményt. Harmadrészt a korábbi full-stack projektjeimből adódóan stabil alappal rendelkezem ebben a stackben, így az időmet a lényegre: az optimalizációs algoritmusokra és a 3D-s renderelésre tudom fókuszálni. A backend (Python vagy Java) felelne a számításokért: a célpozíciók kiosztásáért, a mozgásmodell futtatásáért és az ütközéselkerülésért. A kliensoldalt TypeScript és React felhasználásával készíteném el, a drónok és a célpozíciók 3D vizuális megjelenítését pedig Three.js-el (vagy hasonló WebGL alapú technológiával) oldanám meg. A kliens és a szerver REST API-n vagy WebSocketen kommunikálna egymással.

## Kezdeti terv

1. A specifikáció és a technikai architektúra pontos kidolgozása.
2. A backend optimalizációs és szimulációs magjának lefejlesztése, valamint az algoritmusok automatizált tesztelése.
3. A React + Three.js alapú 3D vizualizációs kliens elkészítése.
4. A backend API és a frontend integrációja, a formációváltások vizuális tesztelése.
5. Különböző optimalizálási stratégiák összehasonlítása és az eredmények mérése (számítási költség, megtett távolság stb. alapján).

## További információ

A projektet a kezdetektől fogva Git-alapú repozitóriumban vezetem, issue-k és Trello board segítségével követve a feladatokat. Titkos kulcsokat, hozzáférési tokeneket természetesen nem kommitolok a repóba. A fontosabb optimalizálási algoritmusokhoz automatizált teszteket fogok írni, ahogy azt a projektkiírás megköveteli.