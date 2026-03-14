# Freelancer Revenue Intelligence System

A full-stack application for freelancers to track revenue, manage invoices, and gain financial insights by integrating bank transactions, payments, scheduling, and AI-powered analytics.

## Overview

This system helps freelancers:
- **Track Income** — Automatically import bank transactions via Plaid
- **Manage Payments** — Process invoices and payments through Stripe
- **Schedule Smart** — Sync with Google Calendar for client meetings and deadlines
- **Stay Informed** — Automated email notifications via SendGrid
- **Get Insights** — AI-powered financial analysis using OpenAI

## Tech Stack

- **Backend:** Python + FastAPI
- **Database:** PostgreSQL 16
- **Cache:** Redis 7
- **Containerization:** Docker (via OrbStack)
- **Deployment:** AWS (planned)

## Integrations

| Service | Purpose |
|---------|---------|
| Plaid | Bank account linking & transaction sync |
| Stripe | Payment processing & invoicing |
| Google Calendar | Scheduling & reminders |
| SendGrid | Email notifications |
| OpenAI | Financial insights & analytics |

## Getting Started

### Prerequisites

- macOS with OrbStack installed
- Python 3.11+
- Git

### Setup

1. **Clone the repository**
```bash
   git clone https://github.com/hitakshiA/freelancer-revenue-system.git
   cd freelancer-revenue-system
```

2. **Configure environment variables**
```bash
   cp .env.example .env
   # Edit .env with your API keys
```

3. **Start the database services**
```bash
   docker compose up -d
```

4. **Verify services are running**
```bash
   docker ps
   # Should show freelancer_postgres and freelancer_redis
```

## Project Structure
```
freelancer-revenue-system/
├── docker-compose.yml    # PostgreSQL & Redis configuration
├── .env.example          # Environment variable template
├── .env                  # Your local environment variables (git-ignored)
├── .gitignore
└── README.md
```

## Development

### Branch Strategy

- `main` — Production-ready code (protected)
- `develop` — Active development branch

### Useful Commands
```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# View logs
docker compose logs -f

# Connect to PostgreSQL
docker exec -it freelancer_postgres psql -U postgres -d freelancer_revenue

# Test Redis
docker exec freelancer_redis redis-cli ping
```

## Roadmap

- [x] Phase 0: Project Setup & API Access
- [ ] Phase 1: Database Schema Design
- [ ] Phase 2: Plaid Integration
- [ ] Phase 3: Stripe Integration
- [ ] Phase 4: Google Calendar Integration
- [ ] Phase 5: SendGrid Integration
- [ ] Phase 6: OpenAI Integration
- [ ] Phase 7: AWS Deployment

## License

Private project — All rights reserved.
EOF
