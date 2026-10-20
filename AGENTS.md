## Règle : commit Git après chaque tâche terminée

À la fin de CHAQUE tâche terminée (code fonctionnel et vérifications pertinentes réussies) :
1. Vérifier l'état avec `git status`.
2. Indexer uniquement les fichiers liés à la tâche avec `git add <fichiers>` (`git add .` seulement si tous les changements en cours appartiennent à la tâche).
3. Commiter avec `git commit -m "<message>"`.

Format du message :
- Rédigé en français, à l'impératif présent (« Ajoute », « Corrige », « Refactorise »), de façon cohérente dans tout le projet.
- Première ligne de 72 caractères maximum, sans point final, qui résume le « quoi ».
- Préfixe optionnel : `feat:`, `fix:`, `refactor:`, `docs:`, `test:`, `chore:`.
- Si nécessaire, ligne vide puis un corps expliquant le « pourquoi ».
- Le message décrit fidèlement les changements réellement effectués. Jamais de message générique (« maj », « modifs », « wip »).

Interdictions :
- Jamais de `git push`, `git commit --amend`, `git reset --hard`, `git rebase` ni `--force` sans demande explicite de ma part.
- Jamais de secrets (`.env`, clés API, mots de passe, tokens) ni de fichiers générés (`node_modules/`, `dist/`, `__pycache__/`, binaires). En cas de doute, vérifie le `.gitignore` et demande-moi.
- Un commit = une tâche cohérente. Ne mélange pas des tâches indépendantes.
- Si le commit échoue (hook, conflit, identité manquante), corrige la cause ou signale-le-moi. Jamais de `--no-verify`.
