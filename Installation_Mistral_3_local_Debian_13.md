<div align="center">

  <br></br>
  
  <a href="https://github.com/0xCyberLiTech">
    <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&size=50&duration=6000&pause=1000000000&color=FF0048&center=true&vCenter=true&width=1100&lines=%3EL'IA_" alt="Titre dynamique OPENVAS" />
  </a>
  
  <br></br>
  
  <h2>Laboratoire numérique pour la cybersécurité, Linux & IT.</h2>

  <p align="center">
    <a href="https://0xcyberlitech.github.io/">
      <img src="https://img.shields.io/badge/Portfolio-0xCyberLiTech-181717?logo=github&style=flat-square" alt="🌐 Portfolio" />
    </a>
    <a href="https://github.com/0xCyberLiTech">
      <img src="https://img.shields.io/badge/Profil-GitHub-181717?logo=github&style=flat-square" alt="🔗 Profil GitHub" />
    </a>
    <a href="https://github.com/0xCyberLiTech/OpenVAS/releases/latest">
      <img src="https://img.shields.io/github/v/release/0xCyberLiTech/OpenVAS?label=version&style=flat-square&color=blue" alt="📦 Dernière version" />
    </a>
    <a href="https://github.com/0xCyberLiTech/OpenVAS/blob/main/CHANGELOG.md">
      <img src="https://img.shields.io/badge/📄%20Changelog-OpenVAS-blue?style=flat-square" alt="📄 CHANGELOG OpenVAS" />
    </a>
    <a href="https://github.com/0xCyberLiTech?tab=repositories">
      <img src="https://img.shields.io/badge/Dépôts-publics-blue?style=flat-square" alt="📂 Dépôts publics" />
    </a>
    <a href="https://github.com/0xCyberLiTech/OpenVAS/graphs/contributors">
      <img src="https://img.shields.io/badge/👥%20Contributeurs-cliquez%20ici-007ec6?style=flat-square" alt="👥 Contributeurs OpenVAS" />
    </a>
  </p>

</div>

<div align="center">
  <img src="https://img.icons8.com/fluency/96/000000/cyber-security.png" alt="CyberSec" width="80"/>
</div>

<div align="center">
  <p>
    <strong>Cybersécurité</strong> <img src="https://img.icons8.com/color/24/000000/lock--v1.png"/> • <strong>Linux Debian</strong> <img src="https://img.icons8.com/color/24/000000/linux.png"/> • <strong>Sécurité informatique</strong> <img src="https://img.icons8.com/color/24/000000/shield-security.png"/>
  </p>
</div>

---

<div align="center">
  
## À propos & Objectifs.

</div>

Ce projet propose des solutions innovantes et accessibles en cybersécurité, avec une approche centrée sur la simplicité d’utilisation et l’efficacité. Il vise à accompagner les utilisateurs dans la protection de leurs données et systèmes, tout en favorisant l’apprentissage et le partage des connaissances.

Le contenu est structuré, accessible et optimisé SEO pour répondre aux besoins de :
- 🎓 Étudiants : approfondir les connaissances
- 👨‍💻 Professionnels IT : outils et pratiques
- 🖥️ Administrateurs système : sécuriser l’infrastructure
- 🛡️ Experts cybersécurité : ressources techniques
- 🚀 Passionnés du numérique : explorer les bonnes pratiques

---

> Guide complet expliquant, étape par étape, le fonctionnement, l’installation et l’utilisation de solutions d’intelligence artificielle sur Debian 12 et Debian 13.

---

<div align="center" style="margin-bottom: 10px;">

### **Sommaire**

🟢 **Actif** – Dépôt totalement accessible  
🟠 **Partiel** – Dépôt partiellement accessible  
🔴 **Inactif** – Dépôt inaccessible ou indisponible

</div>

---
## 🚀 Installation de Mistral 3 en local sous Debian 13

Mistral 3 est un modèle de langage avancé, open source, optimisé pour l’exécution locale sur une machine Linux. Ce guide explique comment installer et commencer à utiliser Mistral 3 sur Debian 13, étape par étape.

---

### 🧩 Prérequis

- Système d’exploitation : **Debian 13** (à jour)
- Un utilisateur avec les droits `sudo`
- **Python 3.9+** (ou version recommandée)
- **Git** installé
- Accès à Internet et suffisamment d’espace disque (plusieurs Go selon la taille du modèle)

---

### 1️⃣ Mise à jour du système et installation des dépendances

```bash
sudo apt update && sudo apt upgrade
sudo apt install python3 python3-venv python3-pip git
```

---

### 2️⃣ 📦 Création d’un environnement Python isolé

```bash
python3 -m venv mistral3-env
source mistral3-env/bin/activate
```

---

### 3️⃣ 🔽 Installation du serveur et du modèle Mistral 3

#### Option 1 : Utiliser `llama-cpp-python` (recommandé pour local)

> La méthode la plus simple pour utiliser Mistral 3 consiste à passer par llama-cpp-python 
compatible avec les modèles Mistral au format GGUF.

1. **Installer llama-cpp-python :**

```bash
pip install --upgrade pip
pip install llama-cpp-python
```

2. **Télécharger le modèle Mistral-3 au format GGUF :**

