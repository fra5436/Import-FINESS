# Import-FINESS
Guide pour l'import des établissements de santé via le fichier FINESS


Pour importer directement les établissements de santé via le dossiers FINESS. 

Nous l'avons utilisé pour les pharmacies d'officines du Grand Est.

Pour l'instant nous ne l'avons fait que en préprod et nous testons la stabilité et l'impact sur le fonctionnement du logiciel.


## Dossier FINESS

Le dossier FINESS est disponible sur [finess.sante.gouv.fr](http://finess.sante.gouv.fr/fininter/jsp/index.jsp).

Il est également disponible sur [data.gouv.fr](https://www.data.gouv.fr/fr/) mais semble moins bien structuré.


## Mise en forme des info du dossier FINESS

Mise en forme dans la table.

[exemple ici](https://docs.google.com/spreadsheets/d/1r8o64Kzl8krQDEwUcx9Brqzp5vm_bQYayPraPVNgW1A/edit?usp=sharing)

Dans cet exemple, j'ai pris les 5 pharmacie que nous avons rentré pour tester.

[ICI](https://docs.google.com/document/d/1YS5k1sECWMutIW5Fw8ymeoL5LGrvxtr2Cn6y8j51r-c/edit?usp=sharing) la correspondance des variables entre les 2 fichiers réalisé par un de nos pharmaciens.

Une fois cette correspondance des variables réalisés, il reste à mettre en forme :

* Mettre une value pour la colonne NIETABLIS (colonne A du fichier Excel). C'est un compteur qui s'implémente de 1 en 1, il faut consulter la table pour voir ou vous en etes et faire l'incrémentation dans Excel.
* Mettre la value F dans la colonne Retrait (Colonne J du fichier Excel)
* Mettre une date de création pour la colonne DATE_CREA, (Colonne U). Au format: JJ/MM/AAAA HH:MM:SS 
* Mettre une value pour la colonne NIUTILCREA (colonne W). C'est l'identifiant de la personne qui implémente, nous avons mis la value du pharmacien qui a fait les tests. Se trouve dans la table.
* Mettre une value pour la colonne	NICATEGORIE (colonne AG), 56 dans les bases pour une pharmacie d'officine.

[Exemple de fichier pret à intégrer](https://docs.google.com/spreadsheets/d/1Ewuf8_q2MXFHj6Vqa_V6WZm9gq4Cr9YrpLqbB0leSGs/edit?usp=sharing)


## Table où importer

Il faut faire l'import data dans la table ETABLIS

