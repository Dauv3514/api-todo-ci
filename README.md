# API TODO - CI/CD

[![CI/CD Pipeline](https://github.com/Dauv3514/api-todo-ci/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/Dauv3514/api-todo-ci/actions/workflows/ci-cd.yml)
API TODO avec déploiement automatique via GitHub Actions et Render.
## Fonctionnalités
- CRUD complet pour les todos
- Tests unitaires (8 tests)
- CI/CD automatique
- Déploiement automatique sur Render
## API Déployée
**URL :** https://api-todo-ci-valentin.onrender.com
## Endpoints
| Méthode | Route | Description |
|---------|-------|-------------|
| GET | `/` | Infos de l'API |
| GET | `/todos` | Liste tous les todos |
| GET | `/todos/:id` | Un todo spécifique |
| POST | `/todos` | Créer un todo |
| PUT | `/todos/:id` | Modifier un todo |
| DELETE | `/todos/:id` | Supprimer un todo |
| GET | `/health` | Status de l'API |
## Exemples d'utilisation
### Récupérer tous les todos
```bash
curl https://api-todo-ci-valentin.onrender.com/todos
```
### Créer un todo
```bash
curl -X POST https://api-todo-ci-valentin.onrender.com/todos \
-H "Content-Type: application/json" \
-d '{"title":"Apprendre le CI/CD"}'
```
### Health check
```bash
curl https://api-todo-ci-valentin.onrender.com/health
```
## Développement Local
```bash
# Installer les dépendances
npm install# Lancer le serveur
npm start
# Lancer les tests
npm test
```
## Pipeline CI/CD
Le pipeline s'exécute automatiquement à chaque push :
1. **Lint** : Vérification de la syntaxe
2. **Test** : Exécution des 8 tests unitaires
3. **Build** : Vérification que tout compile
4. **Deploy** : Déploiement automatique sur Render (seulement sur `main`)
## Projet réalisé dans le cadre du cours CI/CD
**MyDigitalSchool - Janvier 2026**
