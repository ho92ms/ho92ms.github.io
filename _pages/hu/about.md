---
title: "Rolam"
permalink: /hu/about/
layout: single
lang: hu
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <strong>???? Magyar</strong> | <a href="/en/about/">???? English</a>
</div>

## Szakmai Profil

Biztonsagi mernok es rendszerarchitekt vagyok, mely szakertelemmel a vallalati infrastruktura vedelemeben, az elosztott rendszerekben es az alkalmazott gepi tanulasban. Munkam osszeköti a formalis biztonsagi elmeletet es a gyakorlati rendszerimplementaciot, hangsulyt fektetve:

1. **Vedekezo Biztonsagi Mernoki Munka** — fenyegetesdetektalas, hardening keretrendszerek es automatizalt megfelelos-ellenorzes
2. **Elosztott Rendszerarchitektura** — hibaturo tervezes, halozati protokollok es ipari integracio
3. **Empirikus Szigor** — adatvezerelt validacio, reprodukalhato modszertanok es merheto eredmenyek

---

## Filozofia

A rendszertervezeshez harom egymastkiegeszitooszempont bol kozelitek:

### 1. Biztonsag Elsorangu Tulajdonsagkent
A biztonsag nem utolagonost — **architekturalis invarians**. Alkalmazom:
- **Vedekezés melysegben** — retegezett kontrollok fail-safe alapertelmezesekkel
- **Legkisebb jogosultsag elve** — minimalis hozzaferesi jogok GPO-n es RBAC-en keresztul
- **Viselkedeselemzes** — anomaliadetektalas a szignaturaalapu vedekesen tul

### 2. Automatizalas Formalis Specifikacion Keresztul
A manualis folyamatok emberi hibahoz vezetnek. Hangsul yozom:
- **Deklarativ konfiguracio** — infrastructure as code (PowerShell DSC, Ansible-szeru mintak)
- **Idempotens muveletek** — biztonsagosan ujrafuttathato, kiszamithato allapotatmenetetek
- **Esemenyvezerelt architekturak** — valos ideju valasz rendszervaltozasokra

### 3. Empirikus Validacio
Az elmeleti modelleknek ki kell allniuk a valos korlatozasokat. Prioritasom:
- **Merheto metrikak** — atlagos detektalasi ido (MTTD), hamis pozitiv arany, compliance pontszamok
- **Reprodukalhato kiserletek** — verziokezett konfiguraciok, dokumentalt eljarasok
- **Post-mortem elemzes** — tanulas incidensekbol, iterativ fejlesztes

---

## Technikai Teruletek

### Biztonsagi Mernoki Munka

#### Windows Hardening es Megfelelos-ellenorzes
- **STIG** es **CIS Benchmark** alkalmazasa Group Policy-n keresztul
- **Microsoft Security Baseline-ok** telepitese Windows 10/11 es Server 2016/2019-re
- Automatizalt hardening **HardeningKitty** es egyedi PowerShell DSC scriptekkel
- **Windows Defender ASR szabalyok** konfiguralasa zero-day exploitok ellen

#### Fenyegetesdetektalas es Valaszadas
- **Honeypot rendszerek** epitese ransomware korai figyelmeztetesre
- **Viselkedeselemzo scriptek** (PowerShell-alapu EDR) gyanus tevekenysegekre
- **Wazuh SIEM** integracio egyedi szabalyokkal Windows Event Log elemzesre
- **Automatizalt incidensvalasz** RDP brute-force tamadasokra (IP blokolas, riasztas)

#### Halozati Biztonsag
- **Reverse tunnel architektura** tervezese WebSocketen keresztul ipari protokoll hozzafereshez
- **Site-to-site VPN** konfiguralás (IPSec, SSL VPN) tobbhelyszines vallalatokhoz
- **DNS-over-HTTPS (DoH)** telepites titkositott DNS feloldashoz
- **SSH tunneling** megoldasok biztonságos tavoli hozzafereshez

---

### Elosztott Rendszerek es Protokollok

#### WebSocket-alapu Relay Architektura (C# / .NET 8.0)
- **Ketiranyú tunneling** tervezese NAT atjarashoz VPN overhead nelkul
- **Konkurens kapcsolatkezeles** implementalasa `ConcurrentDictionary`-val es `TaskCompletionSource`-szal
- **OPC UA mock szerver** epitese ipari automatizalas teszteleere
- **Aszinkron I/O mintak** alkalmazasa nagy aterestoképessegu adattovabbitashoz

#### Ipari Protokollok
- **OPC UA** integracio (ipari szabvany gep-gep kommunikaciohoz)
- **Protokolladapterek** fejlesztese legacy rendszerekhez
- Interoperabilitas tesztelese **SCADA** kornyezetekkel

