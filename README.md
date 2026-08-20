# ERC20_Airdrop

A hands-on implementation of a **Merkle Tree–based ERC20 token airdrop**, built while learning Solidity, cryptographic proofs, and secure token distribution through the Cyfrin course.

## 🧠 What I'm Learning

This project explores how protocols can efficiently verify user eligibility and distribute tokens without storing large amounts of data on-chain.

### 🌳 Merkle Trees

- Generate a Merkle Tree from eligible addresses and token allocations
- Generate Merkle proofs for individual users
- Verify proofs on-chain using Solidity
- Understand how Merkle Trees reduce on-chain storage and gas costs

### 🎲 Verifiable Random Functions (VRF)

- Understand how verifiable randomness works
- Explore Chainlink VRF concepts
- Learn how randomness can be used safely in smart contracts
- Understand why predictable randomness can be dangerous

### 🪙 ERC20 Airdrop

- ERC20 token implementation
- Merkle-proof-based claim mechanism
- One-time claiming protection
- Gas-efficient eligibility verification
- Testing edge cases and potential attack vectors

## 🏗️ Architecture

```text
Eligible Users
      │
      ▼
┌─────────────────┐
│  Merkle Tree    │
└────────┬────────┘
         │
         ▼
   Merkle Root
         │
         ▼
┌─────────────────┐
│ Airdrop Contract│
└────────┬────────┘
         │
     User Claims
         │
         ▼
┌─────────────────┐
│ Merkle Proof    │
│  Verification   │
└────────┬────────┘
         │
         ▼
      ERC20
      Tokens
