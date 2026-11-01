<!-- MASTER-HEADER-START -->
<div align="center">

<a href="https://0xcyberlitech.com/">
  <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/headers/header-ia.svg" alt="ATELIER IA SOUVERAINE // LLM & GPU" width="100%" />
</a>

<p align="center">
  <a href="https://0xcyberlitech.com/"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-portal.svg" alt="Portail 0xCyberLiTech.com" width="24%" /></a>
  <a href="https://0xcyberlitech.com/soc-rd.html"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-soc-rd.svg" alt="Livre Blanc SOC Cockpit" width="24%" /></a>
  <a href="https://0xcyberlitech.com/jarvis-rd.html"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-jarvis-rd.svg" alt="Livre Blanc JARVIS IA" width="24%" /></a>
  <a href="https://github.com/0xCyberLiTech?tab=repositories"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-github.svg" alt="Catalogue des 23 Dépôts" width="24%" /></a>
</p>
<p align="center">
  <a href="README.md"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-back-readme.svg" alt="Retour au sommaire du dépôt" width="340" /></a>
</p>

<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/divider-hud.svg" alt="" width="100%" />
</div>
<!-- MASTER-HEADER-END -->

<!-- DEBIAN-TRUTH-START -->
> [!IMPORTANT]
> <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-shield.svg" width="18" height="18" align="absmiddle" alt="" /> ** Matrice Officielle Debian — `Debian 12 (Bookworm)` · `Debian 13 (Trixie)` · `Debian 14 (Forky)`**
> - **Sources Officielles Debian.org (`python3-defaults`) :** `Bookworm (12)` : **`3.11.2-1`** &nbsp;·&nbsp; `Trixie (13 — Stable)` : **`3.13.5-1`** &nbsp;·&nbsp; `Forky (14 — Next-Gen)` : **`3.14.7-3`**
> - **Références Officielles :** [Paquet Debian Trixie (`python3`)](https://packages.debian.org/trixie/python3) &nbsp;·&nbsp; [Paquet Debian Forky (`python3`)](https://packages.debian.org/forky/python3) &nbsp;·&nbsp; [Documentation Officielle Debian](https://wiki.debian.org/Python)
> - **Note d'Ingénierie (Divergence 13 vs 14) :** Depuis Debian 12/13 (Trixie) et renforcé sous Debian 14 (Forky), la norme **PEP 668** bloque `pip install` en global pour protéger APT : utilisez systématiquement `python3 -m venv` ou `pipx`.

<details>
<summary><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-doc.svg" width="18" height="18" align="absmiddle" alt="" /> <b>Afficher les Encarts Ligne de Commande : Debian 13 (Trixie — Stable) vs Debian 14 (Forky — Next-Gen)</b></summary>

#### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-ok.svg" width="42" height="16" align="absmiddle" alt="[OK]" /> Profil Production Stable — Commandes pour `Debian 13 (Trixie)`
```bash
# Debian 13 (Trixie — Python 3.13 & PEP 668) : Environnement virtuel obligatoire pour pip
sudo apt update && sudo apt install -y python3-venv python3-pip pipx
python3 -m venv .venv && source .venv/bin/activate
```

#### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-rd.svg" width="46" height="16" align="absmiddle" alt="[R&D]" /> Profil Anticipation Next-Gen — Commandes pour `Debian 14 (Forky)`
```bash
# Debian 14 (Forky — Python 3.13/3.14) : Isolation stricte PEP 668 & outils CLI via pipx
pipx install huggingface-hub
python3 -m venv --upgrade-deps .venv
```

</details>
<!-- DEBIAN-TRUTH-END -->

<!-- CIEL-PEDAGOGY-START -->
<details>
<summary><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-puzzle.svg" width="18" height="18" align="absmiddle" alt="" /> <b>Synthèse d'Architecture, Standards Officiels &amp; Diagnostic (Niveau 1 : Fondamentaux · Niveau 2 : Repères · Niveau 3 : Diagnostic)</b></summary>

- **Niveau 1 — Fondamentaux &amp; Principe d'Architecture :** L'architecture d'**Intelligence Artificielle Souveraine (LLM Local, RAG Vectoriel & Pipeline Vocal)** permet d'orchestrer des modèles de langage (`Qwen 3.5`, `Llama`, `Mistral` via `Ollama`) et une recherche documentaire vectorielle privée (`SQLite-vec` / `Qdrant`) intégralement sur serveur local (*On-Premise*), garantissant la confidentialité absolue des données.
- **Niveau 2 — Repères Officiels (Ports IANA, Fichiers Debian &amp; Commandes de Validation) :** **Ports & Composants standards :** `TCP 11434` (API Ollama `qwen3.5:9b` / `qwen3-embedding:4b`) · Extension native `SQLite-vec` (`vec0` L2/Cosine) · `TCP 6333` (Qdrant) &nbsp;|&nbsp; **Validation & Télémétrie :** `nvidia-smi`, `ollama ps`, `curl -s http://127.0.0.1:11434/api/tags`.
- **Niveau 3 — Diagnostic d'Incidents &amp; Ingénierie Avancée :** **Diagnostic & Architecture :** Contrairement au *Fine-Tuning* qui fige des connaissances dans les poids du modèle, l'architecture **RAG (*Retrieval-Augmented Generation*)** indexe la documentation technique sous forme de vecteurs (*Embeddings*) et injecte dynamiquement les extraits exacts dans le contexte du LLM avec une `temperature` basse (`0.1`), éliminant les hallucinations.
- **Sources de Vérité Officielles Éditeurs &amp; Standards :** [Documentation Officielle Ollama](https://github.com/ollama/ollama) &nbsp;·&nbsp; [Documentation Officielle SQLite-vec](https://alexgarcia.xyz/sqlite-vec/) &nbsp;·&nbsp; [Documentation Llama.cpp / GGML](https://github.com/ggml-org/llama.cpp)
- **Livres Blancs &amp; 67 Podcasts Audio R&amp;D :** [Portail 0xCyberLiTech](https://0xcyberlitech.com/) &nbsp;·&nbsp; [Livre Blanc SOC Cockpit v5.5](https://0xcyberlitech.com/soc-rd.html) &nbsp;·&nbsp; [Livre Blanc JARVIS Mark-VII](https://0xcyberlitech.com/jarvis-rd.html) &nbsp;·&nbsp; [Blueprint Logiciel &amp; Matériel RTX 5080](https://0xcyberlitech.com/blueprint-jarvis.html)

</details>
<!-- CIEL-PEDAGOGY-END -->


> Guide complet expliquant, étape par étape, le fonctionnement, l’installation et l’utilisation de solutions d’intelligence artificielle sur Debian 12 et Debian 13.

---

<div align="center" style="margin-bottom: 10px;">

### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-target.svg" width="18" height="18" align="absmiddle" alt="" /> **Sommaire**

<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-ok.svg" width="42" height="16" align="absmiddle" alt="[OK]" /> **Actif** – Dépôt totalement accessible 
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-rd.svg" width="46" height="16" align="absmiddle" alt="[R&D]" /> **Partiel** – Dépôt partiellement accessible 
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-ko.svg" width="42" height="16" align="absmiddle" alt="[NON]" /> **Inactif** – Dépôt inaccessible ou indisponible

</div>

---

<div align="center">
  
# <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-shield.svg" width="20" height="20" align="absmiddle" alt="" /> Carte mentale : Aperçu de l’Intelligence Artificielle

</div>

<!-- CODE-WINDOW-START -->
> [!CAUTION]
> <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-code-red.svg" width="100%" alt="TERMINAL // BLOC DE CODE" />
>
> ```bash
>                                           +------------------------------+
>                                           |   INTELLIGENCE ARTIFICIELLE  |
>                                           +------------------------------+
>                                                          |
>    -------------------------------------------------------------------------------------------------------------
>    |                |                 |                  |               |            |                        |
> Définitions      Domaines         Techniques          Concepts         Enjeux       Outils                   Futur
>    |           d'application      principales           clés           & défis    & langages              (Évolution)
>    |                |                 |                  |               |            |                        |
>    |                |                 |                  |               |            |                        |
> - Simulation     - Santé          - Machine          - Données       - Éthique    - Python             - IA générative
>   humaine        - Transports       Learning           d'entrai-     - Données    - R, TensorFlow,     - AGI
> - Automatisation - Finance        - Deep               nement        - Emploi       PyTorch...         - Collaboration
>   cognitive      - Service client   Learning         - Modèles       - Sécurité   - Cloud (AWS, GCP,     homme-machine
>                  - Sécurité       - NLP              - Prédiction    - Contrôle     Azure)
>                  - Industrie      - Vision           - IA forte/     - Impact      
>                  - Éducation        par ordinateur   faible            enviro     
>                  - Loisirs                           - Biais           nement
>
> ```
<!-- CODE-WINDOW-END -->

Légende :  
- Chaque branche principale est un grand thème de la carte mentale.
- Les sous-branches (–) montrent des exemples de chaque section.
- Adapte et ajoutes-y ce que tu veux approfondir.

<div align="center">
  
# <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-shield.svg" width="20" height="20" align="absmiddle" alt="" /> Détail carte mentale : Intelligence Artificielle (IA)

</div>

- **Intelligence Artificielle**
    - Définitions
        - Simulation de l’intelligence humaine par des machines
        - Automatisation de tâches cognitives
    - Domaines d’application
        - Santé (diagnostics, imagerie médicale)
        - Transports (voitures autonomes, logistique)
        - Finance (analyse prédictive, trading algorithmique)
        - Service client (chatbots, assistants virtuels)
        - Sécurité (détection de fraudes, cybersécurité)
        - Industrie (automatisation, robots industriels)
        - Éducation (tutoriels adaptatifs, corrections automatiques)
        - Loisirs (jeux vidéo, recommandations de contenu)
    - Techniques principales
        - **Apprentissage automatique (Machine Learning)**
            - Supervisé
            - Non supervisé
            - Apprentissage par renforcement
        - **Réseaux de neurones artificiels**
            - Profonds (Deep Learning)
            - Réseaux convolutifs (images)
            - Réseaux récurrents (suites, textes)
        - **Algorithmes d’optimisation**
        - **Traitement du langage naturel (NLP)**
        - **Vision par ordinateur**
    - Concepts clés
        - Données d’entraînement
        - Modèles
        - Prédiction et classification
        - Biais & éthique
        - IA faible vs IA forte
        - Explicabilité
    - Enjeux et défis
        - Éthique (biais, discrimination, transparence)
        - Protection des données (RGPD, vie privée)
        - Automatisation & emploi
        - Contrôle, sécurité, usage militaire
        - Impact environnemental (consommation des datacenters)
    - Outils & langages
        - Python, R
        - Librairies : TensorFlow, PyTorch, Scikit-learn, Keras
        - Plateformes cloud : AWS, Google Cloud, Azure
    - Evolution et futur
        - IA générative (textes, images, vidéos)
        - Intelligence artificielle générale (AGI)
        - Collaboration homme-machine
---
> **En résumé** : L’IA doit rester un outil au service de l’humain, respectueux de la loi, éthique et transparent. Apprendre l’IA, c’est aussi apprendre à construire un futur technologique plus juste et plus sûr.
<!-- MASTER-FOOTER-START -->
<div align="center">
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/divider-hud.svg" alt="" width="100%" />

<a href="https://0xcyberlitech.com/">
  <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/footer-master.svg" alt="0xCyberLiTech — Architecture Cyberdéfense, Ingénierie Déterministe & IA Souveraine" width="100%" />
</a>

<p align="center"><a href="https://0xcyberlitech.com/"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/badge-antigravity.svg" alt="Architecturé par Marc & Antigravity (Google DeepMind)" width="520" /></a></p>

<sub><b>Architecturé &amp; Forgé par Marc &amp; Antigravity (Google DeepMind)</b> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/"><b>0xcyberlitech.com</b></a> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/soc-rd.html">Architecture SOC Cockpit v5.5</a> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/jarvis-rd.html">Architecture JARVIS Mark-VII</a> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/blueprint-jarvis.html">Blueprint Matériel RTX 5080</a></sub>

</div>
<!-- MASTER-FOOTER-END -->
