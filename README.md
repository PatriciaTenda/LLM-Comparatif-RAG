🔒 Projet privé — Ce travail a été réalisé dans le cadre d’un projet professionnel encadré par [GRETA Centre Val de loire] pour le compte d’un partenaire entreprise.

#  Évaluation Comparative de Modèles de Langage Locaux pour Application RAG

##  Contexte

Dans le cadre de ma formation en Intelligence Artificielle, ce projet a pour objectif d’évaluer plusieurs **modèles de langage locaux (LLMs)** afin d’identifier celui qui serait le plus adapté à une application de type **RAG (Retrieval-Augmented Generation)**, fonctionnant entièrement en local.

Le projet s’inscrit dans une logique de respect de la confidentialité des données, de performance locale et de fiabilité du raisonnement produit par les modèles.

---

##  Objectifs du projet

- Comparer plusieurs LLMs open-source disponibles localement via Ollama ou LM Studio.
- Évaluer la **qualité des réponses** produites sur des cas RAG typiques.
- Mesurer les **performances** (temps de réponse, consommation mémoire, stabilité).
- Identifier le modèle offrant le **meilleur compromis** pour une intégration locale efficace.

---

## 📁 Structure du dépôt

## 📁 Structure du dépôt

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
-  **Temps de génération**
-  **Consommation mémoire / CPU / GPU**
-  **Verbosité**
-  **Robustesse face aux erreurs**
-  **Facilité d'intégration dans un pipeline RAG**

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
python scripts/run_tests.py --model mistral --prompts prompts/rag_queries.json
```
Les résultats sont sauvegardés dans le dossier results/.

# Analyse
Les données collectées sont analysées dans le notebook analysis/analysis.ipynb via :

- Tableaux comparatifs
- Graphiques radar ou en barres
- Matrice de performances

# Rapport
Le rapport final comprend :

- Méthodologie complète
- Détails sur les modèles
- Résultats bruts et analysés
- Recommandations pour l’intégration dans une app RAG
- Présentation synthétique du projet

Disponible dans le dossier /report.

# Auteur
Projet réalisé par [PatriciaTenda], dans le cadre d’un projet d’évaluation professionnelle en Intelligence Artificielle, 2025.

# Licence & Droits d’usage
Ce projet a été réalisé dans le cadre d’une mission confiée par une entreprise partenaire, dans le cadre de ma formation professionnelle en Intelligence Artificielle.
Le contenu de ce dépôt, y compris les scripts, données et analyses, est soumis à des droits réservés.
Toute reproduction, diffusion ou utilisation sans autorisation expresse est interdite.
Ce dépôt est mis à disposition uniquement à des fins pédagogiques et d’évaluation, dans un cadre strictement privé.

# Remerciements
Merci à l’équipe pédagogique, aux développeurs des modèles open-source, et à la communauté IA qui partage ses outils et connaissances.

