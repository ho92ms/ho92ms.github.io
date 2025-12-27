---
title: "Kutatás"
permalink: /hu/research/
layout: single
lang: hu
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <strong>🇭🇺 Magyar</strong> | <a href="/en/research/">🇬🇧 English</a>
</div>

## Kutatási Érdeklődés

Kutatási érdeklődésem a **védekező biztonsági mérnöki munka**, az **elosztott rendszerek elmélete** és az **alkalmazott gépi tanulás** metszéspontjára összpontosít, olyan módszerekre fókuszálva, amelyek **elméletileg megalapozottak** és **operatívan telepíthetők**.

---

## Fő Kutatási Területek

### 1. Biztonsági Mérnöki Munka és Threat Intelligence

#### Viselkedéselemzés-alapú Fenyegetésdetektálás
- **Anomáliadetektáló rendszerek** — statisztikai modellek baseline viselkedéstől való eltérések azonosítására
- **Honeypot architektúrák** — megtévesztési technikák korai stádiumú támadások azonosítására
- **Eseménykorreláció** — Windows Event Log-ok időbeli elemzése haladó perzisztens fenyegetésekhez (APT)

**Kutatási Kérdések:**
- Hogyan minimalizálhatjuk a **hamis pozitív arányt** magas **detektálási lefedettség** fenntartása mellett?
- Melyek az **optimális elhelyezési stratégiák** honeypot erőforrásokhoz vállalati hálózatokban?
- Felülmúlhatják-e a **gépi tanulási modellek** a szabályalapú SIEM rendszereket zero-day detektálásban?

#### Automatizált Megfelelőség-ellenőrzés és Hardening
- **Biztonsági szabályzatok formális verifikációja** — model checking GPO helyesség bizonyítására
- **Konfiguráció-eltérés detektálás** — folyamatos monitoring jogosulatlan változásokhoz
- **Hardening benchmark-ok** — STIG, CIS és gyártói baseline-ok összehasonlító elemzése

**Kutatási Kérdések:**
- Hogyan **formálisan verifikálhatjuk**, hogy egy GPO konfiguráció megfelel a STIG követelményeknek?
- Mi a hardening **mérhető hatása** a támadási felület csökkentésére?
- **Automatizálhatjuk** a compliance keretrendszerek és GPO beállítások közötti leképezést?

---

### 2. Elosztott Rendszerek és Hálózati Protokollok

#### Hibatűrő Architektúrák
- **Konszenzus protokollok** — Paxos, Raft és bizánci hibatűrés
- **CAP tétel kompromisszumok** — konzisztencia vs. elérhetőség elosztott adatbázisokban
- **Hiba-injektálás tesztelés** — chaos engineering reziliencia validációhoz

**Kutatási Kérdések:**
- Hogyan tervezhetünk **alacsony késleltetésű konszenzust** ipari vezérlőrendszerekhez?
- Melyek a **minimális feltételezések** bizánci hibatűréshez IoT hálózatokban?
- **Kvantifikálhatjuk** a konzisztencia és partíció-tűrés közötti kompromisszumot?

#### WebSocket-alapú Tunneling
- **NAT átjárási technikák** — reverse tunnel-ek, STUN/TURN protokollok
- **Protokoll multiplexelés** — kétirányú kommunikáció egyetlen kapcsolaton keresztül
- **Kapcsolatkezelés** — lekapcsolódások, újrapróbálkozások és állapot-egyeztetés kezelése

**Kutatási Kérdések:**
- Mi a WebSocket tunneling **késleltetési többlete** közvetlen TCP-hez képest?
- Hogyan **optimalizálhatjuk a buffer méreteket** nagy áteresztőképességű ipari protokollokhoz (OPC UA)?
- **Bizonyíthatjuk** a relay szerver helyességét konkurens kérések esetén?

#### Ipari IoT és OPC UA
- **Biztonsági bővítések** — autentikáció, titkosítás, tanúsítvány-kezelés
- **Valós idejű korlátozások** — determinisztikus kommunikáció korlátozott késleltetéssel
- **Interoperabilitás** — legacy protokollok áthidalása modern szabványokkal

**Kutatási Kérdések:**
- Hogyan **védjük az OPC UA-t** man-in-the-middle támadások ellen megbízhatatlan hálózatokban?
- Melyek az OPC UA **teljesítményjellemzői** WebSocket vs. TCP esetén?
- **Formálisan modellezhetjük** az OPC UA protokoll stacket verifikációhoz?

---

### 3. Gépi Tanulás Biztonsági Alkalmazásokhoz

#### Adversarial Gépi Tanulás
- **Robusztusság adversarial példákkal szemben** — perturbációk, amelyek becsapják az osztályozókat
- **Modell mérgezési támadások** — betanítási adatok korruptálása a teljesítmény romlásához
- **Certifikált védelem** — bizonyítható garanciák korlátozott perturbációkkal szemben

**Kutatási Kérdések:**
- Hogyan **certifikálhatjuk**, hogy egy malware osztályozó robusztus adversarial példákkal szemben?
- Mi a **kompromisszum** az adversarial robusztusság és a benign pontosság között?
- **Detektálhatjuk** a mérgezési támadásokat betanítás közben?

#### Anomáliadetektálás Mély Tanulással
- **Autoencode-ok outlier detektáláshoz** — felügyelet nélküli tanulás normál viselkedésről
- **Rekurrens hálózatok szekvencia-anomáliákhoz** — időbeli minták event log-okban
- **One-class SVM-ek** — csak benign mintákon betanított osztályozók

