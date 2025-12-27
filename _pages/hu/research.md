---
title: "Kutatás"
permalink: /hu/research/
layout: single
lang: hu
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <strong>HU Magyar</strong> | <a href="/en/research/">EN English</a>
</div>

## Kutatási Érdeklődés

Kutatási érdeklődésem a biztonsági mérnöki munka, az elosztott rendszerek elmélete és az alkalmazott gépi tanulás metszéspontjára összpontosít.

## Fő Kutatási Területek

### 1. Biztonsági Mérnöki Munka és Threat Intelligence

#### Viselkedéselemzés-alapú Fenyegetésdetektálás
- Anomáliadetektáló rendszerek
- Honeypot architektúrák
- Eseménykorreláció

Kutatási Kérdések:
- Hogyan minimalizálhatjuk a hamis pozitív arányt?
- Melyek az optimális elhelyezési stratégiák honeypot erőforrásokhoz?
- Felülmúlhatják-e a gépi tanulási modellek a szabályalapú SIEM rendszereket?

#### Automatizált Megfelelőség-ellenőrzés és Hardening
- Biztonsági szabályzatok formális verifikációja
- Konfiguráció-eltérés detektálás
- Hardening benchmark-ok

### 2. Elosztott Rendszerek és Hálózati Protokollok

#### Hibatűrő Architektúrák
- Konszenzus protokollok (Paxos, Raft)
- CAP tétel kompromisszumok
- Hiba-injektálás tesztelés

#### WebSocket-alapú Tunneling
- NAT átjárási technikák
- Protokoll multiplexelés
- Kapcsolatkezelés

#### Ipari IoT és OPC UA
- Biztonsági bővítések
- Valós idejű korlátozások
- Interoperabilitás

### 3. Gépi Tanulás Biztonsági Alkalmazásokhoz

#### Adversarial Gépi Tanulás
- Robusztusság adversarial példákkal szemben
- Modell mérgezési támadások
- Certifikált védelem

#### Anomáliadetektálás Mély Tanulással
- Autoencode-ok outlier detektáláshoz
- Rekurrens hálózatok szekvencia-anomáliákhoz
- One-class SVM-ek

#### Magyarázható AI Biztonsághoz
- Modell interpretálhatóság
- Feature attribúció (SHAP, LIME)
- Human-in-the-loop rendszerek

### 4. Nagy Nyelvi Modellek és Alkalmazott NLP

#### Finomhangolás Domain-specifikus Feladatokhoz
- Paraméter-hatékony módszerek (LoRA, prefix tuning)
- Domain adaptáció
- Értékelési metrikák

#### Prompt Engineering és Optimalizálás
- Few-shot tanulás
- Chain-of-thought prompting
- Automatizált prompt keresés

#### LLM-alapú Biztonsági Eszközök
- Automatizált threat intelligence
- Log elemzés
- Malware kód generálás detektálása

## Módszertani Alapelvek

1. Elméleti Szigor - formális modellezés, bizonyítható tulajdonságok
2. Empirikus Validáció - reprodukálható kísérletek, statisztikai tesztelés
3. Operatív Megvalósíthatóság - valós korlátozások, fokozatos telepítés

## Jelenlegi Fókusz

### 1. Automatizált Biztonsági Szabályzat Verifikáció
- Cél: Bizonyítani, hogy egy GPO konfiguráció megfelel a STIG követelményeknek
- Megközelítés: GPO modellezés véges állapotú gépként, model checking (SPIN, TLA+)

### 2. Elosztott Honeypot Hálózatok
- Cél: Koordinált honeypot-ok telepítése vállalati környezetekben
- Megközelítés: Központosított log aggregáció, korrelációs elemzés

### 3. LLM-támogatott Threat Hunting
- Cél: LLM-ek használata event log-ok természetes nyelvű lekérdezéséhez
- Megközelítés: Finomhangolás annotált biztonsági adathalmazokon

## Publikációk és Nyílt Forráskód

Kiválasztott munkák és kísérletek elérhetőek a GitHub-on.

Együttműködéshez vagy beszélgetésekhez lépj kapcsolatba a neduabi@pm.me címen.
