<div align="center">

<img src="../logo.png" alt="ResidenzaBoi Logo" width="320"/>

<br/><br/>

**Dalla vita in residenza a una community che gioca, compete e cresce insieme.**

<br/>

[![Status](https://img.shields.io/badge/status-in%20sviluppo-yellow?style=for-the-badge)](https://github.com/ResidenzaBoi)
[![Community](https://img.shields.io/badge/community-ELIS-00D084?style=for-the-badge)](https://github.com/ResidenzaBoi)
[![Contribuisci](https://img.shields.io/badge/contribuisci-PR%20benvenute-white?style=for-the-badge)](https://github.com/ResidenzaBoi)

</div>

---

## 💡 Cos'è ResidenzaBoi?

**ResidenzaBoi** è l'organizzazione che sviluppa **ELIS Sport**, un'app nata da un'idea semplice: trasformare il tradizionale registro del calcio della residenza **ELIS** in un'esperienza più completa, moderna e coinvolgente.

Dopo l'ultimo esame della sessione, invece di fermarci a riposare, abbiamo scelto di continuare a costruire. Abbiamo così iniziato a sviluppare una **piattaforma dedicata allo sport e alla vita della community ELIS**.

---

## 🏆 ELIS Sport — un'unica piattaforma per lo sport in ELIS

<div align="center">

| ⚽ **Calcio** | 🏀 **Basket** | 🏐 **Pallavolo** |
|:-------------:|:-------------:|:----------------:|

</div>

<br/>

Per ogni sport offriamo un'esperienza chiara e completa:

> 📊 Classifiche aggiornate in tempo reale
>
> 📈 Statistiche individuali e di squadra
>
> 📋 Risultati e andamento delle partite
>
> 🔔 Notifiche direttamente nell'app
>
> 🤝 Uno spazio digitale pensato per favorire partecipazione e competizione sana

---

## ⚙️ Tech Stack

<div align="center">

![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)

</div>

---

## 🏗️ Architettura

```
┌──────────────────┐         ┌──────────────────────┐
│   🖥️ Frontend    │  HTTP   │    🔧 Backend         │
│   Angular + TS   │────────▶│    Spring Boot        │
│                  │  REST   │                       │
│  • Components    │◀────────│  Controller           │
│  • Services      │   JSON  │    ↓                  │
│  • Routing       │         │  Service / Policy     │
│  • Guards        │         │    ↓                  │
└──────────────────┘         │  Repository           │
                             │    ↓                  │
                             │  Entity ←→ DTO        │
                             └─────────┬────────────┘
                                       │
                                       ▼
                             ┌──────────────────────┐
                             │    🗄️ MySQL           │
                             │                       │
                             │  • Utenti e profili   │
                             │  • Partite e risultati│
                             │  • Classifiche        │
                             └──────────────────────┘
```

---

## 🧩 Design Pattern

Il backend segue un'architettura **layered** con separazione chiara delle responsabilità:

| Layer | Package | Responsabilità |
|:--|:--|:--|
| **Presentazione** | `controller` | REST API endpoints |
| **Business Logic** | `service`, `policy` | Logica di gioco, regole e autorizzazioni |
| **Trasformazione** | `dto`, `mapper` | Conversione Entity ↔ DTO |
| **Persistenza** | `repository`, `entity` | Accesso dati con Spring Data JPA |
| **Infrastruttura** | `config`, `exception`, `listener`, `scheduler` | Configurazione, gestione errori, eventi e task schedulati |

```
📂 com.residenza.com.calcioelis
├── 📂 config          # Configurazione app e sicurezza
├── 📂 controller      # REST Controller (API endpoints)
├── 📂 dto             # Data Transfer Objects
├── 📂 entity          # Entità JPA (modello dati)
├── 📂 exception       # Gestione centralizzata degli errori
├── 📂 listener        # Event Listener
├── 📂 mapper          # Entity ↔ DTO mapping
├── 📂 policy          # Regole di business e autorizzazione
├── 📂 repository      # Spring Data JPA Repositories
├── 📂 scheduler       # Task schedulati
├── 📂 service         # Logica di business
└── 📄 CalcioElisApplication.java
```

---

## 📁 Struttura del progetto

| Repository | Descrizione | Tech | Stato |
|:--|:--|:--|:--:|
| [`CalcioElis_BE`](https://github.com/ResidenzaBoi/CalcioElis_BE) | Backend — API REST e logica di business | Spring Boot, Java | 🔒 Private |
| [`CalcioElis_FE`](https://github.com/ResidenzaBoi/CalcioElis_FE) | Frontend — Web app e interfaccia utente | Angular, TypeScript | 🔒 Private |
| [`.github`](https://github.com/ResidenzaBoi/.github) | Profilo dell'organizzazione | — | 🌐 Public |

---

## 📋 Project Board

Gestiamo bug, feature e miglioramenti tramite il nostro **GitHub Project Board**:

👉 [**ResidenzaBoi — Board**](https://github.com/orgs/ResidenzaBoi/projects/1)

Hai trovato un bug o hai un'idea? [Apri una issue](https://github.com/orgs/ResidenzaBoi/projects/1) e la prenderemo in carico!

---

## 🫂 Più di un'app: una community

**ELIS Sport** non è soltanto uno strumento per registrare risultati. È un progetto **nato dalla community e per la community**, con l'obiettivo di rendere più semplice partecipare, seguire i propri progressi e vivere lo sport della residenza in modo ancora più coinvolgente.

> *Vogliamo creare un ambiente in cui ogni partita racconti qualcosa:*
> *la sfida, il gruppo, il miglioramento e il piacere di condividere un'esperienza.*

---

## 🛠️ Costruito insieme

Il progetto nasce dalla voglia di trasformare un'esigenza concreta in qualcosa di **utile, funzionale e bello da usare**.

Siamo all'inizio del percorso e stiamo costruendo **ELIS Sport** passo dopo passo, ascoltando la community e raccogliendo idee per migliorare continuamente.

---

## 🎯 Il nostro obiettivo

<div align="center">

*Trasformare il registro delle partite in una piattaforma sportiva completa:*
*più funzionale, più connessa e soprattutto più vicina alle persone*
*che vivono la residenza ogni giorno.*

<br/>

<img src="../logo.png" alt="ResidenzaBoi" width="80"/>

<br/>

**ResidenzaBoi**

`>_`

</div>
