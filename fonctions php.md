# fonctions php


### général 
- *empty($variable)* : permet de vérifier si une variable (**argument 1**) est vide. **Renvoie true / false.**
- *isset($variable)* : permet de vérifier si une variable (**argument 1**) existe. **Renvoie true / false.**
### strings


### int
- *number_format($number, $nbDécimales, $séparateurDecimales, $séparateurMilliers)* : Permet de formater un nombre $number(**argument 1**), de préciser le nombre de chiffres après la virgule à afficher (**argument 2**), de préciser comment séparer visuellement les décimales (**argument 3**), de préciser comment spéarer visuellement les milliers et les centaines (**argument 4**). **Renvoie le nombre reformaté.**


### arrays
- *count($array)* ou *sizeof($array)*  : retourne la taille (nombre de valeurs) d'un tableau $array(**argument1**).
- *array_push($array, $valeur)* : ajoute une valeur (**argument 2**) à la fin d'un array(**argument 1**). **Retourne la longueur du nouveau tableau**.
- *array_unshift($array, $valeur)* : ajoute une valeur (**argument 2**) au début d'un array (**argument 1**). **Retourne la longueur du nouveau tableau**.
- *array_pop($array)* : supprime la dernière valeur d'un array(**argument 1**). **Retourne la valeur supprimée**.
- *array_shift($array)* : supprime la premiere valeur d'un array(**argument 1**). **Retourne la valeur supprimée**.
- *in_array($valeur, $array)* : recherche si une valeur (**argument 1**) apparait dans un array (**argument 2**).**Renvoie true ou false**.
- *array_search($valeur, $array)* : recherche si une valeur(**argument 1**) apparait dans un array (**argument 2**).**Renvoie false si la valeur n'apparait pas. Renvoie son index dans la tableau si la valeur apparait**.
- *array_key_exists($key, $array)* : recherche si une valeur(**argument 1**) apparait comme index dans un array (**argument 2**).**Renvoie true ou false**.


## Changements de types
- *implode($séparateur, $array)* : convertit un array en string. Met bout à bout les valeurs d'un tableau(**argument 2**) en les séparant par le séparateur indiqué (**argument 1**). **Retourne la string finale**.
- *explode($separateur, $string)* : convertit une string en array. Eclate les valeurs d'une string(**argument 2**) en différentes valeurs dans un array. A chaque occurrence du séparateur indiqué (**argument 1**), une nouvelle valeur sera créee dans le tableau. **Retourne l'array final**.
- *intval($variable)* : transforme une string (**argument 1**) en int.**Retourne l'int créé**.
- *substr($variable, $index de départ, $nb_caractères)* : renvoie une portion d'une string (**argument 1**). Cette portion débutera par la valeur précisée en (**argument 2**), et récupèrera le nombre de caractères spécifié en (**argument 3**).**Retourne la portion choisie**.
*l'index correspond au nombre de caractères à partir duquel débuter la sélection, à partir de 0. Si l'index est négatif, il indique le nombre de caractères à partir duquel débuter la sélection, mais en partant de la fin*
*Le nombre de caractères correspond à la lingueur du texte à sélectionner s'il est positif. Si le nombre est négatif, il correspond à l'index où la sélection s'arrête, à partir de la fin*
*Dans une string,l'index commence à 0 et augmente de 1 à chaque caractère (ex : Dans "Hello World, le "e" a un index de 2*
- *substr_replace($variable de départ, $variable à remplacer, $index de départ, $nb_caractères)* : remplace une string ou une partie d'une string(**argument 1**) par une autre(**argument 2**). La portion à remplacer dans l'(**argument 1**) débutera par la valeur précisée en (**argument 3**), et récupèrera le nombre de caractères spécifié en (**argument 4**). Le texte en **argument 2** sera ajouté à la place de la portion définie grâce aux arguments 3 et 4. **Retourne la string créée**.

*Mêmes remarque que pour substr*

strstr($string, $motàchercher) => retourne la portion de string partant de la premiere occurence du mot à chercher, jusqu'à la fin
stristr =>
min($var)=> minimum tableau
