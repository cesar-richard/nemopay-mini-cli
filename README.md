# Introduction
Outil d'importation de droits sur Nemopay.

Dans la version actuelle il faut recuperer un id de session existant en se connectant manuellement sur le back office nemopay.

## Utilisation
```bash
python moulinette.py -i <inputfile> -a <addGroup|addRight> -s <sessionid> [-f <fundationid>]
```

* **-i ou --inputfile** : fichier au format CSV contenant les modifications à apporter (structure du fichier plus bas)
* **-a ou --action**    : action à executer
* **-s ou --sessionid** : sessionid a utiliser pour envoyer les requetes au nom de daphne
* **-f ou --fundation** : Id de la fondation sur laquelle mettre les droits (dans le cas de l'action **addRight**) s'il est omis la permission s'applique à tout le système 

## Structure du fichier d'entrée
 Les entêtes ne sont pas à recopier dans le fichier d'entrée, ils sont donnés ici à titre d'explication.

### Action addRight
Noter que le paramètre -f permet de ne donner les permission que sur 1 fondation particulière.

| Prenom | Nom | Login | Permission |
|--|--|--|--|
| Cesar | Richard | cerichar | SALE |
| Quentin | Richard | qrichard | SALE |

### Action addGroup

| Prenom | Nom | Login | Id du WalletGroup |
|--|--|--|--|
| Cesar | Richard | cerichar | 4 |
| Quentin | Richard | qrichard | 3 |
