# 📧 Configuration du Formulaire de Contact - ShowRoom d'Oliv

## ✅ ÉTAPE 1 : Obtenir votre clé API Web3Forms (GRATUIT)

1. **Allez sur** : https://web3forms.com
2. **Cliquez sur** : "Get Started Free" (Commencer gratuitement)
3. **Entrez votre email** : `contact@show-room-oliv.fr`
4. **Vérifiez votre boîte mail** : Vous recevrez un email de Web3Forms
5. **Copiez la clé API** : Elle ressemble à `xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`

---

## ✅ ÉTAPE 2 : Configurer la clé dans le site

1. **Ouvrez le fichier** : `index.html`
2. **Recherchez** (ligne 3714) :
   ```html
   <input type="hidden" name="access_key" value="VOTRE_CLE_WEB3FORMS_ICI">
   ```
3. **Remplacez** `VOTRE_CLE_WEB3FORMS_ICI` par votre vraie clé API
4. **Exemple** :
   ```html
   <input type="hidden" name="access_key" value="abc12345-6789-defg-hijk-lmnopqrstuvw">
   ```

---

## ✅ ÉTAPE 3 : Pousser sur GitHub

```powershell
git add index.html
git commit -m "feat: configuration formulaire Web3Forms avec protections anti-spam"
git push
```

---

## 🛡️ Protections Anti-Spam Installées

### ✅ Protection 1 : **Honeypot** (Piège à bots)
- Champ caché invisible pour les humains
- Les bots cochent automatiquement toutes les cases
- Si coché → Message rejeté silencieusement

### ✅ Protection 2 : **Rate Limiting**
- 1 message par minute maximum par personne
- Empêche l'envoi massif de spam
- Compteur affiché à l'utilisateur

### ✅ Protection 3 : **Validation stricte**
- Nom : 2-100 caractères
- Message : 10-2000 caractères
- Email : format valide obligatoire

### ✅ Protection 4 : **Détection mots-clés spam**
- Liste de mots suspects : viagra, casino, crypto, bitcoin, lottery, porn, sex, pills
- Si détecté → Message rejeté silencieusement

---

## 📧 Où vont les emails ?

**Destination** : `contact@show-room-oliv.fr`

**Format de l'email reçu** :
```
De : contact@show-room-oliv.fr
Sujet : Nouveau message depuis ShowRoom d'Oliv

Nom : Jean Dupont
Email : jean.dupont@example.com
Téléphone : 06 12 34 56 78
Sujet : Prendre rendez-vous

Message :
Bonjour, je souhaiterais prendre rendez-vous pour découvrir 
vos collections See u Soon. Êtes-vous disponible jeudi après-midi ?
```

---

## 📊 Limites gratuites Web3Forms

- ✅ **250 emails par mois** (gratuit à vie)
- ✅ Anti-spam intégré
- ✅ Notifications par email en temps réel
- ✅ Pas de limite de durée

**Si vous dépassez 250 emails/mois** :
- Plan Premium : 9$/mois pour 1000 emails
- Ou basculer sur un autre service gratuit

---

## 🧪 TESTER LE FORMULAIRE

1. Une fois la clé configurée et poussée sur GitHub
2. Attendez 2-3 minutes (GitHub Pages met à jour)
3. Allez sur : https://poloveni.github.io/show-room-oliv/#contact
4. Remplissez le formulaire de test
5. Vérifiez `contact@show-room-oliv.fr` → vous devriez recevoir l'email !

---

## ❓ En cas de problème

### Le formulaire ne fonctionne pas
1. Vérifiez que la clé API est bien configurée (ligne 3714)
2. Vérifiez que vous avez validé votre email sur Web3Forms
3. Regardez la console du navigateur (F12) pour les erreurs

### Je ne reçois pas les emails
1. Vérifiez les SPAMS de `contact@show-room-oliv.fr`
2. Vérifiez que l'email est confirmé sur Web3Forms
3. Testez avec un autre email

---

## 📞 Besoin d'aide ?

Contactez le développeur : Paul Schricke
Site : https://depannagepcgard.fr
