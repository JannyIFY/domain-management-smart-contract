# Domain Management Smart Contract

A Clarity smart contract for managing domain names on the Stacks blockchain.

## Overview

This smart contract provides functionality for registering, managing, and transferring domain names. It serves as a decentralized domain name registry with the following key features:

- Domain name registration for periods between 1-5 years
- Domain validity extension
- Domain name validation rules
- Fee-based registration and extension

## Domain Name Rules

Domain names must adhere to the following rules:
- Must be between 3-64 characters in length
- Can only contain lowercase letters (a-z), numbers (0-9), and hyphens (-)
- Cannot start or end with a hyphen
- All names are stored in ASCII format

## Functions

### Public Functions

- `register-name`: Register a new domain name for a specified period
- `extend-validity`: Extend the validity of an existing domain name

### Read-Only Functions

- `get-name-info`: Retrieve information about a registered domain name
- `is-valid-name`: Check if a domain name meets the formatting requirements
- `current-time`: Get the current block time (used as a timestamp)

## Error Codes

| Code | Description |
|------|-------------|
| 100 | Unauthorized action |
| 101 | Name is unavailable (already registered) |
| 102 | Name not found |
| 103 | Invalid name format |
| 104 | Transaction failed |
| 105 | Payment required |

## Fees

- Base fee: 0.1 STX per year of registration
- Registration and extension fees are proportional to the registration period

## Security

- Administrative functions are restricted to the contract deployer
- Domain ownership is tracked and enforced

## Deployment

This contract can be deployed to the Stacks blockchain using the Clarinet CLI or other Stacks deployment tools.

## Future Improvements

Planned features for future versions:
- Domain name marketplace
- Domain name transfer between users
- Domain metadata and resolution