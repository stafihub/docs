# Relayers
Relayers module manager kinds of relayers.

## Available Commands

| Name                                  | Description                                            |
| ------------------------------------- | ------------------------------------------------------ |
| [relayers](#stafihubd-query-relayers-relayers) | Query relayers                  |
| [threshold](#stafihubd-query-relayers-threshold)       | Query threshold           |
| [add-relayers](#stafihubd-tx-relayers-add-relayers)            | Add new relayers |
| [delete-relayer](#stafihubd-tx-relayers-delete-relayer)            | Delete a relayer |
| [set-threshold](#stafihubd-tx-relayers-set-threshold)            | Set threshold |


## stafihubd query relayers relayers
Query the relayers of a specific denomination and arena.
```bash
stafihubd query relayers relayers [arena] [denom] [flags]
```

## stafihubd query relayers threshold
Query the threshold of a specific denomination and arena.
```bash
stafihubd query relayers threshold [arena] [denom] [flags]
```

## stafihubd tx relayers add-relayers
Add relayers for a specific denomination and arena.
```bash
stafihubd tx relayers add-relayers [arena] [denom] [addresses] [flags]
```

## stafihubd tx relayers delete-relayer
Delete a relayer for a specific denomination and arena.
```bash
stafihubd tx relayers delete-relayer [arena] [denom] [address] [flags]
```

## stafihubd tx relayers set-threshold
Set the threshold for a specific denomination and arena, the default value is 0 if unset.
```bash
stafihubd tx relayers set-threshold [arena] [denom] [value] [flags]
```