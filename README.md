# qa-portfolio-restful-booker
API testing portfolio with Postman &amp; Newman (Restful Booker API)

# QA Portfolio – Restful Booker

Ce dépôt fait partie de mon **portfolio QA** et illustre mes compétences en **tests manuels** et **tests automatisés** sur l’API [Restful Booker](https://restful-booker.herokuapp.com).

## 🚀 Objectifs
- Mettre en pratique mes compétences en **test d’API** avec Postman et Newman.
- Démontrer une structure de projet claire et réutilisable.
- Automatiser l’exécution des tests et générer des rapports.
- Intégrer les tests dans un workflow CI/CD (GitHub Actions).

## 🛠️ Stack utilisée
- [Postman](https://www.postman.com/) – Conception et exécution des collections de tests.
- [Newman](https://www.npmjs.com/package/newman) – Exécution en ligne de commande.
- [GitHub Actions](https://docs.github.com/en/actions) – CI/CD (intégration continue).
- [Node.js](https://nodejs.org/) – Gestion des dépendances.

## 📂 Structure du projet

qa-portfolio-restful-booker/
├── postman/
│ ├── collections/ # Fichiers Postman (.json)
│ ├── environments/ # Variables d’environnement Postman
│ └── reports/ # Rapports générés par Newman
├── .github/workflows/ # CI/CD pipelines (GitHub Actions)
├── README.md # Documentation du projet
└── package.json # Dépendances Node.js (Newman, etc.)


## ▶️ Exécution locale
### 1. Installer les dépendances
```bash
npm install

npx newman run postman/collections/restful-booker.postman_collection.json \
  -e postman/environments/restful-booker.postman_environment.json \
  -r cli,html

Le rapport HTML sera généré dans postman/reports/.

🔄 Intégration continue (CI/CD)

Les tests sont exécutés automatiquement via GitHub Actions à chaque push sur la branche main.
Le workflow est défini dans .github/workflows/newman-tests.yml.

📊 Rapports

Rapport CLI (console)

Rapport HTML (lisible dans un navigateur)

Possibilité future : intégration Allure Reports

👤 Auteur

Mohamed Touaoua

💼 LinkedIn https://www.linkedin.com/in/mohamed-touaoua-859301105/

📧 mtouaoua@yahoo.fr

