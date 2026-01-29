# 🌐 Migration vers show-room-oliv.fr - Guide Complet

## ✅ Ce qui NE change PAS

### Formulaire de contact
- ✅ Web3Forms fonctionne sur n'importe quel domaine
- ✅ Votre clé API reste identique
- ✅ Les emails arrivent toujours sur contact@show-room-oliv.fr
- ✅ Toutes les protections anti-spam restent actives

### Fichiers du site
- ✅ Tous les fichiers HTML, CSS, JS, images restent identiques
- ✅ Aucune modification du code nécessaire (sauf URLs ci-dessous)

---

## 📝 Ce qu'il faudra modifier (5 minutes)

### ÉTAPE 1 : Mettre à jour les URLs dans index.html

**Ouvrez `index.html` et remplacez toutes les occurrences :**

#### Ligne 22 : Open Graph URL
```html
<!-- AVANT -->
<meta property="og:url" content="https://poloveni.github.io/show-room-oliv/">

<!-- APRÈS -->
<meta property="og:url" content="https://show-room-oliv.fr/">
```

#### Ligne 25 : Open Graph Image
```html
<!-- AVANT -->
<meta property="og:image" content="https://poloveni.github.io/show-room-oliv/logo.png">

<!-- APRÈS -->
<meta property="og:image" content="https://show-room-oliv.fr/logo.png">
```

#### Ligne 31 : Twitter Card URL
```html
<!-- AVANT -->
<meta name="twitter:url" content="https://poloveni.github.io/show-room-oliv/">

<!-- APRÈS -->
<meta name="twitter:url" content="https://show-room-oliv.fr/">
```

#### Ligne 34 : Twitter Card Image
```html
<!-- AVANT -->
<meta name="twitter:image" content="https://poloveni.github.io/show-room-oliv/logo.png">

<!-- APRÈS -->
<meta name="twitter:image" content="https://show-room-oliv.fr/logo.png">
```

#### Ligne 37 : Canonical URL
```html
<!-- AVANT -->
<link rel="canonical" href="https://poloveni.github.io/show-room-oliv/">

<!-- APRÈS -->
<link rel="canonical" href="https://show-room-oliv.fr/">
```

#### Ligne 3436 : Schema.org Image
```html
<!-- AVANT -->
"image": "https://poloveni.github.io/show-room-oliv/logo.png",

<!-- APRÈS -->
"image": "https://show-room-oliv.fr/logo.png",
```

#### Ligne 3438 : Schema.org @id
```html
<!-- AVANT -->
"@id": "https://poloveni.github.io/show-room-oliv/",

<!-- APRÈS -->
"@id": "https://show-room-oliv.fr/",
```

#### Ligne 3439 : Schema.org URL
```html
<!-- AVANT -->
"url": "https://poloveni.github.io/show-room-oliv/",

<!-- APRÈS -->
"url": "https://show-room-oliv.fr/",
```

---

### ÉTAPE 2 : Mettre à jour sitemap.xml (si vous en avez un)

Si vous avez un fichier `sitemap.xml`, remplacez :
```xml
<loc>https://poloveni.github.io/show-room-oliv/</loc>
```
Par :
```xml
<loc>https://show-room-oliv.fr/</loc>
```

---

### ÉTAPE 3 : Configuration de l'hébergement

#### Option A : Hébergement classique (OVH, O2Switch, etc.)
1. **Uploadez tous les fichiers** via FTP/SFTP sur votre serveur
2. **Pointez le domaine** `show-room-oliv.fr` vers votre hébergement :
   - Type A : Adresse IP du serveur
   - Ou CNAME si sous-domaine
3. **Attendez 24-48h** pour la propagation DNS

#### Option B : Hébergement GitHub Pages avec domaine personnalisé
1. Créez un fichier `CNAME` à la racine avec :
   ```
   show-room-oliv.fr
   ```
2. Dans les paramètres GitHub du repo :
   - Settings > Pages > Custom domain
   - Entrez : `show-room-oliv.fr`
3. Configurez les DNS chez votre registrar :
   ```
   Type A : 185.199.108.153
   Type A : 185.199.109.153
   Type A : 185.199.110.153
   Type A : 185.199.111.153
   ```

---

## 🔒 Activer HTTPS (Certificat SSL gratuit)

### Si hébergement classique
- **Let's Encrypt** (gratuit) : La plupart des hébergeurs l'installent automatiquement
- Dans le panneau d'administration : Activer SSL/HTTPS

### Si GitHub Pages
- ✅ Certificat SSL automatique après configuration du domaine personnalisé
- Cochez "Enforce HTTPS" dans les paramètres

---

## ✅ Checklist finale après migration

### Tests à faire
- [ ] Le site s'affiche correctement sur `https://show-room-oliv.fr`
- [ ] Toutes les images se chargent
- [ ] Le formulaire de contact fonctionne (tester un envoi)
- [ ] Les emails arrivent bien sur `contact@show-room-oliv.fr`
- [ ] Le certificat HTTPS (cadenas) est actif
- [ ] Tester sur mobile et desktop

### SEO et réseaux sociaux
- [ ] Vérifier l'aperçu Facebook : https://developers.facebook.com/tools/debug/
- [ ] Vérifier l'aperçu Twitter : https://cards-dev.twitter.com/validator
- [ ] Soumettre le nouveau sitemap à Google Search Console

---

## 🚀 Commande rapide pour tout remplacer d'un coup

Si vous êtes à l'aise avec les lignes de commande, vous pouvez remplacer toutes les URLs en une seule fois :

### Windows PowerShell
```powershell
(Get-Content index.html) -replace 'poloveni\.github\.io/show-room-oliv', 'show-room-oliv.fr' | Set-Content index.html
```

### Linux/Mac
```bash
sed -i 's|poloveni\.github\.io/show-room-oliv|show-room-oliv.fr|g' index.html
```

---

## 📞 Besoin d'aide pour la migration ?

**Contact développeur** : Paul Schricke  
**Site** : https://depannagepcgard.fr

---

## 💡 Conseils supplémentaires

### Redirection de l'ancien domaine
Si vous voulez garder l'ancien domaine GitHub Pages actif avec redirection :
1. Créez un fichier `index.html` dans le repo GitHub :
   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <meta http-equiv="refresh" content="0; url=https://show-room-oliv.fr/">
       <link rel="canonical" href="https://show-room-oliv.fr/">
   </head>
   <body>
       <p>Redirection vers <a href="https://show-room-oliv.fr/">show-room-oliv.fr</a>...</p>
   </body>
   </html>
   ```

### Performance
- ✅ Activer la compression GZIP sur votre serveur
- ✅ Configurer le cache navigateur (1 an pour images/CSS/JS)
- ✅ Utiliser un CDN comme Cloudflare (gratuit) pour améliorer la vitesse

---

**Résumé** : Migration très simple, juste 8 URLs à modifier ! 🎉
