 
# 🏪 Best-Quinca — Version Hybride (En ligne + Windows)
**Par ARIORI Adnel Adedeji Fulbert**

---

## 🗂️ Structure du projet

```
bestquinca-final/
└── server/
    ├── backend/          ← API Node.js + SQLite
    │   ├── routes/       ← auth, clients, materials, invoices, sales, trucks, team, backup
    │   ├── database.js   ← Schéma SQLite
    │   ├── middleware.js ← Auth JWT
    │   ├── server.js     ← Serveur Express (sert API + Landing + App)
    │   └── package.json
    ├── frontend/         ← Application React (accessible sur /app)
    │   ├── src/
    │   └── package.json
    ├── landing/          ← Site vitrine (accessible sur /)
    │   └── index.html
    └── downloads/        ← Fichiers téléchargeables
        └── BestQuinca-Windows-Portable.zip
```

---

## 🌐 Déploiement en ligne (Render.com — GRATUIT)

### Étapes :
1. Créer un compte sur https://render.com
2. "New +" → "Web Service"
3. Connecter votre dépôt GitHub (uploadez ce dossier)
4. Configurer :
   - **Build Command** : `cd frontend && npm install && npm run build`
   - **Start Command** : `cd backend && npm install && node server.js`
   - **Root Directory** : `server`
5. Variables d'environnement :
   - `NODE_ENV=production`
   - `JWT_SECRET=votre_secret_ultra_secret`
   - `PORT=10000` (Render assigne automatiquement)
6. Cliquer **Deploy** → votre URL : `https://bestquinca.onrender.com`

### Autres hébergeurs compatibles :
- **Railway.app** → même configuration, gratuit
- **Heroku** → plan gratuit disponible
- **VPS OVH/Contabo** → `node server.js` en production

---

## 💻 Lancement en local (développement)

```bash
# Terminal 1 — Backend + Landing
cd server/backend
npm install
node server.js
# → http://localhost:8081 (landing)
# → http://localhost:8081/app (application)

# Terminal 2 — Frontend dev (hot reload)
cd server/frontend
npm install
npm run dev
# → http://localhost:8000/app
```

---

## 📐 Architecture des URLs

| URL | Contenu |
|-----|---------|
| `https://votredomaine.com/` | Landing page marketing |
| `https://votredomaine.com/app` | Application Best-Quinca |
| `https://votredomaine.com/api/*` | API REST |
| `https://votredomaine.com/download/windows` | Téléchargement Windows |

---

## 🔑 Variables d'environnement (.env)

```env
PORT=8081
JWT_SECRET=changez_cette_valeur_en_production
NODE_ENV=production
```

---

*Best-Quinca v1.0.0 — © 2024 ARIORI Adnel Adedeji Fulbert*
=======
# Best-Quinca-v2
Best-Quinca - Gestion des stocks, ventes et clients  dans les Quincallerie .

