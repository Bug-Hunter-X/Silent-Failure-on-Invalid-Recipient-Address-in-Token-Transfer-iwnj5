# Silent Failure on Invalid Recipient Address in Token Transfer

This repository demonstrates a common bug in Solidity smart contracts: silent failure when attempting to transfer tokens to an invalid recipient address.  The provided `transfer` function lacks proper checks to handle the case where the recipient address is invalid (e.g., 0x000...00). This can lead to unexpected loss of funds.  The solution demonstrates how to prevent this vulnerability by explicitly checking for an invalid recipient address before performing the transfer.

## Bug

The `bug.sol` file contains the vulnerable contract. The `transfer` function fails silently if the recipient address is invalid.