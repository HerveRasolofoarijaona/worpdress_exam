### Ajouter et configurer les plugins PWA sur WordPress

1. **Installer un plugin PWA :**
   - Connectez-vous à votre tableau de bord WordPress.
   - Allez dans **Extensions > Ajouter**.
   - Recherchez "PWA" et choisissez un plugin adapté, comme **PWA by PWA Plugin Contributors** ou **Super Progressive Web Apps**.
   - Cliquez sur **Installer** puis **Activer**.

2. **Configurer le plugin PWA :**
   - Après avoir activé le plugin, allez dans les réglages du plugin via **Réglages > PWA**.
   - Configurez les options de base comme le nom de l'application, la description, l'icône, et les couleurs.
   - Assurez-vous que l'option d'ajout à l'écran d'accueil est activée.

3. **Configurer le service worker et les stratégies de mise en cache :**
   - Certains plugins PWA incluent des configurations par défaut pour le service worker. Vérifiez les paramètres et ajustez-les si nécessaire.
   - Si votre plugin ne configure pas automatiquement le service worker, vous pouvez ajouter manuellement le fichier `service-worker.js` dans le répertoire racine de votre site WordPress.

