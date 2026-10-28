# Todo

Listes de tâches façon org-mode de [mathematovitch.github.io](https://mathematovitch.github.io/),
servies à **https://mathematovitch.github.io/todo/** (site de projet GitHub
Pages, branche `main`, aucun build).

- Une seule page autonome : `index.html` (HTML, CSS et JS en ligne, aucune dépendance).
- Plusieurs listes, export/import en `.txt`, mode sombre, police à chasse fixe.
- Synchronisation par un **Gist GitHub** privé (`todo.txt`, repéré par le
  marqueur `outerovitch-todo-store-v1`) : le jeton (scope `gist` seulement)
  reste dans le `localStorage` du navigateur, jamais dans le dépôt.
- Icônes pixel Windows 95 lues dans `/assets/icons/` du site principal
  (`mathematovitch/mathematovitch.github.io`).

Extrait avec son historique du site principal le 2026-10-28.

## Aperçu local

Depuis `~/work/00.site` (pour que `../assets/` existe) :

```
ln -s ~/code/04-web/todo todo   # une fois, ignoré par git dans le site
python3 -m http.server          # puis http://localhost:8000/todo/
```
