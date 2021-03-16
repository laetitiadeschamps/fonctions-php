# fonctions php


### général 
- *empty($variable)* : permet de vérifier si une variable (**argument 1**) est vide. **Retourne true / false.**
- *isset($variable)* : permet de vérifier si une variable (**argument 1**) existe. **Retourne true / false.**

### int
- *number_format($number, $nbDécimales, $séparateurDecimales, $séparateurMilliers)* : Permet de formater un nombre $number(**argument 1**), de préciser le nombre de chiffres après la virgule à afficher (**argument 2**), de préciser comment séparer visuellement les décimales (**argument 3**), de préciser comment séparer visuellement les milliers et les centaines (**argument 4**). **Retourne le nombre reformaté.**


### arrays
- *count($array)* ou *sizeof($array)*  : retourne la taille (nombre de valeurs) d'un tableau $array(**argument1**).
- *array_push($array, $valeur)* : ajoute une valeur (**argument 2**) à la fin d'un array(**argument 1**). **Retourne la longueur du nouveau tableau**.
- *array_unshift($array, $valeur)* : ajoute une valeur (**argument 2**) au début d'un array (**argument 1**). **Retourne la longueur du nouveau tableau**.
- *array_pop($array)* : supprime la dernière valeur d'un array(**argument 1**). **Retourne la valeur supprimée**.
- *array_shift($array)* : supprime la premiere valeur d'un array(**argument 1**). **Retourne la valeur supprimée**.
- *in_array($valeur, $array)* : recherche si une valeur (**argument 1**) apparait dans un array (**argument 2**). **Retourne true ou false**.
- *array_search($valeur, $array)* : recherche si une valeur(**argument 1**) apparait dans un array (**argument 2**). **Retourne false si la valeur n'apparait pas. Retourne son index dans la tableau si la valeur apparait**.
- *array_key_exists($key, $array)* : recherche si une valeur(**argument 1**) apparait comme index dans un array (**argument 2**). **Retourne true / false**.
- *min($array)* : recupère la valeur minimum dans un array (**argument 1**). **Retourne la valeur récupérée**.

### strings
- *strlen($string)* : renvoie la longueur de la chaîne de caractère en **argument 1**. **Retourne le nombre de caractères**.
- *substr($variable, $index de départ, $nb_caractères)* : renvoie une portion d'une string (**argument 1**). Cette portion débutera par la valeur précisée en (**argument 2**), et s'arrêtera selon la valeur précisée en (**argument 3**).**Retourne la portion choisie**.
*l'index(**argument2**) correspond au nombre de caractères à partir duquel débute la sélection, à partir de 0. Si l'index est négatif, il indique le nombre de caractères à partir duquel débute la sélection, mais en partant de la fin de la chaîne de caractères.*
*Le nombre de caractères(**argument 3**) correspond à la longueur du texte à sélectionner s'il est positif. Si le nombre est négatif, il correspond à l'index où la sélection s'arrête, à partir de la fin. S'il n'est pas précisé, la sélection ira jusqu'à la fin de la chaîne*.
*Dans une string,l'index commence à 0 et augmente de 1 à chaque caractère (ex : Dans "Hello World, le "e" a un index de 1 / "d" a l'index 10 ou -1)*
- *substr_replace($variable de départ, $variable à remplacer, $index de départ, $nb_caractères)* : remplace une string ou une partie d'une string(**argument 1**) par une autre(**argument 2**). La portion à remplacer dans l'**argument 1** débutera par la valeur précisée en **argument 3**, et récupèrera le nombre de caractères spécifié en **argument 4**. Le texte en **argument 2** sera ajouté à la place de la portion définie grâce aux arguments 3 et 4. **Retourne la string créée**. *Mêmes remarques que pour substr*.
- *strstr($string, $valeur)* : recherche une valeur (**argument 2**) dans une chaine de caractères (**argument 1**). **Retourne la portion de la chaîne de caractères débutant à la première occurence du mot cherché et jusqu'à la fin de la chaîne de caractère. Renvoie false si le mot n'apparait pas**. *stristr est identique mais n'est pas sensible à la casse pour la recherche*.

## Changements de types
- *implode($séparateur, $array)* : convertit un array en string. Met bout à bout les valeurs d'un tableau(**argument 2**) en les séparant par le séparateur indiqué (**argument 1**). **Retourne la string finale**.
- *str_split($string, $longueur)* : convertit une string en array. Eclate les valeurs d'une string(**argument 1**) en différentes valeurs dans un array. si la longueur (**argument 2**) n'est pas précisée, chaque lettre sera une valeur du tableau. Si elle est précisée, la string (**argument 1**) sera éclatée en segments de la longueur de l'**argument 2**, et chaque segment sera une valeur du tableau. **Retourne l'array final**.
- *explode($separateur, $string)* : convertit une string en array. Eclate les valeurs d'une string(**argument 2**) en différentes valeurs dans un array. A chaque occurrence du séparateur indiqué (**argument 1**), une nouvelle valeur sera créee dans le tableau. **Retourne l'array final**.
- *intval($variable)* : transforme une string (**argument 1**) en int. **Retourne l'int créé**.

## Serveur
- *mail($destinataire, $sujet, $message)* : envoie un mail au destinataire (**argument 1**) ayant comme sujet l'**argument 2** et comme corps de texte l'**argument 3**. Des paramètres optionnels permettent de rajouter un expéditeur entre autres.  **Retourne true/false selon si l'envoi a fonctionné**.
- *header('Location:$url')* : redirige vers la page indique en $url (**argument 1**). **Pas de valeur de retour**.

## Dates
- *date($format, $timestamp)* : convertit une date au format mentionné en **argument 1**. Si le $timestamp(**argument 2**) n'est pas précisé, la date du jour sera utilisée. Sinon ce sera la date en **argument 2**. **Retourne la date créée** 
- *Ex : Date('j/m/Y') affichera une date au format 01/01/2021* 
Notations pour le $format : j => numéro du jour / m => numéro du mois / F=> nom du mois / y => année sur 2 chiffres Y => année sur 4 chiffres / h=> heures / i=> minutes / s=> secondes / l=> jour de la semaine
Les noms de mois apparaissent en anglais par défaut, il faut configurer la locale en français avec `setlocale(LC_TIME,"fr_FR.UTF-8","French_France.1252");`.