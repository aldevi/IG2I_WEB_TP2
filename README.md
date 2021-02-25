# IG2I - Semestre 2 Module WEB - TP2
## Objectif
 Expérimenter la transmission d'informations à l'aide de formulaires, utilisation d’un serveur pour recevoir des chaînes de requête, premières interactions avec les éléments du DOM à l'aide de javascript.
 
 ## Plan de la séance
 1.  Présentation de l’onglet Firebug/réseau pour visualiser les échanges de données provoqués par la page d’exemple du cours “form1.html”
 2.  Présentation de l'outil Firebug/Console Web pour générer des traces d'éxécution en javascript
 3.  Partie TP : les exercices non réalisés en TP pourront l'être à l'occasion du TNE
 4. Test sur javascript et les formulaires (15 minutes)
 
 ### Exercice 1 :  Serveur Web, Chaînes de requête, champs multiples, GET & POST
 
1. [Optionnel - à faire si vous disposez de votre propre serveur HTTP] Placer le fichier ex1.php fourni dans un répertoire de votre serveur Web. Ce fichier devra être utilisé comme cible des formulaires que vous rédigerez dans tous les exercices suivants. [Si vous n’avez pas de serveur HTTP] : la page ex1.php est disponible à l'adresse http://chaire-ecommerce.ec-lille.fr/web1/ex1.php
2. Activer l'onglet Firebug/Réseau. Entrez une chaîne de caractères dans le champ texte du formulaire et soumettre le formulaire. Constater ce qui s'affiche dans la barre d'adresse et dans la fenêtre de firebug. Quelle méthode a été utilisée ? Pourquoi ? Comment envoyer d'autres données en éditant la barre d'adresse ?
3. Ajouter un champ sans attribut name, un champ à l'extérieur des balises ``<form></form>``, et soumettez les données. Que se passe-t-il ?
4. A quoi sert l'attribut value ?
5. Essayer d'envoyer plusieurs valeurs associées à la même clé. A quel type de champ de formulaire cela correspond-il ? Que se passe-t-il côté serveur ? Comment faire pour récupérer toutes les valeurs côté serveur ?
6. Changer la méthode du formulaire et soumettre des données. Constater que Firebug/Réseau permet toujours de visualiser les données envoyées alors qu'elles ne sont plus visibles dans la barre d'adresse.
7. Est-il possible d'utiliser plusieurs boutons de soumission dans un même formulaire ?

### Exercice 2 : display_ACorriger.html

**Objectif : Comprendre la manière dont le navigateur construit le DOM, découvrir les premières interactions en javascript**

1. Corriger le code du fichier display_ACorriger.html pour que les deux boutons fonctionnent à nouveau
2.  Mettre en oeuvre 3 solutions
3.  Afficher et cacher tour à tour les boutons pour qu'il n'y en ait toujours qu'un seul visible à la fois.
4. Supprimer un bouton et modifier le code pour que le même bouton puisse servir à cacher/afficher. Utiliser le mot-clé « this ».

### Exercice 3 : TryIt Editor

Nous souhaitons implémenter le formulaire proposé sur le site de W3Schools permettant de tester la syntaxe des langages HTML et CSS.

1. Un champ textarea permet d'éditer du code HTML, Un div placé à côté montre le rendu correspondant lorsque l'utilisateur clique sur un bouton. On pensera à utiliser des variables globales pour enregistrer des références vers les cadres d'édition et d'affichage.
2. Une case à cocher est placée à côté du bouton. Elle est associée au label 'automatiquement'.
3. Si la case est cochée, nous souhaitons mettre en place un mécanisme permettant une mise à jour à chaque modification du champ textarea. Nous utiliserons l'événement onkeyup. Pourquoi l'événement onchange n'est pas conseillé pour détecter les changements ? Comment connaître l'état de la case à cocher ?
4. 2ème version : Afficher des infos-bulles lorsque l'utilisateur déplace sa souris au dessus du bouton ou de la case à cocher
5. 3ème version : Nous souhaitons que la mise à jour automatique se déroule à intervalles réguliers, en utilisant la méthode window.setTimeout. Quels sont les arguments de cette méthode ? Quelle est leur nature ?
* On informera l'utilisateur que quelquechose se passe en affichant une image de chargement (que l'on peut récupérer sur le site ajaxload.com), en s'arrangeant pour qu'elle soit visible suffisamment longtemps.
* On désactivera la mise à jour automatique en utilisant la touche « ESC »

### Exercice 4 : Les paragraphes magiques

Nous souhaitons que certains paragraphes de notre page deviennent éditables lorsqu'on les clique.

