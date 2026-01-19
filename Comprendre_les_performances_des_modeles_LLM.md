## Comprendre les performances des modèles LLM

Avant de commencer l'installation d'un modèle de langage (LLM) en local, il est essentiel de comprendre que les performances dépendront fortement de votre matériel et du modèle choisi.

> **À retenir :**
> Vous n'obtiendrez pas exactement les mêmes performances que ChatGPT ou Claude sur une machine standard.

## À propos de ce document

Ce support est conçu pour un environnement Windows (Windows 10/11 et versions serveur récentes). Il a été structuré pour servir de cours pratique et de guide de mise en application : objectifs pédagogiques, circuit d'installation recommandé, exercices pratiques et vérifications pas à pas.

**Objectifs pédagogiques :**
- Comprendre les contraintes matérielles des LLM.
- Installer et configurer Ollama et Open WebUI sur Windows.
- Préparer et optimiser un poste pour l'exécution locale de modèles (GPU/CUDA).
- Savoir gérer les modèles et utiliser RAG (ChromeDB) pour l'analyse de documents.

---

## Sommaire

- **Comprendre les performances des modèles LLM**
- **Qu'est-ce qu'un "B" ?**
- **Tableau comparatif des tailles de modèles**
- **Configuration matérielle recommandée**
- **Conseils pour les petites configurations**
- **Installation d'Ollama sur Windows**
- **Installation d'Open WebUI sous Windows**
- **Exploiter les modèles avec Ollama**
- **Gestion des modèles**
- **Génération de code avec Ollama**
- **Schémas pédagogiques (ASCII)**
- **Conseils pratiques et maintenance**

## Guide par phases (résumé)

Ce guide résume chaque phase avec une action claire à exécuter.

1. Phase 1 — Préparation : vérifier CPU/RAM/stockage et installer `WinGet`/Miniconda si nécessaire.
2. Phase 2 — Installer Ollama : utiliser `winget install ollama.ollama` puis vérifier avec `ollama --version`.
3. Phase 3 — Installer Open WebUI : installer Miniconda puis exécuter `OpenWebUIInstaller.exe`.
4. Phase 4 — Démarrage et accès : lancer Open WebUI et créer le compte admin à `http://localhost:8080/auth`.
5. Phase 5 — Télécharger/Exécuter modèles : `ollama pull [modèle]` ou `ollama run [modèle]`.
6. Phase 6 — Gestion des modèles et UI : liste, suppression, ajout via l'interface ou `ollama list` / `ollama rm`.
7. Phase 7 — Usage avancé : génération de code et RAG/ChromeDB pour l'analyse de documents.
8. Phase 8 — Maintenance : mises à jour régulières, redémarrage des services et gestion de la mémoire.

## Checklist actionnable par phase

Phase 1 — Préparation
- Action : Vérifier RAM, disque et GPU.
  - Commandes/contrôles : Ouvrir `Gestionnaire des tâches` (Ctrl+Shift+Esc) pour RAM/CPU ; vérifier espace SSD via l'Explorateur.
  - Critère : >= 20 Go libre, RAM conforme aux modèles ciblés.

Phase 2 — Installer Ollama
- Action : Installer via WinGet.
  - Commande : `winget install ollama.ollama`
  - Vérifier : `ollama --version` doit afficher un numéro.
  - Critère : exécutable présent et accessible depuis la console.

Phase 3 — Installer Open WebUI
- Action : Installer Miniconda puis OpenWebUIInstaller.
  - Commandes :
    - `winget install anaconda.miniconda3`
    - exécuter `OpenWebUIInstaller.exe` téléchargé depuis le dépôt GitHub
  - Vérifier : navigateur ouvert sur `http://localhost:8080/auth` et création du compte admin.
  - Critère : page d'authentification accessible.

Phase 4 — Démarrage et configuration initiale
- Action : Lancer Open WebUI et configurer l'admin.
  - Vérifier : connexion réussie, modèles listés dans le sélecteur.
  - Critère : pouvoir sélectionner un modèle et lancer une requête test.

