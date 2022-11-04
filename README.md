# TiFiAllverse-EthGlobal
TiFi Allverse for EthGlobal Event

## Introduction
TiFi Allverse Introduction Video:
https://youtu.be/Eeyy7FOZ5WY

TiFi Allverse is an online shopping platform build on blockchain. It will solve the following problems:
* **Protocol**: There is no standard decentralized protocol to track e-Commerce activities on blockchain.
* **Logistic**: People want to exchange the owned items easily without physical logistic process involved.
* **Over-spending**: People usually buy a lot items they don't actually need during discount, and it requires a way to redistributed.
* **Bridge**: On-chain objects (in Metaverse) cannot be redeemed to the real world products directly.
* **Trust**: Vendors need to give confidence to customers by using NFTs or other type of token when there are out of inventory or resource shortage.
* **Motivation**: Lacking of mechanism that stimulate people to trade and purchase.
* **Connection**: Keep good relationship between business and customers with digital collectables.

## Design Specifics

### Defining Object
When you shopping something, some items are identical (e.g. pounds of apples), some are not(e.g. vehicles, each vehicle has different VIN). So we need a protocol that can represent fungible token and non-fungile token.
So we can build something on top of EIP-1155 to implement the flexibility.

### Defining Process
During the process, an object has its states, and the process are manipulated by state transferring. The state is required for the new type of token, so we call it Stateful Universal Token or SUT.

The states for the items(objects) on an online shopping platform could include: MINTED, LISTED, SOLD, REDEEMED, BURNT ( Doesn't exist :D )

### Assumptions
We cannot do a fully online shopping platform like Amazon in 2 days. Here is we will implement:

1. Mint SUT (None -> MINTED)
2. List SUTs (Items to sell, MINTED -> LISTED)
3. Buy Items, and get SUT in customer wallet (LISTED -> SOLD).
4. Redeem SUT (SOLD -> REDEEMED, for SUTs that has value after redeem, like collectables).
5. Redeem SUT (SOLD -> BURNT, for SUTs that has no values after redeem, like groceries).
6. Exchange items (SOLD -> LISTED).

The platform doesn't include:
1. Return items.
2. Replace items after redeemed.
3. Labeling & track shippings.

More information:
https://tifi.net
