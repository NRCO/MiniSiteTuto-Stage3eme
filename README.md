# Mon Premier Site Web - Journal Tech & Gaming

Bienvenue ! Tu vas apprendre à créer ton premier site web : un journal en ligne sur les jeux vidéo et la technologie.

---

## Structure du projet

```
MiniSiteTuto/
├── index.html       ← Page d'accueil (À COMPLÉTER)
├── article1.html    ← Article GTA 6 (À CRÉER)
├── article2.html    ← Article PC Gaming (À CRÉER)
├── article3.html    ← Article Minecraft (À CRÉER)
├── style.css        ← Feuille de style (PRÊTE - à explorer)
├── images/          ← Dossier pour tes images
├── solutions/       ← Solutions (pour le tuteur uniquement !)
└── README.md        ← Ce fichier (instructions)
```

---

## Qu'est-ce qu'on va faire ?

Créer un mini-site web avec :
- Une page d'accueil qui liste des articles
- Des pages pour chaque article
- Des liens pour naviguer entre les pages
- Du style CSS pour rendre le site joli

---

## Comment utiliser ce projet ?

1. **Ouvre VS Code** (ou ton éditeur de code)
2. **Ouvre le dossier** `MiniSiteTuto`
3. **Suis les étapes** de ce README dans l'ordre
4. **Modifie les fichiers** comme demandé
5. **Teste** en ouvrant `index.html` dans ton navigateur

Les fichiers contiennent des commentaires `<!-- ... -->` pour te guider !

---

## JOUR 1 : Les bases du HTML

### Étape 1 : Comprendre ce qu'est le HTML

**HTML** signifie "HyperText Markup Language" (Langage de Balisage HyperTexte).

C'est le langage qui permet de créer des pages web. Il utilise des **balises** pour structurer le contenu.

Une balise ressemble à ça :
```html
<balise>contenu</balise>
```

- `<balise>` = balise ouvrante
- `</balise>` = balise fermante (avec le `/`)
- `contenu` = ce qui est affiché ou structuré

**Exemples concrets :**
```html
<h1>Ceci est un gros titre</h1>
<p>Ceci est un paragraphe de texte.</p>
```

---

### Étape 2 : Créer ta première page HTML

1. **Ouvre le fichier `index.html`** dans ton éditeur de code (VS Code)

2. **Regarde la structure de base :**

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Mon titre de page</title>
</head>
<body>
    <!-- Le contenu visible va ici -->
</body>
</html>
```

**Explications :**
| Balise | À quoi ça sert ? |
|--------|------------------|
| `<!DOCTYPE html>` | Dit au navigateur que c'est du HTML5 |
| `<html>` | Contient TOUT le code de la page |
| `<head>` | Informations sur la page (pas visible) |
| `<title>` | Titre dans l'onglet du navigateur |
| `<body>` | Tout ce qui est visible sur la page |
| `<!-- texte -->` | Commentaire (pas affiché, juste pour toi) |

---

### Étape 3 : Les balises essentielles

#### Les titres (h1 à h6)

Il y a 6 niveaux de titres, du plus grand au plus petit :

```html
<h1>Titre principal (le plus grand)</h1>
<h2>Sous-titre</h2>
<h3>Sous-sous-titre</h3>
<h4>Titre niveau 4</h4>
<h5>Titre niveau 5</h5>
<h6>Titre niveau 6 (le plus petit)</h6>
```

**Règle importante :** Une page ne doit avoir qu'UN SEUL `<h1>` !

#### Les paragraphes

```html
<p>Ceci est un paragraphe. Tu peux écrire autant de texte que tu veux ici.</p>

<p>Ceci est un autre paragraphe. Chaque balise p crée un nouveau bloc de texte.</p>
```

#### Les listes

**Liste à puces :**
```html
<ul>
    <li>Premier élément</li>
    <li>Deuxième élément</li>
    <li>Troisième élément</li>
