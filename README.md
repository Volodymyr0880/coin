# coin
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract Gold is ERC20 {
    uint256 public ethExchangeRate; // Початковий обмінний курс ETH за токен GoldZora

    constructor(uint256 initialSupply, uint256 initialEthExchangeRate) ERC20("GoldZora", "GZ") {
        _mint(msg.sender, initialSupply / 2);
        _mint(address(this), initialSupply / 2);
        ethExchangeRate = initialEthExchangeRate;
    }
}
