# Présentation des Classes et Associations

## 1. Identification des classes

Voici les classes principales à extraire du texte :

- **Vol** : Représente le vol avec ses informations générales.
- **Départ** : Représente un vol programmé à une date donnée avec des informations associées.
- **Passager** : Représente une personne enregistrée pour un départ.
- **Avion** : Représente l’avion affecté à un départ.
- **Personnel** : Représente un employé de la compagnie aérienne.
  - **PersonnelNavigant** (héritant de Personnel) : Représente le personnel qui travaille à bord du vol.
    - **Pilote** (héritant de PersonnelNavigant) : Représente les pilotes.
    - **Hôtesse/Stewart** (héritant de PersonnelNavigant) : Représente les hôtesses et stewards.
  - **PersonnelNonNavigant** (héritant de Personnel) : Représente le personnel non navigant.

## 2. Identification des associations entre classes

- **Vol - Départ** : Un vol peut avoir plusieurs départs, mais un départ est lié à un seul vol.
- **Départ - Passager** : Un départ peut avoir plusieurs passagers, et un passager peut être enregistré pour plusieurs départs.
- **Départ - Avion** : Un avion est affecté à un départ, un avion peut être utilisé pour plusieurs départs.
- **Départ - PersonnelNavigant/PersonnelNonNavigant** : Plusieurs membres du personnel (navigants et non navigants) sont affectés à chaque départ.
- **Pilote/PersonnelNavigant - Départ** : Un ou deux pilotes et entre 2 et 10 hôtesses/stewards sont affectés à chaque départ.

## 3. Position des attributs dans les classes

- **Vol**
  - Numéro de vol
  - Ville de départ
  - Ville d’arrivée
  - Heure de départ
  - Durée
  - Jour de la semaine

- **Départ**
  - Date du départ
  - Quantité de carburant utilisée (en fonction de la date)

- **Avion**
  - Numéro
  - Type
  - Capacité

- **Personne**
  - Nom
  - Adresse
  - Numéro de téléphone

- **Passager** : Pas d’attribut spécifique (hérite de Personne)

- **Personnel** : Pas d’attribut spécifique (hérite de Personne)

- **PersonnelNavigant**
  - Nombre d’heures de vol

- **Pilote** : Pas d’attribut spécifique (hérite de PersonnelNavigant)

- **Hôtesse/Stewart** : Pas d’attribut spécifique (hérite de PersonnelNavigant)

- **PersonnelNonNavigant** : Pas d’attribut spécifique (hérite de Personnel)

## 4. Identification des généralisations

- **Personne** est une classe abstraite.
- **Personnel** et **Passager** sont des spécialisations de **Personne**.
- **PersonnelNavigant** et **PersonnelNonNavigant** sont des spécialisations de **Personnel**.
- **Pilote** et **Hôtesse/Stewart** sont des spécialisations de **PersonnelNavigant**.

PLANTUML