
# Cheatsheet



## Variables et assignations

Les variables servent à stocker des choses en leur donnant un nom.

`var = x` : on assigne la valeur `x` à la variable `var`. C'est à dire qu'on stocke `x` dans la variable `var`. Si la variable `var` n'existe pas encore dans le programme, alors elle est créée. Si elle existe déjà, sa valeur est remplacée par `x`, c'est à dire qu'elle ne stocke plus ce qu'elle stockait avant, mais stocke maintenant `x`.

Exemples :

`ma_variable = 42` : la variable nommée `ma_variable` stocke le nombre 42.
`ma_variable = 66` : la variable nommée `ma_variable` stocke maintenant le nombre 66 et pas 42 !
`amelia = turtle.Turtle()` : la variable nommée `amelia` stocke une nouvelle tortue.

Les noms de variables ne doivent qu'être composés de lettres et chiffres en minuscules, séparés de `_` ("tirets du bas") et sans accents.

Evitez les noms de variables qui ne veulent rien dire comme `a`, `mlkqsd`, etc... Préférez des noms de variables qui correpondent au mieux à ce qu'elles contiennent. Par exemple, si vous avez une variable qui contient une liste de tortues, appellez la `tortues` (au pluriel !), si vous avez une variable qui contient un nombre de pièces d'or, appellez la `nombre_pieces_or`, ...


## Fonctions de base

`print(x)` : affiche `x` dans le terminal.
`input(texte)` : affiche le `texte`, puis récupère ce que l'utilisateur tape au clavier jusqu'à ce qu'il fasse **Entrée**.

## Module `turtle`

**Import et création de tortues**

`import turtle` : ligne à mettre au début du programme pour utiliser la tortue.
`amelia = turtle.Turtle()` : créer une variable `amelia` et stocker une nouvelle tortue dedans.

**Déplacement**

`turtle.forward(x)` : fait **avancer** la tortue de `x` pixels. Raccourci : `turtle.fd(x)`
`turtle.backward(x)` : fait **reculer** la tortue de `x` pixels. Raccourci : `turtle.bk(x)`
`turtle.right(x)` : fait **tourner** la tortue dans le **sens horaire** de `x` degrés. Raccourci : `turtle.rt(x)`
`turtle.left(x)` : fait **tourner** la tortue dans le **sens anti-horaire** de `x` degrés. Raccourci : `turtle.lt(x)`
`turtle.home()` : fait **revenir la tortue au centre de l’écran**.
`turtle.circle(x)` : dessine un cercle de rayon `x` pixels.
`turtle.circle(x, y, z)` : dessine un arc de cercle de rayon `x` pixels, ayant un arc de `y` degrés et un nombre de segments `z`.
`turtle.goto(x, y)` : fait que la tortue se déplace à la position `x`, `y` selon le système de coordonnées.

**Traces et couleurs**

`turtle.penup()` : lève le crayon. La tortue ne trace plus quand elle se déplace.
`turtle.pendown()` : baisse le crayon. La tortue trace à nouveau quand elle se déplace.
`turtle.pensize(x)` : change l'épaisseur du crayon à `x` pixels.
`turtle.pencolor("couleur")` : change la couleur du crayon selon une string ayant un nom de couleur. ex : `"red"`, `"green"`, `"blue"`, ...
`turtle.pencolor(x, y, z)` : change la couleur du crayon avec une valeur RGB.
`turtle.bgcolor("couleur")` : change la couleur du fond d'écran de la fenêtre.
`turtle.fillcolor("couleur")` : détermine la couleur de remplissage.
`turtle.beginfill()` : dit à la tortue de commencer à remplir une forme.
`turtle.endfill()` : dit à la tortue de finir de remplir une forme.
`turtle.clear()` : **efface les traces** laissées par la tortue.

**Divers**

`turtle.shape("turtle")` : remplace la flèche par une tortue.
`turtle.done()` : **ferme la fenêtre** de dessin.

## Module `random`
`import random` : importe le module random.
`random.randint(min, max)` : renvoie un nombre aléatoire entre `min` et `max` inclus.
`random.choice(liste)` : renvoie un élément choisit aléatoirement dans la `liste`.

## Commentaires

Un commentaire est une ligne qui commence par `#`. Cette ligne est ignorée par python et permet de laisser des indications et notes dans le code.

## Types

### String ou Chaînes de caractères

Les strings sont des morceaux de texte que le programme peut utiliser. On dit à python que du  texte qu'on écrit n'est pas du code, mais bien une string grâce aux guillements `""`.

`"ceci est une string"` : str / string (chaîne de caractère)

On peut faire des opérations sur les strings :

