## Ledger
Ledger module allow users to liquidity stake/unstake rTokens and rToken relayers to send proposals.

### Available Query Commands

|Name   |Description   |
| :------------ | :------------ |
|bonded-pools-by-denom   |query bonded pools by denom    |
|era-exchange-rates-by-denom   |get rates of a rToken of all eras by its denom|
|get-account-unbond   |query unbonds for a given account|
|get-bond-pipeline   |query bond pipeline|
|get-bond-record   |query bond record|
|get-chain-bonding-duration   |query bonding duration for a given denom|
|get-chain-era   |query current era for a given denom|
|get-commission   |query commission|
|get-current-era-snap-shot   |query current era snapshot|
|get-era-snap-shot   |query snapshot at a specific era|
|get-era-unbond-limit   |query unbond limit at a specific era|
|get-least-bond   |query least bond for a given denom|
|get-pool-detail   |query subaccounts and threshold of a pool   |
|get-pool-unbond   |query unbonds for a given pool|
|get-r-params   |query r params|
|get-receiver   |query receiver|
|get-signature   |query signature|
|get-snap-shot   |query snap shot for a given shot-id|
|get-total-expected-active   |query total expected actiev for a given denom|
|get-unbond-commission   |query unbond commission|
|get-unbond-fee   |query unbond fee for a given denom|
|list-exchange-rate   |list all rates|
|pools-by-denom   |query pools by denom|
|show-era-exchange-rate   |shows rate of a rToken at a specific era by its denom|
|show-exchange-rate   |shows rate of a rToken by its denom|

#### stafid query ledger bonded-pools-by-denom 
```
stafid query ledger bonded-pools-by-denom [denom] [flags]
```

#### stafid query ledger era-exchange-rates-by-denom 
```
stafid query ledger era-exchange-rates-by-denom [denom] [flags]
```

#### stafid query ledger get-account-unbond 
```
stafid query ledger get-account-unbond [denom] [unbonder] [flags]
```

#### stafid query ledger get-bond-pipeline 
```
stafid query ledger get-bond-pipeline [denom] [pool] [flags]
```

#### stafid query ledger get-bond-record 
```
stafid query ledger get-bond-record [denom] [blockhash] [txhash] [flags]
```

#### stafid query ledger get-chain-bonding-duration 
```
stafid query ledger get-chain-bonding-duration [denom] [flags]
```

#### stafid query ledger get-chain-era 
```
stafid query ledger get-chain-era [denom] [flags]
```

#### stafid query ledger get-commission 
```
stafid query ledger get-commission [flags]
```

#### stafid query ledger get-current-era-snap-shot 
```
stafid query ledger get-current-era-snap-shot [denom] [flags]
```

#### stafid query ledger get-era-snap-shot 
```
stafid query ledger get-era-snap-shot [denom] [era] [flags]
```

#### stafid query ledger get-era-unbond-limit 
```
stafid query ledger get-era-unbond-limit [denom] [flags]
```

#### stafid query ledger get-least-bond
```
stafid query ledger get-least-bond [denom] [flags]
```

#### stafid query ledger get-pool-detail 
```
stafid query ledger get-pool-detail [denom] [pool] [flags]
```

#### stafid query ledger get-pool-unbond
```
stafid query ledger get-pool-unbond [denom] [pool] [era] [flags]
```

get-r-params

#### stafid query ledger get-r-params
```
stafid query ledger get-r-params [denom] [flags]
```

#### stafid query ledger get-receiver
```
stafid query ledger get-receiver [flags]
```

#### stafid query ledger get-signature
```
stafid query ledger get-signature [denom] [era] [pool] [tx-type] [prop-id] [flags]
```

#### stafid query ledger get-snap-shot
```
stafid query ledger get-snap-shot [shot-id] [flags]
```

#### stafid query ledger get-total-expected-active
```
stafid query ledger get-total-expected-active [denom] [era] [flags]]
```

#### stafid query ledger get-unbond-commission
```
stafid query ledger get-unbond-commission [flags]
```

#### stafid query ledger get-unbond-fee
```
stafid query ledger get-unbond-fee [denom] [flags]
```

#### stafid query ledger list-exchange-rate
```
stafid query ledger list-exchange-rate [flags]
```

#### stafid query ledger pools-by-denom 
```
stafid query ledger pools-by-denom [denom] [flags]
```

#### stafid query ledger show-era-exchange-rate 
```
stafid query ledger show-era-exchange-rate [denom] [era] [flags]
```

