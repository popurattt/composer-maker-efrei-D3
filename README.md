# composer-maker-efrei-D3

## Description

On souhaiterait créer un outil qui nous permettent de valider un composer.json.

Notre outil devra logger les erreurs recontrer dans le fichier.

Cette outil devra être utiliser par des collaborateurs de différents pays.

De ce fait on aimerait que ces logs soient traduits dans au moins 3 langues.



### Exercice

1. Écrire une fonction ```validate``` qui va prendre en paramètre un path vers le composer.json a valider et vous retournez:
    - la validité du nom
    - la validité de la description
    - la validité de l'object require 
        - la validité de la version dans le require
2. Avec le maker bundle créez une fonction ```make:my-validator``` qui va vous génerez un boilerplate d'un classe de log tel que
    - FooLog::logTitle
    - FooLog::logMessage
3. Créez une commande composer ```validate``` qui va, a l'aide de la classe créer précedemment, écrire un fichier de log ou chaque ligne devrai correpondre à`:
```
 logTitle: logMessage
```
4. A l'aide d'une librairie de traduction (i18n) de votre choix modifier la commande tel que ```make:my-validator``` prends un parametre ```lang```  qui devra être égal a l'un de 3 [ISO Codes](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements) que vous choissirez ex:
```sh
$ make:my-validator "th"
```
```sh
$ make:my-validator "en"
```
```sh
$ make:my-validator "ch"
```
- Si la valeur donner n'est pas valide, afficher un message d'erreur

```sh
$ make:my-validator "pas un iso code"
 Erreur: les valeurs possibles sont [th, en, ch]
```
- Les logs devront etre traduits dans la langue correspondante


## Rendu

Paris: 24/11/2023

Bordeaux: 04/12/2023


Ajoutez ce profile github en temps que maintainer, je ne regarderai pas les push apres la date de rendu

Si impossible d'utiliser git, zipper le projet, **SANS LE DOSSIER VENDOR** et envoyé le a pmabounda@wedigital.garden
