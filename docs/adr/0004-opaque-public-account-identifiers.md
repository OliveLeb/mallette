# Expose UUIDv7 account identifiers

Accounts retain an internal database identifier where useful, but all API payloads, routes, and client references expose a stable UUIDv7 public identifier. This adds a second identifier and mapping discipline while preventing the direct enumeration inherent in sequential database IDs and avoiding an immediate rewrite of every internal foreign key.
