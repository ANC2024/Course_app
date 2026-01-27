# 🛒 PromoFinder - Application PWA

Application mobile progressive pour trouver automatiquement les meilleures promotions en fonction de votre liste de courses.

## 🚀 Déploiement sur Cloudflare Pages (GRATUIT)

### Prérequis
- Compte GitHub (gratuit)
- Compte Cloudflare (gratuit)

### Étapes de déploiement

#### 1. Créer un repository GitHub
1. Allez sur https://github.com/new
2. Nommez votre repo: `promofinder-app`
3. Créez le repository

#### 2. Uploader les fichiers
1. Clonez ou uploadez tous les fichiers de ce dossier dans votre repo GitHub:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon.svg`
   - (+ les icônes PNG une fois créées)

#### 3. Créer les icônes PNG
Avant de déployer, vous devez créer les icônes:
1. Allez sur https://cloudconvert.com/svg-to-png
2. Uploadez `icon.svg`
3. Convertissez en 192x192px → sauvegardez comme `icon-192.png`
4. Re-convertissez en 512x512px → sauvegardez comme `icon-512.png`
5. Uploadez ces fichiers dans votre repo GitHub

#### 4. Déployer sur Cloudflare Pages
1. Connectez-vous sur https://dash.cloudflare.com/
2. Allez dans **Pages** → **Create a project**
3. Cliquez sur **Connect to Git**
4. Sélectionnez votre repository `promofinder-app`
5. Configurez comme suit:
   - **Framework preset**: None
   - **Build command**: (laissez vide)
   - **Build output directory**: /
6. Cliquez sur **Save and Deploy**

#### 5. Votre app sera disponible en ~2 minutes !
URL: `https://promofinder-app.pages.dev` (ou votre nom personnalisé)

### Ajouter un domaine personnalisé (optionnel)
1. Dans Cloudflare Pages, allez dans l'onglet **Custom domains**
2. Cliquez sur **Set up a custom domain**
3. Entrez votre domaine (ex: `promos.votresite.com`)

## 📱 Installation sur téléphone

### iOS (iPhone/iPad)
1. Ouvrez l'app dans Safari
2. Appuyez sur le bouton Partager
3. Faites défiler et appuyez sur "Sur l'écran d'accueil"
4. Appuyez sur "Ajouter"

### Android
1. Ouvrez l'app dans Chrome
2. Appuyez sur le menu ⋮
3. Appuyez sur "Installer l'application"
4. Confirmez

## 🔧 Configuration

### Modifier l'URL du webhook n8n
Dans `index.html`, ligne 372, remplacez par votre webhook:
```javascript
const WEBHOOK_URL = 'https://votre-instance.app.n8n.cloud/webhook-test/VOTRE-ID';
```

## ✨ Fonctionnalités

- ✅ Upload de photo de liste de courses
- ✅ Analyse IA automatique
- ✅ Comparaison des promos dans tous les supermarchés
- ✅ Historique des recherches (stocké localement)
- ✅ Animation de chargement
- ✅ Design iOS moderne et responsive
- ✅ Installable comme app native
- ✅ Fonctionne hors ligne (historique)
- ✅ Mode sombre automatique

## 🎨 Personnalisation

### Changer les couleurs
Dans `index.html`, modifiez les variables CSS (ligne 25):
```css
:root {
    --primary: #007AFF;  /* Couleur principale */
    --success: #34C759;  /* Vert de succès */
    /* etc... */
}
```

### Changer le nom de l'app
1. Dans `manifest.json`: changez `name` et `short_name`
2. Dans `index.html`: changez `<title>` et `<h1>`

## 🐛 Débogage

### L'app ne charge pas les résultats
1. Vérifiez que votre webhook n8n est actif
2. Ouvrez la console développeur (F12)
3. Regardez les erreurs réseau

### L'installation ne marche pas
1. Vérifiez que vous êtes en HTTPS (requis pour PWA)
2. Assurez-vous que `manifest.json` est accessible
3. Vérifiez que les icônes sont au bon format

## 📊 Structure du projet

```
promo-scanner-app/
├── index.html       # Page principale de l'app
├── manifest.json    # Configuration PWA
├── sw.js           # Service Worker (cache)
├── icon.svg        # Icône source
├── icon-192.png    # Icône 192x192 (à créer)
├── icon-512.png    # Icône 512x512 (à créer)
└── README.md       # Ce fichier
```

## 💡 Améliorations futures possibles

- [ ] Mode comparaison de prix détaillé
- [ ] Notifications push pour nouvelles promos
- [ ] Export PDF du rapport
- [ ] Partage des résultats
- [ ] Filtres par magasin/catégorie
- [ ] Géolocalisation des magasins

## 📝 License

Libre d'utilisation personnelle et commerciale.

## 🆘 Support

Pour toute question, ouvrez une issue sur GitHub.

---

Fait avec ❤️ pour économiser sur les courses !
