# Use PostgreSQL in every environment

The backend uses PostgreSQL in development, tests, and production, with PostgreSQL 18 as the Docker and CI reference and local environments provided through Docker; SQLite support is removed. This adds a database service to self-hosting but ensures that transactions, uniqueness constraints, session storage, rate limiting, and concurrent outbox claims behave consistently and are tested against the production engine.
