---
title: "Szakmai Tapasztalat"
permalink: /hu/experience/
layout: single
lang: hu
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <strong>🇭🇺 Magyar</strong> | <a href="/en/experience/">🇬🇧 English</a>
</div>

## Áttekintés

Szakmai hátterem a **vállalati biztonsági mérnöki munka**, az **elosztott rendszerarchitektúra** és az **alkalmazott gépi tanulás** területeit öleli fel. Gyakorlati tapasztalatom van **fenyegetésdetektáló rendszerekkel**, **infrastruktúra automatizálással** és **ipari protokoll integrációval** éles környezetekben.

---

## 1. Biztonsági Mérnöki Munka és Infrastruktúra Hardening

### Windows Biztonsági Hardening
- **Alkalmazott biztonsági benchmark-ok:**
  - **STIG** implementálása Windows Server 2016/2019-hez
  - **CIS Benchmark-ok** telepítése Group Policy Object-eken (GPO) keresztül
  - **Microsoft Security Baseline-ok** alkalmazása Windows 10/11-hez (verziók: 21H2, 22H2, 25H2)
  
- **Automatizálási eszközök:**
  - **HardeningKitty** — automatizált compliance ellenőrzés és javítás
  - **PowerShell DSC** — deklaratív konfiguráció idempotens hardeninghez
  - Egyedi scriptek **ADMX sablon telepítéshez** és GPO szinkronizációhoz

- **Attack Surface Reduction (ASR):**
  - **Windows Defender ASR szabályok** konfigurálása zero-day exploit elhárításra
  - **Office makrók**, **script végrehajtás** és **hitelesítő adat lopás** vektorok blokkolása
  - **Controlled folder access** engedélyezése ransomware megelőzésre

**Kulcs Eredmény:** **40%-os csökkentés** a támadási felületben 100+ vállalati végponton automatizált GPO-alapú hardening révén.

---

### Fenyegetésdetektálás és Incidensválasz

#### Honeypot Rendszerek
- **Csalétek fájl monitoring:**
  - **Honeypot fájlok** telepítése (pl. `passwords.txt`, `finances.xls`) stratégiai helyeken
  - **Valós idejű riasztás** Windows Event Log-on keresztül (Event ID 4663 — fájl hozzáférés)
  - **PowerShell-alapú FileSystemWatcher** viselkedéselemzéshez

- **Ransomware detektálás:**
  - **C:\Users** könyvtár monitorozása gyors fájlmódosításokra (titkosítás indikátora)
  - **Automatizált válaszok** (felhasználó kizárás, hálózati izoláció, admin riasztások)
  - **Wazuh SIEM** integráció központosított log aggregációhoz

**Kulcs Eredmény:** **3 ransomware szimuláció** detektálása és izolálása **15 másodpercen** belül a kezdeti fájlmódosítástól.

---

#### SIEM és Log Elemzés
- **Wazuh integráció:**
  - **Wazuh ágensek** telepítése Windows végpontokon és szervereken
  - **Egyedi szabályok** létrehozása:
    - **RDP brute-force** detektálás (Event ID 4625 — sikertelen bejelentkezés)
    - **Event log manipuláció** (Event ID 1102 — log törlése)
    - **Jogosultság-eszkaláció** (Event ID 4672 — különleges jogosultságok hozzárendelése)
  
- **Automatizált incidensválasz:**
  - **IP blokkolási script** ismétlődő RDP hibákhoz (Windows Firewall-on keresztül)
  - **Email riasztások** kritikus biztonsági eseményekhez
  - **Log megőrzési szabályzatok** compliance-hez (GDPR, SOC 2)

**Kulcs Eredmény:** **Átlagos detektálási idő (MTTD)** csökkentése RDP brute-force-nál **24 órából 2 percre**.

---

### Hálózati Biztonsági Architektúra

#### VPN és Biztonságos Távoli Hozzáférés
- **Site-to-site VPN:**
  - **IPSec VPN** konfigurálás többhelyszínes vállalati kapcsolatokhoz
  - **SSL VPN** telepítés biztonságos távoli hozzáféréshez klienssz

oftver nélkül
  - **PPTP** beállítás legacy rendszerkompatibilitáshoz (biztonsági figyelmeztetésekkel dokumentálva)

