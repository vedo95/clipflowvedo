# Mettre ClipFlowVedo en ligne sur GitHub Pages

Ce paquet contient le site vitrine et les pages légales du prototype. Ne l'associez jamais à votre code applicatif privé ni à vos clés Twitch/TikTok. Ce n'est **pas** l'application ClipFlow en elle-même.

## 0. Informations à compléter

Avant une vraie demande d'approbation par TikTok ou une distribution publique, ouvrez `conditions.html` et `confidentialite.html` dans un éditeur de texte et remplacez **NOM OU RAISON SOCIALE À RENSEIGNER** et **E-MAIL DE CONTACT À RENSEIGNER** par les coordonnées réelles du responsable. Ne publiez aucune adresse personnelle si vous ne souhaitez pas qu'elle soit publique : utilisez une adresse dédiée au projet.

Le contenu a été rédigé pour la version actuelle du logiciel (application locale, sans serveur de compte ni collecte analytique ajoutée). Il faut l'adapter si les fonctionnalités ou traitements évoluent. Ces textes sont des modèles de travail, pas un avis juridique.

## 1. Créer le dépôt public (nécessaire)

1. Connectez-vous à https://github.com/ (compte GitHub : vedo95).
2. Allez sur https://github.com/new.
3. Owner : `vedo95` ; Repository name : `clipflowvedo` ; Visibility : `Public`.
4. Cliquez sur **Create repository**. Il est possible de laisser l'option README désactivée.

## 2. Importer les fichiers du site

1. Décompressez `ClipFlowVedo_site_GitHub_Pages.zip` sur votre PC.
2. Dans le dépôt `vedo95/clipflowvedo`, cliquez sur **Add file > Upload files** (ou "uploading an existing file" dans un dépôt vide).
3. Sélectionnez les fichiers **contenus dans** le dossier décompressé, pas le ZIP lui-même : `index.html`, `conditions.html`, `confidentialite.html`, `style.css`, `favicon.svg` et `.nojekyll` (ce dernier garantit que les fichiers de vérification restent publiés tels quels).
4. Validez avec **Commit changes** sur `main`.

Vous pouvez également importer ce README (facultatif).

## 3. Activer GitHub Pages

1. Ouvrez `https://github.com/vedo95/clipflowvedo/settings/pages`.
2. Sous **Build and deployment**, choisissez **Source: Deploy from a branch**.
3. Réglez **Branch: main** et **Folder: /(root)**, puis cliquez sur **Save**.
4. Le site sera publié à : `https://vedo95.github.io/clipflowvedo/` (un délai de déploiement est normal).
5. Vérifiez l'ouverture des trois liens ci-dessous dans un navigateur privé.

## 4. Coller les URL réelles dans TikTok for Developers

- **Web/Desktop URL** : `https://vedo95.github.io/clipflowvedo/`
- **Terms of Service URL** : `https://vedo95.github.io/clipflowvedo/conditions.html`
- **Privacy Policy URL** : `https://vedo95.github.io/clipflowvedo/confidentialite.html`

Ne copiez ces URL qu'une fois le site effectivement publié et accessible.

## 5. Vérifier l'appartenance des URL dans TikTok

Dans TikTok > ClipFlowVedo > **Production** > **URL properties** > **Verify properties** :

1. Sélectionnez **URL prefix** (et non Domain, car GitHub possède `github.io`).
2. Indiquez le préfixe `https://vedo95.github.io/clipflowvedo/`, **avec le slash final**.
3. TikTok fournit un **fichier signature spécifique à votre compte/application**. Téléchargez-le. Ne fabriquez pas vous-même ce fichier.
4. Dans `https://github.com/vedo95/clipflowvedo`, cliquez **Add file > Upload files** et déposez ce fichier de vérification **à la racine** du dépôt, au même niveau que `index.html` (ne changez ni son nom ni son contenu).
5. **Commit changes** et attendez le déploiement GitHub Pages. Ouvrez dans un navigateur le fichier à son adresse exacte, sous `https://vedo95.github.io/clipflowvedo/NOM_DU_FICHIER_TIKTOK` ; il doit s'afficher sans demander de connexion.
6. Retournez dans TikTok pour cliquer sur **Verify**. Le préfixe vérifié est censé couvrir les trois pages de ce dossier. Si TikTok continue à marquer une URL comme non vérifiée, vérifiez le préfixe exact ou faites une vérification séparée pour la page concernée.
7. Revenez sur les détails de l'application, collez les trois URL, puis cliquez sur **Save**.

Ne cliquez pas encore sur Submit for review avant d'avoir finalisé les pages, les autres configurations TikTok et la vidéo de démonstration.

**Important :** ces instructions utilisent la méthode officielle de vérification par préfixe, mais la réussite dépend du fichier fourni par TikTok et de ses contrôles. Aucune garantie de validation ou d'approbation.

## Sources officielles

- https://docs.github.com/fr/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://developers.tiktok.com/docs/en/getting-started-create-an-app
- https://developers.tiktok.com/docs/en/content-posting-api-media-transfer-guide