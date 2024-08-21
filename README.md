# ICP Development Environment with TaigahG
## Welcome to simple todo list with bad ui
A basic Web3 To-Do List application built using the Internet Computer Protocol (ICP) network. This project demonstrates how to deploy a fully on-chain dApp with a minimalistic (and admittedly bad) user interface. Perfect for learning the basics of Web3 development on ICP.

## 🚀 Develop

When the editor opened, run the following commands to start a local ICP node and deploy the canister smart contract:

```bash
dfx start --clean # Start a local ICP node
# In a new terminal window:
dfx deploy # Deploy smart contract locally
```

The smart contract will be reachable under `http://bkyz2-fmaaa-aaaaa-qaaaq-cai.localhost:4943`.
Call the smart contract using `curl` on the command line: 

```bash
# contacts endpoint
curl http://bkyz2-fmaaa-aaaaa-qaaaq-cai.localhost:4943/contacts
# price-oracle endpoint
curl -X POST http://bkyz2-fmaaa-aaaaa-qaaaq-cai.localhost:4943/price-oracle -H 'content-type: application/json' -d '{"pair": "ICP-USD"}'
```
You can also use tools like Postman or HTTPie to interact with the smart contract.
To redeploy the smart contract, run `dfx deploy` again.

When ready, run `dfx deploy --ic` to deploy your application to the ICP mainnet.
The command will print a different canister URL for mainnet, ending in `.raw.icp0.io`.
You can make calls to the smart contract on mainnet just like to the local one!
