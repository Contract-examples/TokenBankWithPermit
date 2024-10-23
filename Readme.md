# Token bank with permit

### Create a ``.env`` file
```
API_KEY_INFURA=your infura api key 
API_KEY_ARBISCAN=your arbiscan api key 
SEPOLIA_WALLET_PRIVATE_KEY=your wallet private key 
BANK_CONTRACT_ADDRESS=your contract address
TOKEN_CONTRACT_ADDRESS=your erc20 token address
RECIPIENT_ADDRESS=recipient address
RECIPIENT_PRIVATE_KEY=recipient private key 
```


## Deploy to Arbitrum-Sepolia
```
forge script script/Deploy.s.sol:DeployTokenBankAndTokenScript --rpc-url arbitrum_sepolia --broadcast --verify -vvvv
```

## Token address
- https://sepolia.arbiscan.io/address/0x01656ba9826a86dec6cd8b0c38eaf5270e2fbc28#events

## Tokenbank address
- https://sepolia.arbiscan.io/address/0x0368ad1a77e9e03ff2b34bfc453ae6d166ed6be5#code

## Distribute 1000 tokens to recipient address
```
forge script script/DistributeSimpleToken.s.sol:DistributeSimpleTokenScript --rpc-url arbitrum_sepolia --broadcast -vvvv
```
txhash: https://sepolia.arbiscan.io/tx/0xdb8efe967a12637d979d2ff48a3d339841469d918bb6d77eda5522445bf3f742

## Deposit 1 token to Tokenbank
```
forge script script/DepositToTokenBank.s.sol:DepositToTokenBankScript --rpc-url arbitrum_sepolia --broadcast -vvvv
```
txhash: https://sepolia.arbiscan.io/tx/0x0cb63c35021c74e4a217e87aec795def2f563835359012e466f4c45038ed1648

## Withdraw 1 token from Tokenbank
```
forge script script/WithdrawFromTokenBank.s.sol:WithdrawFromTokenBankScript --rpc-url arbitrum_sepolia --broadcast -vvvv
```
txhash: https://sepolia.arbiscan.io/tx/0x141a51e9894cc0940b58946a0695dfa6bacafe2780cf1f1107ef56384f9af35f
