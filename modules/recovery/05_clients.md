---
sidebar_position: 5
---

# Clients

A user can query the `x/recovery` module using the CLI, gRPC or REST.

## CLI

Find below a list of `matchd` commands added with the `x/recovery` module.
You can obtain the full list by using the `matchd` -h command.

### Queries

The query commands allow users to query Recovery state.

**`params`**
Allows users to query the module parameters.

```bash
matchd query recovery params [flags]
```

## gRPC

### Queries

| Verb   |              Method              |           Description |
| :----- | :------------------------------- | :-------------------- |
| `gRPC` | `match.recovery.v1.Query/Params` | `Get Recovery params` |
| `GET`  |   `/match/recovery/v1/params`    | `Get Recovery params` |
