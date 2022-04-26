# rVote
rBank module allows admin to add new denom and its metadata and address-prefix.

## Available Commands

| Name                                  | Description                                            |
| ------------------------------------- | ------------------------------------------------------ |
| [proposal](#stafihubd-query-rvote-proposal) | Query Proposal                  |
| [proposal-life](#stafihubd-query-rvote-proposal-life)       | Query ProposalLife           |
| [set-proposal-life](#stafihubd-tx-rvote-set-proposal-life)            | Set ProposalLife |

## stafihubd query rvote proposal
Query the proposal of a specific prop-id.
```bash
stafihubd query rvote proposal [prop-id] [flags]
```

## stafihubd query rvote proposal-life
Query `ProposalLife`, `ProposalLife` indicates how long a proposal can be voted on.
```bash
stafihubd query rvote proposal-life [flags]
```

## stafihubd tx rvote set-proposal-life
Add a new denom, and its metadata and address-prefix.
```bash
stafihubd tx rvote set-proposal-life [proposal-life] [flags]
```