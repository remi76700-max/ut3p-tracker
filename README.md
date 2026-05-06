# UT3P Tracker — Road to 90K

Application de suivi de préparation trail pour le **LHUT 42km (31 Mai 2026)** et l'**UT3P 90km (20 Sept. 2026)**.

---

## 🚀 Déploiement initial (une seule fois)

### Étape 1 — Créer le repository GitHub

1. Va sur **github.com** → connecte-toi (ou crée un compte gratuit)
2. Clique le **+** en haut à droite → **"New repository"**
3. Remplis :
   - **Repository name** : `ut3p-tracker`
   - **Description** : `Trail prep tracker - LHUT & UT3P`
   - Coche **"Public"** (nécessaire pour GitHub Pages gratuit)
   - Coche **"Add a README file"**
4. Clique **"Create repository"**

### Étape 2 — Uploader les fichiers

1. Dans ton repository, clique **"Add file"** → **"Upload files"**
2. Glisse-dépose ces 4 fichiers :
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-512.svg`
3. En bas, écris dans "Commit changes" : `Initial deploy`
4. Clique **"Commit changes"**

### Étape 3 — Activer GitHub Pages

1. Dans ton repository → clique **"Settings"** (onglet en haut)
2. Dans le menu gauche → **"Pages"**
3. Sous "Source" → sélectionne **"Deploy from a branch"**
4. Branch : **main** / Folder : **/ (root)**
5. Clique **"Save"**
6. Attends 2-3 minutes → ton app sera live sur :
   **`https://TON-USERNAME.github.io/ut3p-tracker`**

### Étape 4 — Connecter Netlify (optionnel mais recommandé)

Netlify donne un déploiement plus rapide et un vrai domaine custom.

1. Va sur **netlify.com** → **"Sign up with GitHub"**
2. Clique **"Add new site"** → **"Import an existing project"**
3. Sélectionne **GitHub** → autorise l'accès
4. Choisis le repository **ut3p-tracker**
5. Laisse tout par défaut → clique **"Deploy site"**
6. Ton app est live sur `random-name.netlify.app`
7. Optionnel : dans "Site settings" → renomme en `ut3p-tracker`

---

## 📱 Installer comme une vraie app (PWA)

### Sur iPhone/iPad
1. Ouvre l'URL dans **Safari** (pas Chrome, Safari obligatoire sur iOS)
2. Appuie sur l'icône **Partager** (carré avec flèche vers le haut)
3. Fais défiler → appuie **"Sur l'écran d'accueil"**
4. Donne le nom **"UT3P"** → **"Ajouter"**
5. L'app apparaît sur ton écran d'accueil avec l'icône orange 🔥

### Sur Android
1. Ouvre l'URL dans **Chrome**
2. Menu ⋮ → **"Ajouter à l'écran d'accueil"**
3. Confirme → c'est installé

---

## 🔄 Mettre à jour l'app

### Méthode simple (depuis le navigateur, même sur mobile)

1. Va sur **github.com/TON-USERNAME/ut3p-tracker**
2. Clique sur **`index.html`**
3. Clique l'icône **crayon** ✏️ (Edit this file)
4. Sélectionne tout (Ctrl+A) → colle le nouveau contenu
5. En bas → "Commit changes" → ajoute un message (ex: "Ajout feature X")
6. Clique **"Commit changes"**
7. **30 secondes** → app mise à jour automatiquement

### Méthode confortable (GitHub Desktop sur Mac/PC)

1. Télécharge **GitHub Desktop** sur desktop.github.com
2. Clone ton repository
3. Remplace `index.html` dans le dossier local
4. Dans GitHub Desktop : écris un message → clique **"Commit to main"** → **"Push origin"**
5. Déployé automatiquement

---

## 📋 Fichiers du projet

| Fichier | Description |
|---------|-------------|
| `index.html` | L'app complète (tout en un seul fichier) |
| `manifest.json` | Config PWA (nom, icône, couleurs) |
| `sw.js` | Service Worker (mode offline) |
| `icon-512.svg` | Icône de l'app |
| `README.md` | Ce fichier |

---

## ⚠️ Notes importantes

- **Les données** sont sauvegardées dans le `localStorage` du navigateur — elles restent sur ton téléphone, pas sur GitHub
- **Strava OAuth** : le Client Secret ne doit jamais être committé sur GitHub public — il reste dans ton localStorage
- **Mises à jour** : quand tu updates l'app, les données existantes ne sont pas perdues (localStorage séparé du code)

---

## 🛠️ Stack technique

- HTML/CSS/JS vanilla — zéro framework, zéro dépendance locale
- Chart.js (CDN) pour les graphiques
- API Anthropic Claude Sonnet 4.6 pour les features IA
- API Strava OAuth 2.0 pour la synchronisation
- PWA avec Service Worker pour le mode offline

---

*Made with Claude · UT3P 2026 🏔️*
