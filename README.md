# 100% Ramonté — plateforme de jeu

Quiz façon « 12 coups de midi » : candidats, tirage des matchs, match en direct avec chrono,
points, classement, questionnaires (préliminaires → huitièmes → quarts), rapports.
Site statique (aucune compilation) + Supabase (base de données, temps réel, connexion admin).

## 1. Supabase
1. Créez un projet sur https://supabase.com.
2. **SQL Editor** → collez le contenu de `supabase/schema.sql` → **Run**.
3. **Authentication → Users → Add user** : créez votre compte administrateur (e-mail + mot de passe).
4. **Authentication → Sign In / Providers** : désactivez « Allow new users to sign up »
   (sinon n'importe qui pourrait créer un compte et modifier le jeu).
5. **Project Settings → API** : copiez *Project URL* et la clé *anon public*.
6. Collez-les dans `config.js`.

## 2. GitHub
```
git init && git add . && git commit -m "100% Ramonté"
git branch -M main
git remote add origin https://github.com/VOTRE-COMPTE/ramonte.git
git push -u origin main
```

## 3. Vercel
**Add New → Project** → importez le dépôt GitHub → Framework : *Other* → **Deploy**
(pas de commande de build, pas de dossier de sortie à renseigner).

## Utilisation
- Les spectateurs ouvrent le lien : ils suivent tout en direct, sans connexion.
- Vous : menu ☰ → **Mon compte** → connexion. Vous contrôlez ensuite candidats, tirage,
  matchs, questions, règles et remises à zéro.
- Sans `config.js` rempli, le site fonctionne en mode local (données dans le navigateur).
