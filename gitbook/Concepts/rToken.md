## rToken Concepts

### Relay service
Relay service play a role as cross chain bridge to connect StaFiHub and other chains.

### Pool Account
A pool is a multisig account of foreign chain to gather origin token and invoke staking related calls such like Bond, Unbond and Claim on the foreign chain to earn more tokens. As a multisig account, a pool has no private key but an address and several sub-accounts and a threshold. There might be several pools for a rtoken.

### Relayer
A relayer is a sub-account of a pool. Each relay service requires a relayer to send proposals to StaFiHub.

### Era
Era was introduced as a concept of period to solve problems like when the pool should invoke bond and unbond call. Pools invoke all the necessary calls on the foreign chain once and only once for each Era.

### Rate
Rate of rToken is used to calculate how many rToken to mint or burn.

### rValidator
An rValidator is a validator of the origin token's chain. 