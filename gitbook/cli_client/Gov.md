# Gov

This module provides the basic functionalities for [Governance](../features/governance.md).

## Available Commands

| Name                                            | Description                                                       |
| ----------------------------------------------- | ----------------------------------------------------------------- |
| [proposal](#stafihubd-query-gov-proposal)            | Query details of a single proposal                                |
| [proposals](#stafihubd-query-gov-proposals)          | Query proposals with optional filter                              |
| [vote](#stafihubd-query-gov-vote)                    | Query details of a single vote                                    |
| [votes](#stafihubd-query-gov-votes)                  | Query votes on a proposal                                         |
| [deposit](#stafihubd-query-gov-deposit)              | Query details of a deposit                                        |
| [deposits](#stafihubd-query-gov-deposits)            | Query deposits on a proposal                                      |
| [tally](#stafihubd-query-gov-tally)                  | Get the tally of a proposal vote                                  |
| [param](#stafihubd-query-gov-param)                  | Query the parameters (voting                                      |
| [params](#stafihubd-query-gov-params)                | Query the parameters of the governance process                    |
| [proposer](#stafihubd-query-gov-proposer)            | Query which address proposed a proposal with a given ID.          |
| [submit-proposal](#stafihubd-tx-gov-submit-proposal) | Submit a proposal along with an initial deposit                   |
| [deposit](#stafihubd-tx-gov-deposit)                 | Deposit tokens for an active proposal                             |
| [vote](#stafihubd-tx-gov-vote)                       | Vote for an active proposal, options: yes/no/no_with_veto/abstain |

## stafihubd query gov proposal

Query details of a proposal.

```bash
stafihubd query gov proposal [proposal-id] [flags]
```

### Query a proposal

```bash
stafihubd query gov proposal <proposal-id>
```

## stafihubd query gov proposals

Query proposals with optional filter.

```bash
stafihubd query gov proposals [flags]
```

**Flags:**

| Name, shorthand | Type    | Required | Default | Description                                                         |
| --------------- | ------- | -------- | ------- | ------------------------------------------------------------------- |
| --depositor     | Address |          |         | Filter proposals by depositor address                               |
| --limit         | uint    |          |         | Limit to the latest [number] of proposals. Default to all proposals |
| --status        | string  |          |         | Filter proposals by status                                          |
| --voter         | Address |          |         | Filter proposals by voter address                                   |

### Query all proposals

```bash
stafihubd query gov proposals
```

### Query proposals by conditions

```bash
stafihubd query gov proposals --limit=3 --status=Passed --depositor=<iaa...>
```

## stafihubd query gov vote

Query details of a single vote.

```bash
stafihubd query gov vote [proposal-id] [voter-addr] [flags]
```

### Query a vote

```bash
stafihubd query gov vote <proposal-id> <iaa...>
```

## stafihubd query gov votes

Query votes on a proposal.

```bash
stafihubd query gov votes [proposal-id] [flags]
```

### Query all votes of a proposal

```bash
stafihubd query gov votes <proposal-id>
```

## stafihubd query gov deposit

Query details for a single proposal deposit on a proposal by its identifier.

```bash
stafihubd query gov deposit [proposal-id] [depositer-addr] [flags]
```

### Query a deposit of a proposal

```bash
stafihubd query gov deposit <proposal-id> <iaa...>
```

## stafihubd query gov deposits

Query details for all deposits on a proposal.

```bash
stafihubd query gov deposits [proposal-id] [flags]
```

### Query all deposits of a proposal

```bash
stafihubd query gov deposits <proposal-id>
```

## stafihubd query gov tally

Query tally of votes on a proposal. You can find the proposal-id by running "stafihubd query gov proposals".

```bash
stafihubd query gov tally [proposal-id] [flags]
```

### Query the statistics of a proposal

```bash
stafihubd query gov tally <proposal-id>
```

## stafihubd query gov param

Query the parameters (voting|tallying|deposit) of the governance process.

```bash
stafihubd query gov param [param-type] [flags]
```

Example:

```bash
> stafihubd query gov param voting
> stafihubd query gov param tallying
> stafihubd query gov param deposit
```

## stafihubd query gov params

Query the all the parameters for the governance process.

```bash
stafihubd query gov params [flags]
```

## stafihubd query gov proposer

Query which address proposed a proposal with a given ID.

```bash
stafihubd query gov proposer [proposal-id] [flags]
```

## stafihubd tx gov submit-proposal

Submit a proposal along with an initial deposit. Proposal title, description, type and deposit can be given directly or through a proposal JSON file.
Available Commands:  `community-pool-spend`, `param-change`, `software-upgrade`, `cancel-software-upgrade` .

### stafihubd tx gov submit-proposal community-pool-spend

Submit a community pool spend proposal along with an initial deposit.
The proposal details must be supplied via a JSON file.

```bash
stafihubd tx gov submit-proposal community-pool-spend <path/to/proposal.json> --from=<key_or_address>
```

Where proposal.json contains:

```json
{
    "title": "Community Pool Spend",
    "description": "Pay me some Fis!",
    "recipient": "iaa1mjk4p68mmulwla3x5uzlgjwsc3zrms448rel3q",
    "amount": "1000fis",
    "deposit": "1000fis"
}
```

### stafihubd tx gov submit-proposal param-change

Submit a parameter proposal along with an initial deposit.
The proposal details must be supplied via a JSON file. For values that contains objects, only non-empty fields will be updated.

IMPORTANT: Currently parameter changes are evaluated but not validated, so it is very important that any "value" change is valid (ie. correct type and within bounds) for its respective parameter, eg. "MaxValidators" should be an integer and not a decimal.

Proper vetting of a parameter change proposal should prevent this from happening (no deposits should occur during the governance process), but it should be noted regardless.

```bash
stafihubd tx gov submit-proposal param-change <path/to/proposal.json> --from=<key_or_address>
```

Where proposal.json contains:

```json
{
    "title": "Staking Param Change",
    "description": "Update max validators",
    "changes": [
        {
        "subspace": "staking",
        "key": "MaxValidators",
        "value": 105
        }
    ],
    "deposit": "1000fis"
}
```

### stafihubd tx gov submit-proposal software-upgrade

Submit a software upgrade along with an initial deposit.
Please specify a unique name and height OR time for the upgrade to take effect.

```bash
stafihubd tx gov submit-proposal software-upgrade [name] (--upgrade-height [height] | --upgrade-time [time]) (--upgrade-info [info]) [flags]
```

**Flags:**

| Name, shorthand  | Type   | Required | Default | Description                                                                               |
| ---------------- | ------ | -------- | ------- | ----------------------------------------------------------------------------------------- |
| --deposit        | Coin   | Yes      |         | Deposit of the proposal                                                                   |
| --title          | string | Yes      |         | Title of proposal                                                                         |
| --description    | string | Yes      |         | Description of proposal                                                                   |
| --upgrade-height | int64  |          |         | The height at which the upgrade must happen (not to be used together with --upgrade-time) |
| --time           | string |          |         | The time at which the upgrade must happen (not to be used together with --upgrade-height) |
| --info           | string |          |         | Optional info for the planned upgrade such as commit hash, etc.                           |

### stafihubd tx gov submit-proposal cancel-software-upgrade

Cancel a software upgrade along with an initial deposit.

```bash
stafihubd tx gov submit-proposal cancel-software-upgrade [flags]
```

**Flags:**

| Name, shorthand | Type   | Required | Default | Description             |
| --------------- | ------ | -------- | ------- | ----------------------- |
| --deposit       | Coin   | Yes      |         | Deposit of the proposal |
| --title         | string | Yes      |         | Title of proposal       |
| --description   | string | Yes      |         | Description of proposal |

## stafihubd tx gov deposit

Submit a deposit for an active proposal. You can find the proposal-id by running "stafihubd query gov proposals".

```bash
stafihubd tx gov deposit [proposal-id] [deposit] [flags]
```

### Deposit for an active proposal

```bash
stafihubd tx gov deposit [proposal-id] [deposit]
```

## stafihubd tx gov vote

Submit a vote for an active proposal. You can find the proposal-id by running "stafihubd query gov proposals".
Vote for an active proposal, options: yes/no/no_with_veto/abstain.

```bash
stafihubd tx gov vote [proposal-id] [option] [flags]
```

### Vote for an active proposal

```bash
stafihubd tx gov vote <proposal-id> <option> --from=<key-name> --fees=0.3stafihubd
```