MET

Scored on submit-OK, not on inclusion. Inclusion, reported and not scored: in 0 of 4 minutes our payments included (desk counter) were within 10 percent of submit-OK.

# HOLD-3, desk, pre-run 35

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-3 offers 3040 simple payments a second at 150 sompi/gram (three thirds of 3,040 payments a second) on the kept public TN10 nodes. The covenant families, the KCC-20 mint line and the tic-tac-toe guest keep running on the desk node. No heavy lane. The desk node is not restarted.

Payment offer 3,040 tx/s at 150 sompi/gram, from 9 payment senders, 3 per kept public node (3 unique kaspads), each its own process and connection. Families offer 1.2 hop/s, 13 families live, one family-sender process and one builder: floor (families 1–12) 200 sompi/gram on the desk's private node, kcc (families 13–13) 100 sompi/gram on the desk's private node (public map ).

Payment pile: 5,408 coins on the payment key at the preflight, dealt evenly over the 9 senders before the first payment (last deal, repair: 5,408 coins in all, 601 / 601 / 601 / 601 / 601 / 601 / 601 / 601 / 600, even). A deal never holds more coins than the preflight pile. A coin is re-used about once a second, so one sender's ceiling is about its pool per second.

## Submit-OK and included, per minute

| Minute (UTC) | Pay submit-OK | Our payments included | Included, all non-coinbase | Counter |
|---|---:|---:|---:|---|
| 2026-11-14T15:19 | 182,242 | 118,500 | 121,886 | kept pace |
| 2026-11-14T15:20 | 181,475 | 124,352 | 127,691 | kept pace |
| 2026-11-14T15:21 | 183,542 | 122,557 | 123,673 | kept pace |
| 2026-11-14T15:22 | 181,944 | 126,056 | 126,198 | kept pace |

Submit-OK counts in the minute a submit was answered. Included counts in the minute of the chain block that accepted it, so a payment submitted late in one minute can be included in the next. "Kept pace" means the desk node's DAA stayed within 100 of the kept public kaspad and its sink was under 30 s old in every sample of that minute; "LAGGING" means it did not, and the count is what the node had accepted, not a network figure.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (200) | Kcc hops (100) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-14T15:19 | 121,886 | 118,500 | 347 | 2 | 3,037 | 266 | 0 | 590 | 20 | kept pace |
| 2026-11-14T15:20 | 127,691 | 124,352 | 327 | 2 | 3,010 | 273 | 1 | 500 | 20 | kept pace |
| 2026-11-14T15:21 | 123,673 | 122,557 | 340 | 3 | 800 | 260 | 0 | 845 | 20 | kept pace |
| 2026-11-14T15:22 | 126,198 | 126,056 | 318 | 3 | 23 | 270 | 0 | 327 | 20 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–12, desk private node): 200 sompi/gram per hop. Kcc (families 13–13, desk private node): no rows sompi/gram per hop. In pre-run 35 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (200) | 200.13 (200–200.32) | 641 | 41,797 (40,391–43,822) | - |
| kcc (100) | - | - | - | - |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 19 (21), 23 (16), 22 (16), 27 (15), 24 (15), 14 (14), 15 (14), 17 (12), 20 (12), 21 (11), 11 (11), 28 (9), and 81 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | Kcc OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---:|---:|---|
| 2026-11-14T15:19 | 182,242 | 182,242 | 0 | 0 | 0 | 347 / 994 / 0 / 0 / 11 | 0 / 0 / 0 / 0 / 0 | 0 | 1 | yes |
| 2026-11-14T15:20 | 181,475 | 181,475 | 0 | 0 | 0 | 327 / 979 / 0 / 0 / 11 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-14T15:21 | 183,542 | 183,542 | 0 | 0 | 0 | 341 / 996 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-14T15:22 | 181,944 | 181,944 | 0 | 0 | 0 | 318 / 984 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 35 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 164,160 to 200,640 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 3, 7. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 7 candidate endpoints passed the check and were 3 kaspads (node 2 is node 1, node 4 is node 1, node 5 is node 1, node 6 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 623334739 | 243,254 | 0 | 0 | 39 |
| 3 | yes | 623334739 | 243,209 | 0 | 0 | 33 |
| 7 | yes | 623334740 | 242,740 | 0 | 0 | 72 |

## Payment senders

| Sender | Node | Pay submit-OK | Rejects | Minutes with a row |
|---|---:|---:|---:|---:|
| 1.1 | 1 | 81,072 | 0 | 4 of 4 |
| 1.2 | 1 | 81,106 | 0 | 4 of 4 |
| 1.3 | 1 | 81,076 | 0 | 4 of 4 |
| 3.1 | 3 | 81,074 | 0 | 4 of 4 |
| 3.2 | 3 | 81,064 | 0 | 4 of 4 |
| 3.3 | 3 | 81,071 | 0 | 4 of 4 |
| 7.1 | 7 | 81,081 | 0 | 4 of 4 |
| 7.2 | 7 | 80,834 | 0 | 4 of 4 |
| 7.3 | 7 | 80,825 | 0 | 4 of 4 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 1333 of 1333 | 1748 | 4473 |
| kcc | 0 of 0 | - | - |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | Kcc in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: kcc | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 3 mempool | Public 7 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T15:19 | 3 (entries skipped: over the read cap) | 95,586 | 5,567 | 27.78 | - | - | - | - | - | - / - | - / - | - / - | 281 | 41,846 | 0 | 0 | 0 | 0 | 0 | 0 | 401.2 / 182.2 / 114.3 | 99,830 | 99,141 | 99,141 |
| 2026-11-14T15:20 | 3 (entries skipped: over the read cap) | 161,354 | 5,603 | 28.05 | - | - | - | - | - | - / - | - / - | - / - | 306 | 262 | 0 | 0 | 0 | 0 | 0 | 0 | 400.7 / 182.2 / 114.3 | 164,632 | 163,879 | 164,241 |
| 2026-11-14T15:21 | 3 (entries skipped: over the read cap) | 218,658 | 5,345 | 27.42 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 397.6 / 181.9 / 114.3 | 221,249 | 220,622 | 221,287 |
| 2026-11-14T15:22 | 3 (entries skipped: over the read cap) | 279,570 | 5,294 | 26.21 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 396.3 / 181.8 / 114.3 | 283,825 | 283,177 | 283,172 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Pre-run 17: ready count and ready mass come from the full mempool read up to 10,000 entries and from the node's own figures (getFeeEstimateExperimental, verbose) above that, where the per-class columns stay blank (the node's wRPC replies are capped at 128 MiB, about 12,500 entries). Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
