# 🛡️ SafeSats — Borrow MUSD Safely, Save It Automatically

**Mezo Buildathon Wave 2 · Track 1 (DeFi) + Track 2 (Access & Distribution) · Mezo Testnet (31611)**

SafeSats is a beginner-first DeFi safety tool for first-time Bitcoin borrowers. In plain English and traffic lights, it shows how much MUSD you can borrow *without* risking liquidation — then puts idle MUSD to work in Mezo's native sMUSD Savings Vault in two clicks.

## The problem
New BTC holders borrow the maximum Mezo allows, get liquidated in the first price dip (loans liquidate below 110% collateral), and never return to DeFi. Existing buildathon tools target experts: looping vaults, escrows, pro dashboards.

## The gap we fill
Nobody owns the **first-time borrower safety** niche. SafeSats is the seatbelt:
1. **Wallet snapshot** — live BTC / MUSD / MEZO / sMUSD balances + existing trove (loan) status, read on-chain
2. **Safe-Borrow Planner** — enter BTC + pick a safety level (we recommend 250%, never the 110% max); get a safe borrow number, liquidation price, and a 🟢/🟡/🔴 rating
3. **Save & Earn** — approve + deposit MUSD into the native sMUSD Savings Vault, withdraw, claim yield — real transactions the user signs

Borrowing itself stays in Mezo's official audited app (deep-linked). SafeSats never custodies funds and never asks for keys.

## Mezo integration (testnet)
| Contract | Address | Used for |
|---|---|---|
| MUSD | `0x118917a40FAF1CD7a13dB0Ef56C86De7973Ac503` | balance, approve |
| MEZO | `0x7B7c000000000000000000000000000000000001` | balance |
| sMUSD Savings Vault | `0x6f461c68B2c5492C0F5CCEc5a264d692aA7A8e16` | `deposit(uint256)`, `withdraw(uint256)`, `claimYield()` (not ERC-4626 — native interface) |
| BorrowerOperations | `0xCdF7028ceAB81fA0C6971208e83fa7872994beE5` | protocol reference / future one-click borrow |
| TroveManager | `0xE47c80e8c23f6B4A1aE41c34837a0599D5D16bb0` | `getTroveColl/Debt/Status` for live loan display |

## Run it
No build step. Serve the folder statically:
```bash
npx serve .        # or: python3 -m http.server 5173
# open http://localhost:5173
```
Or deploy free: drag this folder into **Netlify Drop**, or push to GitHub and enable **GitHub Pages**, or import into **Vercel**.

**To test:** MetaMask → add Mezo Testnet (the app auto-prompts) → get test BTC/MEZO at https://faucet.test.mezo.org → get MUSD by borrowing/swapping at https://testnet.mezo.org → come back and Save.

## Tech stack
Single-file HTML/CSS/JS + ethers.js v6 (CDN), direct RPC/wallet calls to Mezo testnet. No backend, no database, no custody.

## Roadmap
1. Telegram/SMS liquidation alerts when a trove falls below 150% ICR
2. One-click "borrow at 250% + auto-save the MUSD" combined flow
3. Mezo mainnet launch, local-language (starting with Nigerian English/Pidgin) safety guides

## Disclaimer
Testnet demo. Testnet assets have no value. Not financial advice.
