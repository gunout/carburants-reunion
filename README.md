# ⛽ Prix des Carburants — La Réunion (974)

### Dashboard analytique · 2016-2026 · 8 graphiques · 20 KPI · 4 onglets

[![Préfecture](https://img.shields.io/badge/Préfecture-La%20Réunion-0d7a8a?style=for-the-badge)](https://www.reunion.gouv.fr/)
[![Département](https://img.shields.io/badge/Département-974-c0392b?style=for-the-badge)](https://www.reunion.gouv.fr/)
[![Région](https://img.shields.io/badge/Région-La%20Réunion-0d7a8a?style=for-the-badge)](https://www.reunion.gouv.fr/)

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![License](https://img.shields.io/badge/License-MIT-000091?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/version-2.0.0-ffb800?style=for-the-badge)]()
[![Statut](https://img.shields.io/badge/statut-actif-00a95f?style=for-the-badge)]()

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)]()
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)]()
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)]()
[![DSFR](https://img.shields.io/badge/DSFR-1.12.1-000091?style=flat-square)](https://www.systeme-de-design.gouv.fr/)
[![SVG](https://img.shields.io/badge/SVG-natif-FFB13B?style=flat-square&logo=svg&logoColor=white)]()
[![INSEE](https://img.shields.io/badge/INSEE-Série%20001769773-000091?style=flat-square)](https://www.insee.fr/fr/statistiques/serie/001769773)
[![PRs](https://img.shields.io/badge/PRs-welcome-00a95f?style=flat-square)](https://github.com/gunout/carburants-reunion/pulls)

[![GitHub stars](https://img.shields.io/github/stars/gunout/carburants-reunion?style=social)](https://github.com/gunout/carburants-reunion/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/gunout/carburants-reunion?style=social)](https://github.com/gunout/carburants-reunion/network/members)
[![GitHub issues](https://img.shields.io/github/issues/gunout/carburants-reunion?style=flat-square)](https://github.com/gunout/carburants-reunion/issues)
[![GitHub last commit](https://img.shields.io/github/last-commit/gunout/carburants-reunion?style=flat-square)](https://github.com/gunout/carburants-reunion/commits/main)
[![GitHub repo size](https://img.shields.io/github/repo-size/gunout/carburants-reunion?style=flat-square)](https://github.com/gunout/carburants-reunion)

---

## 📖 Présentation

**Prix des Carburants — La Réunion** est un **dashboard analytique complet** qui retrace l'évolution des prix des carburants à La Réunion de **2016 à 2026**.

L'outil combine deux sources officielles :

1. **INSEE** — Indice mensuel des prix des produits pétroliers (base 100 = 2015), série `001769773`, couvrant 1998-2025.
2. **Communiqués de la Préfecture** — Prix officiels en €/L des 9 mois de 2026.

> ⚡ **100 % statique** : le dashboard est un simple fichier HTML qui charge un JSON via `fetch()`. Aucun backend requis.

---

## ✨ Fonctionnalités

### 📊 8 graphiques analytiques

- 📈 **Évolution Super + Gazole** — Courbes avec pics/creux annotés
- 📊 **Indice INSEE** — Aire + ligne base 100 + points remarquables
- 📅 **Moyennes annuelles** — Barres groupées Super/Gazole par année
- 📉 **Écart Super - Gazole** — Aire violette avec écart max annoté
- 📊 **Distribution** — Histogramme des prix du Super par tranche
- 🎯 **Volatilité mensuelle** — Barres rouges/vertes des variations %
- 🔥 **Heatmap annuelle** — Matrice 11 ans × 12 mois avec gradient
- 🌡️ **Profil saisonnier** — Prix moyen par mois toutes années confondues

### 🎯 20 KPI en temps réel

- Super : dernier, moyenne, pic, creux
- Gazole : dernier, moyenne
- Écart actuel et moyen Super - Gazole
- Évolution mensuelle (%)
- Détection automatique des extrêmes

### 📋 4 onglets navigables

| Onglet | Contenu |
|---|---|
| **📊 Vue d'ensemble** | KPI + graphiques 1, 2, 3 |
| **📈 Analyse avancée** | Graphiques 4, 5, 6, 7 |
| **📅 Saisonnalité** | Graphique 8 + tableau comparatif annuel |
| **📋 Données** | Tableau complet + filtres + export CSV |

### 🛠️ Outils intégrés

- 🔍 **Filtres interactifs** : année, mois, recherche texte
- 📥 **Export CSV** avec toutes les colonnes
- 🎨 **Design DSFR** (charte de l'État français)
- 📱 **Responsive** (mobile, tablette, desktop)
- ⚡ **Aucune dépendance externe** (SVG natif)
- 🎯 **Surlignage 2026** en jaune dans le tableau

---

## 🚀 Installation

### Prérequis

- **Python** ≥ 3.8 (pour le serveur HTTP local)
- **Node.js** ≥ 18 (pour les scripts de génération JSON)
- Un navigateur moderne (Chrome, Firefox, Safari, Edge)

### Étapes rapides

```bash
# 1. Cloner le dépôt
git clone https://github.com/gunout/carburants-reunion.git
cd carburants-reunion

# 2. Installer les dépendances (si utilisation des scrapers)
npm install

# 3. Lancer le serveur HTTP
python3 -m http.server 8021

# 4. Ouvrir le dashboard
# → http://localhost:8021
```

> ⚠️ **Important** : n'ouvrez **jamais** `index.html` en double-clic (`file://`). Le navigateur bloquera le chargement du JSON pour des raisons de sécurité (CORS). Passez toujours par `http://localhost:8021`.

---

## 🎮 Utilisation

### Lancer le dashboard

```bash
cd ~/Desktop/carburants-reunion

# Python 3 (recommandé)
python3 -m http.server 8021

# Ou Python 2
python -m SimpleHTTPServer 8021

# Ou Node.js (alternative)
npx http-server -p 8021 -c-1
```

Puis ouvrez **http://localhost:8021**

### Régénérer les données

```bash
# Parser la série INSEE
node parse-insee.js
# → génère json/prix_carburants_reunion.json (119 points)

# Fusionner avec 2026
node fusion_2026.js
# → génère json/prix_carburants_reunion_complet.json (128 points)
```

### Automatisation (cron)

Pour régénérer les données chaque mois :

```bash
crontab -e

# Ajouter cette ligne (1er du mois à 3h)
0 3 1 * * cd /home/user/carburants-reunion && node fusion_2026.js >> /var/log/carburants.log 2>&1
```

---

## 🏗️ Architecture

```
carburants-reunion/
├── 📄 index.html                          # Dashboard principal
├── 🐍 parse-insee.js                      # Parseur série INSEE
├── 🐍 fusion_2026.js                      # Fusion INSEE + 2026
├── 📦 package.json                        # Dépendances Node
├── 📖 README.md                           # Ce fichier
├── 📜 LICENSE                             # MIT
├── 📁 json/
│   ├── 📊 prix_carburants_reunion.json            # Données INSEE (119 pts)
│   └── 📊 prix_carburants_reunion_complet.json    # Fusion 2016-2026 (128 pts)
└── 📁 debug/                              # Fichiers HTML téléchargés (optionnel)
```

### Stack technique

| Composant | Technologie |
|---|---|
| **Dashboard** | HTML5 + CSS3 + JavaScript Vanilla (ES6+) |
| **Graphiques** | SVG natif (aucune librairie externe) |
| **UI** | [DSFR 1.12.1](https://www.systeme-de-design.gouv.fr/) |
| **Police** | Marianne |
| **Couleurs** | Bleu France `#000091`, Rouge Marianne `#E1000F`, Bleu Océan `#0d7a8a` |
| **Source INSEE** | API SDMX série `001769773` |
| **Source 2026** | Communiqués Préfecture de La Réunion |

### Flux de données

```
┌─────────────────────┐     ┌─────────────────────┐
│  INSEE (SDMX)       │     │  Préfecture 974     │
│  Série 001769773    │     │  Communiqués 2026   │
└──────────┬──────────┘     └──────────┬──────────┘
           │  parse-insee.js           │
           ▼                           ▼
┌──────────────────────────────────────────────┐
│  prix_carburants_reunion.json (119 pts)      │
│         +  fusion_2026.js                    │
│  prix_carburants_reunion_complet.json (128)  │
└──────────────────┬───────────────────────────┘
                   │  fetch() HTTP
                   ▼
┌──────────────────────────────────────────────┐
│  index.html — Dashboard interactif           │
│  8 graphiques · 20 KPI · 4 onglets           │
└──────────────────────────────────────────────┘
```

### Structure d'un relevé (JSON)

```json
{
  "date": "2026-10-01",
  "annee": 2026,
  "mois": 10,
  "indice": null,
  "super": 2.00,
  "gazole": 1.80,
  "gnr": null,
  "gaz": 20.81,
  "source": "Communiqué préfecture octobre 2026"
}
```

---

## 📊 Données couvertes

| Période | Nombre de points | Source |
|---|---|---|
| **Janvier 2016 → Décembre 2025** | 119 mois | INSEE (indice interpolé) |
| **Janvier 2026 → Octobre 2026** | 9 mois | Communiqués Préfecture |
| **TOTAL** | **128 relevés** | Combiné |

### Points remarquables

| Date | Événement | Indice |
|---|---|---|
| **Juillet 2022** | 🔴 Pic historique | 150,07 |
| **Mai 2020** | 🟢 Creux COVID | 83,20 |
| **Octobre 2026** | 🔴 Record Super | 2,00 €/L |

---

## 🔍 Sources officielles

- **[INSEE](https://www.insee.fr/fr/statistiques/serie/001769773)** — Indice des prix des produits pétroliers à La Réunion (base 2015)
- **[Préfecture de La Réunion](https://www.reunion.gouv.fr/)** — Communiqués mensuels sur les prix des carburants
- **[OPMR](https://www.opmr.re/)** — Observatoire des Prix, des Marges et des Revenus
- **[Code de l'énergie](https://www.legifrance.gouv.fr/)** — Articles R.671-14 à R.671-22

---

## ❓ FAQ

<details>
<summary><strong>Le dashboard affiche « Impossible de charger json/... »</strong></summary>

Vous avez probablement ouvert le HTML en `file://` (double-clic). Utilisez un serveur HTTP :

```bash
python3 -m http.server 8021
```

Puis ouvrez `http://localhost:8021`.
</details>

<details>
<summary><strong>Comment obtenir les prix avant 2016 ?</strong></summary>

La série INSEE `000642079` (base 1998) contient les données 1998-2015. Modifiez `parse-insee.js` pour utiliser cet ID.
</details>

<details>
<summary><strong>Les prix en €/L sont-ils exacts ?</strong></summary>

Pour 2026 : oui, ce sont les prix officiels. Pour 2016-2025 : ils sont **estimés par interpolation** sur 3 ancres confirmées (2016-01, 2024-11, 2025-12) à partir de l'indice INSEE. La tendance est fidèle mais l'incertitude peut atteindre ±5 %.
</details>

<details>
<summary><strong>Le port 8021 est déjà utilisé</strong></summary>

Utilisez un autre port :

```bash
python3 -m http.server 8080
```

Puis ouvrez `http://localhost:8080`.
</details>

<details>
<summary><strong>Comment ajouter 2027 ?</strong></summary>

Ajoutez les nouveaux points dans `fusion_2026.js` (tableau `data2026`), puis relancez :

```bash
node fusion_2026.js
```
</details>

<details>
<summary><strong>Puis-je héberger le dashboard en ligne ?</strong></summary>

Oui ! Le dashboard est 100 % statique. Déposez `index.html` et `json/` sur :
- GitHub Pages
- Netlify
- Vercel
- Un simple nginx / apache

Aucun backend nécessaire.
</details>

---

## 🤝 Contribuer

Les contributions sont **les bienvenues** !

1. **Fork** le projet ([github.com/gunout/carburants-reunion/fork](https://github.com/gunout/carburants-reunion/fork))
2. **Créez** une branche (`git checkout -b feature/ma-fonctionnalite`)
3. **Committez** (`git commit -m 'Ajout de ma fonctionnalité'`)
4. **Pushez** (`git push origin feature/ma-fonctionnalite`)
5. **Ouvrez** une Pull Request ([github.com/gunout/carburants-reunion/pulls](https://github.com/gunout/carburants-reunion/pulls))

### Idées d'amélioration

- [ ] Intégration API INSEE en temps réel
- [ ] Comparaison avec d'autres DROM (Guadeloupe, Martinique, Guyane, Mayotte)
- [ ] Prédictions par ML (Prophet, ARIMA)
- [ ] Notifications email sur nouveaux pics
- [ ] Mode PWA offline
- [ ] Export Excel (`.xlsx`)
- [ ] Thème sombre
- [ ] Timeline interactive

### Conventions

- **Code** : français pour les commentaires, anglais pour les variables
- **Commits** : [Conventional Commits](https://www.conventionalcommits.org/fr/)
- **Style** : 2 espaces, point-virgules, ES6+

---

## 📜 License

Ce projet est sous licence **MIT**. Voir [LICENSE](https://github.com/gunout/carburants-reunion/blob/main/LICENSE) pour plus de détails.

```
MIT License

Copyright (c) 2026 gunout

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Remerciements

- [INSEE](https://www.insee.fr/) pour la série officielle des prix
- [Préfecture de La Réunion](https://www.reunion.gouv.fr/) pour les communiqués mensuels
- [Système de Design de l'État (DSFR)](https://www.systeme-de-design.gouv.fr/) pour la charte graphique
- [Shields.io](https://shields.io/) pour les badges

---

## 📞 Contact

- 🐛 **Bug / Suggestion** : [Ouvrir une issue](https://github.com/gunout/carburants-reunion/issues)
- 💬 **Discussion** : [Ouvrir une discussion](https://github.com/gunout/carburants-reunion/discussions)
- 👤 **Auteur** : [@gunout](https://github.com/gunout)

---

<div align="center">

**🇷🇪 Fait avec ❤️ pour La Réunion**

[![Préfecture](https://img.shields.io/badge/Préfecture-La%20Réunion-0d7a8a?style=flat-square)](https://www.reunion.gouv.fr/)
[![République](https://img.shields.io/badge/République-Française-000091?style=flat-square)](https://www.gouvernement.fr/)
[![GitHub](https://img.shields.io/badge/GitHub-gunout%2Fcarburants--reunion-181717?style=flat-square&logo=github)](https://github.com/gunout/carburants-reunion)

*Liberté · Égalité · Fraternité*

**Dernière mise à jour** : Octobre 2026

</div>

---

---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>
