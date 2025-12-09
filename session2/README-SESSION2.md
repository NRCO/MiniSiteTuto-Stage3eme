# Session 2 : CSS Avancé, Tailwind & JavaScript

**Durée : 2 jours (Jour 3 et Jour 4)**

Bravo d'avoir terminé la Session 1 ! Tu sais maintenant créer des pages HTML et les styliser avec du CSS.

Dans cette session, tu vas apprendre :
- **Flexbox** : la mise en page moderne
- **Tailwind CSS** : un framework CSS ultra-populaire
- **JavaScript** : rendre ton site interactif !

> Tu as besoin d'avoir terminé la **Session 1** avant de commencer celle-ci.

---

## Fichiers de cette session

```
session2/
├── README-SESSION2.md      ← Ce fichier (instructions)
├── flexbox.html            ← Exercice Flexbox (À COMPLÉTER)
├── tailwind-demo.html      ← Découverte Tailwind (À EXPLORER)
├── mode-sombre.html        ← JS : Bouton mode sombre (À COMPLÉTER)
├── compteur-likes.html     ← JS : Compteur de likes (À COMPLÉTER)
├── quiz-gaming.html        ← JS : Quiz interactif (À COMPLÉTER)
└── solutions/              ← Solutions (pour le tuteur uniquement !)
```

---

## JOUR 3 : CSS Avancé

### Partie 1 : Flexbox - La mise en page moderne

#### Qu'est-ce que Flexbox ?

Flexbox (Flexible Box) est une méthode CSS pour organiser des éléments en lignes ou en colonnes. C'est **LA** technique moderne pour faire des mises en page.

Avant Flexbox, centrer un élément était compliqué. Maintenant :

```css
.conteneur {
    display: flex;
    justify-content: center;  /* Centre horizontalement */
    align-items: center;      /* Centre verticalement */
}
```

Et voilà, c'est centré !

---

#### Les propriétés Flexbox essentielles

**Sur le conteneur parent :**

| Propriété | Ce qu'elle fait | Valeurs courantes |
|-----------|-----------------|-------------------|
| `display: flex` | Active Flexbox | `flex` |
| `flex-direction` | Direction des éléments | `row` (ligne), `column` (colonne) |
| `justify-content` | Alignement horizontal | `flex-start`, `center`, `flex-end`, `space-between`, `space-around` |
| `align-items` | Alignement vertical | `flex-start`, `center`, `flex-end`, `stretch` |
| `gap` | Espace entre les éléments | `10px`, `20px`, `1rem` |
| `flex-wrap` | Retour à la ligne | `nowrap`, `wrap` |

**Exemple visuel :**

```
justify-content: space-between
┌─────────────────────────────────┐
│ [Élém 1]    [Élém 2]    [Élém 3]│
└─────────────────────────────────┘

justify-content: center
┌─────────────────────────────────┐
│      [Élém 1][Élém 2][Élém 3]   │
└─────────────────────────────────┘
```

---

#### Exercice 1 : Ouvre `flexbox.html`

Dans ce fichier, tu vas créer une galerie de cartes de jeux vidéo en utilisant Flexbox.

**Objectifs :**
1. Afficher les cartes côte à côte (pas empilées)
2. Centrer le titre de la page
3. Ajouter de l'espace entre les cartes
4. Faire en sorte que les cartes passent à la ligne sur petit écran

---

### Partie 2 : Les transitions CSS

Les transitions permettent d'animer les changements de style en douceur.

**Sans transition :**
```css
.bouton {
    background-color: blue;
}
.bouton:hover {
    background-color: red;  /* Changement instantané */
}
```

**Avec transition :**
```css
.bouton {
    background-color: blue;
    transition: background-color 0.3s ease;  /* Animation de 0.3 secondes */
}
.bouton:hover {
    background-color: red;  /* Changement progressif ! */
}
```

**Syntaxe :**
```css
transition: propriété durée timing-function;
```

- `propriété` : ce qui change (`background-color`, `transform`, `all`...)
- `durée` : temps de l'animation (`0.3s`, `500ms`...)
- `timing-function` : type d'animation (`ease`, `linear`, `ease-in-out`...)

**Astuce :** Utilise `transition: all 0.3s ease;` pour animer toutes les propriétés.

---

### Partie 3 : Les variables CSS

Les variables CSS permettent de définir des valeurs réutilisables.

**Déclarer des variables :**
```css
:root {
    --couleur-principale: #3498db;
    --couleur-texte: #333333;
    --espacement: 20px;
}
```

**Utiliser des variables :**
```css
h1 {
    color: var(--couleur-principale);
    margin-bottom: var(--espacement);
}

a {
    color: var(--couleur-principale);
}
```

**Avantage :** Change une seule fois `--couleur-principale` et tout le site change !