- Rendez-vous sur [HuggingFace - mistralai/Mistral-7B-Instruct-v0.3-GGUF](https://huggingface.co/mistralai)
- Téléchargez un modèle GGUF (exemple : `mistral-7b-instruct-v0.3.Q4_K_M.gguf`) dans un dossier.

3. **Lancer un prompt avec le modèle local :**

```bash
python3 -m llama_cpp.server \
  --model ./chemin/vers/modele/mistral-7b-instruct-v0.3.Q4_K_M.gguf \
  --host 127.0.0.1 --port 8000
```

- Le serveur REST sera accessible sur `http://127.0.0.1:8000/v1/chat/completions`

---

#### Option 2 : Utiliser [LM Studio](https://lmstudio.ai/) (interface graphique multiplateforme)

- Télécharge LM Studio (AppImage ou .deb) depuis le site officiel.
- Utilise LM Studio pour importer le modèle Mistral 3.
- Démarre le modèle en local via l’interface.

---

### 4️⃣ 🖲️ Tester le modèle

Avec llama-cpp-python :
```python
from llama_cpp import Llama

llm = Llama(model_path="chemin/vers/le-modele/mistral-7b-instruct-v0.3.Q4_K_M.gguf")
result = llm.create_completion("Explique le machine learning en une phrase.")
print(result)
```

---

### 🛠️ Dépannage

- **Erreur “out of memory” :** essaye une version du modèle en quantification plus légère (Q4, Q5…).
- **Pas d’AVX2 sur l’ordinateur :** prends un binaire compilé sans instructions AVX2 ou utilise des versions plus légères.
- **Pour GPU Nvidia :** consulte la doc`llama-cpp-python` pour installer avec CUDA.

---

### 🔗 Ressources utiles

- [Mistral AI - Site officiel](https://mistral.ai/)
- [HuggingFace - Page des modèles Mistral-3](https://huggingface.co/models?search=mistral)
- [Documentation llama-cpp-python](https://github.com/abetlen/llama-cpp-python)
- [LM Studio - Interface locale](https://lmstudio.ai/)

---
## 🎯 Télécharger Mistral 3 – Liens & Versions

### 📥 Lien direct pour récupérer un modèle Mistral 3

Les modèles Mistral sont disponibles publiquement sur HuggingFace.  
Voici un lien exploitable pour Mistral 3 (formats .gguf, adapté à une utilisation locale) :

- **Page officielle HuggingFace des modèles Mistral 3 (GGUF) :**  
  👉 [TheBloke/Mistral sur HuggingFace](https://huggingface.co/mistralai/)

*Astuce : Tu peux remplacer le nom du fichier pour choisir une autre version/quantification si besoin. Le téléchargement peut se faire en cliquant ou via `wget` :*
```bash
wget "https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.3-GGUF/resolve/main/mistral-7b-instruct-v0.3.Q4_K_M.gguf"
```

---

### 🧩 Quelle version choisir ?  
Les modèles publiés en GGUF proposent plusieurs **versions selon la "quantification"** :

| Version GGUF                    | RAM requise (approx.) | Vitesse        | Qualité         | Usage conseillé                   |
|----------------------------------|----------------------|----------------|-----------------|-----------------------------------|
| **Q2_K**                        | Faible               | Très rapide    | Qualité basse   | Démo, anciens PC                  |
| **Q4_K_M** _(recommandé)_        | Moyenne (~5-6 Go)    | Rapide         | Bonne           | Usage quotidien                   |
| **Q5_K_M**                      | Moyenne à élevée     | Moins rapide   | Très bonne      | Précision accrue                  |
| **Q6_K, F16** _(float 16 bits)_ | Haute (>16 Go RAM)   | Plus lent      | Optimale        | Pour la meilleure qualité, gros PC/GPU|

**Résumé**  
- Version **Q4_K_M** : Bon compromis entre taille mémoire, rapidité et performance – idéale pour PC personnels et serveurs modestes.
- Version **Q5, Q6, F16** : Plus gourmandes en RAM, mais meilleure fidélité de génération de texte (proche du modèle d’origine).
- **Plus le chiffre est bas, plus le modèle est léger, mais la génération de texte est moins précise.**

---

### 🔎 Aller plus loin

- Parcours toutes les versions et tailles sur la page du modèle :  
  👉 [Liste des fichiers sur HuggingFace](https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.3-GGUF/tree/main)
- Vérifie si ton ordinateur dispose de la mémoire RAM suffisante en fonction de la version choisie.

---

> **Astuce** : Il est possible d’utiliser plusieurs versions selon ton besoin : rapide pour le test, plus lourde pour la production ou la recherche de qualité optimale.

> L’installation est rapide et te permet d’expérimenter localement tout le potentiel du modèle Mistral 3 sur Debian 13 !

---

<div align="center">
  <a href="https://github.com/0xCyberLiTech" target="_blank" rel="noopener">
    <img src="https://skillicons.dev/icons?i=linux,debian,bash,docker,nginx,git,vim,python,markdown" alt="Skills" width="440">
  </a>
</div>

<div align="center">
  <b>🔒 Un guide proposé par <a href="https://github.com/0xCyberLiTech">0xCyberLiTech</a> • Pour des tutoriels accessibles à tous. 🔒</b>
</div>



