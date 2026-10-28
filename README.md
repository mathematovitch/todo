# Todo

Listes de tâches façon org-mode de [mathematovitch.github.io](https://mathematovitch.github.io/),
servies à **https://mathematovitch.github.io/todo/** (site de projet GitHub
Pages, branche `main`, aucun build).

- Une seule page autonome : `index.html` (HTML, CSS et JS en ligne, aucune dépendance),
  installable comme une appli (`manifest.webmanifest`, `sw.js`, `icons/`) et
  utilisable hors ligne (les changements partent au retour du réseau).
- Plusieurs listes (une par domaine : bouton « Listes conseillées »), export/import en
  `.txt`, mode sombre, police à chasse fixe.
- **Échéances** : vue « ⏰ Échéances » (toutes listes, en retard / aujourd'hui / 7 jours /
  plus tard), bandeau d'alerte, compteur dans le titre de l'onglet.
- Saisie rapide : `!Appeler le pédiatre @demain` (aussi `@lundi`, `@lun`, `@3/11`,
  `@3/11/27`) ; clic sur une tâche pour changer texte, date, importance ou liste.
- Multi-appareils : rechargement du gist au retour sur l'onglet ; si deux appareils ont
  modifié la todo, un bandeau propose de garder l'une ou l'autre version.
- Synchronisation par un **Gist GitHub** privé (`todo.txt`, repéré par le
  marqueur `outerovitch-todo-store-v1`) : le jeton (scope `gist` seulement)
  reste dans le `localStorage` du navigateur, jamais dans le dépôt.
- Icônes pixel Windows 95 lues dans `/assets/icons/` du site principal
  (`mathematovitch/mathematovitch.github.io`).

## Format de `todo.txt`

```
* Enfants & santé
- [ ] [#A] Appeler le pédiatre DEADLINE: <2026-11-03>
- [X] Racheter du Doliprane
```

`* ` = liste, `- [ ]` / `- [X]` = tâche, `[#A]` en tête = importante, `DEADLINE: <AAAA-MM-JJ>`
en fin = échéance (syntaxe org-mode). Une ancienne version de la page garde ces
marqueurs dans le texte sans rien perdre. La commande `envie` (coach,
`~/code/05-claude/coach`) lit ce fichier.

Extrait avec son historique du site principal le 2026-10-28.

## Aperçu local

Depuis `~/work/00.site` (pour que `../assets/` existe) :

```
ln -s ~/code/04-web/todo todo   # une fois, ignoré par git dans le site
python3 -m http.server          # puis http://localhost:8000/todo/
```
