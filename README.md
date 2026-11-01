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
> [!TIP]
> <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-target.svg" width="18" height="18" align="absmiddle" alt="" /> **Guide de Lecture &amp; Progression par Niveau (IA)**
> - **Rôle de la brique :** L'architecture d'**Intelligence Artificielle Souveraine (LLM Local, RAG Vectoriel & Pipeline Vocal)** permet d'orchestrer des modèles de langage (`Qwen 3.5`, `Llama`, `Mistral` via `Ollama`) et une recherche documentaire vectorielle privée (`SQLite-vec` / `Qdrant`) intégralement sur serveur local (*On-Premise*), garantissant la confidentialité absolue des données.
> - **Parcours recommandé :** **Niveau 1 (Fondamentaux &amp; Installation initiale)** pour déployer une base saine &rarr; **Niveau 2 (Configuration &amp; Intégration)** &rarr; **Niveau 3 (Haute Disponibilité, Durcissement &amp; Exploitation)**.

<details>
<summary><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-puzzle.svg" width="18" height="18" align="absmiddle" alt="" /> <b>Synthèse d'Architecture, Standards Officiels &amp; Diagnostic (Niveau 1 : Fondamentaux · Niveau 2 : Repères · Niveau 3 : Diagnostic)</b></summary>

- **Niveau 1 — Fondamentaux &amp; Principe d'Architecture :** L'architecture d'**Intelligence Artificielle Souveraine (LLM Local, RAG Vectoriel & Pipeline Vocal)** permet d'orchestrer des modèles de langage (`Qwen 3.5`, `Llama`, `Mistral` via `Ollama`) et une recherche documentaire vectorielle privée (`SQLite-vec` / `Qdrant`) intégralement sur serveur local (*On-Premise*), garantissant la confidentialité absolue des données.
- **Niveau 2 — Repères Officiels (Ports IANA, Fichiers Debian &amp; Commandes de Validation) :** **Ports & Composants standards :** `TCP 11434` (API Ollama `qwen3.5:9b` / `qwen3-embedding:4b`) · Extension native `SQLite-vec` (`vec0` L2/Cosine) · `TCP 6333` (Qdrant) &nbsp;|&nbsp; **Validation & Télémétrie :** `nvidia-smi`, `ollama ps`, `curl -s http://127.0.0.1:11434/api/tags`.
- **Niveau 3 — Diagnostic d'Incidents &amp; Ingénierie Avancée :** **Diagnostic & Architecture :** Contrairement au *Fine-Tuning* qui fige des connaissances dans les poids du modèle, l'architecture **RAG (*Retrieval-Augmented Generation*)** indexe la documentation technique sous forme de vecteurs (*Embeddings*) et injecte dynamiquement les extraits exacts dans le contexte du LLM avec une `temperature` basse (`0.1`), éliminant les hallucinations.
- **Sources de Vérité Officielles Éditeurs &amp; Standards :** [Documentation Officielle Ollama](https://github.com/ollama/ollama) &nbsp;·&nbsp; [Documentation Officielle SQLite-vec](https://alexgarcia.xyz/sqlite-vec/) &nbsp;·&nbsp; [Documentation Llama.cpp / GGML](https://github.com/ggml-org/llama.cpp)
- **Livres Blancs &amp; 67 Podcasts Audio R&amp;D :** [Portail 0xCyberLiTech](https://0xcyberlitech.com/) &nbsp;·&nbsp; [Livre Blanc SOC Cockpit v5.5](https://0xcyberlitech.com/soc-rd.html) &nbsp;·&nbsp; [Livre Blanc JARVIS Mark-VII](https://0xcyberlitech.com/jarvis-rd.html) &nbsp;·&nbsp; [Blueprint Logiciel &amp; Matériel RTX 5080](https://0xcyberlitech.com/blueprint-jarvis.html)

</details>
<!-- CIEL-PEDAGOGY-END -->


## <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-plan.svg" width="18" height="18" align="absmiddle" alt="" /> 01 // SOMMAIRE DES DOSSIERS TECHNIQUES — ATELIER IA SOUVERAINE // LLM & GPU
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-section-cyan.svg" width="100%" alt="" />

<div align="center" style="margin-bottom: 10px;">

### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-target.svg" width="18" height="18" align="absmiddle" alt="" /> **Sommaire**

<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-ok.svg" width="42" height="16" align="absmiddle" alt="[OK]" /> **Actif** – Dépôt totalement accessible 
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-rd.svg" width="46" height="16" align="absmiddle" alt="[R&D]" /> **Partiel** – Dépôt partiellement accessible 
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-ko.svg" width="42" height="16" align="absmiddle" alt="[NON]" /> **Inactif** – Dépôt inaccessible ou indisponible

</div>

---

<div align="center">

| **Ressource**                                   | **Description**                                            | **Niveau**       | **Accès rapide**                                                                                                                              |
|-------------------------------------------------|------------------------------------------------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **Introduction à l’IA**                         | Concepts, enjeux et historique de l’IA | Débutant         | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/IA/blob/main/Introduction_IA.md) |
| **Types d’IA**                                  | Symbolique, connexionniste, hybride, forte/faible           | Débutant         | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/IA/blob/main/Types_IA.md) |
| **Architectures matérielles IA**                 | CPU, NPU, GPU : rôles, schéma et spécificités              | Tous publics     | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/IA/blob/main/Architecture_CPU_IA.md) |
| **Machine Learning et Deep Learning**            | Méthodes, usages, illustrations, exemples                   | Intermédiaire    | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](Machine_Learning,_et_Deep_Learning.md) |
| **Éthique et limites de l’IA**                   | RGPD et éthique IA     | Tous publics     | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](Éthique_limites_de_l_IA.md) |
| **Carte mentale synthétique IA**                 | Vue schématique et branches majeures de l’IA| Tous publics     | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/IA/blob/main/Carte_mental_IA.md) |
| **Logigramme du raisonnement IA**                | Logigramme et post-traitement IA     | Tous publics     | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/IA/blob/main/Post_traitement_logigramme.md) |
| **Cybersécurité et IA**                          | Renforcement de la sécurité par IA | Avancé           | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/IA/blob/main/Cybersecurite_ia.md) |
| **Déploiement IA Mistral 3 (Debian 12/13/14)**   | Déploiement en local        | Avancé           | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](Installation_Mistral_3_local_Debian_13.md) |
| **L'IA et Calcul Quantique** | L'IA et Calcul Quantique        | Avancé           | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/IA/blob/main/IA_calcul_quantique.md) |
| **Architecture IA Souveraine (LLM + RAG + Audio)** | Déploiement On-Premise : LLM Local, RAG Vectoriel Qdrant & Pipeline Vocal sur Debian 12, 13 & 14 | Avancé | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](IA-ASSISTANT-VOCAL-RAG-LOCAL-DEBIAN-13-14.md) |

</div>

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