#### stafid query ledger show-exchange-rate 
```
stafid query ledger show-exchange-rate [denom] [flags]
```

### Available Tx Commands

|Name   |Description   |
| :------------ | :------------ |
|active-report   |propose active-report proposal    |
|add-new-pool   |add a new pool    |
|bond-and-report-active   |propose bond-and-report-active proposal   |
|bond-report   |propose bond-report proposal    |
|clear-current-era-snap-shots   |clear current era snapshots    |
|execute-bond-proposal   |propose execute-bond-proposal proposal    |
|liquidity-unbond   |redeem rToken    |
|remove-pool   |remove a pool    |
|set-chain-bonding-duration   |set bonding-duration for a given denom    |
|set-chain-era   |propose set-chain-era proposal    |
|set-commission   |set commission    |
|set-era-unbond-limit   |set unbond limit for each era    |
|set-init-bond   |set init bond for a given denom and pool    |
|set-least-bond   |set the minimum quantity to perform staking for a new era    |
|set-pool-detail   |set subaccounts and threshold for a given pool    |
|set-r-params   |set common params of relayers    |
|set-receiver   |set commission receiver    |
|set-unbond-commission   |set unbond commission    |
|set-unbond-fee   |set unbond fee for a given denom    |
|submit-signature   |allow a relayer to submit signature for staking related operations    |
|transfer-report   |propose transfer-report proposal    |
|withdraw-report   |propose withdraw-report proposal    |

#### stafid tx ledger active-report
```
stafid tx ledger active-report [denom] [shot-id] [staked] [unstaked] [flags]
```

#### stafid tx ledger add-new-pool
```
stafid tx ledger add-new-pool [denom] [addr] [flags]
```

#### stafid tx ledger bond-and-report-active
```
stafid tx ledger bond-and-report-active [denom] [shot-id] [action] [staked] [unstaked] [flags]
```

#### stafid tx ledger bond-report
```
stafid tx ledger bond-report [denom] [shot-id] [action] [flags]
```

#### stafid tx ledger clear-current-era-snap-shots
```
stafid tx ledger clear-current-era-snap-shots [denom] [flags]
```

#### stafid tx ledger execute-bond-proposal
```
stafid tx ledger execute-bond-proposal [denom] [bonder] [pool] [blockhash] [txhash] [amount] [flags]
```

#### stafid tx ledger liquidity-unbond
```
stafid tx ledger liquidity-unbond [pool] [value] [recipient] [flags]
```

#### stafid tx ledger remove-pool
```
stafid tx ledger remove-pool [denom] [addr] [flags]
```

#### stafid tx ledger set-chain-bonding-duration
```
stafid tx ledger set-chain-bonding-duration [denom] [era] [flags]
```

#### stafid tx ledger set-chain-era
```
stafid tx ledger set-chain-era [denom] [era] [flags]
```

#### stafid tx ledger set-commission
```
stafid tx ledger set-commission [rate] [flags]
```

#### stafid tx ledger set-era-unbond-limit
```
stafid tx ledger set-era-unbond-limit [denom] [limit] [flags]
```

#### stafid tx ledger set-init-bond
```
stafid tx ledger set-init-bond [pool] [coin] [receiver] [flags]
```

#### stafid tx ledger set-least-bond
```
stafid tx ledger set-least-bond [denom] [amount] [flags]
```

#### stafid tx ledger set-pool-detail
```
stafid tx ledger set-pool-detail [denom] [pool] [sub-accounts] [threshold] [flags]
```

#### stafid tx ledger set-r-params
```
stafid tx ledger set-r-params [denom] [chain-id] [native-denom] [gas-price] [era-seconds] [least-bond] [validators] [flags]
```

#### stafid tx ledger set-receiver
```
stafid tx ledger set-receiver [receiver] [flags]
```

#### stafid tx ledger set-unbond-commission
```
stafid tx ledger set-unbond-commission [commission] [flags]
```

#### stafid tx ledger set-unbond-fee
```
stafid tx ledger set-unbond-fee [denom] [value] [flags]
```

#### stafid tx ledger submit-signature
```
stafid tx ledger submit-signature [denom] [era] [pool] [tx-type] [prop-id] [signature] [flags]
```

#### stafid tx ledger transfer-report
```
stafid tx ledger transfer-report [denom] [shot-id] [flags]
```

#### stafid tx ledger withdraw-report
```
stafid tx ledger withdraw-report [denom] [shot-id] [flags]
```

