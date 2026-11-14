NOT MET

Scored on submit-OK, not on inclusion. Inclusion, reported and not scored: in 11 of 12 minutes our payments included (desk counter) were within 10 percent of submit-OK.

# HOLD-1, desk, pre-run 35

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-1 offers 1013 simple payments a second at 150 sompi/gram (one third of 3,040 payments a second) on the kept public TN10 nodes. The covenant families, the KCC-20 mint line and the tic-tac-toe guest keep running on the desk node. No heavy lane. The desk node is not restarted.

Payment offer 1,013 tx/s at 150 sompi/gram, from 9 payment senders, 3 per kept public node (3 unique kaspads), each its own process and connection. Families offer 1.2 hop/s, 13 families live, one family-sender process and one builder: floor (families 1–12) 200 sompi/gram on the desk's private node, kcc (families 13–13) 100 sompi/gram on the desk's private node (public map ).

Payment pile: 5,408 coins on the payment key at the preflight, dealt evenly over the 9 senders before the first payment (last deal, repair: 5,408 coins in all, 601 / 601 / 601 / 601 / 601 / 601 / 601 / 601 / 600, even). A deal never holds more coins than the preflight pile. A coin is re-used about once a second, so one sender's ceiling is about its pool per second.

## Submit-OK and included, per minute

| Minute (UTC) | Pay submit-OK | Our payments included | Included, all non-coinbase | Counter |
|---|---:|---:|---:|---|
| 2026-11-14T15:00 | 34,681 | 34,335 | 38,225 | kept pace |
| 2026-11-14T15:01 | 34,082 | 33,995 | 37,995 | kept pace |
| 2026-11-14T15:02 | 11,293 | 11,427 | 15,359 | kept pace |
| 2026-11-14T15:03 | 6,407 | 6,362 | 10,336 | kept pace |
| 2026-11-14T15:04 | 6,328 | 6,362 | 10,537 | kept pace |
| 2026-11-14T15:05 | 6,284 | 6,328 | 10,409 | kept pace |
| 2026-11-14T15:07 | 9,322 | 9,430 | 13,554 | kept pace |
| 2026-11-14T15:08 | 9,320 | 9,318 | 13,377 | kept pace |
| 2026-11-14T15:09 | 0 | 1,147 | 5,110 | kept pace |
| 2026-11-14T15:10 | 0 | 0 | 4,116 | kept pace |
| 2026-11-14T15:11 | 0 | 0 | 4,075 | kept pace |
| 2026-11-14T15:12 | 0 | 0 | 4,129 | kept pace |

Submit-OK counts in the minute a submit was answered. Included counts in the minute of the chain block that accepted it, so a payment submitted late in one minute can be included in the next. "Kept pace" means the desk node's DAA stayed within 100 of the kept public kaspad and its sink was under 30 s old in every sample of that minute; "LAGGING" means it did not, and the count is what the node had accepted, not a network figure.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (200) | Kcc hops (100) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-14T15:00 | 38,225 | 34,335 | 878 | 4 | 3,068 | 344 | 0 | 359 | 20 | kept pace |
| 2026-11-14T15:01 | 37,995 | 33,995 | 901 | 4 | 3,159 | 370 | 0 | 446 | 20 | kept pace |
| 2026-11-14T15:02 | 15,359 | 11,427 | 843 | 3 | 3,128 | 342 | 1 | 566 | 20 | kept pace |
| 2026-11-14T15:03 | 10,336 | 6,362 | 861 | 4 | 3,153 | 368 | 1 | 451 | 20 | kept pace |
| 2026-11-14T15:04 | 10,537 | 6,362 | 961 | 4 | 3,260 | 380 | 1 | 422 | 19 | kept pace |
| 2026-11-14T15:05 | 10,409 | 6,328 | 976 | 4 | 3,133 | 366 | 1 | 384 | 20 | kept pace |
| 2026-11-14T15:07 | 13,554 | 9,430 | 896 | 4 | 3,280 | 341 | 1 | 482 | 19 | kept pace |
| 2026-11-14T15:08 | 13,377 | 9,318 | 856 | 4 | 3,262 | 350 | 1 | 457 | 20 | kept pace |
| 2026-11-14T15:09 | 5,110 | 1,147 | 892 | 4 | 3,108 | 368 | 0 | 924 | 20 | kept pace |
| 2026-11-14T15:10 | 4,116 | 0 | 944 | 3 | 3,190 | 408 | 0 | 351 | 20 | kept pace |
| 2026-11-14T15:11 | 4,075 | 0 | 959 | 4 | 3,150 | 378 | 0 | 378 | 20 | kept pace |
| 2026-11-14T15:12 | 4,129 | 0 | 933 | 4 | 3,223 | 362 | 0 | 461 | 19 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–12, desk private node): 200 sompi/gram per hop. Kcc (families 13–13, desk private node): no rows sompi/gram per hop. In pre-run 35 that rate is on the hop's node-side mass (kit21): the builder is asked for a bill rate on its own mass so that fee / node mass is the tier's rate.

