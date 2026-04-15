# x402-use-cases
Breakdown of x402 transaction activity by usecase category.

x402 has processed 98M categorized transactions across six use case types. This notebook looks at where the volume actually goes, how concentrated it is, and which categories correlate with gamed activity.

## Findings

**Agent-to-Agent dominates.** 41% of classified volume and 40% of transactions. This is the core use case: agents paying other agents directly.

**Token Launches punch above their weight.** Only 5% of transactions but 23% of volume, with the highest avg value per tx at $0.58. These are fewer, larger payments.

**Utilities are high frequency, but low value.** 30% of all transactions but just 5% of volume at $0.02/tx. Cheap, repetitive calls as expected.

**The protocol is heavily concentrated.** HHI has never dropped below 3,900. One category has dominated volume share in every single month since launch. The dominant category shifted from Data (May-Jun '25) to Agent-to-Agent (Jul '25 onward), with Token Launches briefly taking over in Oct '25.

**Gaming correlates with micro-transaction categories.** Agent-to-Agent, Utilities, and Data all show strong positive Spearman correlation with gamed % (rho > 0.73). Token Launches shows no significant correlation (rho = 0.12). Gaming concentrates where transactions are cheap and easy to farm, not where value per tx is highest.

## Data

Artemis x402 categorized daily aggregates, May 2025 to March 2026, 309 active days. Classified volume only ($12.2M of ~$108M total). Unclassified transactions excluded.

## Stack

Python, pandas, matplotlib, scipy.
