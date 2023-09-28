# Tutoriel TP1 Application Android

1. Lancez Android Studio
2. Créez un nouveau projet via le + ou `Fichier > Nouveau > Projet`
	1. Choisissez “Empty activity”
![img](https://i.imgur.com/oChHj7y.png)
	2. Attention a bien sélectionner “Java” et non Kotlin comme langage.
![img](https://i.imgur.com/LIJ3ehy.png)
3. On veut d’abord construire le layout de notre application, avec ses affichages et ses boutons. Dans le panneau de gauche exposant l’arborescence des fichiers, ouvrez donc dans `app > res > layout > activity_main.xml` 

4. Il y a en haut à droite trois options d’affichage pour les fichiers xml
![img](https://i.imgur.com/gM3eQ3Z.png)
![img](https://i.imgur.com/n3vjROv.png)
![img](https://i.imgur.com/7eedLid.png)

5. D’abord, supprimez l’élément texte “Hello World”, et ajoutez les éléments dont vous avez besoin par glisser-déposer de la palette vers l’écran blanc, 
![img](https://i.imgur.com/3p7LSXK.png)
![img](https://i.imgur.com/QFJmptD.png)

6. Bon maintenant la partie avec un truc a comprendre : L’objectif est de designer une interface en définissant l’apparence des éléments seulement les uns par rapport aux autres, et par rapport à l’écran : *pas de valeurs en pixels !* Pour ça on va utiliser les *constraints*, les *layout_constraints* et *layout*.
	1. On séléctionne un élément
![img](https://i.imgur.com/czesny3.png)

On clique sur un des “+” dans le Constraint widget pour ajouter une constraint
![img](https://i.imgur.com/31tB5Lk.png)

Une nouvelle constraint est ajoutée. 
![img](https://i.imgur.com/tddGPLC.png)

Ensuite, mettez des constraints à zéro sur tous les éléments : Pour chaque élément, le constraint widget doit afficher 0 dans toutes les directions et la visualisation montrer les contraintes entre les éléments et entre les éléments et le bord.
![img](https://i.imgur.com/EDEpg1r.png)

Dans le panneau de droite, changez les *layout_width* et *layout_height* de tous les éléments de **wrap_content** à **0dp**.
![img](https://i.imgur.com/zVuB948.png)

wrap_content donne aux boutons la taille suffisante pour afficher leur contenu + un peu de padding, alors que 0dp prend toute la place disponible, étant donné les contraintes mises en place. 

Toujours dans le panneau de droite “Attributes”, cherchez “weight”
![img](https://i.imgur.com/ItLtQ8k.png)

Ce qui affiche les layout constraints : Personnellement je les ai tous mis à 1, sauf la layout constraint du bouton qui fera l’affichage couleur, que j’ai set à 2 pour qu’il soit 2 fois plus haut que les boutons.
![img](https://i.imgur.com/9j0apC7.png)

Vous pouvez revenir sur les constraints et ajouter des marges et des gaps : 

![img](https://i.imgur.com/SXtEPjq.png)

Vous pouvez maintenant tester l’émulateur comme expliqué dans le TD : 
![img](https://i.imgur.com/41wCUtk.png)
