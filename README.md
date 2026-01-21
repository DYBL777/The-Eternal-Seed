# SeedEngine

A payment primitive where capital locks, yield compounds, and the floor can only rise.

## What It Is

The Eternal Seed is a mechanism for permanent capital retention:

- A percentage of capital flows locked during active operation
- Locked capital earns yield, which compounds
- No withdrawal during operation — dormancy timelock protects users if the system ends
- The floor can only rise

## Why It Matters

This isn't product-specific. It's a financial primitive that could apply to:

- Lotteries with rising floors
- Savings products that can't collapse
- Stablecoins with backing that exceeds circulation over time
- Pensions with guaranteed minimums
- Any system with recurring capital flows

## 15 Variants Documented

| Variant | Description |
|---------|-------------|
| Fixed Seed | Permanent lock, never releases |
| Flexible Seed | Partial release under stress conditions |
| Rolling Seed | Lock % adjusts based on oracle data |
| Counter-Cyclical Seed | Absorbs more during stress, stabilises recovery |
| Capped Seed | Grows to threshold, then overflows |
| Tiered Seed | Different rates by user tenure/size |
| Yield-Split Seed | Yield distributed to multiple destinations |
| Insurance Seed | Pays out during black swan events |
| Burning Seed | Burns to create deflationary pressure |
| Time-Decay Seed | Slow release over decades |
| Matched Seed | Protocol matches user contributions |
| Governance Seed | Seed holdings unlock governance rights |
| Compound-Only Seed | Grows only from yield, not deposits |
| Emergency Release Seed | Multi-sig release for emergencies |
| Charitable Seed | All yield to verified charities |

All variants documented in `SeedEngine.sol` NatSpec.

## License

**BUSL-1.1** until **10 May 2029**, then **MIT**.

Production use before the Change Date requires a commercial license from DYBL Foundation.

## Contact

DYBL Foundation

- 📧 dybl7@proton.me
- 🐦 @DYBL77
- 💬 Discord: dybl777

## Related

- [DYBL-v1](https://github.com/DYBL777/DYBL-v1) — Lettery implementation using SeedEngine

---

🌱