---

## JOUR 3 (suite) : Découverte de Tailwind CSS

### Qu'est-ce que Tailwind CSS ?

Tailwind est un framework CSS "utility-first". Au lieu d'écrire du CSS dans un fichier séparé, tu utilises des classes directement dans ton HTML.

**CSS classique :**
```html
<div class="carte">
    <h2>Titre</h2>
</div>
```
```css
.carte {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
```

**Avec Tailwind :**
```html
<div class="bg-white p-5 rounded-lg shadow">
    <h2>Titre</h2>
</div>
```

Pas besoin de fichier CSS séparé ! Tout est dans les classes.

---

### Installation via CDN (la méthode simple)

Ajoute simplement cette ligne dans le `<head>` de ton HTML :

```html
<script src="https://cdn.tailwindcss.com"></script>
```

C'est tout ! Tailwind est prêt à utiliser.

---

### Les classes Tailwind essentielles

#### Couleurs

| Classe | Effet |
|--------|-------|
| `bg-blue-500` | Fond bleu |
| `bg-red-500` | Fond rouge |
| `bg-green-500` | Fond vert |
| `bg-gray-100` | Fond gris clair |
| `bg-white` | Fond blanc |
| `text-blue-500` | Texte bleu |
| `text-white` | Texte blanc |
| `text-gray-700` | Texte gris foncé |

Les nombres (100 à 900) indiquent l'intensité : 100 = très clair, 900 = très foncé.

#### Espacements

| Classe | Effet |
|--------|-------|
| `p-4` | Padding de 1rem (16px) |
| `p-6` | Padding de 1.5rem (24px) |
| `px-4` | Padding horizontal |
| `py-2` | Padding vertical |
| `m-4` | Margin de 1rem |
| `mt-4` | Margin-top |
| `mb-4` | Margin-bottom |

#### Flexbox

| Classe | Effet |
|--------|-------|
| `flex` | display: flex |
| `flex-col` | flex-direction: column |
| `justify-center` | justify-content: center |
| `justify-between` | justify-content: space-between |
| `items-center` | align-items: center |
| `gap-4` | gap: 1rem |

#### Tailles et formes

| Classe | Effet |
|--------|-------|
| `w-full` | width: 100% |
| `max-w-md` | max-width: 28rem |
| `h-12` | height: 3rem |
| `rounded` | border-radius: 0.25rem |
| `rounded-lg` | border-radius: 0.5rem |
| `rounded-full` | border-radius: 9999px (cercle) |
| `shadow` | box-shadow léger |
| `shadow-lg` | box-shadow prononcé |

#### Texte

| Classe | Effet |
|--------|-------|
| `text-sm` | Petit texte |
| `text-lg` | Grand texte |
| `text-2xl` | Très grand texte |
| `font-bold` | Gras |
| `text-center` | Centré |

#### États (hover, focus)

| Classe | Effet |
|--------|-------|
| `hover:bg-blue-600` | Fond bleu au survol |
| `hover:scale-105` | Agrandir au survol |
| `focus:outline-none` | Pas de contour au focus |

---

### Exercice 2 : Ouvre `tailwind-demo.html`

Explore le fichier et essaie de :
1. Changer les couleurs des boutons
2. Modifier les espacements
3. Ajouter des effets au survol

---

## JOUR 4 : Introduction à JavaScript

### Qu'est-ce que JavaScript ?

JavaScript (JS) est le langage qui rend les sites web **interactifs**.

- **HTML** = Structure (le squelette)
- **CSS** = Apparence (les vêtements)
- **JavaScript** = Comportement (les actions)

Exemples d'utilisation :
- Réagir aux clics
- Modifier le contenu de la page
- Afficher/cacher des éléments
- Valider un formulaire
- Créer des jeux

---

### Où écrire du JavaScript ?

**Dans le HTML, avec la balise `<script>` :**

```html
<body>
    <!-- Ton contenu HTML -->

    <script>
        // Ton code JavaScript ici
        console.log("Bonjour !");
    </script>
</body>
```

**Important :** Place le `<script>` juste avant `</body>` pour que le HTML soit chargé avant l'exécution du JS.

---

### Les bases de JavaScript

#### 1. Les variables

Une variable stocke une valeur.

```javascript
// Déclarer une variable
let score = 0;
let pseudo = "Gamer42";
let estConnecte = true;

// Modifier une variable
score = 10;
score = score + 5;  // score vaut maintenant 15
```

- `let` = variable qui peut changer
- `const` = constante (ne change jamais)

#### 2. Les fonctions

Une fonction est un bloc de code réutilisable.

```javascript
// Déclarer une fonction
function direBonjour() {
    alert("Bonjour !");
}

// Appeler la fonction
direBonjour();
```

