# 🦊 Renardis – Guide interne et conventions techniques

Bienvenue dans l’organisation GitHub de **Renardis**.

Ce document présente les conventions internes **obligatoires** à respecter par tous les contributeurs et membres techniques de l’association.

Ces conventions garantissent :

- 🤝 Une collaboration efficace
- 🔒 Une sécurité rigoureuse
- 🧹 Un code propre et maintenable
- 📈 Une évolutivité durable
- 🧠 Un onboarding rapide des nouveaux membres

---

## 📂 Arborescence type d’un projet

```
project-name/
│
├── src/                  # Code source (frontend/backend/module)
│   ├── components/       # Composants (UI / modules réutilisables)
│   ├── pages/            # Pages (si applicable)
│   ├── services/         # Accès à des API ou logique métier
│   └── utils/            # Fonctions utilitaires
│
├── public/               # Assets publics (images, favicon, etc.)
├── tests/                # Fichiers de test
├── docs/                 # Documentation technique du projet
├── .env.example          # Variables d'environnement (modèle)
├── .gitignore
├── package.json / pyproject.toml / etc.
└── README.md
```

---

## 🌿 Git — conventions de branches

### 🌱 Branches principales

| Nom      | Description                                |
|----------|--------------------------------------------|
| `main`   | Production stable                          |
| `dev`    | Intégration des fonctionnalités validées   |

### 🌾 Branches secondaires

Toutes les branches doivent suivre le format :
```
type/identifiant-court-description
```

| Type        | Usage                                | Exemple                       |
|-------------|--------------------------------------|-------------------------------|
| `feature`   | Nouvelle fonctionnalité               | `feature/user-login`          |
| `fix`       | Correction de bug                     | `fix/login-error`             |
| `hotfix`    | Correction urgente sur `main`         | `hotfix/db-rollback`          |
| `refactor`  | Réécriture sans modification visible  | `refactor/user-service`       |
| `chore`     | Tâche technique (CI, config, etc.)    | `chore/update-eslint`         |
| `doc`       | Documentation                         | `doc/architecture-schema`     |
| `test`      | Ajout ou refonte de tests             | `test/form-validation`        |

> 🧠 Astuce : Évite les noms trop longs ou vagues. Pas de nom de branche comme `patch`, `dev2` ou `newstuff`.

---

## 💬 Git — conventions de commit

### Format standard

```bash
type(scope): message au présent, concis et en anglais
```

### Types autorisés

- `feat` : ajout de fonctionnalité
- `fix` : correction de bug
- `docs` : documentation uniquement
- `style` : code non-fonctionnel (indentation, CSS, nommages…)
- `refactor` : amélioration du code sans changement de comportement
- `perf` : amélioration des performances
- `test` : ajout ou mise à jour de tests
- `chore` : tâches annexes (CI, dépendances…)
- `ci` / `build` : intégration continue / scripts de build

### Exemples

```bash
feat(auth): add OAuth2 token support
fix(api): prevent null user crash on login
docs(README): clarify environment setup
refactor(core): split large function into smaller ones
test(api): add edge case tests for login
```
--- 

🦊 **Renardis – Pour un numérique éthique, structuré et collaboratif.**

