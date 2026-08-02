# Mallette

Mallette is a self-hosted service that lets people store and share their files within an instance they control.

## Language

**Instance**:
One independently deployed Mallette backend and database, with its own administration, community of people, and data. Independent communities use separate deployments rather than sharing a multi-tenant backend.
_Avoid_: Server, application

**Instance administrator**:
A person authorized to configure an instance and manage its accounts and invitations. Administration grants no implicit access to another account's personal files or credentials; an instance may have several administrators but must always retain at least one.
_Avoid_: Admin, superuser

**Server operator**:
A person who controls the infrastructure hosting an instance and can therefore access its stored data and application secrets. Mallette does not protect data from its server operator.
_Avoid_: Instance administrator, host admin

**Instance member**:
A person with a verified account in an instance. Every instance administrator is also an instance member, with additional administrative capabilities.
_Avoid_: User, regular user

**Registration policy**:
An instance's choice to allow new open registrations or restrict them to invited people. Registration is restricted by default, and policy changes do not alter existing pending accounts or invitations.
_Avoid_: Private mode, registration lock

**Invitation**:
Revocable, time-limited permission granted by an instance administrator to one email address to create an account when open registration is not allowed. Accepting it demonstrates control of the invited email address.
_Avoid_: Pre-registration, access

**Account**:
A person's identity within one Mallette instance, identified by one normalized email address and used to access that person's files and spaces. Email identity is case-insensitive within an instance.
_Avoid_: User, profile, login

**Display name**:
An optional, non-unique name by which a person is shown to others. It is never an account identifier or login credential.
_Avoid_: Username, full name

**Pending account**:
An account whose email address has not yet been verified. It has no access to files or spaces and is discarded if it remains pending for 30 days.
_Avoid_: Inactive user, unverified user

**Verified account**:
An account whose owner has demonstrated control of its email address and which may access files and spaces.
_Avoid_: Active user, confirmed user

**Suspended account**:
An account whose data is retained but whose access has been disabled by an instance administrator. Reactivation permits future authentication but restores no previous connection.
_Avoid_: Banned user, deleted account, inactive user

**Pending email change**:
A time-limited request to replace an account's current verified email address with a new address. The current address remains authoritative until both the current and proposed addresses have independently approved the change.
_Avoid_: New email, unverified email

**Security event**:
An auditable record of authentication or account-security activity, visible to the affected account and to instance administrators. It contains operational metadata but never credentials or personal file content; internal administrative notes remain visible only to instance administrators.
_Avoid_: Audit log, application log