</ul>
```

**Liste numérotée :**
```html
<ol>
    <li>Étape 1</li>
    <li>Étape 2</li>
    <li>Étape 3</li>
</ol>
```

- `<ul>` = Unordered List (liste non ordonnée = puces)
- `<ol>` = Ordered List (liste ordonnée = numéros)
- `<li>` = List Item (élément de liste)

---

### Étape 4 : Exercice pratique - Créer la page d'accueil

**Objectif :** Modifier le fichier `index.html` pour créer la page d'accueil du journal.

1. Ouvre `index.html`
2. Entre les balises `<body>` et `</body>`, ajoute :
   - Un titre `<h1>` avec le nom de ton journal (exemple : "GameZone News")
   - Un paragraphe `<p>` de bienvenue
   - Un titre `<h2>` "Nos derniers articles"
   - Une liste `<ul>` avec 3 titres d'articles fictifs

**Exemple de résultat attendu :**
```html
<body>
    <h1>GameZone News</h1>
    <p>Bienvenue sur le meilleur journal gaming du web !</p>

    <h2>Nos derniers articles</h2>
    <ul>
        <li>GTA 6 : Date de sortie confirmée !</li>
        <li>Les meilleurs PC gaming de 2024</li>
        <li>Minecraft : La nouvelle mise à jour arrive</li>
    </ul>
</body>
```

3. **Sauvegarde** (Ctrl + S)
4. **Ouvre le fichier dans ton navigateur** (double-clic sur le fichier ou clic droit > Ouvrir avec > Chrome/Firefox)

---

### Étape 5 : Les liens hypertextes

Les liens permettent de naviguer vers d'autres pages. C'est la balise `<a>` :

```html
<a href="page.html">Texte du lien</a>
```

- `href` = l'adresse de destination (une autre page, un site web...)
- Le texte entre `<a>` et `</a>` = ce qui est cliquable

**Exemples :**
```html
<!-- Lien vers une autre page de ton site -->
<a href="article1.html">Lire l'article</a>

<!-- Lien vers un site externe -->
<a href="https://www.google.com">Aller sur Google</a>
```

---

### Étape 6 : Exercice - Ajouter des liens

Modifie ta liste d'articles pour que chaque titre soit un lien cliquable :

```html
<ul>
    <li><a href="article1.html">GTA 6 : Date de sortie confirmée !</a></li>
    <li><a href="article2.html">Les meilleurs PC gaming de 2024</a></li>
    <li><a href="article3.html">Minecraft : La nouvelle mise à jour arrive</a></li>
</ul>
```

---

## JOUR 2 : Créer les pages d'articles

### Étape 7 : Structure d'un article

Un article de journal contient généralement :
- Un titre principal (`<h1>`)
- La date de publication
- Le contenu (plusieurs paragraphes)
- Un lien pour revenir à l'accueil

---

### Étape 8 : Créer ton premier article

1. **Ouvre le fichier `article1.html`**

2. **Complète-le avec ce contenu** (tu peux modifier le texte !) :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>GTA 6 - GameZone News</title>
</head>
<body>
    <a href="index.html">← Retour à l'accueil</a>

    <h1>GTA 6 : Date de sortie confirmée !</h1>
    <p><strong>Publié le 15 janvier 2024</strong></p>

    <p>Rockstar Games a enfin annoncé la date de sortie tant attendue de GTA 6 !
    Le jeu sortira à l'automne 2025 sur PlayStation 5 et Xbox Series X.</p>

    <h2>Ce qu'on sait sur le jeu</h2>
    <p>L'action se déroulera à Vice City, une ville inspirée de Miami.
    Pour la première fois, on pourra jouer une protagoniste féminine nommée Lucia.</p>

    <h2>Les nouveautés attendues</h2>
    <ul>
        <li>Carte plus grande que jamais</li>
        <li>Graphismes ultra-réalistes</li>
        <li>Nouveau mode multijoueur</li>
    </ul>

    <p><a href="index.html">← Retour à l'accueil</a></p>
</body>
</html>
```

