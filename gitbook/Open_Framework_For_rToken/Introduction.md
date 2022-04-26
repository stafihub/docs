## rToken Open Framework(ROF)
ROF is a modular design that enables other teams and developers to join us to create rToken more securely and efficiently.

The implementation of rToken on StaFiHub mainly consists of three main parts:
- **[Necessary settings](#Necessary Settings)** mainly includes:
    - Denom and its metadata
    - Pool account and its detail which includes sub-accounts and thresholds
    - Relayers to send proposals to StaFiHub. 
    - Reward commission, unbond commission and unbond fee. 
- **Relay service** play a role as cross-chain bridge to connect StaFiHub and other chains,
take [rtoken-relay-core](https://github.com/stafihub/rtoken-relay-core) as an example, it integrates two SDKs:
    - [stafi-hub-relay-sdk](https://github.com/stafihub/stafi-hub-relay-sdk) is used to connect StaFiHub such like reporting staking datas, all reports are made in the form of proposal.
    - A Go-client-SDK to connect origin token's chain, for instance, [cosmos-relay-sdk](https://github.com/stafihub/cosmos-relay-sdk) is the SDK to connect [Cosmos Hub](https://hub.cosmos.network/main/hub-overview/overview.html).
- **rValidator service** includes two parts:
    - A module that manages validators on others chains.
    - An another kind of relay service that helps to decide whom to bond for the pool account.

