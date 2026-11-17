# Rouvanta

Application web de **location de voitures** avec un **assistant IA** intégré.

Les clients recherchent, réservent et paient (paiement simulé) une voiture en ligne ;
les agents gèrent les départs et retours ; l'administrateur gère la flotte et suit des indicateurs.
Un assistant conversationnel peut répondre aux questions et effectuer une réservation complète par le chat.

Projet réalisé par Mickaël Zongo — Mastère EISI, EPSI Paris.

## Stack technique

| Couche | Technologie |
|---|---|
| Frontend | Angular, Angular Material |
| Backend | Spring Boot (Java 21), Maven, Spring Security + JWT |
| Base de données | PostgreSQL 16 (Docker), migrations Flyway |
| IA | Spring AI + Ollama (local) |
| Tests / CI | JUnit 5, Mockito, GitHub Actions |

## Structure du dépôt

```
rouvanta/
├── backend/            # API REST Spring Boot
├── frontend/           # Application Angular
├── docker-compose.yml  # PostgreSQL (+ pgAdmin optionnel)
└── .env.example        # Modèle des variables d'environnement
```

## Prérequis

- Git
- Docker Desktop
- Java 21 (JDK)
- Node.js (LTS) et npm

## Lancer le projet

### 1. Variables d'environnement

```bash
cp .env.example .env
```

Ouvrir `.env` et remplacer les valeurs `change-me` par vos propres valeurs.

### 2. Base de données

```bash
docker compose up -d
docker compose ps
```

Le service `rouvanta-db` doit être à l'état `running (healthy)`.

pgAdmin (optionnel), accessible sur http://localhost:5050 :

```bash
docker compose --profile tools up -d
```

### 3. Backend et frontend

*Instructions ajoutées au fil du projet.*

## Licence

Projet pédagogique.
