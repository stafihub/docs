## General Concepts

### Denom and Metadata
Assets in the Cosmos SDK are represented via a Coins type that consists of an amount and a denom, where the amount can be any arbitrarily large or small value, module bank keeps track of metadata per denom in order to help clients, wallet providers, and explorers improve their UX and remove the requirement for making any assumptions on the unit of denomination.

To avoid upgrading the chain when adding a new rToken, module sudo provider an interface to add a new denom and its metadata, this action can only be operated by the admin account which is initialized in the genesis file.

