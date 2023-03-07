---
sidebar_position: 8
---

# Clients

## CLI

Find below a list of  `matchd` commands added with the  `x/revenue` module.
You can obtain the full list by using the `matchd -h` command.
A CLI command can look like this:

```bash
matchd query revenue params
```

### Queries

| Command            | Subcommand             | Description                              |
| :----------------- | :--------------------- | :--------------------------------------- |
| `query` `revenue` | `params`               | Get revenue params                          |
| `query` `revenue` | `contract`             | Get the revenue for a given contract   |
| `query` `revenue` | `contracts`            | Get all revenues                       |
| `query` `revenue` | `deployer-contracts`   | Get all revenues of a given deployer   |
| `query` `revenue` | `withdrawer-contracts` | Get all revenues of a given withdrawer |

### Transactions

| Command         | Subcommand | Description                                |
| :-------------- | :--------- | :----------------------------------------- |
| `tx` `revenue` | `register` | Register a contract for receiving revenue     |
| `tx` `revenue` | `update`   | Update the withdraw address for a contract |
| `tx` `revenue` | `cancel`   | Remove the revenue for a contract        |

## gRPC

### Queries

| Verb   | Method                                            | Description                              |
| :----- | :------------------------------------------------ | :--------------------------------------- |
| `gRPC` | `match.revenue.v1.Query/Params`                  | Get revenue params                          |
| `gRPC` | `match.revenue.v1.Query/Revenue`                | Get the revenue for a given contract   |
| `gRPC` | `match.revenue.v1.Query/Revenues`               | Get all revenues                       |
| `gRPC` | `match.revenue.v1.Query/DeployerRevenues`       | Get all revenues of a given deployer   |
| `gRPC` | `match.revenue.v1.Query/WithdrawerRevenues`     | Get all revenues of a given withdrawer |
| `GET`  | `/match/revenue/v1/params`                       | Get revenue params                          |
| `GET`  | `/match/revenue/v1/revenues/{contract_address}`  | Get the revenue for a given contract   |
| `GET`  | `/match/revenue/v1/revenues`                    | Get all revenues                       |
| `GET`  | `/match/revenue/v1/revenues/{deployer_address}` | Get all revenues of a given deployer   |
| `GET`  | `/match/revenue/v1/revenues/{withdraw_address}` | Get all revenues of a given withdrawer |

### Transactions

| Verb   | Method                                     | Description                                |
| :----- | :----------------------------------------- | :----------------------------------------- |
| `gRPC` | `match.revenue.v1.Msg/RegisterRevenue`   | Register a contract for receiving revenue     |
| `gRPC` | `match.revenue.v1.Msg/UpdateRevenue`     | Update the withdraw address for a contract |
| `gRPC` | `match.revenue.v1.Msg/CancelRevenue`     | Remove the revenue for a contract        |
| `POST` | `/match/revenue/v1/tx/register_revenue` | Register a contract for receiving revenue     |
| `POST` | `/match/revenue/v1/tx/update_revenue`   | Update the withdraw address for a contract |
| `POST` | `/match/revenue/v1/tx/cancel_revenue`   | Remove the revenue for a contract        |
