# Mettre ton site sur GitHub Pages (gratuit)

## Les 4 fichiers
- `index.html` : ton site
- `latest.json` : la dernière vidéo (rempli automatiquement)
- `update-video.yml` : le petit robot qui met à jour la vidéo toutes les heures
- `LISEZMOI.md` : ce guide (pas besoin de le mettre sur GitHub)

## Étapes (ça marche depuis le téléphone, en mode « version pour ordinateur » du navigateur)

1. Va sur **github.com** et crée un compte gratuit.
2. Crée un **nouveau dépôt** (bouton « New »). Nom conseillé : `TONPSEUDO.github.io`
   (remplace TONPSEUDO par ton nom d'utilisateur GitHub). Mets-le en **Public**.
3. Dans le dépôt : **Add file → Upload files**, envoie `index.html` et `latest.json`, puis **Commit changes**.
4. **Add file → Create new file**. Dans le nom, tape exactement :
   `.github/workflows/update-video.yml`
   (les `/` créent les dossiers). Colle tout le contenu de `update-video.yml`, puis **Commit changes**.
5. **Settings → Pages** : choisis **Deploy from a branch**, branche **main**, dossier **/ (root)**, puis **Save**.
6. **Settings → Actions → General → Workflow permissions** : coche **Read and write permissions**, puis **Save**.
7. Onglet **Actions → « Mettre à jour la dernière vidéo » → Run workflow**. Lance-le une première fois à la main.
8. Attends 1 à 2 minutes : ton site est en ligne sur `https://TONPSEUDO.github.io`.

## Ensuite
- Ta dernière vidéo se met à jour **toute seule, toutes les heures**.
- Pour changer un texte ou un lien : ouvre `index.html` sur GitHub, clique sur le crayon ✏️, modifie la partie `CONFIG` en haut du script, puis **Commit changes**.
- Les Shorts sont ignorés par défaut. Pour les inclure, mets `SKIP_SHORTS = False` dans `update-video.yml`.
