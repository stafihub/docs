# Integration Instructions

## Introduction
In order to make it easily and quickly for other Cosmos Eco projects to get their own liquid staking derivatives, StaFiHub has developed a Liquid Staking SDK and here are the detail instructions about the entire integration process of the SDK.

### Step 1
**Contact the StaFiHub Foundation to confirm the following access parameters：**

|MsgType    |Module    | Description |
| :------------ | :------------ | :------------ |
|MsgAddDenom   | rbank | Set multi-signature accounts and its sub-accounts and threshold, multi-signature accounts are used to  gather user's token|
|MsgAddRelayer   | relayers | Set relayers for the new rToken|
|MsgSetThreshold   | relayers | Set threshold of relayers for the new rToken|
|MsgSetPoolDetail   | ledger | Set multi-signature accounts and its sub-accounts and threshold, multi-signature accounts are used to  gather user's token|
|MsgSetRParams    | ledger   | Common params of rtoken relayers |
|MsgSetUnbondRelayFee   | ledger | To specify an amount of relay fee which will be charged when the users redeem |
|MsgSetRelayFeeReceiver   | ledger | To specify an account to collect relay fees  |
|MsgSetUnbondCommission   | ledger | Set unbond commission  |
|MsgSetStakingRewardCommission   | ledger | Set staking reward commission  |
|MsgSetProtocolFeeReceiver   | ledger | To specify an account to collect commission fee of unbonding and staking reward  |

### Step 2
**Run [relay service](https://github.com/stafihub/rtoken-relay-core)**
> One of the relay service's tasks is to invoke staking related calls based on the multi-signature pool accounts on the target chain. Multiple relay services work together to manager these pool accounts which are secure only if as many parties as possible are running the relay service.

1. Check the staking mechanism of the target chain. Current code of relay service  is perfectly aligned with the current staking module of the Cosmos-SDK, however, if the target chain does not adopt staking Module of the Cosmos-SDK, instead, a self-built staking module is used, then [the SDK](https://github.com/stafihub/cosmos-relay-sdk) for the target chain on which relay service depends needs to be rebuild to fit that module.

2. Prepare RPC endpoints.
   A relay service connects both StaFiHub and the target chain, so RPC endpoints of both two chains are needed to provide. In addition, to ensure that a relay service will not break down due to the disconnection of an RPC endpoint, it is best to configure multiple RPC endpoints. We suggest that the target chain run the nodes themselves, or cooperate with other validators and node service providers in the network.
   
3. Prepare the configuration file for the relay service like [this](https://github.com/stafihub/rtoken-relay-core/blob/main/config_template_stafihub_cosmoshub.json).

    - Install Go.
    - Use [the key tool](https://github.com/stafihub/rtoken-relay-core/tree/main/cmd/keytool) to build keys for the relay service.

4. Run relay service. You can refer to the [README.md file](https://github.com/stafihub/rtoken-relay-core/blob/main/README.md) under the project.

### Step 3