**Kutatási Kérdések:**
- Hogyan **hangolhatjuk** az autoencoder rekonstrukciós küszöbét a hamis pozitívok minimalizálásához?
- **Felülmúlhatják** az LSTM-ek a statisztikai baseline-okat ransomware viselkedés detektálásában?
- Mi a **címkehatékonyság** a félfelügyelt anomáliadetektálásban?

#### Magyarázható AI Biztonsághoz
- **Modell interpretálhatóság** — megértés, miért jelölt meg egy modellt egy eseményt rosszindulatúként
- **Feature attribúció** — SHAP, LIME és gradiens-alapú magyarázatok
- **Human-in-the-loop rendszerek** — elemzői visszajelzés integrálása modellekbe

**Kutatási Kérdések:**
- **Megbízhatunk** a modell magyarázatokban nagy tétű biztonsági döntéseknél?
- Hogyan **kvantifikálhatjuk** különböző modellarchitektúrák interpretálhatóságát?
- Mi a **hatása** az emberi visszajelzésnek a modell pontosságára idővel?

---

### 4. Nagy Nyelvi Modellek (LLM-ek) és Alkalmazott NLP

#### Finomhangolás Domain-specifikus Feladatokhoz
- **Paraméter-hatékony módszerek** — LoRA, prefix tuning, adapter rétegek
- **Domain adaptáció** — transfer learning általános corpusokról specializáltakra
- **Értékelési metrikák** — perplexitás, BLEU, emberi értékelés

**Kutatási Kérdések:**
- Hány **domain-specifikus példa** szükséges hatékony finomhangoláshoz?
- Mi a **kompromisszum** a paraméterhatékonyság és a feladat teljesítmény között?
- **Kvantifikálhatjuk** az előbetanítási adat minőségének hatását downstream feladatokra?

#### Prompt Engineering és Optimalizálás
- **Few-shot tanulás** — hatékony prompt-ok tervezése minimális példákkal
- **Chain-of-thought prompting** — érvelési lépések kinyerése LLM-ekből
- **Automatizált prompt keresés** — gradiens-alapú optimalizálás diszkrét prompt-okhoz

**Kutatási Kérdések:**
- Melyek az **elméleti határai** a few-shot tanulásnak LLM-ekkel?
- **Automatizálhatjuk** az optimális prompt-ok felfedezését?
- Hogyan **biztosíthatjuk**, hogy az LLM-ek tényszerűen helyes kimeneteket produkálnak?

#### LLM-alapú Biztonsági Eszközök
- **Automatizált threat intelligence** — kompromittálás indikátorok (IOC-k) kinyerése jelentésekből
- **Log elemzés** — természetes nyelvi lekérdezések strukturált eseményadatokon
- **Malware kód generálás detektálása** — AI-generált exploitok azonosítása

**Kutatási Kérdések:**
- **Pontosan** kinyerhetik az LLM-ek az IOC-kat strukturálatlan threat jelentésekből?
- Mi a **hamis pozitív arány** LLM-alapú log elemzésnél?
- Hogyan **detektálhatjuk**, amikor LLM-eket rosszindulatú kód generálásra használnak?

---

## Módszertani Alapelvek

Olyan megközelítéseket hangsúlyozok, amelyek prioritást adnak:

### 1. Elméleti Szigor
- **Formális modellezés** — matematikai keretrendszerek használata (automaták, Petri hálók, temporális logika)
- **Bizonyítható tulajdonságok** — helyesség, élőség, biztonság garanciák
- **Komplexitás elemzés** — idő/tér korlátok, skálázhatósági határok

### 2. Empirikus Validáció
- **Reprodukálható kísérletek** — verziókezelt kód, dokumentált eljárások, nyilvános adathalmazok
- **Statisztikai tesztelés** — hipotézis tesztelés, konfidencia intervallumok, power analízis
- **Ablációs tanulmányok** — egyedi komponensek hatásának izolálása

### 3. Operatív Megvalósíthatóság
- **Valós korlátozások** — telepítési költségek, visszafelé kompatibilitás, emberi tényezők
- **Fokozatos telepítés** — A/B tesztelés, canary release-ek, rollback stratégiák
- **Költség-haszon elemzés** — biztonság és használhatóság közötti kompromisszum kvantifikálása

---

## Jelenlegi Fókusz

Jelenlegi munkám a következőket vizsgálja:

### 1. Automatizált Biztonsági Szabályzat Verifikáció
- **Cél:** Bizonyítani, hogy egy GPO konfiguráció megfelel a STIG követelményeknek
- **Megközelítés:** GPO modellezése véges állapotú gépként, model checking használata (SPIN, TLA+)
- **Hatás:** Manuális audit teher eliminálása, compliance biztosítása konstrukcióból

### 2. Elosztott Honeypot Hálózatok
- **Cél:** Koordinált honeypot-ok telepítése vállalati környezetekben
- **Megközelítés:** Központosított log aggregáció, korrelációs elemzés, automatizált válasz
- **Hatás:** Oldalirányú mozgás korai detektálása, csökkentett támadói tartózkodási idő

### 3. LLM-támogatott Threat Hunting
- **Cél:** LLM-ek használata event log-ok természetes nyelvű lekérdezéséhez
- **Megközelítés:** Finomhangolás annotált biztonsági adathalmazokon, SIEM integráció
- **Hatás:** Alacsonyabb belépési küszöb threat hunter-eknek, gyorsabb hipotézis tesztelés

---

## Publikációk és Nyílt Forráskód

Kiválasztott munkák és kísérletek elérhetők a [GitHub](https://github.com/ho92ms)-on.

Együttműködéshez vagy beszélgetésekhez lépj kapcsolatba a [neduabi@pm.me](mailto:neduabi@pm.me) címen.

---

> *"Biztonság formális módszerekkel. Reziliencia elosztott tervezéssel. Intelligencia empirikus tudománnyal."*



