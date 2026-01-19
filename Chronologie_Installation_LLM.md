# Chronologie — Installation et mise en œuvre d'un LLM local (Windows)

Ce document fournit une chronologie pas-à-pas (durées estimées et checklist) pour un déploiement local de LLM sous Windows en utilisant Ollama et Open WebUI.

Important : les durées sont indicatives et dépendent du matériel et de la connexion Internet.

## Vue d'ensemble (temps total estimé)
- Préparation et vérifications : 30–60 minutes
- Installation des prérequis : 20–60 minutes
- Installation d'Ollama : 5–15 minutes
- Téléchargement d'un modèle (selon taille) : 5 minutes → plusieurs heures
- Installation Open WebUI : 10–30 minutes
- Tests et optimisation initiale : 30–90 minutes

Temps total réaliste : 1h à plusieurs heures (majoritairement dépendant du téléchargement des modèles).

## Chronologie détaillée (séquence parfaite)

Jour 0 — Préparation (30–60 minutes)
- Vérifier Windows Update et redémarrer si nécessaire.
- Ouvrir `Gestionnaire des tâches` pour vérifier RAM/CPU.
- Vérifier espace disque (SSD) : viser >= 20 Go libres.
- Vérifier présence GPU NVIDIA (si disponible) : `nvidia-smi`.

Jour 0 — Installer outils de base (20–60 minutes)
- Installer/mettre à jour `WinGet` (si nécessaire).
- Installer Miniconda : `winget install anaconda.miniconda3`.
- Installer Ollama : `winget install ollama.ollama`.
- Vérifier installations : `ollama --version` ; `conda --version`.

Jour 0 — Installer/mettre à jour drivers GPU (si GPU présent) (30–90 minutes)
- Télécharger et installer le driver NVIDIA compatible.
- Installer CUDA Toolkit et cuDNN si vous comptez exécuter des runtimes CUDA.
- Vérifier `nvidia-smi` et `nvcc --version`.

Jour 0 — Télécharger un modèle test (variable)
- Petite taille (2–7B) : 5–30 minutes selon connexion.
- Taille moyenne (8–14B) : 15–120 minutes.
- Grande taille (14B+) : plusieurs heures.

Jour 1 — Installer Open WebUI et configurer (10–30 minutes)
- Exécuter `OpenWebUIInstaller.exe`.
- Créer l'admin à `http://localhost:8080/auth`.
- Lier Open WebUI à Ollama (vérifier que les modèles apparaissent).

Jour 1 — Tests et réglages (30–90 minutes)
- Lancer `ollama run [modèle]` et faire un test simple.
- Sur Open WebUI : exécuter une requête, tester le rendu Markdown, vérifier l'indexation RAG si nécessaire.
- Mesurer temps de réponse, utilisation RAM/GPU et ajuster les paramètres.

Jour 1–2 — Mise en production locale et maintenance
- Planifier des sauvegardes et un nettoyage régulier des modèles inutilisés (`ollama rm`).
- Mettre en place un calendrier de mises à jour (ex. `winget upgrade` mensuel).

## Checklist minimale (exécutable)
- [ ] Windows à jour
- [ ] Espace disque libre >= 20 Go
- [ ] `WinGet` installé
- [ ] Miniconda installé
- [ ] Ollama installé et testé (`ollama --version`)
- [ ] (Optionnel) Drivers NVIDIA, CUDA, cuDNN installés
- [ ] Open WebUI installé et accès admin configuré
- [ ] Modèle téléchargé et test de prompt effectué
- [ ] Plan de maintenance défini

## Raccourcis et commandes utiles
- Installer Ollama : `winget install ollama.ollama`
- Vérifier Ollama : `ollama --version`
- Lister modèles : `ollama list`
- Télécharger modèle : `ollama pull [modèle]`
- Lancer modèle : `ollama run [modèle]`
- Supprimer modèle : `ollama rm [nom-du-modèle]`

## Notes finales
Suivez la chronologie dans l'ordre pour minimiser les erreurs. Réservez la majeure partie du temps au téléchargement des modèles et aux tests d'inférence réels : ce sont ces étapes qui prennent le plus de temps et nécessitent des ajustements selon la machine.
