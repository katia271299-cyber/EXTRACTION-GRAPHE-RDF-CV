# EXTRACTION-GRAPHE-RDF-CV
extraction graphes rdfs cv , grande echelle , db kaggle 
Extraction et Visualisation de CV en Graphe RDF
Ce projet permet d'extraire automatiquement les informations clés d'un CV, de les structurer dans un graphe RDF enrichi, et de générer un résumé complet et lisible.
Fonctionnalités principales
Chargement des CVs
Téléchargement automatique depuis un dataset Kaggle (snehaanbhawal/resume-dataset).
Lecture des CVs au format CSV.
Traitement du texte
Utilisation de spaCy pour la reconnaissance d'entités nommées (ORG, PERSON, etc.).
Nettoyage et normalisation du texte.
Extraction d’informations
Compétences : identification via une liste prédéfinie (Python, SQL, Machine Learning, etc.).
Postes occupés : extraction depuis le texte et les sections « Experience ».
Domaines d’études : détection des formations ou spécialités.
Établissements éducatifs : reconnaissance via spaCy et filtrage intelligent.
Organisations professionnelles : entreprises précédemment fréquentées, avec nettoyage des doublons et exceptions.
Représentation RDF
Création d’un graphe RDF utilisant les namespaces schema.org et FOAF.
Chaque CV devient un nœud central relié à des compétences, postes, formations et organisations.
Export possible au format Turtle (.ttl).
Visualisation du graphe
Graphe orienté avec NetworkX et Matplotlib.
Couleurs distinctes pour :
Personnes / CV
Compétences
Domaines d’études / établissements
Organisations professionnelles
Labels clairs pour toutes les entités et relations.
Résumé du CV
Affichage propre et synthétique :
Compétences clés
Postes occupés
Domaines d’études
Établissements fréquentés
Organisations professionnelles
Sans doublons, prêt pour intégration ou analyse.
Export et réutilisation
Graphe RDF exporté au format Turtle (resume_graph_<ID>_final.ttl) pour utilisation dans d’autres systèmes ou analyses sémantiques.

**data base** : https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset/data

**lien notebook**: https://colab.research.google.com/drive/1LBu7A9r7Gz1hlfS8PTXNXJiKDEMHjShg#scrollTo=eu_XHxXtB0dq
