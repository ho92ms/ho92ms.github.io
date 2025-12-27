---
title: "Kutatas"
permalink: /hu/research/
layout: single
lang: hu
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <strong>HU Magyar</strong> | <a href="/en/research/">EN English</a>
</div>

## Kutatasi Erdeklodes

Kutatasi erdeklodesem a biztonsagi mernoki munka, az elosztott rendszerek elmelet e es az alkalmazott gepi tanulas metsespontjara osszpontosit.

## Fo Kutatasi Teruletek

### 1. Biztonsagi Mernoki Munka es Threat Intelligence

#### Viselkedeselemzes-alapu Fenyegetesdetektalas
- Anomaliadetektalo rendszerek
- Honeypot architekturak
- Esemenykorrelacio

Kutatasi Kerdesek:
- Hogyan minimalizalhatjuk a hamis pozitiv aranyt?
- Melyek az optimalis elhelyezesi strategiak honeypot eroforrásokhoz?
- Felulmulhatjak-e a gepi tanulasi modellek a szabalyalapu SIEM rendszereket?

#### Automatizalt Megfelelos-ellenorzes es Hardening
- Biztonsagi szabalyzatok formalis verifikacioja
- Konfiguracio-elteres detektalas
- Hardening benchmark-ok

### 2. Elosztott Rendszerek es Halozati Protokollok

#### Hibaturo Architekturak
- Konszenzus protokollok (Paxos, Raft)
- CAP tetel kompromisszumok
- Hiba-injektalas teszteles

#### WebSocket-alapu Tunneling
- NAT atjarasi technikak
- Protokoll multiplexeles
- Kapcsolatkezeles

#### Ipari IoT es OPC UA
- Biztonsagi bovitesek
- Valos ideju korlatozasok
- Interoperabilitas

### 3. Gepi Tanulas Biztonsagi Alkalmazasokhoz

#### Adversarial Gepi Tanulas
- Robusztusság adversarial peldakkal szemben
- Modell mergezesi tamadasok
- Certifikalt vedelem

#### Anomaliadetektalas Mely Tanulassal
- Autoencode-ok outlier detektalashoz
- Rekurrens halozatok szekvencia-anomaliakhoz
- One-class SVM-ek

#### Magyarazhato AI Biztonsaghoz
- Modell interpretalhatos ag
- Feature attribucio (SHAP, LIME)
- Human-in-the-loop rendszerek

### 4. Nagy Nyelvi Modellek es Alkalmazott NLP

#### Finomhangolas Domain-specifikus Feladatokhoz
- Parameter-hatekony modszerek (LoRA, prefix tuning)
- Domain adaptacio
- Ertekelesi metrikak

#### Prompt Engineering es Optimalizalas
- Few-shot tanulas
- Chain-of-thought prompting
- Automatizalt prompt kereses

#### LLM-alapu Biztonsagi Eszkozok
- Automatizalt threat intelligence
- Log elemzes
- Malware kod generalas detektalasa

## Modszertani Alapelvek

1. Elmeleti Szigor - formalis modellezes, bizonyithato tulajdonsagok
2. Empirikus Validacio - reprodukalhato kiserletek, statisztikai teszteles
3. Operativ Megvalosithatosag - valos korlatozasok, fokozatos telepites

## Jelenlegi Fokusz

### 1. Automatizalt Biztonsagi Szabalyzat Verifikacio
- Cel: Bizonyitani, hogy egy GPO konfiguracio megfelel a STIG kovetelmenyeknek
- Megkozelites: GPO modellezes veges allapotu gepkent, model checking (SPIN, TLA+)

### 2. Elosztott Honeypot Halozatok
- Cel: Koordinalt honeypot-ok telepitese vallalati kornyezetekben
- Megkozelites: Kozpontositott log aggregacio, korrelaci os elemzes

### 3. LLM-tamogatott Threat Hunting
- Cel: LLM-ek hasznalata event log-ok termeszetes nyelvü lekerdez esehez
- Megkozelites: Finomhangolas annotalt biztonsagi adathalmazokon

## Publikaciok es Nyilt Forraskod

Kivalasztott munkak es kiserletek elerhetoek a GitHub-on.

Egyuttmukodeshez vagy beszelgetesekhez lepj kapcsolatba a neduabi@pm.me cimen.
