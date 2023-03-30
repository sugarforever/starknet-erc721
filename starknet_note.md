# How to Use Starknet CLI to Deploy Smart Contract

## Install a Python Package

```
@ > pip3 install openzeppelin-cairo-contracts
```

## Export Environment Variable

```
@ > export STARKNET_WALLET=starkware.starknet.wallets.open_zeppelin.OpenZeppelinAccount
```
## Create a New Account

```
@ > starknet new_account
Account address: 0x036aba3e15486bd1cd336acc147db2163fb1d92d1a93d77857d985981da9b645
Public key: 0x03d9953bcb7dec9528691b09c2b69f995fd867ef49b6d2b9a535b612a586cd6a
Move the appropriate amount of funds to the account, and then deploy the account
by invoking the 'starknet deploy_account' command.

NOTE: This is a modified version of the OpenZeppelin account contract. The signature is computed
differently.
```

## Deploy The New Account

```
@ > starknet deploy_account
Sending the transaction with max_fee: 0.001013 ETH (1013253482408779 WEI).
Sent deploy account contract transaction.

Contract address: 0x009ab9c33e8ec288f16152ad3e133af5aa8f5fa3a423c93d48eb52a860b2b528
Transaction hash: 0x5afb0e67e804c9abfb8acd639a912da661e4e06cde60de1648813bfa4228c4f
```

## Fund the New Account

You need to fund the new account so that it can submit transactions later on. You may do so by sending a small amount from your ArgentX wallet, which will also deploy the new account on Starknet testnet.

## Prepare The ERC721 Contract

We can download the copy of https://github.com/OpenZeppelin/cairo-contracts/blob/release-v0.5.0/src/openzeppelin/token/erc721/presets/ERC721MintableBurnable.cairo and put it in the src/ folder.

## Compile

```
@ > starknet-compile src/erc721.cairo --output build/erc721.json --abi build/erc721_abi.json
```

## Declare

```
@ > starknet declare --contract build/erc721.json --deprecated
```

## Deploy

```
@ > starknet deploy --inputs 71804493054284 4279881 1545509733194854778647923347933833388212704958270379292394134815523094509125 --class_hash 0xb38daee6e2c9efc29eb48e29d063843e004cce72cde635e75546075c94483c
```