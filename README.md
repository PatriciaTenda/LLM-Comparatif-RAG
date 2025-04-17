🔒 Projet privé — Ce travail a été réalisé dans le cadre d’un projet professionnel encadré par [Greta Centre-Val de Loire] pour le compte d’un partenaire entreprise.

#  Évaluation Comparative de Modèles de Langage Locaux pour Application RAG

##  Contexte

Ce projet s’inscrit dans le cadre d’une mission professionnelle en Intelligence Artificielle, visant à construire une **méthodologie d’évaluation rigoureuse et automatisée** des modèles de langage locaux (**LLMs**) pour des cas d’usage **RAG** (Retrieval-Augmented Generation), le tout dans un environnement **100% local**.

Il intègre une approche complète mêlant **tests, métriques, analyses** et **observabilité** afin d’identifier les modèles les plus adaptés à des contextes exigeants dans une logique de respect de la confidentialité des données, de performance locale, de fiabilité du raisonnement produit par les modèles et de robustesse.

---

##  Objectifs du projet

- Définir une **méthodologie réutilisable** d’évaluation de modèles LLM
- Mettre en œuvre un **pipeline automatisé** : prompts → modèles → évaluation → analyse
- Comparer des LLMs open-source tournant en local (via Ollama / LM Studio)
- Générer des **résultats chiffrés, interprétables et visualisables**
- Évaluer la **qualité des réponses** produites sur des cas RAG typiques.
- Mesurer les **performances** (temps de réponse, consommation mémoire, stabilité).
- Identifier le modèle offrant le **meilleur compromis** pour une intégration locale efficace
- Proposer un début de **système de monitoring** pour le suivi des performances dans le temps.

---
##  Étapes du pipeline

1.  Préparation des prompts de test (cas réalistes RAG)
2.  Exécution automatique des modèles sur chaque prompt
3.  Collecte des réponses, temps, usages mémoire/CPU
4.  Évaluation qualitative et quantitative (scoring, métriques)
5.  Analyse comparative (tableaux, graphiques)
6.  Monitoring : détection d’écarts, performances anormales (WIP)

---

## Structure du dépôt

```

├── prompts/                 # Contient les prompts de test (questions types pour RAG)
│   └── rag_queries.json
│
├── scripts/                 # Scripts Python pour exécuter les modèles et enregistrer les résultats
│   └── run_tests.py
│
├── results/                 # Données de sortie (réponses, temps, usage mémoire, etc.)
│   └── model_outputs.csv
│
├── analysis/                # Notebooks d’analyse et visualisations
│   └── analysis.ipynb
│
├── report/                  # Rapport final du projet + support de présentation
│   └── rapport_final.md / .pdf
│
├── PLAN.md                  # Plan d’organisation du projet (planning, étapes, métriques)
└── README.md                # Présentation générale du projet (ce fichier)
```

---

##  Modèles testés

Les modèles sont exécutés **localement** via [Ollama](https://ollama.com/) :

| Modèle       | Taille      | Type de licence | Atout principal |
|--------------|-------------|------------------|-----------------|
| Mistral 7B   | Léger       | Apache 2.0       | Rapide et précis |
| LLaMA 3 8B   | Moyen       | Meta (non-commercial) | Très performant |
| Phi-3 Small  | Très léger  | MIT              | CPU-friendly |
| Qwen 7B      | Moyen       | Apache 2.0       | Bonne compréhension |
| Falcon 7B    | Moyen       | Apache 2.0       | Robuste et open |

---

##  Métriques d’évaluation

Chaque modèle est évalué selon plusieurs **critères objectifs** :

-  **Pertinence de la réponse**
-  **Utilisation correcte du contexte**
-  **Temps de génération ou de réponse**
-  **Consommation mémoire / CPU / GPU**
-  **Verbosité**
-  **Robustesse face aux erreurs**
-  **Facilité d'intégration dans un pipeline RAG**
-  **Observabilité (monitoring de cohérence)**

---

##  Jeu de données

Le fichier `prompts/rag_queries.json` contient un ensemble de **questions simulées** (entre 15 et 20) représentant des cas réels d’utilisation RAG :
- Questions simples
- Questions avec raisonnement
- Cas ambigus
- Cas bruités (erreurs dans le contexte)

---

##  Lancement des tests

Les scripts Python permettent de tester automatiquement chaque modèle avec les prompts fournis :

```bash
    # Mise en place de l'environnement
    py -3.12 -m venv .venv
    .venv\Scripts\Activate.ps1  # ou activate.bat selon ton terminal
    pip install -r requirements.txt

    # Test des prompts
    python scripts/run_tests.py --model mistral --prompts prompts/rag_queries.json
```
Les résultats sont sauvegardés dans le dossier results/.

# Analyse
Les données collectées sont analysées dans le notebook analysis/analysis.ipynb via :

- Tableaux comparatifs
- Graphiques radar et / ou en barres
- Matrice de performances (Pour montrer comment chaque modèle se comporte en conditions réelles (temps, ressources, stabilité))
- Matrices de scoring (Pour montrer la valeur des réponses produites (pertinence, logique, robustesse...))

# Rapport
Le rapport final comprend :

- Méthodologie complète
- Détails sur les modèles
- Résultats bruts et analysés
- Recommandations pour l’intégration dans une app RAG
- Présentation synthétique du projet

Disponible dans le dossier /report.

# Auteur
Projet réalisé par [ PatriciaTenda](https://github.com/PatriciaTenda/LLM-Comparatif-RAG/), Dans le cadre de la formation "Développeuse en Intelligence Artificielle", Greta Centre-Val de Loire – 2025.

# Licence & Droits d’usage
Ce projet a été réalisé dans le cadre d’une mission confiée par une entreprise partenaire, dans le cadre de ma formation professionnelle en Intelligence Artificielle.
Le contenu de ce dépôt, y compris les scripts, données et analyses, est soumis à des droits réservés.
Toute reproduction, diffusion ou utilisation sans autorisation expresse est interdite.
Ce dépôt est mis à disposition uniquement à des fins pédagogiques et d’évaluation.

# Remerciements
Merci à l’équipe pédagogique, aux développeurs des modèles open-source, et à la communauté IA qui partage ses outils et connaissances et les rendent accessibles.

