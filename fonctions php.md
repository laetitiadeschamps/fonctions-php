# fonctions php


### général 
- *empty($variable)* : permet de vérifier si une variable (**argument 1**) est vide. **Retourne true / false.**
- *isset($variable)* : permet de vérifier si une variable (**argument 1**) existe. **Retourne true / false.**


### int
- *number_format($number, $nbDécimales, $séparateurDecimales, $séparateurMilliers)* : Permet de formater un nombre $number(**argument 1**), de préciser le nombre de chiffres après la virgule à afficher (**argument 2**), de préciser comment séparer visuellement les décimales (**argument 3**), de préciser comment séparer visuellement les milliers et les centaines (**argument 4**). **Retourne le nombre reformaté.**
- *base_convert($numero, $basedépart, $basefin)* : convertit un nombre (**argument 1**) d'une base **argument 2** à une base **argument 3**. **Retourne le nombre converti.**

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
- *splice($array, $indexDépart, $longueur, $remplacement)* : Supprime et remplace certaines valeurs dans un tableau (**argument 1**), la sélection supprime les valeurs en partant de celle à  l'index **argument 2**, jusqu'à la valeur en index **argument 3**. Les caractères en **argument 4** seront ajoutés à la place de la section supprimée. **Retourne la portion du tableau conservée**.
  *L'**argument 2** si positif : index de la valeur  à partir de laquelle la supression commence. Si négatif, position de la valeur de départ en partant de la fin du tableau*
  *L'**argument 3** si positif : nombre de valeurs à supprimer. Si absent, supprime toutes les valeurs jusqu'à la fin de l'array.*
  
### strings
- *strlen($string)* : renvoie la longueur de la chaîne de caractère en **argument 1**. **Retourne le nombre de caractères**.
- *substr($variable, $index de départ, $nb_caractères)* : renvoie une portion d'une string (**argument 1**). Cette portion débutera par la valeur précisée en (**argument 2**), et s'arrêtera selon la valeur précisée en (**argument 3**).**Retourne la portion choisie**.
*l'index(**argument2**) correspond au nombre de caractères à partir duquel débute la sélection, à partir de 0. Si l'index est négatif, il indique le nombre de caractères à partir duquel débute la sélection, mais en partant de la fin de la chaîne de caractères.*
*Le nombre de caractères(**argument 3**) correspond à la longueur du texte à sélectionner s'il est positif. Si le nombre est négatif, il correspond à l'index où la sélection s'arrête, à partir de la fin. S'il n'est pas précisé, la sélection ira jusqu'à la fin de la chaîne*.
*Dans une string,l'index commence à 0 et augmente de 1 à chaque caractère (ex : Dans "Hello World, le "e" a un index de 1 / "d" a l'index 10 ou -1)*
- *substr_replace($variable de départ, $variable à remplacer, $index de départ, $nb_caractères)* : remplace une string ou une partie d'une string(**argument 1**) par une autre(**argument 2**). La portion à remplacer dans l'**argument 1** débutera par la valeur précisée en **argument 3**, et récupèrera le nombre de caractères spécifié en **argument 4**. Le texte en **argument 2** sera ajouté à la place de la portion définie grâce aux arguments 3 et 4. **Retourne la string créée**. *Mêmes remarques que pour substr*.
- *strstr($string, $valeur)* : recherche une valeur (**argument 2**) dans une chaine de caractères (**argument 1**). **Retourne la portion de la chaîne de caractères débutant à la première occurence du mot cherché et jusqu'à la fin de la chaîne de caractère. Renvoie false si le mot n'apparait pas**. *stristr est identique mais n'est pas sensible à la casse pour la recherche*.

