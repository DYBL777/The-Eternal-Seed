# The Eternal Seed

**DYBL Foundation**  
*January 2026*  
*Version 1.3 (Draft)*

---

## Abstract

The Eternal Seed is a payment primitive where a percentage of every transaction is retained, compounding through yield to create a rising floor. We've developed 16 variants for lotteries, savings, protocol protection, and more.

The idea itself is simple: a percentage retained from every payment. The seed grows with each new transaction, yield from lending is a bonus, not the engine. The floor only rises under normal conditions. The real strength comes from building on that foundation carefully, together with the right partners.

**The simplest example:**

Traditional lottery: Jackpot won. Pot empties. Starts from zero.

Eternal Seed lottery: Jackpot won. 10% stays. Next pot starts higher.

That's it. The rest is variants.

---

## Origin: Built for Recurring Payments

The Eternal Seed was not designed for DeFi users.

It was designed for Web2: people buying lottery tickets, paying subscriptions, making recurring payments. Users who don't know what Aave is. Don't need to. Don't care.

Web3 is under the hood. The experience is Web2.

The primitive works because these payments are:
- Recurring (steady inflow)
- Small (low individual risk)
- Habitual (predictable behaviour)

From this, the seed compounds. The floor rises. Users see better products, not better protocols.

We are now developing a DeFi-native variant (The Breathing Seed) for users who want the mechanism exposed and their principal liquid. But the core was built for payments, not deposits.

---

## The Core Mechanism

The original idea was simple:

```
User pays (ticket, subscription, fee)
      │
      ├──► e.g. 85% ──► ACTIVE POOL (payouts, operations, rewards)
      │
      └──► e.g. 15% ──► ETERNAL SEED (never leaves, compounds forever)
      
      Both earn yield. The seed floor only rises.
```

*Percentages configurable at deployment. Immutable thereafter.*

**Properties:**

| Property | Behaviour |
|----------|-----------|
| Retention | A percentage of every payment joins the seed. |
| Yield | The seed earns yield (Aave, Compound, or similar). |
| Compounding | Seed grows two ways: yield + new payments. |
| Rising floor | Under normal conditions, it only goes up. |
| Dormancy protection | If system goes inactive, users can withdraw pro-rata. |

That was Variant 1: the Fixed Seed.

We thought we were done. We were not.

---

## Why We Diversified

Three concerns forced us to adapt:

### 1. The Insurance Label

Calling anything "insurance" invites regulatory scrutiny. Licensing requirements. Consumer protection rules. Jurisdictional complexity.

We did not want to build something that could not scale because of a word.

### 2. Locked Capital

Holding user funds indefinitely raises questions:
- Is this a security?
- Who has custody?
- What are the user's rights?

Different jurisdictions answer these differently. We needed flexibility.

### 3. Growth Limits

What happens when the seed gets large? Very large?

- Does it distort the market?
- Should it cap and overflow?
- Who decides where overflow goes?

We needed mechanisms for responsible scaling.

**The solution:** Do not build one product. Build a primitive with variants. Let each deployment configure for its context, jurisdiction, and purpose.

These adaptations ensure the primitive scales for payments while addressing edge cases in other domains.

The Eternal Seed became a family of 16 mechanisms (so far).

---

## The Variants

We group them by purpose:

### Core Variants

| Variant | Mechanism | Use Case |
|---------|-----------|----------|
| **Fixed Seed** | Static percentage locked | Lotteries, prize pools |
| **Flexible Seed** | Partial release under conditions | Volatile assets, buffers |
| **Capped Seed** | Grows to cap, then overflows | Sustainable growth, charity |

### Adaptive Variants

| Variant | Mechanism | Use Case |
|---------|-----------|----------|
| **Rolling Seed** | Percentage adjusts via oracle | Economic-responsive products |
| **Counter-Cyclical Seed** | Absorbs more during stress | DeFi stability mechanisms |
| **Tiered Seed** | Different rates for different users | Loyalty, institutional products |

