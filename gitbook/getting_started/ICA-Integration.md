# Integrating with Interchain Accounts

> It is highly recommended to read [this](https://ibc.cosmos.network/main/apps/interchain-accounts/overview.html#) before reading this instruction.

With the release of InterChain Accounts, which enables cross-chain account management built upon IBC, a solution to build rTokens via InterChain Accounts is implemented on StaFiHub and brings more security, decentralization and ease of integration.

> The target chain is supposed to integrate Interchain Accounts(ICA) module. 

Like the way to [integrate with multisig accounts](#https://app.gitbook.com/o/PkZ9s2zCpTrmEqTqHIQh/s/zmKNtlFtsE0JPahPkNCA/rtoken/integrate-rtoken/integrating-with-multisign-accounts), no development is required at all, the integration process is also a three-step process and the main step is to configure the following parameters, of which most are the same except pool accounts, the other two steps are the same and we won't belabor it here.

|Flags    |Description    | Example |
| :------------ | :------------ | :------------ |
|denom   | The denomination used by the target chain | uatom |
|decimals   | Decimal points to covert minimal denomination to user-facing denomination | 6 |
|bech32PrefixAccAddr   | Prefix of account address | cosmos |
|bech32PrefixValAddr   | Prefix of validator address | cosmosvaloper |
|stafiRelayers   | Relay accounts of StaFiHub. Each rToken realy service needs to import an account to initiate transactions with the StaFiHub. 7 accounts recommended on mainnet | stafi17yl0s0zh7u87uhluzn2egg5ru2hy3jqxfspdlp:stafi12a0n3294pncp24c93d0as3g3t5zjhcnrnugsd7:stafi1tjg6cw5lklvz7nwd0ck9veua9ldm4lxnrr99y4 |
|stafiRelayerThreshold   | Threshold of the relayers. 4 recommended on mainnet | 2 |
|gasPrice   | Gas price. Ensure that each rToken realy service can successfully initiate a transaction to the target chain | 0.025uatom |
|bondingDuration   | Unbonding time of the target chain | 21days |
|leastBond   | Minimum staking amount to mint rToken(Optional). Usually decided by StaFiHub | 0.1ATOM |
|ica-pool   | An ica-pools contains two ica-accounts, one of them is a real pool account, and the other is a secondary account used to collect staking rewards | cosmos1lyqrtft9x286gfsf30rf8vtvmc3jgd0mevd8p3:cosmos1u5dfrwye0vgtf706wc0h55vl06v0mc23fsu225:cosmos1pv9vxz6d38thesq82dgfuhdlujj0vwkddkpkvp |

As the target chain already supports the ICA module, StaFiHub can register ICA accounts on the target chain through its module [Ledger](https://github.com/stafihub/stafihub/tree/main/x/ledger) and use them as the ICA pool accounts.

 







