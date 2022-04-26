# Bank
Bank module allows you to manage assets in your local accounts.

## Available Commands
		
|Name   |Description   |
| :------------ | :------------ |
|[balances](#qbalances)   |Query for account balances by address    |
|[total](#qtotal)   |Query the total supply of coins of the chain    |
|[send](#txsend)   |Create and/or sign and broadcast a MsgSend transaction    |

### stafihubd query bank balances<span id='qbalances'></span>
Query the total balance of an account or of a specific denomination.
```
stafihubd query bank balances [address] [flags]
```

**Flags:**

|Name, shorthand    |Type    |Required    |Default    |Description    |
| :------------ | :------------ | :------------ | :------------ | :------------ |
|-h, --help   |   |   |   |Help for coin-type    |
|--denom    |string    |   |   |The specific balance denomination to query for    |
|--count-total   |   |   |   |Count total number of records in all balances to query for    |

## stafihubd query bank total<span id='qtotal'></span>
Query total supply of coins that are held by accounts in the chain.
```
stafihubd query bank total [flags]
```
**Flags:**

|Name, shorthand    |Type    |Required    |Default    |Description    |
| :------------ | :------------ | :------------ | :------------ | :------------ |
|-h, --help   |   |   |   |Help for coin-type    |
|--denom    |string    |   |   |The specific balance denomination to query for    |

## stafihubd tx bank send<span id='txsend'></span>
Sending tokens to another address, this command includes `generate`, `sign` and `broadcast` steps.
```
stafihubd tx bank send [from_key_or_address] [to_address] [amount] [flags]
```
**Flags:**

|Name, shorthand    |Type    |Required    |Default    |Description    |
| :------------ | :------------ | :------------ | :------------ | :------------ |
|-h, --help   |   |   |   |Help for coin-type    |