**Nouvelle balise découverte :**
- `<strong>` = met le texte en **gras** (pour insister sur quelque chose)

---

### Étape 9 : Les images

Pour ajouter une image, on utilise la balise `<img>` :

```html
<img src="images/photo.jpg" alt="Description de l'image">
```

**Attention :** La balise `<img>` n'a PAS de balise fermante !

- `src` = source, le chemin vers l'image
- `alt` = texte alternatif (affiché si l'image ne charge pas, important pour l'accessibilité)

**Exemples :**
```html
<!-- Image dans le dossier images -->
<img src="images/gta6.jpg" alt="Screenshot de GTA 6">

<!-- Image depuis internet (URL) -->
<img src="https://exemple.com/image.jpg" alt="Une image du web">
```

**Pour redimensionner une image :**
```html
<img src="images/gta6.jpg" alt="GTA 6" width="400">
```
`width="400"` = largeur de 400 pixels

---

### Étape 10 : Exercice - Créer les autres articles

Maintenant, crée les fichiers `article2.html` et `article3.html` en suivant le même modèle.

**Pour article2.html (PC Gaming) :**
- Parle des composants importants (carte graphique, processeur, RAM...)
- Fais une liste des meilleurs PC

**Pour article3.html (Minecraft) :**
- Invente une mise à jour fictive
- Liste les nouvelles fonctionnalités

---

### Étape 11 : Améliorer la page d'accueil

Maintenant que tu maîtrises les bases, améliore ta page d'accueil :

1. Ajoute une description sous chaque lien d'article :

```html
<h2>Nos derniers articles</h2>

<h3><a href="article1.html">GTA 6 : Date de sortie confirmée !</a></h3>
<p>Rockstar Games annonce enfin la sortie du jeu le plus attendu...</p>

<h3><a href="article2.html">Les meilleurs PC gaming de 2024</a></h3>
<p>Notre sélection des meilleures configurations pour jouer...</p>

<h3><a href="article3.html">Minecraft : La nouvelle mise à jour arrive</a></h3>
<p>Découvrez toutes les nouveautés de la prochaine version...</p>
```

2. Ajoute une section "À propos" en bas de page :

```html
<h2>À propos</h2>
<p>GameZone News est un journal créé par [TON PRÉNOM] pendant un stage de découverte.</p>
```

---

### Étape 12 : Ajouter une barre de navigation

Une barre de navigation permet d'accéder rapidement aux différentes pages.

Ajoute ce code au début du `<body>` de CHAQUE page :

```html
<nav>
    <a href="index.html">Accueil</a> |
    <a href="article1.html">GTA 6</a> |
    <a href="article2.html">PC Gaming</a> |
    <a href="article3.html">Minecraft</a>
</nav>
```

La balise `<nav>` indique que c'est une zone de navigation.

---

## JOUR 2 (suite) : Introduction au CSS

### Étape 13 : Qu'est-ce que le CSS ?

**CSS** signifie "Cascading Style Sheets" (Feuilles de Style en Cascade).

Le CSS sert à **styliser** ta page web :
- Changer les couleurs
- Modifier les polices
- Ajouter des marges et espacements
- Organiser la mise en page

**HTML** = le contenu (texte, images, structure)
**CSS** = l'apparence (couleurs, tailles, positions)

---

### Étape 14 : Lier le CSS au HTML

Pour utiliser du CSS, on le met dans un fichier séparé `.css` et on le lie au HTML.

Dans le `<head>` de ta page HTML, ajoute cette ligne :

```html
<head>
    <meta charset="UTF-8">
    <title>Ma page</title>
    <link rel="stylesheet" href="style.css">
</head>
```

La balise `<link>` dit au navigateur d'aller chercher le fichier `style.css`.

---

### Étape 15 : Syntaxe du CSS

