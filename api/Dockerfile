FROM python:3.12.2-bookworm

WORKDIR /api

RUN pip install poetry

COPY pyproject.toml* poetry.lock* ./

RUN poetry install --no-root

ENTRYPOINT ["poetry", "run", "uvicorn", "src.main:app", "--host", "0.0.0.0", "--reload"]