# Why don't I see my funds or transactions on my wallet?
### Overview
Explanation why you don't see you zkSync Lite funds on your L1 wallet (Metamask, etc.)

## Background information
Layer 2 solutions on Ethereum, such as zkSync, are implemented as smart contracts on the Ethereum mainnet. 

When you **deposit** funds into a Layer 2 solution, you're actually sending your funds to a smart contract on the Ethereum mainnet. This smart contract is responsible for maintaining the security of your funds while they're being used on Layer 2.

Similarly, when you **withdraw** funds from Layer 2, you're interacting with this same smart contract. The smart contract verifies the validity of your withdrawal request (often using some form of cryptographic proof that the Layer 2 solution provides) and then sends the requested funds to your Ethereum address.

Because these deposit and withdrawal operations involve interacting with a smart contract on the Ethereum mainnet, they show up as smart contract transactions on Etherscan and do not show as "activity" on most wallets such as Metamask.

## What does this mean for users?
In order to access the zkSync Lite network, it is required to use Ethereum mainnet instead of connecting to a custom RPC. This approach means that users cannot view both their Ethereum funds and zkSync Lite funds on their wallet simultaneously. 

To view their zkSync Lite funds, users must either use the [zkSync Lite browser wallet](https://lite.zksync.io/) or check the [zkSync Lite block explorer](https://zkscan.io/). Unless a user's wallet is specifically designed to interact with the zkSync Lite protocol, such as [Argent](https://www.argent.xyz/), they will not be able to view their funds on zkSync Lite through their wallet.

## How do I know if a withdrawal was successful from zkSync Lite to Ethereum?
These steps **only** apply if you used the official zkSync Lite bridge through the [zkSync Lite browser wallet](https://lite.zksync.io/). If you used a third party bridge such as [Orbiter Finance](https://www.orbiter.finance/?source=Ethereum&dest=Arbitrum) or the [ZigZag bridge](https://trade.zigzag.exchange/bridge) you will need to reach out to them for support. 
1. Go to the [zkSync Lite block explorer](https://zkscan.io/). 
2. In the search bar enter the address that you used to make the withdrawal from zkSync Lite. 
3. Open the Tx Hash of the withdrawal. 
4. If the "Status" is marked as "Verified" click the address link in the "To" section.*
5. This will take you to a page showing all transactions involving your Ethereum address. Click on the "Internal Txns" tab. This tab shows all transactions involving your address that were internal to smart contracts, including withdrawals from zkSync Lite.
6. Look for a transaction that involves the zkSync Lite smart contract. The address of the [zkSync Lite smart contract](https://etherscan.io/address/0xabea9132b05a70803a4e85094fd0e1800777fbef) should be listed in the "From" column of the transaction. The amount of the transaction should match the amount that you withdrew from zkSync Lite. 

**If the "Status" is not "Verified", please check [How long are withdrawals?]()*