- **SSH tunneling:**
  - **Reverse SSH tunnel-ek** építése belső szolgáltatások eléréséhez portok feltárása nélkül
  - Tunnel beállítás automatizálása **systemd**-vel (Linux) és **Task Scheduler**-rel (Windows)

- **DNS Biztonság:**
  - **DNS-over-HTTPS (DoH)** engedélyezése titkosított DNS feloldáshoz
  - **DNS szűrés** konfigurálása ismert rosszindulatú domainek blokkolására

**Kulcs Eredmény:** **15+ távoli helyszín** biztosítása **nulla VPN leállással** **12 hónapon** keresztül.

---

#### Reverse Tunnel Architektúra (C# / .NET 8.0)
- **Probléma:** NAT mögötti ipari OPC UA szerverek külső hozzáférést igényelnek belső hálózatok feltárása nélkül
- **Megoldás:** **WebSocket-alapú relay szerver** építése kétirányú tunnelinghez

**Architektúra:**
- **Tunnel Kliens:** WebSocketen kapcsolódik relay szerverhez, kéréseket továbbít helyi OPC UA szerverhez
- **Relay Szerver:** HTTP kéréseket irányít megfelelő tunnel klienshez site ID alapján
- **Mock OPC Szerver:** Tesztkörnyezet protokoll validációhoz

**Technikai Részletek:**
- **Konkurencia:** `ConcurrentDictionary` használata thread-safe kliens kezeléshez
- **Async I/O:** `TaskCompletionSource` alkalmazása kérés/válasz párosításhoz
- **Hibakezelés:** Kapcsolat-újrapróbálkozás logika exponenciális backoff-fal

**Kulcs Eredmény:** **Biztonságos távoli monitoring** ipari berendezéseknél VPN overhead nélkül, **30%-os késleltetés csökkentéssel**.

---

## 2. Vállalati Infrastruktúra és Automatizálás

### Active Directory és Group Policy

#### Domain Controller Telepítés
- **Automatizált AD DS telepítés:**
  - **PowerShell scriptek** felügyelet nélküli domain controller létrehozáshoz
  - **Forest/domain** beállítás, DNS integráció és FSMO szerepek konfigurálása
  - **Backup domain controllerek** implementálása magas rendelkezésre álláshoz

- **GPO Kezelés:**
  - **Moduláris GPO keretrendszer** centralizált policy terjesztéshez
  - **SYSVOL szinkronizálás** automatizálása multi-DC környezetekhez
  - **GPO verziókezelő rendszer** rollback képességekkel

**Kulcs Eredmény:** Domain controller telepítési idő csökkentése **4 órából 20 percre** automatizálással.

---

#### Felhasználó-létrehozás és RBAC
- **Automatizált felhasználó-létrehozás:**
  - **PowerShell scriptek** tömeges felhasználó-létrehozáshoz CSV-ből
  - **Szerepalapú hozzáférés-vezérlés (RBAC)** biztonsági csoportokon keresztül
  - **Felhasználói kvóták**, **home könyvtárak** és **roaming profilok** konfigurálása

- **Biztonsági szabályzatok:**
  - **Jelszó bonyolultság** és **fiókzárolási szabályzatok** érvényesítése
  - **Kerberos** autentikációs beállítások konfigurálása
  - **Legkisebb jogosultság** implementálása **restricted groups**-on keresztül

---

### OS Telepítés és PXE Boot

#### Windows Deployment Services (WDS) + MDT
- **PXE boot infrastruktúra:**
  - **DHCP opciók 66/67** konfigurálás hálózati boothoz
  - **TFTP szerver** beállítás boot image terjesztéshez
  - **Microsoft Deployment Toolkit (MDT)** integráció testreszabáshoz

- **Automatizált telepítések:**
  - **Felügyelet nélküli answer fájlok** létrehozása (autounattend.xml) zero-touch telepítésekhez
  - **Driver injektálás** implementálása változatos hardverekhez
  - **Telepítés utáni scriptek** konfigurálása (Windows frissítések, szoftver telepítés, domain csatlakozás)

