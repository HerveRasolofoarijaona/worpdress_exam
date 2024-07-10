Créer une page avec les plugins Ultimate Member et Everest Forms imbriqués dans WordPress est une excellente idée pour gérer les inscriptions des utilisateurs et les soumissions de formulaires de manière centralisée. Voici comment procéder :

### Étapes pour créer une page avec Ultimate Member et Everest Forms

1. **Créer un formulaire d'inscription avec Ultimate Member :**

   Ultimate Member fournit des shortcodes pour les formulaires d'inscription, de connexion et de profil. Vous pouvez utiliser ces shortcodes pour insérer les formulaires sur n'importe quelle page.

   - Connectez-vous à votre tableau de bord WordPress.
   - Allez dans **Ultimate Member > Forms**.
   - Créez un nouveau formulaire ou utilisez un formulaire existant.
   - Notez le shortcode du formulaire d'inscription. Par exemple : `[ultimatemember form_id="123"]`.

2. **Créer un formulaire avec Everest Forms :**

   - Allez dans **Everest Forms > All Forms**.
   - Créez un nouveau formulaire ou utilisez un formulaire existant.
   - Configurez les champs nécessaires pour votre formulaire (par exemple, ajouter une nouvelle voiture à vendre).
   - Notez le shortcode du formulaire. Par exemple : `[everest_form id="456"]`.

3. **Créer une nouvelle page :**

   - Allez dans **Pages > Ajouter**.
   - Donnez un titre à votre page, par exemple "Inscription et Soumission de Voiture".
   - Dans l'éditeur de page, ajoutez les shortcodes des formulaires Ultimate Member et Everest Forms.

   Exemple de contenu de la page :

   ```html
   <h2>Inscription</h2>
   [ultimatemember form_id="123"]

   <h2>Soumettre une Voiture</h2>
   [everest_form id="456"]
# Interaction avec la Base de Données

## Formulaire d'inscription Ultimate Member :

- Lorsque les utilisateurs s'inscrivent via le formulaire d'inscription, leurs informations sont stockées dans les tables `wp_users` et `wp_um_metadata`.
- Une entrée est créée dans `wp_users` pour chaque utilisateur.
- Les champs personnalisés du profil sont stockés dans `wp_um_metadata`.

## Formulaire Everest Forms :

- Lorsqu'un utilisateur connecté soumet le formulaire Everest Forms, les données sont enregistrées dans la table `wp_evf_entries`.
- Chaque soumission contient l'ID du formulaire, les champs soumis, et la date de soumission.

# Fonctionnement d'utilisation

## Un utilisateur visite la page :

- L'utilisateur voit le formulaire d'inscription en haut et le formulaire de soumission de voiture en dessous.
- Si l'utilisateur n'est pas connecté, il doit d'abord s'inscrire ou se connecter via le formulaire Ultimate Member.

## L'utilisateur s'inscrit :

- Remplit le formulaire d'inscription Ultimate Member.
- Les informations sont enregistrées dans `wp_users` et `wp_um_metadata`.
- L'utilisateur est redirigé vers la page ou une autre page de votre choix après l'inscription.

## L'utilisateur soumet une voiture :

- Remplit le formulaire Everest Forms pour ajouter une nouvelle voiture à vendre.
- Les données de la voiture sont enregistrées dans `wp_evf_entries`.

