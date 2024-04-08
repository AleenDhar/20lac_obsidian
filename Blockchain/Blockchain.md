# Blockchain Overview
install hardhat , ethers@5.7.2 ,web3modal@1.9.12 
```ccard
type: folder_brief_live
```
```
npm i hardhat@2.13.0
npx hardhat
npm i ethers@5.7.2
npm i web3modal@1.9.12
```

[connecting ganache with metamash](https://www.youtube.com/watch?v=3Eo6euUnlVU&ab_channel=Soft.Tomatoes)

connecting react and hardhat:

```
npx create-react-app .
```

```
npm install "react-router-dom" "hardhat" "ethers" "dotenv" "@nomicfoundation/hardhat-ignition" "@nomicfoundation/hardhat-toolbox"
```

```
npx hardhat init
```

```
npx hardhat compile
npx hardhat ignition deploy ignition/modules/Apple.js --network TestGanache
```


# ether.js

gets access to metamask wallet
```
await window.ethereum.request({method:"eth_requestAccounts"})

await window.ethereum.isConnected()

await window.ethereum.isMetaMask
```
get balance
```
const balan
```
