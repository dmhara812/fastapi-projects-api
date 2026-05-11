# FastAPI Projects API

API REST profissional para gerenciamento de projetos e tarefas, construída com FastAPI, PostgreSQL, SQLAlchemy, Alembic, JWT, Docker, pytest e GitHub Actions.

## Status

Projeto em desenvolvimento incremental.

Etapa atual: estrutura base e configuração inicial.

## Stack

- Python 3.12+
- FastAPI
- PostgreSQL
- SQLAlchemy
- Alembic
- JWT
- Docker
- pytest
- Ruff
- GitHub Actions

## Arquitetura

```text
app/
  api/          -> rotas/controllers
  core/         -> configurações, segurança e dependências
  models/       -> modelos SQLAlchemy
  schemas/      -> schemas Pydantic
  repositories/ -> acesso ao banco
  services/     -> regras de negócio
  tests/        -> testes com pytest
alembic/
```

## Rodando localmente

Crie e ative o ambiente virtual:

```bash
python -m venv .venv
source .venv/bin/activate
.venv\Scripts\Activate.ps1
```

Instale dependências:

```bash
pip install -e ".[dev]"
```

Configure o ambiente:

```bash
cp .env.example .env
```

Suba a API localmente:

```bash
uvicorn app.main:app --reload
```

Acesse:

- API: http://localhost:8000
- Swagger: http://localhost:8000/docs
- Health check: http://localhost:8000/api/v1/health

## Próximos passos

- Configurar models SQLAlchemy
- Configurar Alembic
- Criar schemas Pydantic
- Criar repositories
- Criar services
- Implementar autenticação JWT
- Criar rotas CRUD
- Adicionar testes
- Finalizar Docker
- Configurar CI
