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
let balance = await window.ethereum.request({method:"eth_getBalance"})
```

change account and change chain
```
useEffect(()=>{//works when account is chnaged "accountsChanged"=> event

    ethereum.on("accountsChanged", (accounts)=>{

      setAddress(accounts[0])

      const getBal=async()=>{

        let balance = await window.ethereum.request({method:"eth_getBalance", params: [accounts[0],'latest']})

        setbalance((parseInt(String(balance),16)/10**18))

      }

      getBal()

    })

  })


useEffect(()=>{//works when account is chnaged "accountsChanged"=> event

    ethereum.on("chainChanged", (chain)=>{

     console.log(chain)

    })

  })
```
add and change chain
```
 const changeChain = async()=>{

    await window.ethereum.request({

      "method": "wallet_addEthereumChain",

      "params": [

        {

          "chainId": "0x64",

          "chainName": "Gnosis",

          "rpcUrls": [

            "https://rpc.ankr.com/gnosis"

          ],

          "iconUrls": [

            "https://xdaichain.com/fake/example/url/xdai.svg",

            "https://xdaichain.com/fake/example/url/xdai.png"

          ],

          "nativeCurrency": {

            "name": "xDAI",

            "symbol": "xDAI",

            "decimals": 18

          },

          "blockExplorerUrls": [

            "https://blockscout.com/poa/xdai/"

          ]

        }

      ]

    });

  }
```

switch chain
```
 const changeChain = async()=>{

    await window.ethereum.request({

      "method": "wallet_switchEthereumChain",

      "params": [

        {
          "chainId": "0x64"

        }

      ]

    });

  }
```