Le CSS fonctionne avec des **règles**. Chaque règle a :
- Un **sélecteur** : ce qu'on veut styliser
- Des **propriétés** : ce qu'on veut changer
- Des **valeurs** : comment on veut le changer

```css
sélecteur {
    propriété: valeur;
    autre-propriété: autre-valeur;
}
```

**Exemple concret :**
```css
h1 {
    color: blue;
    font-size: 32px;
}
```

Ce code signifie : "Tous les `<h1>` seront bleus et auront une taille de 32 pixels"

---

### Étape 16 : Les sélecteurs de base

| Sélecteur | Ce qu'il cible | Exemple |
|-----------|----------------|---------|
| `balise` | Toutes les balises de ce type | `p { }` cible tous les paragraphes |
| `.classe` | Éléments avec cette classe | `.date { }` cible `class="date"` |
| `#id` | L'élément avec cet id | `#menu { }` cible `id="menu"` |

**Exemple avec une classe :**

Dans le HTML :
```html
<p class="date">Publié le 15 janvier 2024</p>
```

Dans le CSS :
```css
.date {
    color: gray;
    font-style: italic;
}
```

---

### Étape 17 : Les propriétés CSS essentielles

#### Couleurs

```css
/* Couleur du texte */
color: red;
color: #3498db;           /* Code hexadécimal */
color: rgb(52, 152, 219); /* RGB */

/* Couleur de fond */
background-color: yellow;
background-color: #f5f5f5;
```

**Couleurs courantes :**
| Nom | Code hexa | Aperçu |
|-----|-----------|--------|
| black | #000000 | Noir |
| white | #ffffff | Blanc |
| red | #ff0000 | Rouge |
| blue | #0000ff | Bleu |
| green | #008000 | Vert |
| gray | #808080 | Gris |

#### Texte

```css
font-size: 16px;           /* Taille du texte */
font-family: Arial, sans-serif; /* Police */
font-weight: bold;         /* Gras */
font-style: italic;        /* Italique */
text-align: center;        /* Alignement (left, center, right) */
text-decoration: underline; /* Soulignement */
```

#### Espacements

```css
margin: 20px;      /* Espace EXTÉRIEUR (autour de l'élément) */
padding: 15px;     /* Espace INTÉRIEUR (dans l'élément) */

/* On peut aussi cibler un côté */
margin-top: 10px;
margin-bottom: 10px;
padding-left: 20px;
```

#### Bordures

```css
border: 1px solid black;  /* Épaisseur, style, couleur */
border-radius: 5px;       /* Coins arrondis */
```

---

### Étape 18 : Exercice - Explorer le fichier style.css

1. **Ouvre le fichier `style.css`** dans VS Code
2. **Lis les commentaires** (les lignes qui commencent par `/*`)
3. **Modifie quelques valeurs** et observe le résultat :
   - Change la couleur de `header` (ligne `background-color`)
   - Modifie la taille du titre `h1`
   - Change la couleur des liens

**Astuce :** Après chaque modification :
1. Sauvegarde le fichier CSS (Ctrl + S)
2. Actualise la page dans ton navigateur (F5)

---

### Étape 19 : Exercice - Personnaliser ton journal

Voici quelques modifications à essayer dans `style.css` :

**1. Changer le thème de couleurs :**
```css
/* Remplace les couleurs bleues par du vert */
nav {
    background-color: #27ae60; /* Vert */
}

header {
    background-color: #2ecc71; /* Vert clair */
}
```

**2. Modifier la police :**
```css
body {
    font-family: 'Georgia', serif; /* Police avec empattements */
}
```

**3. Ajouter un effet au survol des articles :**
```css
article:hover {
    background-color: #f0f0f0;
}
```

---

## Récapitulatif des balises HTML apprises

