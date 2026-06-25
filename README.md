# Můj Hybridní Home-Lab 🚀

Ahoj! Tady mám zdokumentované svoje testovací prostředí, které mi běží doma ve VirtualBoxu. Nechtěl jsem se učit teorii jen z knížek, tak jsem si postavil vlastní síť, kde kombinuju Windows Server pro správu uživatelů a Linux/Docker pro provozování webů. 

Ukazuju tím, že sice hledám svoji první juniorní pozici, ale základy z inzerátů už mám osahané z praxe v labu.

---

## 🛠️ Co mi v labu běží a co s tím dělám

### 🖥️ Windows Server 2019 (Firemní síť)
Tady simuluju klasické kancelářské prostředí.
*   **Active Directory:** Mám založenou testovací firmu, vytvořené organizační jednotky (OU) a uživatele.
*   **GPO (Skupinové politiky):** Testuju, jak uživatelům hromadně zakázat blbosti, nastavit jim tapetu nebo automaticky namapovat síťové disky.
*   **Sdílené složky:** Nastavená NTFS práva (kdo kam může a nemůže).

### 🐧 Linux (Ubuntu Server) + Docker
Tohle mě baví, protože to má blízko k modernímu hostingu.
*   **Docker & Docker Compose:** Neinstaluju služby přímo do systému, ale balím je do kontejnerů. Používám i perzistentní volume, aby se mi při restartu nesmazala data.
*   **Nginx:** Používám ho jako reverzní proxy – stará se o to, aby se požadavky zvenku správně nasměrovaly do mých Docker kontejnerů.
*   **Databáze:** Mám tu nahozené PostgreSQL a MongoDB pro svoje vývojářské pokusy v Reactu a TypeScriptu.

---

## 📁 Důkazy místo slibů (Screenshoty & Konfigurace)

Abyste mi věřili, že to opravdu běží a jen nekecám, v těchhle složkách mám screeny a konfiguráky:

*   📂 **`/windows`** – Jak vypadá moje Active Directory, GPO a správa disků.
*   📂 **`/linux`** – Ukázky mých Docker Compose souborů, konfigurace Nginxu a screeny z terminálu.

---

## 🎯 Co mám v plánu dodělat v nejbližších dnech?
*   Nasadit **Uptime Kuma** nebo **Netdata** pro monitoring, abych viděl, kdyby mi nějaký kontejner spadl.
*   Napsat si jednoduchý **Bash skript** na automatické zálohování databází.
