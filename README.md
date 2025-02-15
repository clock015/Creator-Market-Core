# Creator-Market-Core
This smart contract protocol builds a decentralized company model that allows for investing in the real world by investing in creators. Since every node in the system can be invested in and can grow, this model is inherently decentralized and divisible, greatly enhancing investment efficiency.

## Smart Contract Image：

![Creator-Market](./public/contract-logic.png)

![Expense contract](./public/vesting4626.png)

## Smart Contract Usage:

### 1. clone folder "contracts" to Remix

### 2. deploy contract MyToken

any name and any symbol

### 3. deploy contract Vesting4626

owner_ = test wallet (0x5B38Da6a701c568545dCfcB03FcB875f56beddC4)

token_ = contract MyToken address

### 4. deposit:

call MyToken.approve, spender = contract Vesting4626 address, value = 1e21

call Vesting4626.deposit, assets = 1e18, receiver = test wallet (0x5B38Da6a701c568545dCfcB03FcB875f56beddC4)

### 5. update salary:

call Vesting4626.updateSalary, creator_ = test wallet (0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2), amount = 1e18

call Vesting4626.finishUpdate, creator_ = test wallet (0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2)

### 6. call view function

Vesting4626.totalAssets:assets - pending salary

Vesting4626.totalPendingSalary:current pending salary across all participants

Vesting4626.totalInvestment:total expenses

Vesting4626.investmentOf:expenses for an account, When distributing the income, calculate the share for each account based on the ratio of investmentOf(account) to totalInvestment.