| Balise | Utilité |
|--------|---------|
| `<html>` | Contient toute la page |
| `<head>` | Métadonnées (titre, encodage...) |
| `<body>` | Contenu visible |
| `<h1>` à `<h6>` | Titres (du plus grand au plus petit) |
| `<p>` | Paragraphe |
| `<a href="...">` | Lien hypertexte |
| `<ul>` | Liste à puces |
| `<ol>` | Liste numérotée |
| `<li>` | Élément de liste |
| `<img src="..." alt="...">` | Image |
| `<strong>` | Texte en gras |
| `<nav>` | Zone de navigation |
| `<header>` | En-tête de la page |
| `<main>` | Contenu principal |
| `<article>` | Un article |
| `<footer>` | Pied de page |
| `<link>` | Lien vers un fichier externe (CSS) |
| `<!-- commentaire -->` | Commentaire (invisible) |

---

## Récapitulatif des propriétés CSS apprises

| Propriété | Utilité | Exemple |
|-----------|---------|---------|
| `color` | Couleur du texte | `color: blue;` |
| `background-color` | Couleur de fond | `background-color: #fff;` |
| `font-size` | Taille du texte | `font-size: 16px;` |
| `font-family` | Police | `font-family: Arial;` |
| `font-weight` | Graisse (gras) | `font-weight: bold;` |
| `text-align` | Alignement | `text-align: center;` |
| `margin` | Marge extérieure | `margin: 20px;` |
| `padding` | Marge intérieure | `padding: 15px;` |
| `border` | Bordure | `border: 1px solid black;` |
| `max-width` | Largeur maximum | `max-width: 800px;` |

---

## Bonus : Aller plus loin

Si tu as fini en avance, voici des défis supplémentaires :

### Défi 1 : Ajouter des images
Trouve des images libres de droits sur [Unsplash](https://unsplash.com) ou [Pexels](https://www.pexels.com/fr-fr/) et ajoute-les à tes articles.

### Défi 2 : Créer une page "Contact"
Crée une page `contact.html` avec :
- Un titre
- Un paragraphe expliquant comment te contacter
- Un lien email : `<a href="mailto:ton@email.com">Envoie-moi un email</a>`

### Défi 3 : Texte en italique et souligné
Découvre ces nouvelles balises :
- `<em>` = texte en *italique* (emphasis)
- `<u>` = texte souligné (underline)

### Défi 4 : Les tableaux
Crée un tableau comparatif :
```html
<table border="1">
    <tr>
        <th>Jeu</th>
        <th>Note</th>
    </tr>
    <tr>
        <td>GTA 6</td>
        <td>10/10</td>
    </tr>
    <tr>
        <td>Minecraft</td>
        <td>9/10</td>
    </tr>
</table>
```

---

## Comment tester ton site ?

1. **Sauvegarde tous tes fichiers** (Ctrl + S)
2. **Double-clique sur `index.html`** pour l'ouvrir dans ton navigateur
3. **Clique sur les liens** pour vérifier qu'ils fonctionnent
4. **Actualise la page** (F5) après chaque modification

---

## Problèmes fréquents

### "Mon lien ne marche pas"
- Vérifie que le nom du fichier dans `href="..."` correspond exactement au nom du fichier
- Attention aux majuscules ! `Article1.html` ≠ `article1.html`

### "Mon image ne s'affiche pas"
- Vérifie le chemin dans `src="..."`
- L'image doit être dans le bon dossier
- Vérifie l'extension (.jpg, .png, .gif...)

### "Le texte n'est pas formaté"
- Vérifie que tu as bien fermé toutes tes balises
- Une balise ouverte `<p>` doit être fermée `</p>`

---

## Bravo !

Tu as créé ton premier site web ! Tu connais maintenant :
- La structure d'une page HTML
- Comment créer des titres et paragraphes
- Comment faire des liens entre les pages
- Comment ajouter des images
- Comment créer des listes

C'est la base de TOUS les sites web sur internet !

---

*Projet créé pour un stage de découverte - 2 jours*
