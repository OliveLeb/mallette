# Use one Mallette instance per deployment

One deployed backend and PostgreSQL database represent exactly one independently administered Mallette instance; hosting another isolated community requires another deployment. This rejects database-level multi-tenancy and its operational consolidation benefits in favor of simpler authorization, configuration, data isolation, and self-hosting.
