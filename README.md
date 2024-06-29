# Myo-Min-Hlaing
A complete Ethereum development toolkit featuring Hardhat for testing, deployment scripts, Solidity contract templates, and example DApps. Ideal for rapid development and deployment of blockchain applications.
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint256 private storedData;

    event DataStored(uint256 data);

    function set(uint256 x) public {
        storedData = x;
        emit DataStored(x);
    }

    function get() public view returns (uint256) {
        return storedData;
    }
}