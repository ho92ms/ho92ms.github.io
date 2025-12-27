---
title: "Önéletrajz"
permalink: /hu/cv/
layout: single
lang: hu
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <strong>🇭🇺 Magyar</strong> | <a href="/en/cv/">🇬🇧 English</a>
</div>

## Németh Dávid

**Biztonsági Mérnök | Rendszerarchitekt | Alkalmazott Gépi Tanulás Kutató**

📧 [neduabi@pm.me](mailto:neduabi@pm.me) | 🔗 [github.com/ho92ms](https://github.com/ho92ms)

---

## Tanulmányok

**Gépitanulás BSc** (félévben)  
*Fókusz:* Mélytanulás, statisztikai következtetés, optimalizációs elmélet, neurális architektúrák

**Szoftvermérnök BSc** (lezárva)  
*Fókusz:* Elosztott rendszerek, formális verifikáció, algoritmus tervezés, hálózati protokollok

---

## Szakmai Tapasztalat

### Biztonsági Mérnök és Rendszerarchitekt
**VargaFlex IT Infrastruktúra** | *Vállalati Biztonság és Megfelelőség*

- **Fenyegetés Észlelés és Reagálás**
  - Kialakított és telepített **honeypot rendszerek** ransomware észlelésére és korai figyelmeztetésre
  - Megvalósított **viselkedésalapú megfigyelést** fájlrendszeri anomáliákhoz (PowerShell alapú EDR)
  - Egyedi **SIEM szabályokat** készített a Wazuh platformhoz, célzottan a Windows eseménynaplóihoz (4663-as, 1102-es, 4625-ös esemény azonosítók)
  - Kidolgozott **automatikus fenyegetésválasz** szkripteket RDP brute-force mérséklésére

- **Windows Zárhardverezés és Megfelelőség**
  - Alkalmazta a **STIG és CIS irányelveket** Csoportházirend-objektumokon (GPO) keresztül
  - Telepítette a **Microsoft Biztonsági Alapbeállításait** (Windows 10/11, Windows Server 2016/2019)
  - Automatizálta a zárhardverezési munkafolyamatokat **HardeningKitty** és egyedi PowerShell DSC használatával
  - Beállította a **Windows Defender Támadásfelület Csökkentése (ASR)** szabályait nulladik napi védelemhez

- **Hálózatbiztonsági Architektúra**
  - Tervezett **visszafelé alagút architektúrákat** WebSocketeken keresztül biztonságos ipari protokoll-hozzáféréshez (OPC UA)
  - Megvalósított **helyhez kötött VPN-t** (IPSec, SSL VPN) többhelyszíni vállalati kapcsolatokhoz
  - Beállította a **DNS-over-HTTPS (DoH)** titkosított DNS feloldáshoz
  - Készített **SSH alagút megoldásokat** biztonságos távoli hozzáféréshez

- **Vállalati Telepítés és Automatizálás**
  - Telepítette a **PXE indító infrastruktúrát** (Windows Telepítési Szolgáltatások + Microsoft Telepítési Keretrendszer)
  - Automatizálta az **OS képalkotási** munkafolyamatokat egyedi, felesleges telepítési konfigurációkkal
  - Kifejlesztett **Active Directory telepítési szkripteket** tartományvezérlő-kibővítéshez
  - Létrehozott **GPO kezelés automatizálás** a SYSVOL szinkronizálás és házirend érvényesítése érdekében

---

### Szoftvermérnök és Rendszerfejlesztő
**Elosztott Rendszerek és Ipari Protokollok**

- **WebSocket-alapú Alagút Architektúra (C# / .NET 8.0)**
  - Tervezett **átjáró szerver mintát** bidirekcionális kommunikációhoz NAT határokon keresztül
  - Megvalósított **OPC UA hamis szerver** ipari automatizálási teszteléshez
  - Készített **többhelyszíni alagút kezelést** párhuzamos kapcsolatkezeléssel (`ConcurrentDictionary`)
  - Alkalmazott **aszimmetrikus I/O mintákat** nagy áteresztőképességű adátviteli feladatokhoz

- **PowerShell Automatizálási Keretrendszer**
  - Kifejlesztett **moduláris szkriptkönyvtárat** AD DS, GPO és biztonsági műveletekhez
  - Létrehozott **eseményvezérelt megfigyelési** rendszereket valós idejű figyelmeztetéssel
  - Készített **biztonsági mentés/visszaállítás automatizálást** verziókezeléssel és integritásellenőrzésekkel
  - Megvalósított **felhasználó létrehozási munkafolyamatokat** szerepalapú hozzáférés-vezérléssel (RBAC)

- **Hálózati Protokoll Megvalósítás**
  - Beállította a **PXE indítást** (DHCP 66/67-es opciók, TFTP) hálózaton alapuló OS telepítéshez
  - Tervezett **alhálózati szegmenseket** izolált biztonsági zónákhoz
  - Megvalósított **tűzfal-szabály automatizálást** dinamikus szolgáltatás-kibővítéshez

---

### Gépi Tanulás Mérnök és Kutató
**Alkalmazott Neurális Hálózatok és Adat-vezérelt Rendszerek**

- **Mély Tanulási Keretrendszerek**
  - Tervezett és tanított **neurális hálózati architektúrákat** (PyTorch, TensorFlow/Keras)
  - Végzett **hiperparaméter-optimalizálást** Bayes-i módszerekkel és rács kereséssel
  - Telepített **követési csővezetékeket** REST API-kon keresztül konténerizált környezetekben (Docker)

- **Nagy Nyelvi Modellek (LLM)**
  - Finomhangolt **domain-specifikus modellek** LoRA és prefix tuning használatával
  - Kifejlesztett **prompt mérnöki stratégiák** feladat-specifikus teljesítményhez
  - Készített **LLM-alapú ügynököket** hibakezeléssel és visszaesési mechanizmusokkal

- **Adat Elemzés és Statisztikai Modellezés**
  - Végzett **exploratív adat elemzést (EDA)** statisztikai összefoglalásokkal és vizualizációkkal
  - Alkalmazott **jellemző mérnöki technikák** domain-specifikus reprezentációkhoz
  - Lebonyolított **A/B tesztelést** és statisztikai validálást reprodukálható kutatáshoz

---

## Technikai Készségek

### Programozási Nyelvek
- **Elsődleges:** C#, PowerShell, Python
- **Másodlagos:** C++, Java, JavaScript/TypeScript, Bash

### Biztonság és Infrastruktúra
- **Zárhardverezés:** Windows Biztonsági Alapbeállítások, STIG, CIS Irányelvek, GPO tervezés
- **SIEM/EDR:** Wazuh, Windows Eseménynapló elemzés, fenyegetésvadászat
- **Hálózatbiztonság:** VPN (IPSec, SSL, SSH), DNS-over-HTTPS, tűzfalszabály automatizálás
- **Honeypot és Csapda:** Fájl megfigyelés, viselkedés észlelés, riasztó rendszerek

### Rendszerek és Hálózatok
- **Windows Server:** Active Directory, Csoportházirend, WDS, MDT, DHCP, DNS
- **Felhő:** Microsoft Azure (számítás, hálózatépítés, biztonság)
- **Protokollok:** OPC UA, WebSocket, TCP alagút, PXE indítás (TFTP)

### Szoftvermérnökség
- **Backend:** ASP.NET Core, WebSocket szerverek, RESTful API-k
- **Adatbázisok:** PostgreSQL, MySQL, MongoDB
- **DevOps:** Git, Docker, Kubernetes, CI/CD (Azure DevOps, GitHub Actions)

### Gépi Tanulás
- **Keretrendszerek:** PyTorch, TensorFlow/Keras, scikit-learn
- **LLM:** OpenAI API, Hugging Face Transformers, finomhangolás (LoRA, prefix tuning)
- **Eszközök:** Jupyter, Pandas, NumPy, Matplotlib

---

## Kulcsprojektek

### 1. Visszafelé Alagút Architektúra (C# / .NET 8.0)
*Biztonságos ipari protokoll hozzáférés WebSocketen keresztül*

- **Probléma:** Ipari OPC UA szerverek NAT mögött külső hozzáférést igényelnek anélkül, hogy belső hálózatokat ki kellene tenni
- **Megoldás:** Készített **átjáró szerver** WebSocket-alapú bidirekcionális alagút kialakításával
- **Összetevők:** Hamis OPC szerver, alagút kliens, átjáró szerver párhuzamos kapcsolatkezeléssel
- **Hatás:** Biztosította a biztonságos távoli megfigyelést VPN terhei nélkül

### 2. Vállalati Biztonsági Zárhardverezési Keretrendszer
*Automatizált Windows megfelelőség és fenyegetés észlelés*

- **Terjedelem:** 100+ vállalati munkaállomás és szerver
- **Módszerek:** GPO-alapú STIG végrehajtás, ASR szabályok, honeypot telepítés
- **Eszközök:** HardeningKitty, Wazuh SIEM, egyedi PowerShell szkriptek
- **Eredmények:** Csökkentett támadási felület, valós idejű ransomware észlelés, megfelelőségi audit előkészítettség

### 3. PXE Indító Infrastruktúra
*Automatizált OS telepítés vállalati környezetekben*

- **Technológiai háttér:** Windows Telepítési Szolgáltatások (WDS), Microsoft Telepítési Keretrendszer (MDT)
- **Jellemzők:** Felesleges telepítések, illesztőprogram injekció, telepítés utáni konfiguráció
- **Automatizálás:** PowerShell szkriptek telepítési testreszabáshoz és DHCP opciókezeléshez
- **Eredmény:** Nulla érintésű telepítés Windows 10/11 számára hálózati indítással

---

## Kutatási Érdeklődés

- **Rendszerbiztonság és Zárhardverezés:** A biztonsági politikák formális verifikálása, automatizált megfelelőség
- **Elosztott Rendszerek:** Hibatűrő architektúrák, konszenzus protokollok
- **Gépi Tanulás Biztonság:** Ellenséges robusztusság, modellértelmezhetőség
- **Neurális Architektúra Tervezés:** Induktív torzítások, általánosítási elmélet

---

## Publikációk és Nyílt Forráskód

Kiválasztott munkák és kísérletek elérhetők a [GitHubon](https://github.com/ho92ms).

---

## Tanúsítványok és Képzés

- Windows Server Adminisztráció és Biztonság
- Vállalati Hálózat Tervezés
- Ipari Protokollok és OPC UA
- Gépi Tanulás Specializáció (folyamatban)

---

## Nyelvek

- **Magyar:** Anyanyelvi
- **Angol:** Szakmai munkahelyi szint (C1)

---

## Elvek

> *"Biztonság mérnöki szigorral. Automatizálás rendszerszerű tervezéssel. Intelligencia empirikus validálással."*

---

## Kapcsolat

📧 **Email:** [neduabi@pm.me](mailto:neduabi@pm.me)  
🔗 **GitHub:** [github.com/ho92ms](https://github.com/ho92ms)

---

*Utolsó frissítés: 2025. december*




