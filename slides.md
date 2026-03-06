---
title: "EU AI Act"
author: "Jan Vaorin"
footer: "Jan Vaorin | EU AI Act </b>"
paginate: true
marp: true
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Sans:wght@100;200;300;400;500;600;700;800;900&display=swap');


  
  * {
    font-family: "Fira Sans"
  }

  :root {
    --adesso-blue: #006ec7;
    --adesso-dark-blue: #00439e;
    --adesso-light-blue: #02A5E3 ;
    --adesso-accent: #27d9a7;
    --adesso-green: #7AB800;
    --adesso-orange: #FF6600;
    --adesso-gray-dark: #333333;
    --adesso-gray-medium: #9f9f9f;
    --adesso-gray-light: #F2F4F7;
    --adesso-white: #FFFFFF;
    --logo: "https://upload.wikimedia.org/wikipedia/commons/f/f7/Adesso_AG_logo.svg";
  }

section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;         /* anchor at top-left of slide */
  width: 100%;     /* cover entire slide */
  height: 100%;
  /* 1st background: logo centered at bottom
     2nd background: vertical stripe on the left */
  background-image:
    url("https://upload.wikimedia.org/wikipedia/commons/f/f7/Adesso_AG_logo.svg"),
    linear-gradient(30deg, var(--adesso-blue), var(--adesso-blue));
  background-repeat:
    no-repeat,
    no-repeat;
  background-position:
    right top 30px,  /* logo centered, 10px from bottom */
    left top;            /* stripe starts at top-left */
  background-size:
    120px 40px,          /* logo size */
    20px 100%;           /* stripe width & full height */
  pointer-events: none;  /* don't block clicks */
  z-index: 1;
}

  /* Überschriften */
  section h1 {
    color: var(--adesso-blue);
    font-size: 36pt;
    font-weight: 700;
    border-bottom: 3px solid var(--adesso-blue);
    padding-bottom: 10px;
    margin-bottom: 20px;
  }

  section h2 {
    color: var(--adesso-light-blue);
    font-size: 26pt;
    font-weight: 600;
    margin-bottom: 16px;
  }

  section h3 {
    color: var(--adesso-dark-blue);
    font-size: 22pt;
    font-weight: 600;
  }

  /* Links */
  section a {
    color: var(--adesso-light-blue);
    text-decoration: none;
  }
  section a:hover {
    text-decoration: underline;
  }

  /* Blockquote – Definition-Style */
  section blockquote {
    border-left: 5px solid var(--adesso-light-blue);
    background: var(--adesso-gray-light);
    padding: 20px 25px;
    margin: 20px 0;
    border-radius: 0 8px 8px 0;
    font-size: 20pt;
    color: var(--adesso-gray-dark);
  }

  /* Tabellen */
  section table {
    width: 100%;
    border-collapse: collapse;
    font-size: 20pt;
  }
  section table thead th {
    background: var(--adesso-blue);
    color: var(--adesso-white);
    padding: 12px 16px;
    text-align: left;
    font-weight: 600;
  }
  section table tbody td {
    padding: 10px 16px;
    border-bottom: 1px solid #dde1e6;
  }
  section table tbody tr:nth-child(even) {
    background: var(--adesso-gray-light);
  }

  /* Listen */
  section ul, section ol {
    margin-left: 10px;
  }
  section li {
    margin-bottom: 6px;
    line-height: 1.5;
  }

  /* Footer */
  footer {
    color: var(--adesso-gray-medium);
    font-size: 11pt;
  }

  /* ===== TITELFOLIE2 ===== */
  section.title2 {
    background: linear-gradient(
    180deg,
    var(--adesso-blue) 0%,
    var(--adesso-blue) 30%,   /* flat area at top */
    var(--adesso-dark-blue) 70%,
    var(--adesso-dark-blue) 100%
  );
    color: var(--adesso-white);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 80px;
  }
  section.title2::before {
    display: none;
  }
  section.title2 h1 {
    color: var(--adesso-white);
    border-bottom: 3px solid var(--adesso-light-blue);
    font-size: 40pt;
    margin-bottom: 10px;
  }
  section.title2 h2 {
    color: var(--adesso-light-blue);
    font-size: 26pt;
    font-weight: 400;
  }
  section.title2 p {
    color: rgba(255,255,255,0.85);
    font-size: 20pt;
  }
  /* ===== TITELFOLIE ===== */
  section.title {
    background: linear-gradient(300deg, var(--adesso-dark-blue) 0%, var(--adesso-blue) 60%, var(--adesso-accent) 100%);
    color: var(--adesso-white);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 80px;
  }
  section.title::before {
    display: none;
  }
  section.title h1 {
    color: var(--adesso-white);
    border-bottom: 3px solid var(--adesso-light-blue);
    font-size: 40pt;
    margin-bottom: 10px;
  }
  section.title h2 {
    color: var(--adesso-light-blue);
    font-size: 26pt;
    font-weight: 400;
  }
  section.title p {
    color: rgba(255,255,255,0.85);
    font-size: 20pt;
  }

  /* ===== KAPITELFOLIE ===== */
  section.chapter {
    background: var(--adesso-blue);
    color: var(--adesso-white);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px;
  }
  section.chapter::before {
    display: none;
  }
  section.chapter h1 {
    color: var(--adesso-white);
    border-bottom: 3px solid var(--adesso-light-blue);
    font-size: 42pt;
  }
  section.chapter h2 {
    color: var(--adesso-light-blue);
    font-size: 24pt;
    font-weight: 400;
  }

  /* ===== ENDFOLIE ===== */
  section.end {
    background: linear-gradient(0deg, var(--adesso-blue) 0%, var(--adesso-dark-blue) 100%);
    color: var(--adesso-white);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  section.end::before {
    display: none;
  }
  section.end h1 {
    color: var(--adesso-white);
    border-bottom: 3px solid var(--adesso-accent);
    font-size: 42pt;
  }
  section.end p {
    color: rgba(255,255,255,0.85);
    font-size: 20pt;
  }

  /* ===== CALLOUT BOX ===== */
  .callout {
    background: var(--adesso-gray-light);
    border-left: 5px solid var(--adesso-accent);
    border-radius: 0 8px 8px 0;
    padding: 18px 24px;
    margin: 16px 0;
    font-size: 19pt;
  }
  .callout h1, .callout h2, .callout h3 {
    color: var(--adesso-blue);
    font-size: 20pt;
    border-bottom: none;
    margin-bottom: 6px;
    padding-bottom: 0;
  }
  .callout.warning {
    border-left-color: var(--adesso-orange);
    background: #FFF7F0;
  }
  .callout.warning h1, .callout.warning h2, .callout.warning h3 {
    color: var(--adesso-orange);
  }
  .callout.note {
    border-left-color: var(--adesso-green);
    background: #F4FAE8;
  }
  .callout.note h1, .callout.note h2, .callout.note h3 {
    color: #5A8F00;
  }

  /* ===== MULTI-COLUMN LAYOUT ===== */
  .container {
    display: flex;
    gap: 30px;
  }
  .col {
    flex: 1;
  }

  /* ===== ADESSO LOGO-BADGE (unten rechts) ===== */
  xx:not(.title):not(.end)::after {
  position: absolute;
  right: 0;
  margin-left: 10px;
  transform: translateX(-50%);   /* center horizontally */
  width: 100px;
  height: 60px;
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/f/f7/Adesso_AG_logo.svg");
  background-repeat: no-repeat;
  background-size: contain;
  content:'';
  /*filter: grayscale(1) brightness(0.5); /* gray + slightly darker */
}

.adessologo:not(.title):not(.end):not(.base2){
  width: 70px;
  position: absoulute;
  bottom:0;
  right:0;
  margin-left:00px;
  margin-bottom: -9px;
}
  /* ===== RISK-TABELLE CUSTOM STYLES ===== */
  .risk-table th {
    font-size: 16pt;
    text-align: center;
    padding: 14px 10px;
  }
  .risk-table td {
    font-size: 16pt;
    text-align: center;
    vertical-align: top;
    padding: 14px 10px;
  }

  /* ===== DISKUSSIONSFOLIE ===== */
  section.base2 {
    background: var(--adesso-blue);
    color: var(--adesso-white);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  section.discussion {
    background: linear-gradient(135deg, var(--adesso-dark-blue) 0%, var(--adesso-blue) 50%, var(--adesso-accent) 100%);
    color: var(--adesso-white);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  section.discussion::before {
    display: none;
  }
  section.discussion h1 {
    color: var(--adesso-white);
    border-bottom: none;
    font-size: 44pt;
  }
  section.discussion h2 {
    color: var(--adesso-accent);
    font-size: 28pt;
    font-weight: 400;
  }
  section.discussion h3 {
    color: rgba(255,255,255,0.9);
    font-size: 22pt;
    font-weight: 400;
    max-width: 80%;
  }

  /* ===== HIGHLIGHT BOX ===== */
  .highlight-box {
    background: linear-gradient(90deg, var(--adesso-blue), var(--adesso-light-blue));
    color: white;
    padding: 20px 28px;
    border-radius: 10px;
    margin: 16px 0;
    font-size: 20pt;
  }

</style>



<!-- _class: base2 -->
<!-- _paginate: false -->
<!-- _footer: "" -->

 <style>
  .logo-white {
    width: 200px;
    height: 60px;
    background-image: url("https://upload.wikimedia.org/wikipedia/commons/f/f7/Adesso_AG_logo.svg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    scale: 350%;
    filter: invert(1) brightness(200); /* inverts colors -> dark becomes light/white */
  }
</style>

<div class="logo-white"></div>

---


<!-- _class: title2 -->
<!-- _paginate: false -->
<!-- _footer: "" -->

# EU AI Act

## An Overview of Europe's AI Regulation

**Jan Vaorin** · adesso SE

<!-- Titelfolie – Überblick über die EU-KI-Verordnung -->



---

![bg right:30%](https://images.unsplash.com/photo-1697577418970-95d99b5a55cf?q=80&w=3000&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

# What is an AI System?

## Article 3, Point 1 (f)

<!-- Einstiegsfrage: Was genau versteht die EU unter einem KI-System? -->

---

# Definition — AI System

> _"A machine-based system designed to operate with **varying levels of autonomy** and that may exhibit **adaptiveness after deployment** and that, for explicit or implicit objectives, **infers**, from the input it receives, how to generate outputs such as **predictions, content, recommendations, or decisions** that can influence **physical or virtual environments**."_

— **Chapter 1, Article 3**

<!--
  Die offizielle Legaldefinition aus Art. 3 Abs. 1 lit. f.
  Bewusst breit gefasst, um möglichst viele Technologien abzudecken –
  von einfachen ML-Modellen bis hin zu komplexen autonomen Systemen.
-->

---

![bg left:35%](https://images.unsplash.com/photo-1620712943543-bcc4688e7485?w=800&auto=format&fit=crop)

# Key Elements

- 🤖 **Machine-based system**
- 🌍 Can influence **physical or virtual environments**
- 🔄 **Varying levels of autonomy**
- 📈 May **adapt after deployment**
- 🧠 **Infers** from input to generate output

<!--
  Die fünf Kernmerkmale der KI-Definition.
  "Inferenz" grenzt KI-Systeme von herkömmlicher regelbasierter Software ab.
  Outputs: Vorhersagen, Inhalte, Empfehlungen, Entscheidungen.
-->

---

# Different Types of Entities

| Role | Example |
|:-----|:--------|
| **Provider** | OpenAI, Anthropic, BayernGPT |
| **Deployer** | Software developer using AI |
| **Importer** | Bringing AI into EU market |
| **Product Manufacturer** | Embedding AI in products |
| **Distributor** | Making AI available on market |
| **Representative** | Acting on behalf of provider |

<!--
  Sechs verschiedene Akteure in der KI-Wertschöpfungskette.
  Jede Rolle bringt unterschiedliche Pflichten mit sich.
  Provider tragen die größte Verantwortung.
-->

---

# Multiple Roles Are Possible

<div class="callout note">

### Recital 83

It is possible to be **multiple types of entity at once**.

</div>

A company that develops an AI model **and** deploys it in its own products acts as both **Provider** and **Deployer**.

<!--
  Praxisbeispiel: Google ist gleichzeitig Provider (Gemini)
  und Deployer (Google-Suche). Pflichten gelten kumulativ.
-->

---

<!-- _class: chapter -->
<!-- _paginate: false -->
<!-- _footer: "" -->

# 🚦 Risk-Based Classification

## The Four Tiers of AI Risk

<!--
  Kernstück des AI Acts: Der risikobasierte Ansatz.
  Je höher das Risiko, desto strenger die Regulierung.
-->

---

# Risk Pyramid Overview

<style scoped>section { font-size: 19pt; }</style>

<table>
  <thead>
    <tr>
      <th style="background:#C0392B; color:white; width:25%;">🔴 Unacceptable</th>
      <th style="background:#E67E22; color:white; width:25%;">🟠 High Risk</th>
      <th style="background:#0073CF; color:white; width:25%;">🟡 Limited Risk</th>
      <th style="background:#7AB800; color:white; width:25%;">🟢 Minimal Risk</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Manipulative AI, social scoring, predictive policing, mass surveillance</td>
      <td>Biometrics, critical infra, education, law enforcement, employment</td>
      <td>LLMs, AI-generated ads, deepfakes — user must be informed</td>
      <td>Gaming AI, spam filters, TTS, STT</td>
    </tr>
    <tr>
      <td><strong>❌ Prohibited (Art 5)</strong></td>
      <td><strong>⚠️ Regulated (Art 6)</strong></td>
      <td><strong>✅ Permitted</strong></td>
      <td><strong>✅ Permitted</strong></td>
    </tr>
  </tbody>
</table>

<!--
  Übersichtstabelle aller vier Risikostufen.
  Die große Mehrheit aller KI-Systeme fällt unter "Minimal Risk"
  und ist damit praktisch unreguliert.
-->

---

# 🔴 Unacceptable Risk — Prohibited

<style scoped>section { font-size: 22pt; }</style>

## Chapter 2, Article 5

These AI practices are **completely banned**:

1. 🎭 **Manipulative or deceptive AI** causing significant harm
2. 🎯 **Exploiting vulnerabilities** (age, disability…)
3. 📊 **Social scoring** of individuals or groups
4. 🔮 **Predictive policing** based solely on profiling
5. 📷 **Facial recognition databases** from untargeted CCTV scraping
6. 😢 **Emotion recognition** in workplaces & educational institutions
7. 🔍 **Real-time remote biometric identification** in public spaces

<!--
  Diese Verbote gelten ausnahmslos und ab Februar 2025.
  Die EU sieht diese Praktiken als unvereinbar mit europäischen Grundwerten.
  Ausnahme bei Nr. 7: Strafverfolgung bei schweren Straftaten
  unter strengen richterlichen Auflagen.
-->

---

![bg left:20%](https://images.unsplash.com/photo-1590859808308-3d2d9c515b1a?w=800&auto=format&fit=crop)

# 🟠 High Risk — Heavily Regulated

## Chapter 3, Article 6

An AI system is **High Risk** when:

1. ✅ It involves **profiling of persons**
2. ✅ It is used in **critical infrastructure**
3. ✅ It does **NOT** perform a narrow procedural task

**All three conditions** contribute to the classification.

<!--
  Art. 6 definiert zwei Wege zur Hochrisiko-Einstufung:
  1. Sicherheitsbauteil eines bereits regulierten Produkts
  2. Fällt in einen der acht Bereiche aus Annex III
  Rein prozedurale Aufgaben sind ausgenommen.
-->

---

# High Risk — Domains (Annex III)

<style scoped>section { font-size: 21pt; }</style>

<div class="container">
<div class="col">

| # | Domain |
|:-:|:-------|
| 1 | 🧬 Biometrics & Emotions |
| 2 | ⚡ Critical Infrastructure |
| 3 | 🎓 Education & Training |
| 4 | 💼 Employment & Workforce Mgmt |

</div>
<div class="col">

| # | Domain |
|:-:|:-------|
| 5 | 🏛️ Essential Services |
| 6 | 👮 Law Enforcement |
| 7 | 🛂 Migration & Border Control |
| 8 | ⚖️ Justice & Democracy |

</div>
</div>

<!--
  Die acht Hochrisiko-Bereiche aus Anhang III.
  Beispiele: KI-gestützte Prüfungsbewertung (Bildung),
  automatisierte Bewerberauswahl (Beschäftigung),
  Gesichtserkennung durch Polizei (Strafverfolgung).
-->

---

![bg right:40%](https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=800&auto=format&fit=crop)

# 🟡 Limited Risk

## Transparency Obligations

**Applies to:**
- LLMs (Large Language Models)
- Ads generated with AI
- Deepfakes

<div class="highlight-box">

🔑 Users **must be informed** about their interaction with AI

</div>

<!--
  Kernpflicht: Transparenz statt Verbot.
  ChatGPT muss kenntlich machen, dass Antworten KI-generiert sind.
  Deepfakes müssen als synthetisch erzeugt gekennzeichnet werden.
  In Kraft ab August 2025.
-->

---

![bg left:35%](https://images.unsplash.com/photo-1614680376593-902f74cf0d41?w=800&auto=format&fit=crop)

# 🟢 Minimal Risk

## No Special Obligations

**Examples:**
- 🎮 Gaming AI
- 📧 Spam filters
- 🗣️ Text-to-Speech (TTS)
- 🎤 Speech-to-Text (STT)

** ✅ Permitted** — no restrictions

<!--
  Ca. 85% aller KI-Anwendungen fallen hierunter.
  Keine regulatorischen Anforderungen.
  EU ermutigt lediglich zu freiwilligen Verhaltenskodizes (Art. 95).
-->

---

<!-- _class: chapter -->
<!-- _paginate: false -->
<!-- _footer: "" -->

# 📋 Requirements for High-Risk Systems

## Chapter 3, Articles 8–17

<!--
  Konkrete Pflichten für Anbieter von Hochrisiko-KI-Systemen.
-->

---

# Six Core Requirements

<style scoped>section { font-size: 20pt; }</style>

![bg right:30%](https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=800&auto=format&fit=crop)

| # | Requirement |
|:-:|:------------|
| **01** | 👁️ **Human Oversight** — Humans must be able to intervene |
| **02** | ⚠️ **Risk Management** — Continuous risk assessment |
| **03** | 📊 **Data Governance** — Quality & representativeness |
| **04** | 📄 **Technical Documentation** + Instructions for use |
| **05** | 🎯 **Accuracy, Robustness & Cybersecurity** — by design |
| **06** | ✅ **Quality Management System** — established & maintained |

<!--
  Besonders hervorzuheben:
  - Human Oversight: "Human-in-the-loop" oder "Human-on-the-loop"
  - Daten-Governance: Trainingsdaten müssen repräsentativ und bias-frei sein
  - Technische Doku: Muss behördliche Prüfung ermöglichen
  Diese Anforderungen gelten über den gesamten Lebenszyklus.
-->

---
<!-- _paginate: false -->
<!-- _footer: "" -->

![bg right:20%](https://images.unsplash.com/photo-1684369175833-4b445ad6bfb5?w=800&auto=format&fit=crop)

# Who is Mostly Affected?

### Deployers of High-Risk AI

- Deployers have obligations, though **less than providers** (developers)
- Downstream users need **some documentation**

<div class="callout note">

### Important Note

**Users** in the AI Act = natural or legal persons deploying AI in a **professional capacity**, not affected end-users.

</div>

<!--
  Wichtige Unterscheidung: "User" ≠ Endverbraucher.
  Provider tragen die Hauptlast der Compliance.
  Deployer: System gemäß Gebrauchsanweisung einsetzen.
-->

---

![bg right:40%](https://images.unsplash.com/photo-1680783954745-3249be59e527?w=800&auto=format&fit=crop)

# 🏛️ The EU AI Office

- 📋 **Oversee** General-Purpose AI model compliance
- 🔍 **Investigate** systemic risks
- 📩 **Accept complaints** from downstream providers
- 🧪 **Conduct independent evaluations** when needed

<!--
  EU AI Office seit Februar 2024, Teil der EU-Kommission.
  Zentrale Durchsetzungsbehörde für General-Purpose AI (GPT-4, Gemini, Claude).
  Nationale Behörden überwachen sektorspezifische Hochrisiko-KI.
  Bußgelder: Bis 35 Mio. € oder 7% des weltweiten Jahresumsatzes.
-->

---

<!-- _class: chapter -->
<!-- _paginate: false -->
<!-- _footer: "" -->

# 📊 Summary

## Putting It All Together

---

# Risk Classification — At a Glance

<style scoped>section { font-size: 19pt; }</style>

<table>
  <thead>
    <tr>
      <th style="background:#C0392B; color:white; width:25%;">🔴 Unacceptable</th>
      <th style="background:#E67E22; color:white; width:25%;">🟠 High Risk</th>
      <th style="background:#0073CF; color:white; width:25%;">🟡 Limited Risk</th>
      <th style="background:#7AB800; color:white; width:25%;">🟢 Minimal Risk</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Manipulative AI, social scoring, predictive policing, mass surveillance</td>
      <td>Biometrics, critical infra, education, law enforcement, employment</td>
      <td>LLMs, AI-generated ads, deepfakes — user must be informed</td>
      <td>Gaming AI, spam filters, TTS, STT</td>
    </tr>
    <tr>
      <td><strong>❌ Prohibited (Art 5)</strong></td>
      <td><strong>⚠️ Regulated (Art 6)</strong></td>
      <td><strong>✅ Permitted</strong></td>
      <td><strong>✅ Permitted</strong></td>
    </tr>
  </tbody>
</table>

<!--
  Kernbotschaft: Der AI Act verbietet wenig, reguliert einiges,
  und lässt das meiste zu – setzt aber auf Transparenz.
-->

---

<!-- _class: discussion -->
<!-- _paginate: false -->
<!-- _paginate: false -->
<!-- _footer: "" -->


# 💬 Discussion

## What do you think?

### Geben wir unseren _Standortvorteil_ ab?

<!--
  Pro: Rechtssicherheit, "Brussels Effect", Vergleich DSGVO
  Contra: Innovationshemmend, US First-Mover-Advantage,
  Abwanderung von Talenten, China fördert KI massiv staatlich
-->

---

<!-- _class: end -->
<!-- _paginate: false -->
<!-- _footer: "" -->

# Thank You!

**Jan Vaorin**
adesso SE

EU AI Act Presentation 2026