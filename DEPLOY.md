# 🚀 TURF IA ULTIMATE — DÉPLOIEMENT 3 ÉTAPES (15 min)

## CE QUE C'EST

Claude analyse chaque course et décide à ta place :
- ✅ JOUER → numéros + mise exacte en € (Kelly criterion)
- ⏭️ PASSER → explication complète pourquoi
- 💡 Apprend de chaque erreur tout seul
- 📱 Telegram : notification immédiate après chaque décision
- 💰 Bankroll suivie en temps réel

---

## ÉTAPE 1 — Bot Telegram (2 min)

1. Telegram → **@BotFather** → `/newbot`
2. Nom : `Turf IA` | Username : `turf_hamani_bot`
3. **Copie le TOKEN** : `123456789:ABCdef...`
4. Telegram → **@userinfobot** → envoie n'importe quoi → copie ton **Chat ID**

---

## ÉTAPE 2 — Base de données (2 min)

1. **https://neon.tech** → Sign Up (GitHub)
2. New Project → `turf-ia` → EU West
3. Dashboard → Connection string → copie l'URL :
   `postgresql://user:pass@ep-xxx.neon.tech/neondb?sslmode=require`

---

## ÉTAPE 3 — Déploiement 1 clic Render (10 min)

1. **https://github.com** → New repo → upload ce dossier
2. **https://render.com** → Sign Up → New → **Blueprint**
3. Connecte ton repo → Render détecte `render.yaml`
4. Renseigne ces **4 variables** :

| Variable | Valeur |
|----------|--------|
| `DATABASE_URL` | URL Neon (étape 2) |
| `ANTHROPIC_API_KEY` | Clé Claude (console.anthropic.com) |
| `TELEGRAM_BOT_TOKEN` | Token BotFather (étape 1) |
| `TELEGRAM_CHAT_ID` | Ton Chat ID (étape 1) |

5. Clique **Apply** → Render déploie tout

---

## RÉSULTAT

Dans 5 minutes tu reçois sur Telegram :
> 🤖 TURF IA ULTIMATE démarré
> 💰 Bankroll: 500.00€

Ensuite, pour chaque course que tu veux analyser :
1. Ouvre le dashboard
2. Choisis la date → réunion → course
3. Clique **CLAUDE DÉCIDE**
4. Telegram te dit immédiatement : JOUER ou PASSER + pourquoi + combien

---

## COÛTS

| Service | Coût |
|---------|------|
| Render (backend + crons) | ~21$/mois |
| Render (dashboard) | Gratuit |
| Neon.tech (DB) | Gratuit |
| Anthropic Claude | ~0.10€/décision |
| **TOTAL** | **~21$/mois + ~3€/100 courses** |

---

## FONCTIONNEMENT AUTO (sans toi)

| Heure | Action |
|-------|--------|
| Toutes les 30min | Vérification des arrivées PMU |
| Après chaque résultat | Claude apprend, met à jour bankroll, notifie Telegram |
| 7h00 chaque matin | Briefing stratégique Claude sur Telegram |
