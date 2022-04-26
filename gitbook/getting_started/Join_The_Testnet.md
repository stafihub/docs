## Join The Testnet

### Public Endpoints
- GRPC: /todo
- RPC: /todo
- REST: /todo

## Run a Full Node

### Start node from genesis

---
You must use StaFiHub /todo to initialize your node.

---
```$xslt
# init node
stafihubd init <moniker> --chain-id=/todo

# download public config.toml and genesis.json
curl -o ~/.stafihub/config/config.toml /todo
curl -o ~/.stafihub/config/genesis.json /todo

# Start the node (also running in the background, such as nohup or systemd)
stafihubd start
```

### faucet
---
Welcome to get test tokens in our (/todo add link)testnet faucet channel

Usage: in stafihub-faucet channel, type "!faucet send " + your address on /todo, to get test tokens (/todo denom) every 12 hours.

### Explorer
---
[https://testnet-explorer.stafihub.io/](https://testnet-explorer.stafihub.io/)

### Community
Welcome to discuss in our /todo channel



     
    