`"salut " + "ca va ?"` renvoie `"salut ca va"` : on concatène (c'est à dire qu'on rejoint ensemble) deux strings.

`"salut" * 5` renvoie `"salutsalutsalutsalutsalut"` : on répète la string un certain nombre de fois.

### Nombres

`42` : int / integer : nombre entier (sans virgules !)

`3.1415` : float / float : nombre décimal (avec virgules !). Attention, on utilise un point `.` et pas une virgule !

On peut faire des opérations mathématiques avec les nombres :

`x + y` : addition
`x - y` : soustraction
`x * y` : multiplication
`x / y` : division
`x ** y` : puissance
`x % y` : modulo

### Booleans

Un booléen (en français), est un type d'objet qui peut être vrai `True` ou faux `False`. C'est très pratiques pour les conditionnels.

`True` et `False` : bool / boolean (booléen)

## Listes

`ma_liste = []` : créer une variable nommée `ma_liste` qui stocke une liste **vide**.

`ingredients = ["beurre", "lait", "farine"]` : créer une variable nommée `ingredients` qui stocke une liste d'ingrédients (sous la forme de strings).

`taille_poids = [174, 65]` : créer une variable nommée `taille_poids` qui stocke une liste de deux nombres.

`ma_liste[i]` : récupère l'élement de la liste contenue dans la variable `ma_liste` selon son **index i**. Exemple : `ingredients[0]` donne `"beurre"`, `ingredients[2]` donne `"farine"`, ...

`ma_liste.append(x)` : ajoute `x` à la fin de la liste contenue dans la variable `ma_liste`.

`ma_liste[i] = x` : remplace l'élément de la liste contenue dans `ma_liste` ayant l'index `i` par le nouvel élément `x`.

`len(ma_liste)` : renvoie la longueur de la liste (c'est à dire, le nombre d'élément qu'elle contient).

Exemples :

```py
# Déclarer des listes
ma_liste = [] # liste vide
une_autre_liste = ["beurre", "lait", "farine"] # liste remplie
# Ajouter à la fin d'une liste
ma_liste.append("un nouveau truc dans ma liste")
# Indéxer un élément
une_autre_liste[0] # = "beurre"
une_autre_liste[1] # = "lait"
une_autre_liste[2] # = "farine"
# Changer un élément
une_autre_liste[1] = "oeuf" # change "lait" par "oeuf"
```

## Boucle for

```py
# Pour chaque nombre i dans la séquence allant de 0 à x - 1
# En gros : répète x fois !
for i in range(x):
	# Ton code à répéter doit être tabulé !
```

**Itérer par élément sur une liste :**
```py
# Pour chaque élément dans ma liste
for element in ma_liste:
	# Code se répètant pour chaque element dans ma_liste
```

**Itérer par index sur une liste :**
```py
# Pour chaque nombre i dans la séquence de nombres allant de 0 à la longueur de ma liste
for i in range(len(ma_liste)):
	# Stocke dans la variable element l'élément de la liste qui a l'index i
	element = ma_liste[i]
	# Code qui répétant pour chaque element dans ma_liste
```

**Générer une liste remplie n fois de l'élément x**

```py
# Créer une liste vide
ma_liste = []
# Répéter n fois
for i in range(n):
	# Ajouter x à la liste
	ma_liste.append(x)
```

**Générer une liste remplie de n tortues**

```py
import turtle
# Créer une liste vide
tortues = []
# Répéter n fois
for i in range(n):
	# Ajouter une tortue à la liste
	tortues.append(turtle.Turtle())
```

## Comparateurs

Les comparateurs permettent de comparer la valeurs de deux choses. Si la comparaison est vraie, le comparateur renvoie `True`, sinon par `False`.

`x == y` : égal à.
`x != y` : différent de.
`x > y` : strictement supérieur à.
`x < y` : strictement inférieur à.
`x >= y` : supérieur ou égal à.
`x <= y` : inférieur ou égal à.

## Opérateurs logiques
Les opérateurs logiques permettent de changer et combiner les booleans (`True` et `False`).

`not x` : change `True` en `False` et inversement.
`x and y` : `True` uniquement si x et y sont `True` ensemble, sinon `False`.
`x or y` : `True` si au moins l'un de x ou y est `True`, sinon `False`.

On peut mettre des parenthèses pour choisir dans quel ordre faire les opérations. Ex : `(not (x and y)) or z`

## Conditionnels

```py
if condition:
	# Code qui s'éxécutant si condition est True
elif condition2:
	# Code s'exécutant si condition2 est True
else:
	# Code s'éxécutant si aucune condition est True
```
