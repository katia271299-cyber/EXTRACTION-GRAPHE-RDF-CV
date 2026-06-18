# Extraction & Visualisation de Graphes RDF — CV

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![spaCy](https://img.shields.io/badge/NLP-spaCy-09A3D5?logo=spacy&logoColor=white)
![RDF](https://img.shields.io/badge/Knowledge%20Graph-RDF%20%7C%20FOAF%20%7C%20schema.org-purple)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter&logoColor=white)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?logo=kaggle&logoColor=white)

Extraction automatique d'informations depuis des CV, structuration en **graphe RDF** enrichi avec ontologies (schema.org, FOAF), et visualisation des relations entre entités.

---

## Fonctionnalités

- **Chargement** : téléchargement automatique depuis le dataset Kaggle [`snehaanbhawal/resume-dataset`](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset)
- **Traitement NLP** : extraction d'entités nommées (ORG, PERSON, GPE) avec spaCy
- **Extraction structurée** :
  - Compétences techniques (Python, SQL, Machine Learning…)
  - Postes occupés et expériences
  - Formations et domaines d'études
  - Établissements éducatifs et organisations
- **Enrichissement** : ontologie toy pour les domaines d'études
- **Graphe RDF** : namespaces schema.org + FOAF, export Turtle (`.ttl`)
- **Visualisation** : graphe orienté avec NetworkX + Matplotlib, couleurs par type d'entité
- **Résumé** : synthèse lisible par CV (sans doublons)

---

## Structure du graphe

```
CV (nœud central)
├── schema:skills       → Compétences
├── schema:jobTitle     → Postes occupés
├── schema:alumniOf     → Établissements
├── schema:studyField   → Domaines d'études
└── org:memberOf        → Organisations professionnelles
```

---

## Stack technique

| Composant | Technologie |
|-----------|-------------|
| NLP | spaCy (`en_core_web_sm`) |
| Graphe RDF | rdflib |
| Visualisation | NetworkX, Matplotlib |
| Dataset | Kaggle API |
| Notebook | Jupyter |

---

## Fichiers

| Fichier | Description |
|---------|-------------|
| `EXTRACTION (1).ipynb` | Notebook principal |
| `extraction (1).py` | Script Python équivalent |
| `Sujets-projets-Texte (5).pdf` | Sujet du projet |

---

## Lancer le projet

```bash
pip install rdflib spacy networkx matplotlib kaggle
python -m spacy download en_core_web_sm
jupyter notebook "EXTRACTION (1).ipynb"
```