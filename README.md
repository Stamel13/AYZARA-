# AYZARA-
# AYZARA — Prototype éditorial

## Ouvrir le site
Ouvrez `index.html` dans un navigateur (double-clic ou glisser dans une fenêtre). Aucun serveur n'est nécessaire — tous les liens sont relatifs.

## Arborescence
```
ayzara/
├── index.html          Accueil
├── journal.html         Listing filtrable (Femmes, Lieux, Histoires, Savoir-faire, Art de vivre, Regards, Carnets)
├── article.html          Template article / essai / carnet
├── portrait.html         Template portrait de femme
├── lieu.html             Template lieu
├── maison.html           À propos
├── fondatrice.html       Page fondatrice
├── experiences.html      Les huit chapitres
├── assets/
│   ├── styles.css        Toute la direction artistique (couleurs, typo, composants)
│   └── script.js         Menu mobile, reveal au scroll, newsletter et recherche simulées, filtres
└── README.md
```

## Remplacer les images
Les visuels sont actuellement des dégradés de couleur (`.ph`) qui tiennent la place des photographies. Pour les remplacer :
1. Dans le HTML, remplacez `<div class="ph"></div>` par `<img class="ph" src="assets/images/votre-photo.jpg" alt="Description">`.
2. Placez vos fichiers dans un dossier `assets/images/`.
3. Conservez les proportions indiquées dans `styles.css` (`aspect-ratio`) pour ne pas casser la mise en page — elles sont réglées par type de carte (portrait rond 1/1, lieu 3/4, hero 16/8, etc.).

## Remplacer un article, un portrait ou un lieu
- **Article** (`article.html`) : dupliquez le fichier, changez le `<title>`, la catégorie (`.cat`), le titre, le sous-titre, les paragraphes de `.article-body`, et la citation dans `.pull-quote`.
- **Portrait** (`portrait.html`) : dupliquez le fichier, changez le nom, la fonction, et les cinq blocs `.qa-block` (Son histoire / Ce qu'elle transmet / Ce qu'elle regarde / Ce qu'elle veut préserver / Conversation).
- **Lieu** (`lieu.html`) : dupliquez le fichier, changez les quatre fiches `.lieu-facts` (territoire, type, époque, état) et le texte narratif.

Renommez chaque copie (ex. `article-femmes-derriere-les-murs.html`) et mettez à jour les liens correspondants dans `index.html` et `journal.html`.

## Ajouter une carte au Journal ou à l'accueil
Copiez un bloc `<a class="card" data-cat="...">…</a>` existant, changez le lien, le libellé de format (`.fmt`), la catégorie (`.cat`) et le titre. L'attribut `data-cat` doit correspondre à l'une des sept rubriques (`femmes`, `lieux`, `histoires`, `savoir-faire`, `art-de-vivre`, `regards`, `carnets`) pour que les filtres de `journal.html` fonctionnent.

## Newsletter et recherche
Le formulaire « Lettre AYZARA » et la barre de recherche sont actuellement simulés côté client (`assets/script.js`) — aucune donnée n'est envoyée à un serveur. Pour les rendre fonctionnels, il faudra les relier à un service d'emailing (Mailchimp, Brevo…) et, pour la recherche, à un index réel des contenus.

## Couleurs et typographies (à ne pas modifier sans raison)
Toutes les valeurs sont centralisées en haut de `styles.css`, dans `:root`. Modifier une couleur ou une police à un seul endroit suffit à la changer sur tout le site.
