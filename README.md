# ERC721 Token
This is an implementation of the ERC721 Non-fungible Token for gifts called GiftsLottery, in which people of the staff will send gifts to the contract and after a given time the contract owner will "randomly" distribute the gifts.

## Requirements
* [Open Zeppelin](https://github.com/OpenZeppelin/openzeppelin-solidity)
   * ERC721
   * SafeMath
   * Ownable

## Open Zeppelin
This is a library for writing secure Smart Contracts on Ethereum. They are providing secure, tested and community-audited code for the most popular standards and used contracts on the Ethereum network. For the purpose of the exercise, go to [Open Zeppelin](https://github.com/OpenZeppelin/openzeppelin-solidity) and download the ERC721 token (in contracts > token > ERC721). In addition, you will need SafeMath and Ownable due to dependencies, which are stored in math and ownership folders respectively. Go through the code, especially in ERC721Token, because you will use it.

## Crypto Raffle
1. Create a new contract called GiftLottery, which will inherit ERC721Token. Do not forget to import the contract.
2. The contract will have an owner, who will distribute the gifts after certain time has passed and will have a list of all the participants.
3. Each gift will have a title, description and a URL of an image (IPFS hash). Each token will store information of itself by a given token id.
4. Upon initialization, the contract will take a due date of the lottery submission and will call the inherited contract's constructor to name the contract.
5. Create a modifier onlyOwner
6. Create an event called CreateGift, which will take a participant and an id of the gift.
7. Create a method called createGift, which will take the gift information as parameters and mint a new gift to the owner of the contract.
8. Create a method called pseudoRandom, which will take the role of a random generator, which by a gift id load the gift and calculate keccak256 on its title, description, URL and gift id. Keep in mind that someone might be left with no gift and someone might receive two or more! The method will "randomly" generate the id of the participant to which the gift will be sent.
9. Create an event called ReceivedGift, which will take a winner address and the id of the gift
10. Create a method called distributeGifts, which after the due date of participation will distribute the gifts
11. Test the contract. Think of a way to avoid participant missing a gift.

## Module
MI1: Module 4: E2