---

### Vallalati Infrastruktura es Automatizalas

#### Active Directory es Group Policy
- **Domain controller telepites** automatizalasa PowerShell-lel
- **GPO kezelesi keretrendszer** centralizalt policy terjeszteshez
- **SYSVOL szinkronizacios eszkozok** multi-DC kornyezetekhez
- **Felhasznalo-letrehozo scriptek** szerepalapu hozzaferes-vezerlessel (RBAC)

#### OS Telepites es PXE Boot
- **Windows Deployment Services (WDS)** + **Microsoft Deployment Toolkit (MDT)** telepites
- **PXE boot** konfiguralás (DHCP opciok 66/67, TFTP)
- **Felügyelet nelkuli telepitesek** egyedi answer fajlokkal
- **Driver injektalas** es telepites utani konfiguracio

#### Scripteles es Automatizalas
- **Modularis PowerShell konyvtar** gyakori muveletekhekhez
- **Esemenyvezerelt monitoring rendszerek** valos ideju Event Log elemzessel
- **Tuzfalszabaly automatizalas** dinamikus szolgaltatas-megnyitashoz
- **Compliance jelenteskeszites** audit keszenlethez

---

### Gepi Tanulas es Adattudomany

#### Neuralis Halozat Tervezes
- **Konvolucios** es **rekurrens** architekturak domain-specifikus feladatokhoz
- **Transfer learning** elorebetanitott modellekkel (ResNet, BERT)
- **Hiperparameter-optimalizalas** Bayes-i modszerekkel

#### Nagy Nyelvi Modellek (LLM-ek)
- **Domain-specifikus modellek** finomhangolasa LoRA es prefix tuning segitsegevel
- **Prompt engineering strategiak** feladatspecifikus teljesitmenyhez
- **LLM-alapu agensek** epitese hibakezeléssel es fallback mechanizmusokkal

#### Adatelemzes
- **Feltaro adatelemzes (EDA)** statisztikai osszefoglalokkal es vizualizaciokkal
- **Feature engineering** domain-specifikus reprezentaciokhoz
- **A/B teszteles** statisztikai validaciohoz

---

## Problemamegoldasi Megkozelites

Kulonosen erdekelnek olyan problemak, ahol az **elmeleti struktura talalakozik az operativ korlatozasokkal**:

### Biztonsag
- **Deteaktalorendszerek** tervezese, amelyek kiegyensulyozzak a **hamis pozitiv aranyt** a **lefedettseggel**
- **Zero-trust architekturak** implementalasa legacy vallalati kornyezetekben
- **Formalis verifikacio** alkalmazasa biztonsagi policy ervenyesitesre

### Elosztott Rendszerek
- **Hibaturo architekturak** epitese **bizantci hiba** rezilienciaval
- **Kesleltetés vs. konzisztencia** kompromisszumok optimalizalasa elosztott adatbazisokban
- **Protokollstackok** tervezese ipari IoT-hez valos ideju korlatozasokkal

### Gepi Tanulas
- **Interpretalhato modellek** letrehozasa nagy tetu dontesekhez (biztonsag, egeszsegugy)
- **Modellkomplexitas** es **generalizacios** teljesitmeny egyensulyozasa
- **Adversarial robustness** biztositasa telepitett ML rendszerekben

---

## Egyuttmukodes

Nyitott vagyok egyuttmukodesre a kovetkezo teruleteken:

- **Biztonsagi mernoki munka** — fenyegetesdetektalas, hardening automatizalas, SIEM integracio
- **Elosztott rendszerek** — protokolltervezés, hibatules, ipari integracio
- **Alkalmazott gepi tanulas** — biztonsagi alkalmazasok, anomaliadetektalas, interpretalhathatatosag
- **Nyilt forrasközü eszkozok** — infrastruktura automatizalas, biztonsagi keretrendszerek, kutatasi prototipusok

Lepj kapcsolatba [email](mailto:neduabi@pm.me) vagy [GitHub](https://github.com/ho92ms) utjan.

---

## Alapertekek

> *"Biztonsag mernoki szigoron keresztul. Automatizalas szisztematikus tervezesen keresztul. Intelligencia empirikus validacion keresztul."*

Ezek az elvek vezetlik **vedekezo mernoki munkam** es **kutatasom**:
1. **Szigor** — formalis modszerek, bizonyithato tulajdonsagok, dokumentalt feltevesek
2. **Pragmatizmus** — operativ megvalosithatosag, koltseg-haszon elemzes, fokozatos telepites
3. **Atlathatosag** — nyilt forrasködu hozzajarulasok, reprodukalhato eredmenyek, tudasmegosztasok