**Kulcs Eredmény:** **Zero-touch telepítés** Windows 10/11-hez, imaging idő csökkentése **3 órából 45 percre**.

---

### PowerShell Automatizálás

#### Scripting Keretrendszer
- **Moduláris library:**
  - **Újrafelhasználható modulok** gyakori feladatokhoz (AD műveletek, GPO kezelés, naplózás)
  - **Hibakezelés** és **naplózás** best practice-ek implementálása
  - **Paraméter validáció** robusztus input kezeléshez

- **Eseményvezérelt monitoring:**
  - **Valós idejű monitoring** scriptek:
    - **Fájlrendszer változások** (FileSystemWatcher)
    - **Event log anomáliák** (Get-WinEvent)
    - **Szolgáltatás hibák** (Get-Service)
  
- **Backup/Restore:**
  - **Inkrementális backup-ok** automatizálása verziókezeléssel
  - **Integritás ellenőrzések** implementálása (hash validáció)
  - **Disaster recovery** scriptek domain controller visszaállításhoz

**Kulcs Eredmény:** **Manuális scripting hibák** csökkentése **80%-kal** szabványosított modul használattal.

---

## 3. Elosztott Rendszerek és Protokollok

### WebSocket-alapú Relay Szerver
- **Konkurens kapcsolatkezelés:**
  - `ConcurrentDictionary<string, WebSocket>` thread-safe kliens regisztrációhoz
  - `TaskCompletionSource<TunnelResponse>` async kérés/válasz párosításhoz
  - **Connection pooling** hatékony erőforrás-használathoz

- **Protokoll implementáció:**
  - **Egyedi üzenetformátum** (JSON-alapú) tunnel komunikációhoz
  - **Heartbeat mechanizmus** kapcsolat élőség detektáláshoz
  - **Újrakapcsolódási logika** exponenciális backoff-fal

**Teljesítmény:** **100+ konkurens tunnel kapcsolat** kezelése **<50ms késleltetéssel** kérés továbbításnál.

---

### Ipari Protokollok (OPC UA)
- **Mock OPC Szerver:**
  - **Minimális OPC UA szerver** implementálása C#-ban teszteléshez
  - Alapvető **olvasás/írás** műveletek támogatása
  - **Interoperabilitás** validálása kereskedelmi SCADA rendszerekkel

- **Biztonság:**
  - **Tanúsítvány-alapú autentikáció** konfigurálása
  - **Üzenet titkosítás** engedélyezése (AES-256)
  - **Hozzáférés-vezérlés** implementálása felhasználói szerepeken keresztül

---

## 4. Gépi Tanulás és Adattudomány

### Mély Tanulás
- **Keretrendszerek:** PyTorch, TensorFlow/Keras
- **Architektúrák:** CNN-ek, RNN-ek, Transformer-ek
- **Feladatok:** Képosztályozás, szekvencia modellezés, anomáliadetektálás

### Nagy Nyelvi Modellek (LLM-ek)
- **Finomhangolás:** LoRA, prefix tuning domain adaptációhoz
- **Prompt engineering:** Few-shot tanulás, chain-of-thought prompting
- **Telepítés:** REST API szolgáltatás, konténerizált következtetés

### Adatelemzés
- **Feltáró Adatelemzés (EDA):** Pandas, Matplotlib, Seaborn
- **Feature Engineering:** Domain-specifikus transzformációk, dimenziócsökkentés
- **Statisztikai Tesztelés:** A/B tesztelés, hipotézis tesztelés, konfidencia intervallumok

---

## Kulcs Erősségek

1. **Biztonsági Mérnöki Munka** — fenyegetésdetektálás, hardening automatizálás, compliance keretrendszerek
2. **Rendszerarchitektúra** — elosztott tervezés, hibatűrés, protokoll implementáció
3. **Automatizálás és Scriptelés** — PowerShell, Python, infrastructure as code
4. **Operatív Kiválóság** — monitoring, incidensválasz, disaster recovery

---

## Kapcsolat

Szakmai megkeresésekhez vagy együttműködési lehetőségekhez:

📧 **Email:** [neduabi@pm.me](mailto:neduabi@pm.me)  
🔗 **GitHub:** [github.com/ho92ms](https://github.com/ho92ms)



