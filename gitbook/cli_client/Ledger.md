# Ledger
Ledger module allow users to liquidity stake/unstake rTokens and rToken relayers to send proposals.

## Way to Stake/Unstake rToken
- Stake:
Take rATOM as an example, only a common transfer on Cosmos Hub is needed to get rATOM.
 By sending an amount of ATOM to the given pool accounts of rATOM, rToken relayers will receive the corresponding event and send an execute-bond-proposal to StafiHub which will mint rATOM for the from account.
 - Unstake:
  [liquidity-unbond](#stafihubd-tx-ledger-liquidity-unbond) is the rpc interface for rToken holders to redeem their origin tokens.
  
  

## Available Query Commands

|Name   |Description   |
| :------------ | :------------ |
|[account-unbond](#stafihubd-query-ledger-account-unbond) |Query AccountUnbond|
|[bond-record](#stafihubd-query-ledger-bond-record) |Query BondRecord|
|[bonded-pools](#stafihubd-query-ledger-bonded-pools) |Query bonded-pools|
|[chain-era](#stafihubd-query-ledger-chain-era) |Query getChainEra|
|[era-exchange-rate](#stafihubd-query-ledger-era-exchange-rate) |Query EraExchangeRate by a given denom and era |
|[era-exchange-rates](#stafihubd-query-ledger-era-exchange-rates) |Query EraExchangeRatesByDenom|
|[era-unbond-limit](#stafihubd-query-ledger-era-unbond-limit) |Query getEraUnbondLimit |
|[exchange-rate](#stafihubd-query-ledger-exchange-rate) |Show ExchangeRate for a given denom |
|[exchange-rate-list](#stafihubd-query-ledger-exchange-rate-list) |List all ExchangeRate |
|[pool-detail](#stafihubd-query-ledger-pool-detail)   |Query subaccounts and threshold of a pool   |
|[pool-unbond](#stafihubd-query-ledger-pool-unbond)   |Query unbonds by a given pool|
|[protocol-fee-receiver](#stafihubd-query-ledger-protocol-fee-receiver)| Query protocol fee receiver|
|[relay-fee-receiver](#stafihubd-query-ledger-relay-fee-receiver) |Query relay fee receiver|
|[staking-reward-commission](#stafihubd-query-ledger-staking-reward-commission) |Query staking reward commission|
|[total-protocol-fee](#stafihubd-query-ledger-total-protocol-fee) |Query total protocol fee|
|[unbond-commission](#stafihubd-query-ledger-unbond-commission) |Query getUnbondCommission|
|[unbond-relay-fee](#stafihubd-query-ledger-unbond-relay-fee) |Query getUnbondRelayFee|

### stafihubd query ledger account-unbond 
```
stafihubd query ledger account-unbond [denom] [unbonder] [flags]
```

### stafihubd query ledger bond-record 
```
stafihubd query ledger bond-record [denom] [txhash] [flags]
```

### stafihubd query ledger bonded-pools 
```
stafihubd query ledger bonded-pools [denom] [flags]
```

### stafihubd query ledger chain-era 
```
stafihubd query ledger chain-era [denom] [flags]
```

### stafihubd query ledger era-exchange-rate 
```
stafihubd query ledger era-exchange-rate [denom] [era] [flags]
```

### stafihubd query ledger era-exchange-rates
```
stafihubd query ledger era-exchange-rates [denom] [flags]
```

### stafihubd query ledger era-unbond-limit
```
stafihubd query ledger era-unbond-limit [denom] [flags]
```

### stafihubd query ledger exchange-rate 
```
stafihubd query ledger exchange-rate [denom] [flags]
```

### stafihubd query ledger exchange-rate-list 
```
stafihubd query ledger exchange-rate-list [flags]
```

### stafihubd query ledger pool-detail
```
stafihubd query ledger pool-detail [denom] [pool] [flags]
```

### stafihubd query ledger pool-unbond 
```
stafihubd query ledger pool-unbond [denom] [pool] [era] [flags]
```

### stafihubd query ledger protocol-fee-receiver 
```
stafihubd query ledger protocol-fee-receiver [flags]
```

### stafihubd query ledger relay-fee-receiver
```
stafihubd query ledger relay-fee-receiver [denom] [flags]
```

### stafihubd query ledger staking-reward-commission 
```
stafihubd query ledger staking-reward-commission [denom] [flags]
```

### stafihubd query ledger total-protocol-fee
```
stafihubd query ledger total-protocol-fee [flags]
```

### stafihubd query ledger unbond-commission
```
stafihubd query ledger unbond-commission [denom] [flags]
```

### stafihubd query ledger unbond-relay-fee
```
stafihubd query ledger unbond-relay-fee [denom] [flags]
```


### Useful Tx Commands

|Name   |Description   |
| :------------ | :------------ |
|[liquidity-unbond](#stafihubd-tx-ledger-liquidity-unbond)   |redeem rToken    |


### stafihubd tx ledger liquidity-unbond
```
stafihubd tx ledger liquidity-unbond [pool] [value] [recipient] [flags]
```

