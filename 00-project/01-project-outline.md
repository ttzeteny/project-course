---
name: Tolnai-Tóth Zétény
neptun: YV4RVH
id: 2026-OG-03
github: https://github.com/ttzeteny/project-course
trello: https://trello.com/b/6QKAU0JP/project-course-drone-swarm
---
# Drónrajok optimális útvonaltervezésének és formációváltásának vizsgálata

A projekt több drónból álló raj formációváltásának 3D-s szimulációja és optimalizálása. A központi kérdés az, hogy egy kezdeti és egy célalakzat között hogyan rendelhetők hozzá az egyes drónok a célpozíciókhoz, és hogyan tervezhetők meg az útvonalaik úgy, hogy a repülési idő és a megtett összes távolság kedvező legyen, a drónok mozgási korlátai (végsebesség, gyorsulás) teljesüljenek, és a drónok ne ütközzenek egymással. A megoldás verziókezelt webalkalmazás: a backend (Python vagy Java) végzi a célpozíciók kiosztását, a mozgásmodell futtatását és az ütközéselkerülést, a React + TypeScript + Three.js kliens pedig 3D-ben megjeleníti a drónok mozgását. A projekt végére a felhasználó megadhat drónszámot, kezdő- és célformációt és repülési paramétereket, majd megtekintheti a megtervezett átmenetet, és összehasonlíthatja a különböző stratégiák mért eredményeit.

## Célok

- **Elsődleges cél:** Működő, verziókezelt 3D szimulációs alkalmazás elkészítése, amely drónrajok formációváltását megtervezi, szimulálja és vizuálisan megjeleníti, valamint legalább két optimalizálási stratégiát összehasonlít.
- **Célfelhasználók / érintettek:** Drónos fényshow-k tervezése és rajrobotika iránt érdeklődő szakemberek, hallgatók és oktatók, akik a formációváltási stratégiákat kísérletezéssel szeretnék megismerni; a témavezető és az értékelők.
- **Mérhető sikerkritériumok:**
  - A felhasználó megadhat kezdő- és célformációt, drónszámot és repülési paramétereket, a rendszer pedig megtervezi és lejátssza az átmenetet.
  - Legalább két hozzárendelési vagy útvonaltervezési stratégia működik, és összehasonlításuk a számítási költség, a repülési idő, a megtett távolság és a skálázhatóság alapján dokumentált (több drónszámmal mérve, pl. 10, 50, 100, 500 drón).
  - A szimuláció minden futásban méri a teljes formációváltási időt és a drónok által megtett összes távolságot.
  - A drónok mozgása betartja a beállított végsebességet és gyorsulást.
  - A drónok közötti minimális távolság a mért futásokban nem csökken a beállított biztonsági távolság alá.
  - A szimulációs és optimalizálási logika a megjelenítés nélkül is futtatható, a fontosabb algoritmusokhoz pedig automatizált tesztek készülnek.
- **Korlátok:** A szimulációs és optimalizálási logika architektúrálisan elkülönül a megjelenítéstől (kliens–szerver felépítés); backend Python vagy Java, kliens React + TypeScript + Three.js; a kommunikáció REST API-n vagy WebSocketen keresztül történik; a forráskód GitHubon van; titkos kulcsok, hozzáférési tokenek nem kerülhetnek a repóba.

## Hatókör

### Benne van a hatókörben

- Tetszőleges számú drón és 3D célpozíció kezelése.
- Kezdő- és célformáció megadása (előre definiált alakzatok és egyedi pozíciólista).
- Konfigurálható mozgási paraméterek: végsebesség, gyorsulás és egyéb releváns korlátok.
- A drónok mozgásmodelljének, a célpozíciók kiosztásának és az ütközéselkerülés működésének meghatározása és megvalósítása.
- Legalább két különböző hozzárendelési vagy útvonaltervezési stratégia.
- Drónok közötti ütközéselkerülés a mozgás során.
- A teljes formációváltási idő és a megtett összes távolság mérése, a stratégiák számítási költségének mérése.
- A megtervezett átmenet 3D-s megjelenítése és lejátszása a böngészőben.
- A stratégiák összehasonlítása és az eredmények dokumentálása.
- Automatizált tesztek a fontosabb algoritmusokhoz.

### Nincs benne a hatókörben

- Dinamikus formációváltás futás közben.
- Akadályok megjelenése a térben.
- Különböző tulajdonságú drónok kezelése.
- Valós drónraj-adatok felhasználása és valódi drónhardver vezérlése.
- Részletes fizikai modell (szél, akkumulátor, aerodinamika).
- Felhasználói fiókok, hitelesítés és többfelhasználós funkciók.
- Hagyományos asztali alkalmazás.

## Jegyzetek

Az első verzió statikus formációváltásra összpontosít: adott kezdő- és célalakzat között tervezi meg és szimulálja az átmenetet. A hatókörön kívül eső bővítések (dinamikus formációváltás, akadályok, heterogén drónok, valós adatok) csak akkor merülhetnek fel, ha az alap szimuláció, a stratégiák összehasonlítása és a tesztek már megbízhatóan működnek. A konkrét stratégiák, a mozgásmodell, az ütközéselkerülési módszer és a backend nyelve (Python vagy Java) a specifikációban és a kezdeti technikai javaslatban kerül véglegesítésre.