### Distribution Variants

| Variant | Mechanism | Use Case |
|---------|-----------|----------|
| **Yield-Split Seed** | Yield flows to multiple destinations | Balanced growth/reward |
| **Charitable Seed** | Yield to verified charities | Perpetual giving |
| **Matched Seed** | Protocol matches user contributions | Savings incentives |

### Protection Variants

| Variant | Mechanism | Use Case |
|---------|-----------|----------|
| **Insurance Seed** | Pays out on verified triggers | Protocol protection |
| **Emergency Release Seed** | Multi-sig release for emergencies | User safety nets |

### Advanced Variants

| Variant | Mechanism | Use Case |
|---------|-----------|----------|
| **Burning Seed** | Burns seed to reduce supply | Deflationary tokens |
| **Time-Decay Seed** | Slow release over decades | Endowments, pensions |
| **Governance Seed** | Seed unlocks voting rights | DAO governance |
| **Compound-Only Seed** | Grows only from yield, no extraction | Non-extractive models |
| **Breathing Seed** | Inhales from yield, exhales to loyal users | DeFi yield wrappers |

Each variant shares the core property: **under normal conditions, the floor only rises.**

---

## Flagship Example: Lettery

Our first full implementation is Lettery, a lottery built on the Fixed Seed variant.

**How it works:**

- Ticket sales split: Prize Pool (55%), Seed (10%), Treasury (35%)
- Both Prize Pool and Seed compound together in same yield source
- Jackpot won? Prize Pool pays out. Seed principal stays.
- Floor rises because Seed principal never leaves, only grows with each ticket sold

**Why lottery first:**
- 40 years of research showing counter-cyclical behaviour, participation increases during downturns
- Clear value proposition (bigger jackpots over time)
- Web2 users with Web3 under the hood
- Proven market ($350B+ globally)

**Open design decisions:**

Yield allocation (how Prize Pool yield vs Seed yield flows on payout) is still being explored. We have strong opinions on the core (seed principal never leaves), but optimal configuration for edge cases will emerge through collaboration with the right team.

---

## Protocol Protection Layer

Our second focus is Variant 11: the Insurance Seed, rebranded as **Protocol Protection Layer (PPL)**.

**Why this variant:**
- Clear value proposition (embedded compensation)
- Strong differentiator (no premiums, no committees)
- Counter-cyclical behaviour (protection more valuable in downturns)
- Partner interest (yield protocols want sticky TVL)

**How it works:**

1. Users deposit into yield protocol (Aave, Compound, etc.)
2. Seed percentage retained, compounds alongside active pool
3. If exploit verified (oracle proposes, multi-sig confirms), seed pays out pro-rata
4. Users do not pay for protection. It is embedded.

**Key distinction:**

| Element | PPL | Traditional Models |
|---------|-----|-------------------|
| Trigger decision | Binary: did event happen? | Discretionary: does user deserve payout? |
| Payout calculation | Code calculates pro-rata | Committee decides amount |
| User cost | None (yield funds it) | Premiums |

---

## The Breathing Seed (DeFi Variant)

Variant 16 adapts the mechanism for DeFi users who want liquidity with their protection. Principal stays liquid. Seed grows from yield split, not payment retention.

This variant is detailed in a separate paper being worked on: *The Breathing Seed: Dynamic Distribution for DeFi Yield*.

---

## Other Applications

The same primitive, different configurations:

| Application | Variant Used | Key Benefit |
|-------------|--------------|-------------|
| **Stablecoin (Fibey)** | Rolling Seed | Supports national currency, user rebates, merchant bonuses |
| **Volatile Token (DYBL)** | Fixed + Burning | Deflationary + accumulating, permanent floor |
| **Savings Products** | Fixed/Matched Seed | Embedded protection, streak incentives |
| **Charitable Giving** | Charitable Seed | Perpetual giving, principal locked |
| **DAO Treasuries** | Capped + Governance | Permanent reserve, aligned incentives |

---

