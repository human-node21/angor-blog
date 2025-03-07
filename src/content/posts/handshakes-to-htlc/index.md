---
title: "Handshakes to HTLC"
published: 2025-03-07
description: ""
image: ""
tags: []
category: ""
draft: false
---

## Hi there,

Ever backed a startup and worried about what happens to your money? What if the founder vanishes? Or the project stalls? On Angor, Hash Time Lock Contracts (HTLC) ensure funds move only when milestones are met, keeping your investment secure until the work is done.

### What is Hash Lock (HL) & Time Lock (TL)?

#### Hashlock (HL):
Imagine ordering a package online, but instead of the delivery driver just handing it over, they ask for a one-time secret code that only you know. Without that code, they can’t unlock the package and give it to anyone else. That’s how a hashlock works. It ensures that only the right person, with the correct secret, can access the funds.

#### Timelock (TL):
Now, imagine that your package is waiting at a pickup locker, but there’s a deadline that you must collect it within 48 hours. If you don’t, the locker automatically locks you out, and the package is sent back to the seller for a refund. That’s how a timelock works. It gives the recipient a set amount of time to claim their funds, and if they don’t, the money automatically returns to the sender.

### Why do I need HTLC for investment or crowdfunding?

Society has always evolved around trust, from the early days of bartering goods and services to using gold, silver, and other scarce materials as money. As global trade expanded, so did the risks. Pirates began attacking shipments, looting wealth, and exposing the vulnerabilities of moving money physically.

To solve this, **Hawala** emerged as a trust-based system where brokers, known as hawaladars, transferred money across regions without physically moving cash. It was faster and safer, but it relied entirely on trust. If a hawaladar disappeared, so did the money.

Then came **banks**, a place to securely store money, facilitate transactions, and reduce risk. At first, it was a breakthrough. But as banks grew more powerful, they dictated who could access their funds, charged endless fees, and even froze accounts. What started as a system of convenience slowly became a system of control.

And then, in **2009, Bitcoin changed everything**.

For the first time, money could move peer-to-peer, without handshakes, without middlemen, just one person sending value directly to another, anywhere in the world. Every transaction was secure, transparent, and recorded on the blockchain, ensuring that no one could alter or erase it.

### Multi-signature (multi-sig) wallets

Multi-sig wallets allowed multiple people to jointly control funds. An investment deal no longer had to rely on a single person holding the money. Instead, a transaction would require **3 out of 5 investors** to approve it before funds were released, adding an extra layer of security and reducing risk.

While multi-sig made transactions more secure, it still required coordination and manual approvals. What if we could take it further? What if financial agreements could be fully automated, enforced by code instead of trust?

### That’s where HTLCs come in 🚀

Let’s start with an example -

Imagine you (**A**) want to invest some Bitcoin. Four of your friends (**B, C, D, and E**) join in. Instead of trusting a single person to manage the funds, you want a system that ensures the money only moves when the agreed conditions are met.

You also want security and transparency with clear rules, automated execution, and no middlemen holding your funds. While browsing the internet for a solution, you come across **Angor.io**.

You learn that on Angor, **Hash Time-Locked Contracts (HTLCs)** enable peer-to-peer transactions without banks or third parties. Instead of relying on a person or institution, you rely on **open-source code**. A code that even you can verify.

### HTLCs automate transactions by combining two essential elements:

#### 1️⃣ Hashed Lock Contract (HLC) – Unlocking Funds with a Secret
Think of an HLC as a smart escrow system. Funds are locked in a contract and can only be claimed if the recipient provides the correct secret key (hash preimage). If they don’t, the money automatically returns to the sender. This ensures payments are secure and conditional without needing a middleman.

#### 2️⃣ Time-Locked Contract (TLC) – Enforcing a Deadline
To ensure funds don’t stay locked indefinitely, TLC sets a deadline for the transaction. There are two ways this can work:

- **CLTV (CheckLockTimeVerify)**: Funds remain locked until a specific date or block height (e.g., “Refund only after January 1, 2026”).
- **CSV (CheckSequenceVerify)**: Funds remain locked for a set period after confirmation (e.g., “Refund if unclaimed after 1,000 blocks”).

If the recipient doesn’t claim the funds in time, the money automatically returns to the sender.

### How does HTLC work on Angor?

#### Step 1: Investors Lock Funds On-Chain
- Each investor deposits **2 BTC**, totaling **10 BTC**, into the HTLC contract on Angor Protocol.
- The funds are now in escrow.
- The contract is **time-locked for 90 days**.
- **Milestone-based release** – **5 BTC is released** when the first milestone is approved, and the remaining **5 BTC is unlocked** after final verification.

#### Step 2: The Secret is generated and shared
- Before funding begins, **Koni** (the startup founder) generates a random **secret (S)**.
- This secret is then **hashed** to create a unique identifier, called the **hash (H)**.
- Instead of sharing **S**, Koni only shares **H** with the investors.
- The investors include **H** in the HTLC contract, ensuring that funds can only be released if the correct secret (**S**) is provided.

#### Step 3: How do investors verify work?
- HTLCs **do not check if the work is done**. It only enforces the payment condition.
- Investors verify Koni’s progress externally (e.g., reviewing reports, product demos, or milestones on Angor).
- If the milestone is met, Koni submits the **secret (S)** to unlock the funds.
- The contract checks if **hash(S) = H**. If correct, it releases the **first 5 BTC**.
- After further review and approval, Koni submits the **secret again** to unlock the remaining **5 BTC**.

#### Step 4: When conditions aren’t fulfilled
- If Koni fails to reveal **S** within **90 days**, the contract **automatically refunds** the **10 BTC** back to the investors.
- If milestones aren’t met, investors can vote to extend the deadline or withdraw their funds using **multi-signature approval**.

#### Step 5: When all conditions are fulfilled
- If Koni submits the correct **secret (S)** and meets all conditions before the deadline, the smart contract automatically releases the **full 10 BTC** to him.

### The Future of Trustless Transactions

Traditionally, **multi-signature wallets** were required where at least **3 out of 5 investors** had to sign and approve a transaction before funds could move. It required coordination among multiple parties for every payout.

Now with **HTLC**, this process is automated i.e., once the secret (**S**) is revealed and verified by the contract, the funds are released **without requiring any additional signatures**. It literally puts control back in the hands of investors.

The **future of trustless transactions is here**. And yes, it’s all possible with **Angor**.

See you next week for another post.

Ciao.