1. Le paragraphe réagit au survol de souris en s'entourant d'une bordure pour montrer à l'utilisateur qu'il est particulier, un popup lui expliquant qu'il peut cliquer se place à côté de la souris.
2. Son contenu peut être édité à l'aide d'un textarea lorsqu’on le clique avec la souris
3. Le code supporte un nombre quelconque de paragraphes magiques, mais il ne faut pas que l'édition d'un paragraphe soit annulée si l'on appuie sur un autre. Les popups sont désactivés lorsqu'une édition est en cours.
4. L’édition se termine lors de l’appui sur la touche ‘ESC’
5. Lors du survol d'un paragraphe, une croix s'affiche pour pouvoir le supprimer si on clique dessus

### Exercice 5 : Formulaire de création de compte

Nous souhaitons construire un formulaire de création de compte en facilitant la tâche de l'utilisateur. Nous lui suggérerons un mot de passe et lui indiquerons si ses identifiants correspondent bien aux contraintes qui lui sont imposées : choisir au moins une lettre minuscule, une lettre majuscule et un chiffre pour son mot de passe, entre 6 et 8 lettres pour son login. Tous les champs texte devront être remplis.

1. Nous utiliserons le formulaire fourni. Définir le paramètre action du formulaire avec comme cible le fichier php de l'exercice 1. Ajouter deux boutons radio pour choisir le sexe, un menu déroulant pour choisir la promo. Permettre la sélection de plusieurs centres d'intérêt et plusieurs compétences à la fois. Donner des noms aux champs, effectuer une première soumission et vérifier que toutes les données sont correctement récupérées côté serveur.
2. Définir les labels de chacun des champs, et donner des légendes pour chaque ensemble proposé, à l'aide des balises fieldset/legend. Associer un identifiant css à chaque ensemble pour pouvoir le contrôler. Associer la classe « info » à chacun des labels de champ d'entrée texte (nom, prenom, dateNaissance, login, passe).
3. Des images sont fournies pour cet exercice, au format svg et png. Quelle est la différence entre ces formats ? Peuvent-il être affichés tous les deux à l'aide d'une balise img ou comme image de fond ?
4. Établir une feuille de style pour cette page : Aligner tous les champs de formulaire verticalement en leur donnant une taille identique. A l'aide de la classe info, afficher à gauche de chaque label un fond comportant l'image « ampoule » fournie. Définir une classe valide et une classe invalide qui sera utilisée pour chaque champ pour lui donner une image de fond. Un champ valide comporte à sa droite un smiley souriant, un champ invalide un smiley mécontent. La bordure d'un champ d'entrée ayant le focus doit être coloriée en rouge.
5. Lorsqu'un champ est cliqué, on souhaite que son contenu soit sélectionné pour faciliter l'édition.
6. Créer une fonction javascript qui sera appelée lorsque l'utilisateur passera la souris au dessus d'un champ label de classe info, pour afficher un popup d'explication sur le champ à remplir. Cette fonction prendra en paramètre une chaîne de caractères précisant le nom du champ survolé. Nous souhaitons offrir à l'utilisateur la possibilité de générer son propre mot de passe automatiquement, et d'afficher ou cacher le champ de mot de passe pour pouvoir visualiser son contenu en toutes lettres.
7. Définir des gestionnaires d'événements pour les boutons du formulaire permettant d'offrir ces fonctionnalités. Le mot de passe généré devra être aléatoire, mais respecter les contraintes indiquées dans l'introduction de l'exercice. Nous souhaitons informer l'utilisateur de l'état de son formulaire, pour lui préciser s'il a oublié de remplir des champs, et si les champs qu'il a remplis respectent les critères précédents.
8. Développer une fonction prenant en paramètre une référence sur le champ à tester et renvoyant un booléen caractérisant le respect des contraintes. On se servira d'expressions régulières pour l'implémentation de cette fonction. La fonction modifiera également la classe du champ considéré pour lui donner la valeur « valide » ou « invalide ».
9. Appeler la fonction de validation d'un champ à chaque modification de son contenu.
10. Rédiger une fonction validant tous les champs textes d'un coup, en utilisant la méthode ``getElementsByTagName``, et l'appeler lorsque le navigateur a terminé de charger la page Nous souhaitons donner l'impression à l'utilisateur que le formulaire est très court, de manière à ne pas le décourager et obtenir le plus haut taux de transformation de notre « tunnel de création de compte » et ne 1 lui afficher que les champs utiles à chaque étape.
11. Une étape est associée à un ensemble de champs dans un fieldset. Au chargement de la page, seul le premier ensemble est affiché. Un bouton est généré dynamiquement lorsque tous les champs de cet ensemble sont valides, pour passer à l'ensemble suivant.
12. Lorsque ce bouton est cliqué, l'ensemble en cours est caché, l'ensemble suivant s'affiche.
13. Vérifier qu'à la fin de la validation du dernier ensemble de champs, l'ensemble des données de formulaire est bien envoyé au serveur.
14. Générer un fil d'Ariane dans l'entête de votre page permettant à l'utilisateur de connaître le nombre d'étapes de votre tunnel, l'étape en cours et de revenir aux étapes précédentes.