| Tier | Node rate as built, median (min–max) | Bill rate, median | Node mass, median (min–max) | Node rate in the desk mempool, lowest–highest (probe) |
|---|---|---:|---|---|
| floor (200) | 200.16 (200–200.32) | 655 | 42,709 (40,392–43,838) | 200–200.31 |
| kcc (100) | - | - | - | 100.12–100.12 |

Node rate as built is kit21's fee / node mass (rusty-kaspa v2.1.0 storage mass with UTXO plurality, or compute or transient/2 if larger). In the desk mempool the probe divides the node's fee by the larger of the storage and compute mass the node reports.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 32 (28), 30 (19), 31 (17), 34 (16), 27 (14), 36 (14), 35 (13), 33 (13), 38 (11), 37 (11), 26 (11), 23 (10), and 75 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | Kcc OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---:|---:|---|
| 2026-11-14T15:00 | 34,681 | 34,686 | 0 | 0 | 5 | 879 / 1103 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:01 | 34,082 | 34,092 | 0 | 0 | 10 | 898 / 1146 / 0 / 0 / 9 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:02 | 11,293 | 11,758 | 0 | 0 | 465 | 834 / 1099 / 0 / 0 / 0 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:03 | 6,407 | 6,407 | 0 | 0 | 0 | 874 / 1143 / 0 / 0 / 13 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:04 | 6,328 | 6,329 | 0 | 0 | 1 | 961 / 1150 / 0 / 0 / 3 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:05 | 6,284 | 6,285 | 0 | 0 | 1 | 965 / 1186 / 0 / 0 / 2 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:07 | 9,322 | 9,322 | 0 | 0 | 0 | 894 / 1136 / 0 / 0 / 0 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:08 | 9,320 | 9,321 | 0 | 0 | 1 | 868 / 1120 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off |
| 2026-11-14T15:09 | 0 | 0 | 0 | 0 | 0 | 881 / 1127 / 0 / 0 / 1 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off;proc-row-missing;proc_exit |
| 2026-11-14T15:10 | 0 | 0 | 0 | 0 | 0 | 944 / 1109 / 0 / 0 / 1 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off;proc-row-missing |
| 2026-11-14T15:11 | 0 | 0 | 0 | 0 | 0 | 970 / 1181 / 0 / 0 / 12 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off;proc-row-missing |
| 2026-11-14T15:12 | 0 | 0 | 0 | 0 | 0 | 932 / 1133 / 0 / 0 / 11 | 0 / 0 / 0 / 0 / 0 | 0 | 0 | no: ok-off;proc-row-missing |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 35 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 54,702 to 66,858 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 3, 7. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 7 candidate endpoints passed the check and were 3 kaspads (node 2 is node 1, node 4 is node 1, node 5 is node 1, node 6 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 623329457 | 39,788 | 178 | 0 | 38 |
| 3 | yes | 623329457 | 43,674 | 166 | 0 | 32 |
| 7 | yes | 623329457 | 34,255 | 139 | 0 | 72 |

## Payment senders

| Sender | Node | Pay submit-OK | Rejects | Minutes with a row |
|---|---:|---:|---:|---:|
| 1.1 | 1 | 13,370 | 58 | 8 of 12 |
| 1.2 | 1 | 13,407 | 63 | 8 of 12 |
| 1.3 | 1 | 13,011 | 57 | 8 of 12 |
| 3.1 | 3 | 15,878 | 58 | 8 of 12 |
| 3.2 | 3 | 12,641 | 55 | 8 of 12 |
| 3.3 | 3 | 15,155 | 53 | 8 of 12 |
| 7.1 | 7 | 13,529 | 55 | 8 of 12 |
| 7.2 | 7 | 14,390 | 62 | 8 of 12 |
| 7.3 | 7 | 6,336 | 22 | 8 of 12 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 11781 of 11781 | 594 | 1155 |
| kcc | 0 of 0 | - | - |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | Kcc in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: kcc | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 3 mempool | Public 7 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T15:00 | 3 | 225 | 225 | 1.80 | 0 | 0 | - | - | 206 | 0 / 0 | 12 / 12 | 0 / 0 | 103 | 344,556 | 0 | 95 | 0 | 8 | 0 | 0 | 213.3 / 154.6 / 111.5 | 320 | 509 | 509 |
| 2026-11-14T15:01 | 3 | 137 | 213 | 1.60 | 0 | 0 | - | - | 202 | 0 / 0 | 11 / 11 | 0 / 0 | 104 | 343,196 | 0 | 96 | 0 | 8 | 0 | 0 | 201.4 / 151.0 / 111.0 | 229 | 177 | 172 |
| 2026-11-14T15:02 | 3 | 31 | 34 | 1.34 | 1 | 1 | - | - | 21 | 0 / 0 | 12 / 12 | 0 / 0 | 28 | 470,788 | 0 | 17 | 0 | 11 | 0 | 0 | 118.0 / 112.5 / 103.7 | 89 | 67 | 76 |
| 2026-11-14T15:03 | 3 | 3 | 12 | 1.03 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 471,160 | 0 | 0 | 0 | 11 | 0 | 0 | 100.0 / 100.0 / 100.0 | 1 | 20 | 11 |
| 2026-11-14T15:04 | 3 | 12 | 12 | 1.03 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 427,783 | 0 | 0 | 0 | 10 | 0 | 0 | 101.6 / 101.2 / 100.4 | 32 | 32 | 32 |
| 2026-11-14T15:05 | 3 | 12 | 12 | 1.02 | 0 | 0 | - | - | 0 | 0 / 0 | 9 / 9 | 0 / 0 | 11 | 385,261 | 0 | 0 | 0 | 9 | 0 | 0 | 100.0 / 100.0 / 100.0 | 33 | 33 | 31 |
| 2026-11-14T15:07 | 3 | 11 | 51 | 1.15 | 0 | 0 | - | - | 39 | 0 / 0 | 12 / 12 | 0 / 0 | 49 | 426,425 | 0 | 39 | 0 | 10 | 0 | 0 | 138.6 / 124.7 / 106.6 | 39 | 48 | 51 |
| 2026-11-14T15:08 | 3 | 50 | 60 | 1.10 | 0 | 0 | 1 | 2,230 | 49 | 0 / 0 | 12 / 12 | 0 / 0 | 29 | 466,157 | 0 | 17 | 0 | 11 | 0 | 0 | 144.3 / 127.7 / 107.2 | 68 | 50 | 51 |
| 2026-11-14T15:09 | 3 | 12 | 62 | 1.21 | 1 | 1 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 47 | 423,321 | 0 | 0 | 0 | 10 | 0 | 1 | 127.4 / 118.4 / 105.2 | 64 | 52 | 51 |
| 2026-11-14T15:10 | 3 | 12 | 12 | 1.01 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 467,649 | 0 | 0 | 0 | 11 | 0 | 0 | 106.2 / 104.5 / 101.5 | 10 | 10 | 2 |
| 2026-11-14T15:11 | 3 | 0 | 11 | 0.93 | 0 | 0 | - | - | 0 | 0 / 0 | 11 / 11 | 0 / 0 | 11 | 462,812 | 0 | 0 | 0 | 11 | 0 | 0 | 100.0 / 100.0 / 100.0 | 0 | 0 | 0 |
| 2026-11-14T15:12 | 3 | 1 | 1 | 0.08 | 0 | 0 | - | - | 0 | 0 / 0 | 1 / 1 | 0 / 0 | 1 | 42,025 | 0 | 0 | 0 | 1 | 0 | 0 | 100.0 / 100.0 / 100.0 | 1 | 0 | 1 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Pre-run 17: ready count and ready mass come from the full mempool read up to 10,000 entries and from the node's own figures (getFeeEstimateExperimental, verbose) above that, where the per-class columns stay blank (the node's wRPC replies are capped at 128 MiB, about 12,500 entries). Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
