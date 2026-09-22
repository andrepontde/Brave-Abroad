# Brave-Abroad

## Requirements

- Python 3.10 or newer
- `uv`
- Docker Desktop

## Install

```bash
git clone <repository-url>
cd Brave-Abroad
uv sync
cp .env.example .env
```

## Run the database

```bash
docker compose up -d
uv run alembic upgrade head
```

To stop the database:

```bash
docker compose down
```

The local database connection is configured through `DATABASE_URL` in `.env`.