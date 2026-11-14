# AKINDO SUBMISSION — copy/paste each field

**Project name:** SafeSats

**Project category:** DeFi safety, borrowing, yield savings

**TL;DR:** SafeSats shows first-time Bitcoin borrowers how much MUSD they can borrow without getting liquidated — in plain English and traffic lights — then lets them earn yield on that MUSD in Mezo's sMUSD Savings Vault in two clicks.

**How it works:**
The problem: new BTC holders borrow the maximum Mezo allows and get liquidated in the first dip, because loans liquidate below 110% collateral and no beginner tool explains this simply. SafeSats solves it in three steps. (1) Connect a wallet on Mezo Testnet and see live BTC, MUSD, MEZO and sMUSD balances plus any existing trove, read directly from Mezo's contracts (MUSD 0x1189…, TroveManager 0xE47c…). (2) Use the Safe-Borrow Planner: enter BTC collateral, choose a safety level — we recommend 250%, not the 110% maximum — and instantly see a safe borrow amount, the BTC price at which liquidation would occur, and a green/amber/red safety rating. Borrowing itself is deep-linked to Mezo's official audited app, so SafeSats never custodies collateral. (3) Put idle MUSD to work: approve and deposit into Mezo's native MUSD Savings Vault (sMUSD, 0x6f46…) using its real deposit/withdraw/claimYield interface, with explorer links for every transaction. MUSD and MEZO are central, not bolted on: MUSD is the borrow asset, the savings asset and the yield asset; MEZO balances and ecosystem access are surfaced in the same wallet view.

**Target group:** First-time BTC borrowers in emerging markets (Africa, LatAm, SE Asia), beginner-to-intermediate, mobile and desktop MetaMask users who need plain English instead of liquidation formulas. Aligns with Track 1 (making MUSD productive capital via sMUSD) and Track 2 (reducing friction/access for new MUSD users).

**Tech stack:** HTML/CSS/JavaScript (single-file app), ethers.js v6, MetaMask/EVM wallet, Mezo Testnet RPC, Mezo core contracts (MUSD, sMUSD Savings Vault, TroveManager). No backend, no custody.

**Track:** Track 1 AND Track 2

**Chain deployed on:** Mezo Testnet (31611)

**Project status:** Entirely new — built during Wave 2 of the hackathon

**Project readiness:** Testnet deployment (live demo + real sMUSD transactions on Mezo testnet)

**Future milestones:**
1. (2 weeks) Telegram/SMS liquidation alerts when a trove drops below 150% collateral ratio
2. (1 month) One-click "borrow at a safe 250% ratio + auto-save MUSD into sMUSD" combined flow
3. (2 months) Mezo mainnet launch with local-language borrower safety guides and first 100 real users onboarded

**Team info:** [YOUR NAME — founder/builder — YOUR X + LinkedIn LINKS] — Solo builder. [EDIT THIS LINE before submitting]

**Updates in this Wave (Wave 2):** New project created in Wave 2: live wallet/balance/trove reader, safe-borrow planner with liquidation-price simulation, and working sMUSD deposit/withdraw/claim-yield transactions on Mezo testnet.
