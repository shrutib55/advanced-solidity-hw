# Unit 21: You sure can attract a crowd!

## Background

Your company has decided to crowdsale their PupperCoin token in order to help fund the network development.
This network will be used to track the dog breeding activity across the globe in a decentralized way, and allow humans to track the genetic trail of their pets. You have already worked with the necessary legal bodies and have the green light on creating a crowdsale open to the public. However, you are required to enable refunds if the crowdsale is successful and the goal is met, and you are only allowed to raise a maximum of 300 Ether. The crowdsale will run for 24 weeks.

You will need to create an ERC20 token that will be minted through a `Crowdsale` contract that you can leverage from the OpenZeppelin Solidity library.

This crowdsale contract will manage the entire process, allowing users to send ETH and get back PUP (PupperCoin).
This contract will mint the tokens automatically and distribute them to buyers in one transaction.

It will need to inherit `Crowdsale`, `CappedCrowdsale`, `TimedCrowdsale`, `RefundableCrowdsale`, and `MintedCrowdsale`.

You will conduct the crowdsale on the Kovan or Ropsten testnet in order to get a real-world pre-production test in.

## Instructions

### Creating your project

Using Remix, create a file called `PupperCoin.sol` and create a standard `ERC20Mintable` token. Since you're already an expert at this, you can simply use this [starter code](../Starter-Code/PupperCoin.sol).

Create a new contract named `PupperCoinCrowdsale.sol`, and prepare it like a standard crowdsale.

### Designing the contracts

#### ERC20 PupperCoin

You will need to simply use a standard `ERC20Mintable` and `ERC20Detailed` contract, hardcoding `18` as the `decimals` parameter, and leaving the `initial_supply` parameter alone.

You don't need to hardcode the decimals, however since most use-cases match Ethereum's default, you may do so.

Simply fill in the `PupperCoin.sol` file with this [starter code](../Starter-Code/PupperCoin.sol), which contains the complete contract you'll need to work with in the Crowdsale.

#### PupperCoinCrowdsale

Leverage the [Crowdsale](../Starter-Code/Crowdsale.sol) starter code, saving the file in Remix as `Crowdsale.sol`.

You will need to bootstrap the contract by inheriting the following OpenZeppelin contracts:

* `Crowdsale`

* `MintedCrowdsale`

* `CappedCrowdsale`

* `TimedCrowdsale`

* `RefundablePostDeliveryCrowdsale`

You will need to provide parameters for all of the features of your crowdsale, such as the `name`, `symbol`, `wallet` for fundraising, `goal`, etc. Feel free to configure these parameters to your liking.

![contract](https://github.com/shrutib55/advanced-solidity-hw/blob/main/Screenshots/Screen%20Shot%202022-01-21%20at%209.40.19%20AM.png)

![contract](https://github.com/shrutib55/advanced-solidity-hw/blob/main/Screenshots/Screen%20Shot%202022-01-21%20at%209.42.17%20AM.png)

![contract](https://github.com/shrutib55/advanced-solidity-hw/blob/main/Screenshots/Screen%20Shot%202022-01-21%20at%209.45.27%20AM.png)

![contract](https://github.com/shrutib55/advanced-solidity-hw/blob/main/Screenshots/Screen%20Shot%202022-01-21%20at%209.46.43%20AM.png)


![contract](https://github.com/shrutib55/advanced-solidity-hw/blob/main/Screenshots/Screen%20Shot%202022-01-21%20at%209.54.11%20AM.png)



### Submission

Create a Github repo, and a `README.md` file explaining the process for purchasing PupperCoin (or whatever name you came up with).

Also, please provide screenshots to illustrate the functionality (e.g. how you send Ether to the contract, how you add the token to MyCrypto and test a transaction, and how you test the time functionality etc.). Alternatively, you can also record your interactions with the contract as a gif (e.g. https://www.screentogif.com/)

Ensure that anyone can run the steps and add the token to MyCrypto, or a similar wallet.

Include information such as the token parameters, token name, crowdsale cap, etc.

---

### Requirements
#### Deploying the Contracts  (30 points)

##### To receive all points, your code must:

* Set up the ERC20 PupperCoin contract. (6 points)
* Set up the PupperCoinCrowdsale with the assigned criteria. (8 points)
* Customize or hardcode the Crowdsale Rate. (8 points)
* Model the PupperCoinCrowdsaleDeployer after the ArcadeTokenCrowdsaleDeployer. (8 points)

#### Testing the Crowdsale  (40 points)

##### To receive all points, your code must:

* Test the Crowdsale by sending ether to a different account, then add screenshots of this to the ReadME.md. (10 points)
* Set up the Crowdsale's finalize function with the assigned criteria. (10 points)
* Properly set up the RefundablePostDeliveryCrowdsale. (10 points)
* Deploy the Crowdsale to either the Kovan or Ropsten testnet, then add screenshots of this to the ReadMe.md. (10 points)

#### Coding Conventions and Formatting (10 points)

##### To receive all points, your code must:

* Place imports at the beginning of the file, just after any module comments and docstrings and before module globals and constants. (3 points)
* Name functions and variables with lowercase characters and with words separated by underscores. (2 points)
* Follow Don't Repeat Yourself (DRY) principles by creating maintainable and reusable code. (3 points)
* Use concise logic and creative engineering where possible. (2 points)

#### Deployment and Submission (10 points)

##### To receive all points, you must:

* Submit a link to a GitHub repository that’s cloned to your local machine and contains your files. (5 points)
* Include appropriate commit messages in your files. (5 points)

#### Code Comments (10 points)

##### To receive all points, your code must:

* Be well commented with concise, relevant notes that other developers can understand. (10 points)

---

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
