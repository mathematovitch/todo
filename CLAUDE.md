# CLAUDE.md

Page `/todo` de mathematovitch.github.io : listes de tâches façon org-mode,
une seule page `index.html` (HTML/CSS/JS en ligne, aucune dépendance). Site de
projet GitHub Pages (dépôt `mathematovitch/todo`, branche `main`, aucun
build), extrait avec son historique du site principal `~/work/00.site`
(2026-10-28). Doc : `README.md`.

- **Dépend du site principal** servi à côté : icônes `../assets/icons/*.png`
  (dont `todo.png` en favicon). Ne marche pas seul en local.
- DA du site principal (« brute old school » : Times, traits noirs 1 px,
  boutons gris en relief, icônes pixel W95) ; voir « Design du site » dans
  `~/work/00.site/CLAUDE.md`.
- Synchronisation : Gist privé `todo.txt` (marqueur `GIST_MARKER`), jeton
  GitHub scope `gist` stocké dans `localStorage` (`LS_TOKEN`), écriture
  différée (`DEBOUNCE_MS`). Clés `localStorage` préfixées `todo…` : ne pas
  les renommer (perte des données déjà en cache chez l'utilisateur).
- Format `todo.txt` (voir `README.md`) : `[#A]` en tête, `DEADLINE: <AAAA-MM-JJ>` en
  fin de tâche ; lu par la commande `envie` (`~/code/05-claude/coach/CLAUDE.md`) : garder
  les deux en accord. Clés de synchro : `todoDirty` (changements non envoyés),
  `todoRemoteBase` (dernier contenu connu du gist, sert à détecter les conflits).
- PWA : `manifest.webmanifest`, `sw.js` (réseau d'abord, ne met jamais en cache
  `api.github.com` ; changer `CACHE` si la liste des fichiers mis en cache change),
  `icons/todo-{192,512}.png` (agrandissement pixel de `todo.png` du site).
- Aperçu local : lien symbolique `~/work/00.site/todo → ~/code/04-web/todo`
  (ignoré par git dans le site), `python3 -m http.server` à la racine de
  `00.site`, http://localhost:8000/todo/.
- Ne jamais committer sans demande explicite de l'utilisateur.