### Changements de types
- *implode($séparateur, $array)* : convertit un array en string. Met bout à bout les valeurs d'un tableau(**argument 2**) en les séparant par le séparateur indiqué (**argument 1**). **Retourne la string finale**.
- *str_split($string, $longueur)* : convertit une string en array. Eclate les valeurs d'une string(**argument 1**) en différentes valeurs dans un array. si la longueur (**argument 2**) n'est pas précisée, chaque lettre sera une valeur du tableau. Si elle est précisée, la string (**argument 1**) sera éclatée en segments de la longueur de l'**argument 2**, et chaque segment sera une valeur du tableau. **Retourne l'array final**.
- *explode($separateur, $string)* : convertit une string en array. Eclate les valeurs d'une string(**argument 2**) en différentes valeurs dans un array. A chaque occurrence du séparateur indiqué (**argument 1**), une nouvelle valeur sera créee dans le tableau. **Retourne l'array final**.
- *intval($variable)* : transforme une string (**argument 1**) en int. **Retourne l'int créé**.

### Serveur
- *mail($destinataire, $sujet, $message)* : envoie un mail au destinataire (**argument 1**) ayant comme sujet l'**argument 2** et comme corps de texte l'**argument 3**. Des paramètres optionnels permettent de rajouter un expéditeur entre autres.  **Retourne true/false selon si l'envoi a fonctionné**.
- *header('Location:$url')* : redirige vers la page indique en $url (**argument 1**). **Pas de valeur de retour**.
*N'oubliez jamais que header() doit être appelée avant que le moindre contenu ne soit envoyé, soit par des lignes HTML habituelles dans le fichier, soit par des affichages PHP. Une erreur très classique est de lire un fichier avec include ou require, et de laisser des espaces ou des lignes vides, qui produiront un affichage avant que la fonction header() ne soit appelée. Le même problème existe avec les fichiers PHP/HTML standards.*


### Dates
- *date($format, $timestamp)* : convertit une date au format mentionné en **argument 1**. Si le $timestamp(**argument 2**) n'est pas précisé, la date du jour sera utilisée. Sinon ce sera la date en **argument 2**. **Retourne la date créée** 
- *Ex : Date('j/m/Y') affichera une date au format 01/01/2021* 
Notations pour le $format : j => numéro du jour / m => numéro du mois / F=> nom du mois / y => année sur 2 chiffres Y => année sur 4 chiffres / h=> heures / i=> minutes / s=> secondes / l=> jour de la semaine
Les noms de mois apparaissent en anglais par défaut, il faut configurer la locale en français avec `setlocale(LC_TIME,"fr_FR.UTF-8","French_France.1252");`.

### Objets
  ## Classes 
Modèles qui permettront ensuite de créer des objets. On paramètre une classe en lui donnant des propriétés, des méthodes etc , et ainsi tous les objets créés à partir de ce modèle (appelées **instances**) auront automatiquement ces propriétés et méthodes. Il suffira lors de la création de l'instance de renseigner les valeurs à affecter aux propriétés. Les classes sont nommées en UpperCamelCase par convention, et on chaque classe créée doit être dans un fichier php séparé du même nom.

- Les propriétés peuvent être public ou private (nom à indiquer avant la déclaration de la propriété, qui determinera si la propriété est private ou public). Une propriété public sera accessible partout, même en dehors de la classe. Un propriété private ne sera accessible qu'à l'intérieur de la classe. Ce qui signifie qu'on ne pourra l'appeler que dans les méthodes de la classe.
On préfère mettre toutes les propriétés en private et les methodes en public, afin que les propriétés ne puissent pas être modifiées directement, mais que l'on soit obligés de passer par une méthode pour les modifier (la méthode permet de ne pas modifier directement la propriété, mais d'écrire du code afin de vérifier la valeur saisie avant de modifier).
Les propriétés d'un objet, si elles sont en public, sont accessible via **nomDeL'objet->nomDeLaPropriété**