Phase 5 — Télécharger / Exécuter modèles
- Action : Télécharger puis exécuter un modèle test.
  - Commandes :
    - `ollama pull deepseek-r1`
    - `ollama run deepseek-r1`
  - Vérifier : le modèle démarre et répond aux prompts ; quitter avec `/bye`.
  - Critère : temps de réponse acceptable (< 10s pour prompts simples sur config recommandée).

Phase 6 — Gestion des modèles
- Action : Lister, supprimer ou ajouter des modèles.
  - Commandes : `ollama list`, `ollama rm [nom-du-modèle]`, ajout via Open WebUI si souhaité.
  - Critère : les actions modifient la liste comme attendu.

Phase 7 — Usage avancé (RAG, analyse de code)
- Action : Indexer un document et exécuter une requête RAG.
  - Vérifier : le document est indexé (Open WebUI / ChromeDB) et les réponses citent des extraits.
  - Critère : réponses contenant références aux passages du document.

Phase 8 — Maintenance et mises à jour
- Action : Mettre à jour les outils et nettoyer les modèles inutilisés.
  - Commandes : `winget upgrade`, vérifier versions `ollama --version`, supprimer modèles obsolètes.
  - Critère : système à jour et espace disque libéré.

## Circuit d'installation recommandé (ordre logique)

1) Préparation

- Vérifier l'espace disque, la RAM et la présence d'un GPU.
- Mettre à jour Windows et `winget`.

2) Installer les prérequis

- Installer `Miniconda` (pour Open WebUI) : `winget install anaconda.miniconda3`.
- Installer/mettre à jour `WinGet` si nécessaire.

3) Installer Ollama

- `winget install ollama.ollama`
- Vérifier : `ollama --version`

4) Télécharger des modèles (optionnel avant UI)

- Pour gagner du temps, téléchargez les modèles souhaités : `ollama pull [modèle]`.

5) Installer Open WebUI

- Exécuter `OpenWebUIInstaller.exe` (fourni par le dépôt GitHub).
- Lancer Open WebUI et créer le compte admin.

6) Tester la communication

- Dans Open WebUI, vérifier que les modèles listés par `ollama list` apparaissent.
- Exécuter une requête test depuis l'UI.

7) Optimiser et maintenir

- Ajuster modèles selon ressources, nettoyer les modèles inutiles, planifier mises à jour.

## Définitions pédagogiques (modules et composants)

### Ollama

Ollama est un gestionnaire et runtime local pour modèles LLM. Il fournit des commandes simples (`ollama run`, `ollama pull`, `ollama list`) pour télécharger, exécuter et gérer des modèles sur votre machine. Ollama sert d'interface entre l'exécutable du modèle et les clients (console ou UI).

Usage clé : exécuter des modèles localement sans configuration complexe d'infrastructure.

### Open WebUI

Open WebUI est une interface web locale qui facilite l'utilisation des LLM (sélecteur de modèles, rendu Markdown, historique, outils d'analyse). Il se connecte à des backends locaux (comme Ollama) pour exécuter les modèles et offre une expérience plus riche que la console.

Usage clé : interaction conviviale, visualisation propre du code et gestion des conversations.

### Miniconda / Conda

Miniconda est un gestionnaire d'environnements Python léger. Il permet d'isoler les dépendances d'Open WebUI, d'installer Python et les paquets nécessaires sans polluer l'installation système.

Usage clé : créer un environnement Python dédié pour Open WebUI et ses dépendances.

### WinGet

WinGet est le gestionnaire de paquets natif de Windows (Windows Package Manager). Il simplifie l'installation d'applications (ex. Ollama, Miniconda) via des commandes uniques.

Usage clé : automatiser l'installation d'outils sur Windows.

### Docker Desktop (option)

Docker Desktop permet d'exécuter Open WebUI dans un conteneur isolé. C'est utile si vous préférez éviter l'installation locale de Python ou souhaitez déployer des configurations reproductibles.

