# 🌱 The Eternal Seed (TES)

**A payment primitive where capital locks, yield compounds, and the floor rises.**

> What if the floor only went up?  
> What if your protocol couldn't be drained?  
> What if capital stayed... and grew?

---

## What It Is

The Eternal Seed is a mechanism for **permanent capital retention**:

- A percentage of capital flows locked during active operation
- Locked capital earns yield, which compounds
- No withdrawal during operation. Dormancy timelock protects users if the system becomes inactive
- Under normal conditions, the floor only rises

This isn't a product. It's **infrastructure**.

---

## Why It Matters

The Eternal Seed is a financial primitive that applies to:

| Use Case | How Seed Helps |
|----------|----------------|
| Lotteries | Rising floor under normal operation |
| Savings products | Principal protected by design |
| Insurance | Self-funding coverage, no external premiums |
| Stablecoins | Backing can exceed circulation over time |
| Pensions | Minimums that compound |
| DAOs | Treasury that grows, not drains |

Any system with recurring capital flows can use a seed.

---

## 15 Variants Documented

| # | Variant | Description |
|---|---------|-------------|
| 1 | **Fixed Seed** | Permanent lock during active operation |
| 2 | **Flexible Seed** | Partial release under stress conditions |
| 3 | **Rolling Seed** | Lock % adjusts based on oracle data |
| 4 | **Counter-Cyclical Seed** | Absorbs more during stress, stabilises recovery |
| 5 | **Capped Seed** | Grows to threshold, then overflows |
| 6 | **Tiered Seed** | Different rates by user tenure/size |
| 7 | **Yield-Split Seed** | Yield distributed to multiple destinations |
| 8 | **Insurance Seed** | Pays out during black swan events |
| 9 | **Burning Seed** | Burns to create deflationary pressure |
| 10 | **Time-Decay Seed** | Slow release over decades |
| 11 | **Matched Seed** | Protocol matches user contributions |
| 12 | **Governance Seed** | Seed holdings unlock governance rights |
| 13 | **Compound-Only Seed** | Grows only from yield, not deposits |
| 14 | **Emergency Release Seed** | Multi-sig release for emergencies |
| 15 | **Charitable Seed** | All yield to verified charities |

All variants fully specified in [`SeedEngine.sol`](./src/SeedEngine.sol) NatSpec.

---

## Implementations

| Variant | Product | Status | Repo |
|---------|---------|--------|------|
| 7 | Lettery | Pre-Audit | [Lettery](https://github.com/DYBL777/Lettery) |
| 8 | Insurance Seed | Pre-Audit | [Seed-Insurance](https://github.com/DYBL777/Seed-Insurance) |
| 1-6, 9-15 | | Specified | This repo |

---

## The Core Invariant

```
┌─────────────────────────────────────────────────────┐
│                                                     │
│   Capital In  ──►  Seed  ──►  Yield  ──►  Compound  │
│                      │                       │      │
│                      └───────────────────────┘      │
│                                                     │
│        Under normal operation, floor rises.         │
│                                                     │
└─────────────────────────────────────────────────────┘
```

During active operation, seed grows. The only exits are:

1. **Dormancy** : System inactive 90+ days, users can withdraw pro-rata
2. **Variant-specific triggers** : Insurance claims, emergency release, etc.

---

## License

**Business Source License 1.1 (BUSL-1.1)**

- **Licensor:** DYBL Foundation
- **Licensed Work:** SeedEngine and all documented variants
- **Change Date:** 10 May 2029
- **Change License:** MIT

Production use before the Change Date requires a commercial license from DYBL Foundation.

---

## Contact

**DYBL Foundation**

| Channel | Handle |
|---------|--------|
| 📧 Email | dybl7@proton.me |
| 🐦 Twitter | [@DYBL77](https://twitter.com/DYBL77) |
| 💬 Discord | dybl777 |
| 🔗 GitHub | [DYBL777](https://github.com/DYBL777) |

---

🌱 *A seed that grows from within. A floor that rises. Eternally fair.*
