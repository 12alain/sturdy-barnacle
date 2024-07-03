
# Exercise 3 

### Descriptioon du resultat de pull https://github.com/LeMeteore/animated-carnival.git de la commande 

- **remote: Enumerating objects: 23, done.**
  - Git commence à énumérer les objets disponibles dans le dépôt distant.

- **remote: Counting objects: 100% (23/23), done.**
  - Git a compté tous les objets nécessaires à récupérer.

- **remote: Compressing objects: 100% (19/19), done.**
  - Les objets récupérés sont compressés pour optimiser le transfert des données.

- **remote: Total 23 (delta 6), reused 0 (delta 0), pack-reused 0**
  - Statistiques sur le processus de récupération des objets.

- **Unpacking objects: 100% (23/23), 8.57 KiB | 107.00 KiB/s, done.**
  - Les objets récupérés sont décompressés et extraits dans le dépôt local.

- **From https://github.com/LeMeteore/animated-carnival**
  - Indique l'URL du dépôt distant à partir duquel les modifications ont été tirées.

- **\* branch HEAD -> FETCH_HEAD**
  - La branche distante HEAD a été mise à jour dans FETCH_HEAD après la récupération.

- **fatal: refusing to merge unrelated histories**
  - Erreur indiquant que Git refuse de fusionner les historiques considérés comme non apparentés.



### Décriptions de  ce qui peut être fait pour revenir à une situation normale.e 

- ### Effectons un fetch

Pour récupérer les dernières modifications du dépôt distant sans essayer de les fusionner immédiatement, utilisons la commande suivante :

```bash
git fetch https://github.com/LeMeteore/animated-carnival.git

```

### Examineons les différences

Pour examiner les différences entre votre branche locale et FETCH_HEAD afin de comprendre pourquoi Git considère les historiques comme non apparentés, utilisez la commande suivante :

```bash
git diff HEAD FETCH_HEAD
```
### Forcons  la fusion avec l'option --allow-unrelated-histories

Si nous décidons de fusionner malgré les historiques non apparentés, utilisons l'option `--allow-unrelated-histories` avec `git merge` :

```bash
git merge FETCH_HEAD --allow-unrelated-histories
```


