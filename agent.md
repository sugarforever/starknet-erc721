# Starknet Toolings

1. Protostar
- How to deploy your ArgentX wallet on Starknet testnet
- Protostar declare command:
```
@ > protostar declare --account-address 0x0736E99ce85cfD72142842d4D7c6760A835eF95Ed5271FFb2a6e51Db44087eC1 --network testnet --max-fee auto ./build/main.json
```
2. Starknet CLI
3. Deploying a contract using ArgentX wallet

protostar calculate-account-address --account-class-hash 0x025ec026985a3bf9d0cc1fe17326b245dfdc3ff89b8fde106542a3ea56c5a918 --account-address-salt 1 

protostar declare --account-address 0x0736E99ce85cfD72142842d4D7c6760A835eF95Ed5271FFb2a6e51Db44087eC1 --max-fee auto --network testnet ./build/main.json

protostar deploy 0x02a5de1b145e18dfeb31c7cd7ff403714ededf5f3fdf75f8b0ac96f2017541bc --network testnet --max-fee auto --account-address 0x0736E99ce85cfD72142842d4D7c6760A835eF95Ed5271FFb2a6e51Db44087eC1

protostar declare ./build/main.json --account-address [ACCOUNT_ADDRESS_FROM_ARGENTX_ WALLET] --max-fee auto --network testnet

protostar deploy 0x02a5de1b145e18dfeb31c7cd7ff403714ededf5f3fdf75f8b0ac96f2017541bc --network testnet --max-fee auto --account-address 0x0736E99ce85cfD72142842d4D7c6760A835eF95Ed5271FFb2a6e51Db44087eC1