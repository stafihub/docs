# rBank
rBank module allows admin to add new denom and its metadata and address-prefix.

## Available Commands

| Name                                  | Description                                            |
| ------------------------------------- | ------------------------------------------------------ |
| [address-prefix](#stafihubd-query-rbank-address-prefix) | Query address prefix of denom                  |
| [params](#stafihubd-query-rbank-params)       | Shows the parameters of the module           |
| [add-denom](#stafihubd-tx-rbank-add-denom)            | Add metadata and addressPrefix |

## stafihubd query rbank address-prefix
Query the address-prefix of a specific denomination.
```bash
stafihubd query rbank address-prefix [denom] [flags]
```

## stafihubd query rbank params
Query the genesis params of rbank module.
```bash
stafihubd query rbank params [flags]
```

## stafihubd tx rbank add-denom
Add a new denom, and its metadata and address-prefix.
```bash
stafihubd tx rbank add-denom [address-prefix] [metadata-path] [flags]
```