Usage clé : isolation, portabilité et déploiement reproductible.

### ChromeDB / RAG

ChromeDB (ou autres indexeurs) fournit des capacités RAG (Retrieval-Augmented Generation). Il indexe des documents locaux pour que le modèle puisse rechercher des informations précises avant de générer une réponse.

Usage clé : améliorer les réponses en les ancrant sur des documents locaux (contrats, manuels, etc.).

## Qu'est-ce qu'un "B" ?

Les modèles LLM sont mesurés en **"B" (milliards de paramètres)**. Un paramètre est une valeur numérique qui influence la façon dont le modèle génère du texte. Plus il y a de paramètres, plus le modèle est puissant, mais aussi plus il est gourmand en ressources.

## Tableau comparatif des tailles de modèles

| Taille      | Paramètres         | Espace disque requis | Ressources recommandées                | Capacités                                      |
|-------------|-------------------|----------------------|----------------------------------------|------------------------------------------------|
| 1-3B        | 1-3 milliards     | 1-2 Go               | CPU récent ou GPU basique, 8 Go RAM    | Tâches simples, réponses basiques              |
| 4-7B        | 4-7 milliards     | 3-5 Go               | GPU 6+ Go VRAM, 16 Go RAM              | Tâches intermédiaires, raisonnement simple     |
| 8-13B       | 8-13 milliards    | 6-8 Go               | GPU 8+ Go VRAM, 24 Go RAM              | Raisonnement avancé, codage complexe           |
| 14-30B      | 14-30 milliards   | 9-15 Go              | GPU 12+ Go VRAM, 32+ Go RAM            | Performance proche des modèles commerciaux      |

## Configuration matérielle recommandée

Pour une expérience fluide, il est conseillé d'avoir au minimum :

- **CPU** : Intel Core i7 / AMD Ryzen 7 (10e génération ou plus récent)
- **RAM** : 16 Go minimum (32 Go recommandés pour les modèles 8B+)
- **GPU** : NVIDIA RTX 3060 (6 Go VRAM) ou équivalent pour les modèles jusqu'à 7B
- **Stockage** : SSD avec au moins 20 Go d'espace libre

## GPU NVIDIA et NVIDIA CUDA — installation et vérification

Pour tirer profit d'un GPU NVIDIA lors de l'exécution de modèles LLM (accélération), il est recommandé d'installer les drivers NVIDIA, le CUDA Toolkit et cuDNN. Cette section explique les étapes essentielles sous Windows.

### Pourquoi installer CUDA ?

CUDA est la plateforme d'accélération GPU de NVIDIA. Beaucoup de runtimes et bibliothèques (TensorRT, PyTorch, TensorFlow) reposent sur CUDA pour exécuter des opérations sur GPU. Sans CUDA et drivers compatibles, le GPU ne sera pas exploité.

### Prérequis

- Un GPU NVIDIA compatible (GeForce RTX/GTX séries récentes, Quadro, Tesla).
- Espace disque (au moins 10 Go pour CUDA+cuDNN selon versions).
- Compte NVIDIA Developer (pour télécharger cuDNN).

### Étapes d'installation (résumé)

1. Installer le driver NVIDIA le plus récent compatible avec votre GPU.
2. Installer le CUDA Toolkit (choisir la version compatible avec vos frameworks).
3. Installer cuDNN (version compatible avec le CUDA Toolkit choisi).
4. Mettre à jour les variables d'environnement (PATH) si nécessaire.
5. Redémarrer la machine si l'installateur le demande.

### Vérifications (PowerShell)

```powershell
nvidia-smi
nvcc --version
```

### Notes et compatibilités

- Choisissez une version CUDA compatible avec le runtime que vous utiliserez.
- Sur Windows, cuDNN nécessite un compte NVIDIA Developer pour le téléchargement.
- Les drivers NVIDIA contiennent souvent la version minimale de CUDA supportée ; installez le driver avant CUDA.

