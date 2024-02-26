Débogage JS
Exécution de scripts JS 

Javascript est un langage qui s’exécute dans le navigateur. Les programmes JS peuvent être directement inclus dans des balises HTML <script>, comme suit:
![alt text](/public/assets/exemple.png)
index.html

<!DOCTYPE html>
<html>
    <head>
        <script>
            alert("ceci est un message");
        </script>
    </head>
    <body></body>
</html>
ou encore inclus comme des fichiers qu’on désigne en utilisant l’attribut src de l’élément <script>:

index.html

<!DOCTYPE html>
<html>
    <head>
        <script src="monProgramme.js"></script>
    </head>
    <body></body>
</html>
monProgramme.js

alert("ceci est un message")
Outils de développement

Dans ce cours nous utiliserons les outils de développement de Firefox. Pour y accéder, faites CTRL-Maj-I dans le navigateur.

Console

La console permet d’évaluer directement des expressions en JS ou encore d’afficher des messages à partir d’un programme.

Pour évaluer des expressions il suffit de les taper sur la ligne de commande : console

Pour afficher des messages à partir d’un programme il faut utiliser console.log() dans le programme, comme ceci:

monProgramme.js:

console.log("Message à la console");
Au chargement de la page (et donc, de l’exécution du script JS), on verra le message apparaître: console-log

Débogueur

Les outils de développement de Firefox incluent un débogueur; parmi ses fonctionnalités il y a les points d’arrêt qui permettent de suspendre le flot d’exécution du programme et d’y inspecter les valeurs des variables. Ceci est très utile pour de détecter la cause des erreurs qui apparaissent au moment de l’exécution.

Pour mettre en pause un programme lorsqu’il arrive à une instruction donnée, il suffit de cliquer sur la marge de la ligne correspondante, ce qui crée un point d’arrêt (représenté par un marqueur bleu). Lors du rechargement de la page, l’exécution sera suspendue à cet endroit et les valeurs des variables (ici, i: 1 et limite: 1000) seront affichées:

debug-bp

La touche F10 permet de passer à la prochaine instruction et ainsi de poursuivre ligne par ligne l’exécution du programme.
La touche F8 continue l’exécution du programme. Évidemment, puisqu’ici le point d’arrêt est dans une boucle, le programme sera de nouveau suspendu à la prochaine itération.
Il est possible d’associer des conditions aux points d’arrêt afin que le programme s’arrête seulement lorsque les variables ont une valeur spécifique. Pour ce faire il faut se placer sur la ligne du point d’arrêt et faire CTRL-Maj-B, puis définir la condition:

debug-bpcond

Les points d’arrêt conditionnels sont identifiés par un marqueur jaune.
