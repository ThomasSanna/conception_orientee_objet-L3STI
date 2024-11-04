# Modélisation des Classes pour une Université

## 1. Identification des Classes

Les classes principales à modéliser dans ce contexte sont :

- **Université** : L'entité qui propose les diplômes et gère les inscriptions.
- **Diplôme** : Représente un diplôme, qui est composé de plusieurs unités d'enseignement (UE).
- **UE (Unité d'Enseignement)** : Représente une unité d'enseignement obligatoire ou optionnelle.
- **Étudiant** : Représente un étudiant qui s'inscrit à des diplômes et à des UE.
- **Dossier** : Représente le dossier universitaire d'un étudiant, contenant ses informations personnelles et académiques.
- **InscriptionDiplôme** : Représente l'inscription d'un étudiant à un diplôme, avec le choix des UE optionnelles.
- **InscriptionUE** : Représente l'inscription d'un étudiant à une UE spécifique.
- **Scolarité** : Le service qui gère les inscriptions et l’édition des listes.

## 2. Identification des Associations entre Classes

- **Université - Diplôme** : L’université propose plusieurs diplômes.
- **Diplôme - UE** : Un diplôme est composé de 6 UE obligatoires et 2 optionnelles. Une UE peut appartenir à plusieurs diplômes.
- **Étudiant - Diplôme** : Un étudiant peut s’inscrire à un ou plusieurs diplômes (maximum 3).
- **Étudiant - Dossier** : Chaque étudiant possède un dossier universitaire.
- **InscriptionDiplôme - Étudiant** : Un étudiant peut s’inscrire à plusieurs diplômes via une inscription qui enregistre la date et les UE optionnelles choisies.
- **InscriptionUE - UE** : L’inscription à une UE vérifie les prérequis et la disponibilité des places.
- **UE - Prérequis** : Certaines UE ont des prérequis, c’est-à-dire des UE devant être validées avant l'inscription.
- **Scolarité - InscriptionUE** : Le service de la scolarité gère les inscriptions aux UE et les listes affichées.

## 3. Position des Attributs dans les Classes

### Université
- Nom de l’université

### Diplôme
- Nom
- Liste d’UE obligatoires (6)
- Liste d’UE optionnelles (2 à choisir parmi 2 à 8)

### UE
- Nom
- Nombre de places (limité à 20)
- Liste des prérequis (UE à valider avant inscription)

### Étudiant
- Nom
- Prénom
- Adresse
- Téléphone
- Login
- Mot de passe

### Dossier
- Liste des diplômes obtenus (avec moyenne générale et mention)

### InscriptionDiplôme
- Date d’inscription

### InscriptionUE
- Statut d’inscription (validée ou non)
- Date d’inscription

### Scolarité
- Nom du service

## 4. Identification des Généralisations

Il n’y a pas de généralisations évidentes à ce stade. Les classes décrites représentent des entités distinctes avec leurs propres caractéristiques.