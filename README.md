# 🥗 Formulaire FOUD – Commande de Plateaux Repas

Ce dépôt contient le code HTML complet du formulaire de commande **FOUD**, prêt à être intégré dans :
- un site **WordPress / Divi** (par shortcode HTML ou bloc code),
- un hébergement **OVH** (via FTP),
- ou directement sur **Netlify** avec gestion des soumissions et envoi d’e-mails automatiques via **Brevo**.

---

## 🚀 Déploiement sur Netlify

1. **Crée un dépôt GitHub public** nommé `FOUD-Form`.
2. Glisse les fichiers du ZIP (ou clone depuis ton PC).
3. Connecte ton compte Netlify et choisis le dépôt GitHub.
4. Active les formulaires Netlify :
   - Va dans le panneau Netlify > **Forms**
   - Vérifie que le formulaire `"commande-foud"` est détecté.
5. Ajoute ton e-mail de réception (ex. `manager@foud.com`) dans les notifications Netlify.

---

## 💌 Intégration e-mail (Brevo)

Pour relier les confirmations client via **Brevo** :

1. Crée un compte gratuit sur [https://www.brevo.com](https://www.brevo.com)
2. Configure un template d’e-mail “Confirmation de commande FOUD”
3. Utilise l’automation “Lorsqu’un formulaire Netlify est soumis”
   - Connecte l’API Brevo via **Zapier** ou **Make (Integromat)**
   - Champs recommandés :
     - `nom-client`
     - `email-client`
     - `commentaires`
     - Détail des plateaux (Netlify enverra le contenu complet du formulaire)

---

## 🧱 Structure du formulaire

Chaque commande contient :
- Jusqu’à **5 plateaux repas** (ajoutables/supprimables)
- Champs :  
  `Nom`, `Entrée`, `Plat`, `Dessert`, `Boisson`, `Pain (Oui par défaut)`, `Fromage`, `Commentaires`
- Section finale : informations client + commentaires de commande.

---

## 🖨️ PDF imprimable

- La mise en page est adaptée pour une impression **A4**
- Utiliser le bouton **🖨️ Imprimer** pour obtenir un rendu propre
- 5 plateaux maximum par page.

---

## 🧰 Personnalisation

Pour changer la carte :
- Ouvre `index.html`
- Modifie les listes JavaScript :
  ```js
  const plats = [ ... ]
  const entrees = [ ... ]
  const desserts = [ ... ]
  const boissons = [ ... ]
  ```
- Sauvegarde et redéploie.

---

## 📧 Support FOUD

Pour assistance technique :
**Email :** manager@foud.com  
**Site :** [https://foud.com](https://foud.com)