- La methode __construct est à créer pour chaque classe. Toute méthode nommée __construct sera automatiquement exécutée lors de la création d'instances.
  Cette méthode sert principalement à affecter les bonnes valeurs aux propriétés de la nouvelle instance. En effet, lors de la déclaration des propriétés, on ne leur attribue pas de valeur, elles sont vides, mais elles existent. dans la méthode __construct, on indique en paramètre les informations dont la classe a besoin pour fonctionner. Ces informations seront fournies à chaque création d'instances. On donne ainsi le nombre de paramètres à fournir, et on affecte ces paramètres aux propriétés de nos variables.
  De même, Toute méthode nommée  __destruct sera automatiquement exécutée à la destruction d'un objet (fin de script ou destruction de la variable).
- les autres méthodes sont accessibles comme les propriétés via **nomDeL'objet->nomDeLaMethode()**. Elles permettent d'exécuter un même bout de code qui changera pour chaque objet selon les valeurs de ses propriétés.
- Getters et setters : On préfère comme dit plus haut être obligés de passer par des méthodes pour récupérer une propriété d'un objet ou pour modifier sa valeur. On peut donc créer des méthodes get et set pour chaque propriété. On peut aussi passer par des méthodes natives de php faites exprès pour : __get et __set :
- 
Au lieu d'avoir une méthode get par propriété et une méthode set par propriété, on aura une seule méthode get, qui prendra en argument la propriété que l'on souhaite récupérer, et une méthode set, qui prendra comme argument la propriété que l'on souhaite modifier et la nouvelle valeur que l'on souhaite lui attribuer. On pourra ensuite faire des conditions pour éxecuter un code ou un autre selon la propriété appelée.

* class Article {*--> création d'une classe nommée Article*
  * *--> Création des propriétés qu'auront les objets créés à partir de cette classe*
  * private $name;
  * private $title;
  * private $content;
  * 
  * *--> Création d'un constructor*
  * public function __construct($newName, $newTitle, $newContent) { *--> Ici on signale que pour que la classe fonctionne, à chaque création d'un nouvel objet Article il nous faudra 3 infos, la première sera stockée dans une variable $name, la deuxième dans une variable $title et la dernière dans une variable $content.*
  * $this->name = $newName; *-->Ici on indique que la première info reçue lors de la création de l'instance (que l'on avait stockée dans une variable $name) est à affecter à la propriété $name de notre objet. Le $this permet de dire que cette valeur sera à affecter à l'objet qui a appelé la méthode, donc celui qui vient d'être créé (la méthode __construct étant appelée automatiquement lors de la création de l'objet).*
  * $this->newTitle = $title;
  * $this->newContent = $content;
  * }
  *  *--> Création d'une méthode*
  *  public function getArticleName() {
     *  return $this->name; *Ici les $this permet de dire que l'on récupèrera la propriété $name de l'objet qui appelera la méthode. Par exemple, si l'on créé un objet article1 à partir de notre classe, la fonction $article1->getArticleName() renverra la propriété $name de l'article 1.*
  *  }
  *  *--> Création d'un getter*
  *  public function __get($property) { *--> lorsque l'on appelera cette méthode, on attend une info, que l'on stockera dans la variable $property*
     *  if('name' == $property) {
     *  *-->On execute du code spécifique si on a appelé __get(name)*
     *  } else if ('title' == $property) {
     *  } else if('content' == $property) {
     *  } else {
     *  echo "Cette propriété n'existe pas";
     *  }
  *  }

* }

- création d'un objet à partir de la classe Article (une instance) :
- $article1 = new Article('valeur 1', 'valeur 2','valeur 3');
- *Comme on l'a indiqué dans le constructor, il nous faut 3 valeurs pour faire fonctionner notre objet. Ici 'valeur 1' étant la première info entre parenthèses, quand le construcotr sera exécuté, il stockera dans la variable $newName la valeur 'valeur 1', et affectera cette valeur à la propriété $name de l'objet article1(avec le $this->name = $newName.*
- Notre article1 étant une instance de la classe Article, il aura par défaut les propriétés déclarées dans la classe Article, auquel PHP attribuera les valeurs indiquées entre parenthèses grâce au constructor, et pourra utiliser les méthodes déclarées dans la classe Article.