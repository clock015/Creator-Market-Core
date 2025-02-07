# Creator-Market-Core
This smart contract protocol builds a decentralized company model that allows for investing in the real world by investing in creators. Since every node in the system can be invested in and can grow, this model is inherently decentralized and divisible, greatly enhancing investment efficiency.

## Smart Contract Image：

![Creator-Market](./public/contract-logic.png)

## Smart Contract Usage:

### 1. clone folder "contracts" to Remix

any name and any symbol

### 2. deploy contract MyToken

### 3. deploy contract Vesting4626

owner_ = test wallet (0x5B38Da6a701c568545dCfcB03FcB875f56beddC4)

token_ = contract MyToken address

### 4. deposit:

call MyToken.approve, spender = contract Vesting4626 address, value = 1e21

call Vesting4626.deposit, assets = 1e18, receiver = test wallet (0x5B38Da6a701c568545dCfcB03FcB875f56beddC4)

### 5. update salary:

call Vesting4626.updateSalary, creator_ = test wallet (0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2), amount = 1e18

call Vesting4626.finishUpdate, creator_ = test wallet (0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2)