## Web2 Precedent: Embedded Compensation

Many Web2 services embed automatic compensation without separate coverage:

| Service | Trigger | Compensation | User Pays Extra? |
|---------|---------|--------------|------------------|
| UK Trains (Delay Repay) | 15-30 min delay | Up to 100% refund | No |
| EU Airlines (Reg 261) | 3+ hour delay | Up to €600 + expenses | No |
| US Airlines (DOT) | Cancellation | Full refund | No |
| Credit Cards | Trip delay | Up to $500 expenses | No |
| Product Warranties | Defect | Repair or refund | No |

**The pattern:** Compensation built into the service. No opt-in. No premiums. Protection is inherent.

DeFi can be the same. Embedded protection reduces friction, increases TVL, and aligns with models that already work at scale in Web2. We believe the Eternal Seed makes this possible.

---

## Technical Summary

### Core Parameters

| Parameter | Description |
|-----------|-------------|
| seedBps | Seed percentage in basis points |
| yieldSource | Aave, Compound, or similar |
| dormancyPeriod | Time before dormancy withdrawal enabled |

### Variant-Specific Parameters

Each variant adds configuration for its purpose:
- Trigger conditions (protection variants)
- Overflow destinations (capped variants)
- Decay rates (time-decay variants)
- Tier definitions (tiered variants)
- Breathing zones (breathing variant)

All parameters configured at deployment. Core mechanics immutable thereafter.

---

## Infrastructure

### Yield Source: Aave, Compound, and Others

The primitive is yield-source agnostic. Current implementations use Aave V3 as an example. Future versions may support multiple sources.

### Chain Agnostic

The primitive is designed to be portable. Current implementations are EVM-native, but the logic works anywhere with a reliable yield source and oracle.

### Oracle: Chainlink (Our Choice)

| Service | Use |
|---------|-----|
| Price Feeds | Trigger conditions, stress detection |
| VRF | Randomness for lottery variants |
| Automation | Scheduled operations |

We believe it is prudent to maintain a Chainlink reserve for ongoing services.

### Security: Audit Partners

Considering established firms: Cyfrin, OpenZeppelin, Trail of Bits, and others.

A deployment without audit is a deployment we do not want to make.

---

## Risk Assessment

| Risk | Mitigation |
|------|------------|
| Yield source exploit | Diversification in future versions |
| Yield source failure | Try/catch redirect to yield pool, no stuck funds |
| Oracle failure | Multi-sig confirmation + time delay |
| Locked capital concerns | Dormancy protection, variant flexibility |
| Regulatory | Compensation framing, jurisdictional configuration, proactive dialogue |

**Honest disclosure:** Not immune to smart contract risks, protocol exploits, or stablecoin depegs.

---

## Intellectual Property

Defensive patent filed November 2025 to prevent capture by bad actors. The goal is protection, not restriction.

Licensed under BUSL-1.1, converting to MIT in 2029 for open use. We want this primitive to be built on, not locked away.

---

## Approach

We are not trying to launch first and prove it works later.

**We want to find the right partners who share the vision and build this together.**

Some implementation details remain open by design. We have strong opinions on the core mechanics (seed principal never leaves, floor only rises) but believe the optimal configuration for yield flows, payout timing, and edge cases will emerge through collaboration with the right team. We are not pretending to have solved everything alone.

We built a framework for others to build on. What started as "the best lottery in the world" became a payment primitive. We are glad it did.

This primitive is ready. The code is written. What's needed now is the right team to build it properly, security-minded developers, integration expertise, and believers who see what this could become.

One deployment at a time. Each one audited. Each one partnered. Each one measured before the next.

We believe this will become a standard.

---

## Contact

**DYBL Foundation**

If this primitive resonates, let's explore variants together.

📧 dybl7@proton.me  
🐦 [@DYBL77](https://x.com/DYBL77)  
💻 [github.com/DYBL777](https://github.com/DYBL777)

---

*A percentage retained. The floor only rises.*

*The Eternal Seed.*
