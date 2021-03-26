# fonctions php


### général 
- *typeof(variable)* :**Retourne le type de la variable en argument 1**.

### int
- *num.toFixed(nbDécimales)* : Arrondit un **num** avec un nombre spécifique de chiffres apres la virgule (spécifié en **argument 1**). **Retourne le nombre arrondi**.

### arrays
- *array.length*  : retourne la taille (nombre de valeurs) d'un **array**.
- *array.push(valeur)* : ajoute une valeur (**argument 1**) à la fin d'un **array** . **Retourne la longueur du nouveau tableau**.
- *array.unshift(valeur)* : ajoute une valeur (**argument 1**) au début d'un **array** . **Retourne la longueur du nouveau tableau**.
- *array.pop()* : supprime la dernière valeur d'un **array** . **Retourne la valeur supprimée**.
- *array.shift()* : supprime la premiere valeur d'un **array** . **Retourne la valeur supprimée**.
- *array.indexOf(valeur, départ)* : recherche si une valeur (**argument 1**) est contenu dans **un array** . Si un départ (**argument 2**) est spécifié, la recherche commence au point de départ spécifié. **Retourne -1 si pas de correspondance ou l'index de la première occurence de la valeur.**
- - *array.includes(valeur)* : recherche si une valeur (**argument 1**) est contenu dans un **array**. **Retourne true / false**.
- *array.splice(indexDépart, longueur, remplacement)* : Supprime et remplace certaines valeurs dans un **array**, la sélection supprime les valeurs en partant de celle à  l'index **argument 1**, jusqu'à la valeur en index **argument 2**. Les caractères en **argument 3** seront ajoutés à la place de la section supprimée. **Retourne la portion du tableau conservée**.
  *L'**argument 1** si positif : index de la valeur  à partir de laquelle la supression commence. Si négatif, position de la valeur de départ en partant de la fin du tableau.*
   *L'**argument 2** si positif : nombre de valeurs à supprimer. Si absent, supprime toutes les valeurs jusqu'à la fin de l'array.*
- *array.slice(indexDépart, longueur)* : Conserve certaines valeurs dans un array, la sélection démarre selon l'index **argument 1**, jusqu'à la valeur en index **argument 2**.  **Retourne la portion du tableau conservée**.
  *L'**argument 1** si positif : index de la valeur  à partir de laquelle la sélection commence. Si négatif, position de la valeur de départ en partant de la fin du tableau.*
   *L'**argument 2** si positif : nombre de valeurs à sélectionner. Si absent, sélectionne toutes les valeurs jusqu'à la fin de l'array. Si négatif, la sélections s'arrête à l'élement ayant l'index **argument 2** en partant de la fin*.
   - *array.concat(array2, array3 ...)* : créé un seul tableau à partir de plusieurs tableau (**array** + les arrays en **arguments**)
  
### strings
- *string.length* : renvoie la longueur de la **string**. **Retourne le nombre de caractères**.
- *string.substr(index de départ, nb_caractères)* : renvoie une portion d'une **string**. Cette portion débutera par la valeur précisée en (**argument 1**), et s'arrêtera selon la valeur précisée en (**argument 2**).**Retourne la portion choisie**.
*l'index(**argument 1**) correspond au nombre de caractères à partir duquel débute la sélection, à partir de 0. Si l'index est négatif, il indique le nombre de caractères à partir duquel débute la sélection, mais en partant de la fin de la chaîne de caractères.*
*Le nombre de caractères(**argument 2**) correspond à la longueur du texte à sélectionner. Si le nombre est négatif, il sera dremplacé par 0. S'il n'est pas précisé, la sélection ira jusqu'à la fin de la chaîne*.
*Dans une string,l'index commence à 0 et augmente de 1 à chaque caractère (ex : Dans "Hello World, le "e" a un index de 1 / "d" a l'index 10 ou -1)*

### Changements de types
- *array.join(separateur)* : convertit un **array** en string. Met bout à bout les valeurs d'un array en les séparant par le séparateur indiqué (**argument 1**). **Retourne la string finale**.

- *string.split(separateur)* : convertit une **string** en array. Eclate les valeurs d'une string en différentes valeurs dans un array. A chaque occurrence du séparateur indiqué (**argument 1**), une nouvelle valeur sera créee dans le tableau. **Retourne l'array final**.

- *parseInt(string, base)* : convertit un string (**argument 1**) en nombre selon la base choisie en **argument 2**. **Retourne le nombre**.
- *Number(string)* : convertit un string (**argument 1**) en nombre. **Retourne le nombre**.
- *number.toString()* : convertit un **number** en string. **Retourne la chaine de caractères créée**.
### Serveur

### Autres

- *prompt(texte à afficher)* : Ouvre une fenêtre contenant le texte en **argument 1** et un champ de saisie. **Retourne la valeur saisie par l'utilisateur.**

### Boucles

for(... in ...) : récupère les clés d'un tableau
for(... of ...) : récupère les valeur d'un tableau

### DOM

#### Création élement
- *document.createElement('balise')* : créé un élement de type balise (**argument 1**). Il n'est pour l'instant pas dans l'arborescence du DOM. **Retourne l'élement créé**.
- *element.appendChild(nouvelElememnt)* : ajoute le nouvelElement (**argument 1**) dans l'arborescence du DOM. Il sera placé comme dernier enfant de l'élement spécifié **element**. **Retourne l'enfant ainsi ajouté à l'arbo**.

### Modification d'un élement
- *element.textContent = 'texte'* : ajoute du texte dans **element**.
- *element.innerHTML = 'texte'* : ajoute du contenu HTML dans **element** (balises HTML, texte).
- *element.classList.add('nom de classe')* : ajoute à **element** une classe spécifiée en **argument 1**.
- *element.classList.remove('nom de classe')* : enlève à **element** une classe spécifiée en **argument 1**.
- *element.classList.toggle('nom de classe', condition)* : enlève ou ajoute à **element** une classe spécifiée en **argument 1** selon une condition (**argument 2**). Si pas de condition, l'ajoute ou l'enlève selon si elle est présente ou non.
- *element.classList.replace('nom de classe à remplacer', nom de la nouvelle classe)* : remplace pour **element** une classe spécifiée en **argument 1** par une classe spécifiée en **argument 2**.
- *element.attribut =texte*  : ajoute ou modifie la valeur d'un **attribut** d'un **element**.

### events
(à utiliser avec un argument (event) dans la fonction qui gère l'évènement)
- *event.target* : renvoie la cible de l'évènement (si clic, renvoie l'objet qui a été cliqué.) On peut donc récupérer toutes les infos de cet élement avec event.target.id, event.target.value etc ...
- *event.currentTarget* : élement sur lequel est placé l'eventlistener. Si l'eventhandler est placé sur une élement 1 qui contient un élement 2. Si on clique sur l'élement 2, currentTarget sera = 1, car l'eventlistener est placé sur l'élement 1. event.target sera 2, car c'est l'élement réel sur lequel le clic a été fait (mmais étant enfant de l'élement 1, il aura déclenché l'eventlistener placé sur 1).