### Exercice pratique (cours)

1. Installez le driver NVIDIA et exécutez `nvidia-smi`.
2. Installez CUDA Toolkit v11.8 (ou la version recommandée pour votre runtime) et vérifiez `nvcc --version`.
3. Téléchargez et installez cuDNN compatible, puis lancez une inférence simple via le framework de votre choix pour confirmer l'accélération GPU.

> **Exemple réel :**
>
> Sur un système équipé d'un Intel Core Ultra 9 185H avec 32 Go de RAM, le modèle DeepSeek R1 14B consomme environ 10 Go de RAM et utilise près de 60% des ressources CPU. Les temps de réponse restent acceptables (quelques secondes), mais varient selon la complexité des requêtes.

## Conseils pour les petites configurations

Si vous ne disposez pas de GPU dédié, privilégiez les modèles plus légers comme **Gemma3 2B** ou **DeepSeek R1 7B** pour des performances acceptables.

## Installation d'Ollama sur Windows

### Méthodes d'installation

- Via le paquet d'installation disponible sur le site officiel.
- Via `WinGet` (méthode recommandée si disponible).

### Commande recommandée

```powershell
winget install ollama.ollama
```

### Vérification

```powershell
ollama --version
```

## Installation d'Open WebUI sous Windows

### Installation avec Miniconda 3

1. `winget install anaconda.miniconda3`
2. Téléchargez `OpenWebUIInstaller.exe` depuis le dépôt officiel.
3. Exécutez l'installeur et suivez les instructions.

### Premiers pas

Ouvrez `http://localhost:8080/auth`, créez un admin et testez la connexion aux modèles locaux.

## Exploiter les modèles avec Ollama

### Télécharger et exécuter un modèle

- `ollama pull [modèle]`
- `ollama run [modèle]`

Pour quitter une session : `/bye`

## Gestion des modèles

- `ollama list`
- `ollama rm [nom-du-modèle]`

## Génération de code avec Ollama

Les modèles locaux peuvent générer du code. Pour une meilleure lisibilité, utilisez Open WebUI.

## Schémas pédagogiques (flux et composants) — ASCII

### A — Flux d'installation et d'utilisation

```
+----------------------+    +----------------------+    +--------------------+
| Utilisateur Windows  | -> | WinGet / Installeur  | -> |  Ollama installé   |
+----------------------+    +----------------------+    +--------------------+
                                                                                                            |
                                                                                                            v
                                                                             +-----------------------------+
                                                                             |  ollama run <modèle>        |
                                                                             +-----------------------------+
                                                                                                            |
                                                                                                            v
                                       +--------------------+    +----------------------------+
                                       |  Modèle local      | -> | Console / Open WebUI (UI)  |
                                       +--------------------+    +----------------------------+
```

### B — Séquence simplifiée d'exécution (interaction)

```
User -> Ollama: lance `ollama run <model>`
Ollama -> Model: charge et initialise
User -> Model: envoie le prompt
Model -> User: retourne la réponse
```

### C — Diagramme composants (vue générale)

```
+-------------------+     +------------------+     +------------------+
|  Ollama Service   |<--->|  Modèles locaux  |<--->| Stockage (disk)  |
+-------------------+     +------------------+     +------------------+
                ^  |
                |  v
        +-----------------+
        | Console / UI    |
        | (PowerShell /   |
        |  Open WebUI)    |
        +-----------------+
```

## Conseils pratiques

- Préférez des modèles 1–7B sur des machines sans GPU dédié.
- Sur des stations avec 16–32 Go RAM et GPU 8+ Go VRAM, testez 8–14B en ajustant la charge.
- Utilisez Open WebUI pour une meilleure lecture du Markdown et pour copier-coller du code proprement.

## Maintenance

- Mettre à jour régulièrement `Ollama` et `Open WebUI`.
- Redémarrer le service `Ollama` si des lenteurs apparaissent.
