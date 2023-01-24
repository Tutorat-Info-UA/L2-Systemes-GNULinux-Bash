
# 👹 TP - Bash is evil 😈
L'objectif final de ce TP est de réalisé un petit programme bash, comme `ls` `sl` etc


## 1️⃣
Vous trouverez dans les fichiers `Demon.txt` et `Demon_extended.txt` un petit démon en [ASCII art](https://en.wikipedia.org/wiki/ASCII_art)
Télécharger ces deux fichiers, il vous seront utile pour la suite

Réalisé ensuite un script bash qui affiche le démon de `Demon.txt`

## 2️⃣
On souhaite désormais que ce script éfface le terminal au complet avant d'afficher le démon.

## 3️⃣
L'utilisateur doit ensuite pouvoir saisir du texte pour fournir des commandes, et le programme ne s'achèvera pas tant que l'utilisateur n'aura pas fourni la commande `e`
S'il saisie autre chose on ne fait rien

## 4️⃣
Faire une fonction bash `print_demon` dans votre script elle prend en paramètre une position x et une position y deux entier elle :
 - éffacera le terminal
 - affichera le démon ligne par ligne !

Pour déplacer le démon on utilisera des saut de ligne et des espaces.

## 5️⃣
On va maintenant ajouter plusieurs commandes :
Nom    | Commande | Action 
-------|----------|------------------------------------------
Exit   | e        | quitte le programme (déjà faite)
Gauche | q        | déplace le démon à gauche
Droite | d        | déplace le démon à droite
Haut   | z        | déplace le démon vers le haut
Bas    | s        | déplace le démon vers le bas

## 6️⃣
La fonction `print_demon` va désormais prendre un paramètre en plus qui affichera le démon  `Demon_extended.sh` pendant une seconde puis de retour à `Demon.sh` si le troisième paramètre est à 1

## 7️⃣
On ajoutera la commande
Nom    | Commande | Action 
-------|----------|------------------------------------------
Attack | a        | fait attacker le démon

et on adaptera le programme pour intégrer la commande

## 8️⃣
On ajoutera la gestion de paramètre de manière à pouvoir par exemple saisir : 
`./evil.sh -x 3 -y 9 --random`

 - `-x <int>` position initial horizontal du démon
 - `-y <int>` position initial vertical du démon
 - `--random` si cette option est choisi on n'utilisera pas des commandes utilisateurs mais des actions aléatoires

## *️⃣

Pour la partie aléatoire en bash on pourra s'aider de :

```bash
act=$(expr $RANDOM % 6)
```