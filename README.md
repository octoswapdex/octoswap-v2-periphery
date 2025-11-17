# OctoSwap CL-V2 Periphery Contracts

## **Contract Details**
- **Contract Name**: `OctoswapV2Router`
- **Solidity Version**: `^0.7.6`
- **Compiler Settings**:
  - **Optimization**: `Enabled` (Runs: `1000000`)
  - **EVM Version**: `Istanbul` 
  
- **Deployed Address (Monad Mainnet)**: `0xBfd2cf709A17c4eEE8DaaF3B96E134408881259e`


## **Contract Details**
- **Contract Name**: `NonfungiblePositionManager`
- **Solidity Version**: `^0.7.6`
- **Compiler Settings**:
  - **Optimization**: `Enabled` (Runs: `2000`)
  - **EVM Version**: `Istanbul` 

- **Deployed Address (Monad Mainnet)**: `0x16eb676BbBe51EB6E4E9DDF57BfBEe0537aA4d7B`


## **Contract Details**
- **Contract Name**: `NonfungibleTokenPositionDescriptor`
- **Solidity Version**: `^0.7.6`
- **Compiler Settings**:
  - **Optimization**: `Enabled` (Runs: `1000`)
  - **EVM Version**: `Istanbul` 

- **Deployed Address - Proxy (Monad Mainnet)**: `0x2Ff18d8Ca8447DB19392AA3e27DCB640CEe83882`

_nativeCurrencyLabel: 0x4d4f4e0000000000000000000000000000000000000000000000000000000000

# OctoSwap CL-V2 Periphery Changes (Uniswap V3 Periphery)

Comparison between `octoswap-v2-periphery` and original `uniswap/v3-periphery`.

## Contract Changes

### OctoswapV2Router.sol (SwapRouter.sol)
- **Line 22**: Contract name `SwapRouter` → `OctoswapV2Router`

### NonfungiblePositionManager.sol
- **Line 75**: NFT metadata `'Uniswap V3 Positions NFT-V1', 'UNI-V3-POS'` → `'OctoSwap CL POSITION', 'OCTO-CL'`

### libraries/NFTDescriptor.sol
- **Line 115**: Description text `'Uniswap V3'` → `'OctoSwap CL'`
- **Line 163**: NFT name prefix `'Uniswap - '` → `'Octoswap - '`
- **Lines 423-426**: Color values `136, 136, 0, 0` → `130, 130, 6, 6`

### libraries/PoolAddress.sol
- **Line 6**: Pool init code hash `0xe34f199b19b2b4f47f68442619d555527d244f78a3297ea89325f843f87b8b54` → `0x574937a78cfdd44f299af1e468b13c9405677431f9e9d1eb8763760416e3bd73`

## Unchanged Components

- **Base contracts**: All base contracts identical (100% match)
- **Interfaces**: All interface files identical (100% match)
- **Libraries**: All library files except NFTDescriptor.sol and PoolAddress.sol identical (100% match)

## Dependencies

All dependencies byte-for-byte identical to Uniswap V3 Periphery:
- `@openzeppelin/contracts`: 3.4.2-solc-0.7
- `@uniswap/lib`: 4.0.1-alpha
- `@uniswap/v2-core`: 1.0.1
- `@uniswap/v3-core`: 1.0.1
- `base64-sol`: 1.1.0 (Identical to Uniswap's Monad Mainnet Deployment)

---

## Summary

All changes are purely branding-related (contract names, NFT metadata, visual styling). All functional code, including routing logic, position management, swap calculations, callback validations, Solidity versions, and compiler optimization settings remain 100% identical to the original Uniswap V3 Periphery contracts. The init code hash change reflects the renamed core pool contract.

