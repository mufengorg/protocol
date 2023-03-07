---
sidebar_position: 7
---

# Clients

A user can query the `x/claims` module using the CLI, gRPC or REST.

## CLI

Find below a list of `matchd` commands added with the `x/claims` module.
You can obtain the full list by using the `matchd -h` command.

### Queries

The `query` commands allow users to query `claims` state.

**`total-unclaimed`**

Allows users to query total amount of unclaimed tokens from the airdrop.

```bash
matchd query claims total-unclaimed [flags]
```

**`records`**

Allows users to query all the claims records available.

```bash
matchd query claims records [flags]
```

**`record`**

Allows users to query a claims record for a given user.

```bash
matchd query claims record ADDRESS [flags]
```

**`params`**

Allows users to query claims params.

```bash
matchd query claims params [flags]
```

## gRPC

### Queries

| Verb   | Method                                     | Description                                      |
|--------|--------------------------------------------|--------------------------------------------------|
| `gRPC` | `match.claims.v1.Query/TotalUnclaimed`     | Gets the total unclaimed tokens from the airdrop |
| `gRPC` | `match.claims.v1.Query/ClaimsRecords`      | Gets all registered claims records               |
| `gRPC` | `match.claims.v1.Query/ClaimsRecord`       | Get the claims record for a given user            |
| `gRPC` | `match.claims.v1.Query/Params`             | Gets claims params                               |
| `GET`  | `/match/claims/v1/total_unclaimed`         | Gets the total unclaimed tokens from the airdrop |
| `GET`  | `/match/claims/v1/claims_records`          | Gets all registered claims records               |
| `GET`  | `/match/claims/v1/claims_records/{address}` | Gets a claims record for a given user            |
| `GET`  | `/match/claims/v1/params`                  | Gets claims params                               |