Fonction avec paramètre :
```javascript
function direBonjour(prenom) {
    alert("Bonjour " + prenom + " !");
}

direBonjour("Lucas");  // Affiche "Bonjour Lucas !"
```

#### 3. Sélectionner un élément HTML

Pour modifier un élément, il faut d'abord le sélectionner :

```javascript
// Par son ID
let titre = document.getElementById("mon-titre");

// Par sa classe (retourne une liste)
let boutons = document.querySelectorAll(".bouton");

// Le premier élément correspondant
let premierBouton = document.querySelector(".bouton");
```

#### 4. Modifier un élément

```javascript
let titre = document.getElementById("mon-titre");

// Changer le texte
titre.textContent = "Nouveau titre !";

// Changer le style
titre.style.color = "red";
titre.style.fontSize = "32px";

// Ajouter/enlever une classe CSS
titre.classList.add("important");
titre.classList.remove("cache");
titre.classList.toggle("visible");  // Ajoute si absente, enlève si présente
```

#### 5. Réagir aux événements

```javascript
let bouton = document.getElementById("mon-bouton");

// Quand on clique sur le bouton
bouton.addEventListener("click", function() {
    alert("Tu as cliqué !");
});
```

Événements courants :
- `click` : clic souris
- `mouseover` : survol
- `mouseout` : fin du survol
- `keydown` : touche pressée
- `submit` : formulaire envoyé

---

### Exercice 3 : Ouvre `mode-sombre.html`

Tu vas créer un bouton qui bascule entre le mode clair et le mode sombre.

**Ce que tu vas apprendre :**
- Sélectionner un élément
- Réagir au clic
- Utiliser `classList.toggle()`
- Manipuler les variables CSS

---

### Exercice 4 : Ouvre `compteur-likes.html`

Tu vas créer un compteur de likes pour un article.

**Ce que tu vas apprendre :**
- Créer et modifier des variables
- Mettre à jour le texte d'un élément
- Gérer plusieurs boutons

---

### Exercice 5 : Ouvre `quiz-gaming.html`

Tu vas créer un quiz sur les jeux vidéo !

**Ce que tu vas apprendre :**
- Les tableaux (arrays)
- Les conditions (if/else)
- Calculer un score
- Afficher un résultat

---

## Récapitulatif des nouvelles notions

### CSS Avancé

| Concept | Utilité |
|---------|---------|
| Flexbox | Mise en page en lignes/colonnes |
| `display: flex` | Active Flexbox |
| `justify-content` | Alignement horizontal |
| `align-items` | Alignement vertical |
| `gap` | Espace entre éléments |
| `transition` | Animation fluide |
| Variables CSS | Valeurs réutilisables |

### Tailwind CSS

| Concept | Exemple |
|---------|---------|
| Classes utilitaires | `bg-blue-500`, `p-4`, `rounded` |
| Hover states | `hover:bg-blue-600` |
| Flexbox | `flex`, `justify-center`, `items-center` |

### JavaScript

| Concept | Syntaxe |
|---------|---------|
| Variable | `let score = 0;` |
| Fonction | `function nom() { }` |
| Sélection | `document.getElementById("id")` |
| Événement | `element.addEventListener("click", ...)` |
| Modifier texte | `element.textContent = "..."` |
| Modifier classe | `element.classList.toggle("classe")` |

---

## Ordre recommandé

1. **Flexbox** (`flexbox.html`) - Comprendre la mise en page moderne
2. **Tailwind** (`tailwind-demo.html`) - Découvrir le framework
3. **Mode sombre** (`mode-sombre.html`) - Premier pas en JS
4. **Compteur** (`compteur-likes.html`) - Manipuler des variables
5. **Quiz** (`quiz-gaming.html`) - Projet final !

---

## Problèmes fréquents

### "Mon JavaScript ne marche pas"
- Ouvre la console du navigateur (F12 > Console) pour voir les erreurs
- Vérifie que le `<script>` est bien avant `</body>`
- Vérifie les fautes de frappe (JS est sensible aux majuscules)

### "classList.toggle ne fonctionne pas"
- Vérifie que l'élément existe (`console.log(element)` pour vérifier)
- Vérifie que la classe CSS existe dans ton fichier de styles

### "Tailwind ne s'applique pas"
- Vérifie que le CDN est bien dans le `<head>`
- Actualise la page (Ctrl + Shift + R pour vider le cache)

---

## Bravo !

À la fin de cette session, tu sauras :
- Créer des mises en page modernes avec Flexbox
- Utiliser Tailwind CSS pour styliser rapidement
- Rendre ton site interactif avec JavaScript

Ce sont les compétences utilisées par les vrais développeurs web !

---

*Session 2 - Projet stage de découverte*
