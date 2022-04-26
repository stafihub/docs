## Introduction
`stafihubd` is a command line client for StaFiHub. StaFiHub users can use `stafihubd` to send transactions and query the blockchain data.

## Working Directory
The default working directory for the `stafihubd` is `$HOME/.stafihub`, which is mainly used to save configuration files and data. The StaFiHub key data is saved in the working directory of `stafihub`. You can also specify the `stafihub` working directory by --home.

## Connecting to a Full Node
The `stafihub` node provides a RPC interface, transactions and query requests are sent to the process listening to it. The default rpc address the `stafihub` is connected to is tcp://localhost:26657, it can also be specified by --node.

## Global Flags

### GET Commands
All GET commands has the following global flags:

|Name, shorthand   |type   |Required   |Default Value   |Description   |
| :------------ | :------------ | :------------ | :------------ | :------------ |
|--chain-id   |string    |   |   |Chain ID of tendermint node    |
|--home   |string    |   |$HOME/.stafihub	   |Directory for config and data    |
|--trace   |string    |   |   |Print out full stack trace on errors    |

### POST Commands
All POST commands have the following global flags:

|Name, shorthand   |type   |Required   |Default Value   |Description   |
| :------------ | :------------ | :------------ | :------------ | :------------ |
|--account-number   |int    |   |0    |AccountNumber to sign the tx    |
|--broadcast-mode   |string    |   |sync    |Transaction broadcasting mode (sync &VerticalLine; async &VerticalLine; block)    |
|--dry-run   |bool    |   |false    |Ignore the --gas flag and perform a simulation of a transaction, but don't broadcast it    |
|--fee-account   |string    |   |   |Fee account pays fees for the transaction instead of deducting from the signer    |
|--fees   |string    |   |   |Fees to pay along with transaction    |
|--from   |string    |   |   |Name of private key with which to sign    |
|--gas   |string    |   |200000    |Gas limit to set per-transaction; set to "simulate" to calculate required gas automatically    |
|--gas-adjustment    |float    |   |1    |Adjustment factor to be multiplied against the estimate returned by the tx simulation; if the gas limit is set    |
|--gas-prices   |string    |   |   |Gas prices in decimal format to determine the transaction fee    |
|--generate-only   |bool    |   |false    |Build an unsigned transaction and write it to STDOUT    |
|--help, -h   |string    |   |   |Print help message    |
|--keyring-backend   |string    |   |os    |Select keyring's backend    |
|--keyring-dir   |string    |   |    |The client Keyring directory; if omitted, the default 'home' directory will be used    |
|--ledger   |bool    |   |false    |Use a connected Ledger device    |
|--node    |string    |   |tcp://localhost:26657    |<host>:<port> to tendermint rpc interface for this chain   |
|--note    |string    |   |    |Note to add a description to the transaction (previously --memo)   |
|--offline   |string    |   |   |Offline mode (does not allow any online functionality)    |
|-o, --output   |string    |   |json   |Output format (text|json) (default "json")    |
|--sequence   |uint    |   |0   |The sequence number of the signing account (offline mode only)    |
|--sign-mode   |string    |   |   |Choose sign mode (direct &VerticalLine; amino-json), this is an advanced feature    |
|--timeout-height   |uint    |   |    |Set a block timeout height to prevent the tx from being committed past a certain height    |
|--yes   |bool    |   |true    |Skip tx broadcasting prompt confirmation    |
|--chain-id    |string    |   |   |Chain ID of tendermint node    |
|--home   |string    |   |   |Directory for config and data (default "$HOME/.stafihubd")    |
|--trace   |string    |   |   |Print out full stack trace on errors    |

### Module Commands
## Module Commands

| **Subcommand**                    | **Description**                                                |
| --------------------------------- | -------------------------------------------------------------- |
| [bank](./Bank.md)                 | Bank subcommands for querying acccounts and sending coins etc. |
| [debug](./Debug.md)               | Debug subcommands                                              |
| [keys](./Keys.md)                 | Keys allows you to manage your local keystore for tendermint   |
| [gov](./Gov.md)                   | Governance and voting subcommands                              |
| [ledger](./Ledger.md)             | Ledger subcommands for querying tToken rates and mint or redeem rToken etc. |
| [rbank](./rBank.md)               | rBank Allow adding denom                                       |
| [relayers](./Relayers.md)         | Relayers subcommands for relayers                              |
| [rvote](./rVote.md)               | rVote handles proposals from relayers                          |
| [staking](./staking.md)           | Staking subcommands for validators and delegators              | 





