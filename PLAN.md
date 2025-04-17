##  PLAN DU PROJET – Évaluation Méthodologique des Modèles de Langage Locaux (LLMs)

###  Objectif général
Mettre en place une **méthodologie rigoureuse et automatisée** d’évaluation des modèles de langage (LLMs) locaux, adaptée à des cas d’usage de type **RAG (Retrieval-Augmented Generation)**.

Le projet repose sur la création d’un **pipeline complet** combinant :
- des jeux de prompts et de jeux de données (JDD),
- l’exécution automatique sur différents modèles locaux,
- l’évaluation par des métriques objectives et personnalisables,
- l’analyse comparative des performances,
- l’intégration d’un système de monitoring ou d’audit pour l’observabilité des modèles.

---

###  Objectifs techniques
- Définir un **ensemble de métriques** pour l’évaluation des réponses générées
- Développer un **pipeline automatisé** d'exécution de tests (via Python)
- Permettre l’évaluation de différents modèles exécutés **en local** (Ollama, LM Studio, etc.)
- Centraliser les résultats dans un format exploitable (CSV / JSON)
- Fournir des **analyses visuelles et statistiques** des résultats
- Concevoir un début de **système de monitoring** pour détecter les dérives ou comportements anormaux

---

##  Organisation du travail – 2 Semaines

###  Semaine 1 : Conception et Mise en place

| Jour | Étape | Résultat attendu |
|------|-------|------------------|
| J1   | Cadrage du projet | Objectifs + périmètre technique clair |
| J2   | Choix des métriques | Grille d’évaluation des modèles |
| J3   | Conception des prompts et JDD | Fichier `rag_queries.json` prêt à l’emploi |
| J4   | Installation des modèles locaux | Ollama prêt avec Mistral, LLaMA3, Phi, Qwen, etc. |
| J5   | Développement du script de test | Pipeline Python initial (input → output → logs) |

###  Semaine 2 : Tests, Analyse et Valorisation

| Jour | Étape | Résultat attendu |
|------|-------|------------------|
| J6   | Lancement des tests | Résultats bruts dans `results/` |
| J7   | Analyse comparative | Graphiques, matrices de score |
| J8   | Recommandations | Classement des modèles selon les usages |
| J9   | Système de monitoring | Début de système d’alerte ou suivi |
| J10  | Rapport final | Rapport + présentation prêt à livrer |

---

##  Étapes du pipeline LLM à implémenter

1. **Préparation des prompts et du jeu de données**
2. **Exécution automatique** : chaque modèle reçoit chaque prompt
3. **Mesure des performances** : temps, RAM, verbosité, etc.
4. **Évaluation de la qualité** : notation, scoring contextuel, etc.
5. **Centralisation des résultats** dans un format standard
6. **Analyse comparative** : visualisation, stats, classements
7. **Monitoring / Observabilité** (étape avancée)

---

## 📊 Métriques envisagées

| Critère | Description |
|--------|-------------|
|  Pertinence de la réponse | Qualité et exactitude du contenu généré |
|  Utilisation correcte du contexte | Bon usage du corpus de référence |
|  Temps de génération | Délai entre question et réponse |
|  Mémoire utilisée | RAM/CPU/GPU mobilisés |
|  Verbosité | Longueur, répétition inutile |
|  Robustesse | Réaction face aux erreurs ou données bruitées |
|  Monitoring | Suivi des comportements anormaux |

---

##  Livrables attendus
- Scripts Python de test et d’analyse
- Jeu de prompts complet (`prompts/rag_queries.json`)
- Résultats exportés (`results/model_outputs.csv`)
- Visualisations d’analyse (`analysis/`)
- Rapport final structuré (`report/rapport_final.md` ou PDF)
- README documenté et clair

---

##  Prochaines étapes
- [ ] Ajouter le jeu de prompts
- [ ] Compléter les scripts
- [ ] Intégrer les modèles
- [ ] Exécuter les tests
- [ ] Lancer les analyses
- [ ] Documenter et livrer

---

