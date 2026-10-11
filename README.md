# Site académique d’Ayoub Naji

Site statique en français, conçu pour GitHub Pages : **https://ayoubnaji.me/**.

## Structure

- `index.html` : accueil, biographie, axes de recherche, travaux, formation et contact.
- `assets/style.css` : couleurs, typographie et mise en page responsive.
- `assets/favicon.svg` : icône du site.
- `CNAME` : domaine personnalisé existant, `ayoubnaji.me`.
- `.nojekyll` : désactive le traitement Jekyll pour servir directement les fichiers.
- `robots.txt` et `sitemap.xml` : exploration et indexation du site.

Aucun framework, JavaScript, outil de compilation ou dépendance externe n’est requis. L’illustration est conceptuelle : elle ne représente ni une carte ni une mesure réelle.

## Modifier le contenu

1. Ouvrir `index.html` sur GitHub, puis cliquer sur le bouton d’édition.
2. Modifier le texte de la section souhaitée. Conserver les identifiants (`biographie`, `recherche`, `travaux`, `formation`, `contact`) pour préserver les liens de navigation.
3. Pour ajouter un travail, dupliquer un bloc `<article class="work">…</article>` dans la section `travaux`.
4. Renseigner explicitement le statut d’un article (soumis, accepté ou publié). Ajouter un DOI ou un lien uniquement lorsqu’il est disponible et vérifié.
5. Enregistrer le changement avec un message explicite. Sur `main`, il sera pris en compte au prochain déploiement Pages si la publication depuis cette branche est configurée.

Le contact se modifie dans le texte de l’adresse **et** dans son lien `mailto:`. Les couleurs sont regroupées au début de `assets/style.css`. Mettre à jour l’année du pied de page si nécessaire. Les statuts des travaux reflètent les informations disponibles lors de la création de cette version ; ils doivent être actualisés en fonction des décisions éditoriales.

## Prévisualiser localement

Cloner le dépôt, puis exécuter depuis sa racine :

```bash
python3 -m http.server 8000
```

Ouvrir http://localhost:8000. On peut aussi ouvrir `index.html` directement dans un navigateur. Vérifier la navigation, les liens, le rendu mobile et le contact avant de publier.

## Publier avec GitHub Pages

Dans **Settings → Pages** du dépôt :

1. Sélectionner **Deploy from a branch** comme source.
2. Sélectionner **main** et le dossier **/ (root)**, puis enregistrer.
3. Vérifier que le domaine personnalisé est **ayoubnaji.me**.
4. Activer **Enforce HTTPS** lorsque GitHub rend l’option disponible.
5. Suivre le déploiement dans l’onglet **Actions** et le lien du site dans **Settings → Pages**.

Ces étapes décrivent la configuration attendue ; la présence des fichiers ne garantit pas à elle seule que Pages ou le DNS soient configurés. Aucun workflow Actions supplémentaire n’est nécessaire avec cette méthode.

## Domaine personnalisé

**Conserver `CNAME` à la racine, contenant uniquement `ayoubnaji.me`.** Cette version préserve le fichier existant. Les liens vers les ressources sont relatifs et fonctionnent sur le domaine personnalisé comme sur une prévisualisation locale. La balise canonique et le sitemap utilisent `https://ayoubnaji.me/`.

Ne pas remplacer le domaine par `ayoub-naji.github.io` dans `CNAME`. En cas de problème de domaine, vérifier le DNS et le contrôle de domaine dans Settings → Pages ; modifier le HTML ne corrige pas le DNS.

## Contenu académique

Le site distingue le manuscrit Issougrid soumis à *Advances in Space Research*, le projet PRISMA–EMIT à Tizert en préparation, le mémoire de master et la communication ICATH’23. Aucun DOI, acceptation ou résultat non confirmé n’a été ajouté.
