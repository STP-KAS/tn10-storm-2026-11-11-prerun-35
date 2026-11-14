> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value. Counts only.

> **Our own testing.** What this page shows is what our probe read on our own desk node in this run; it is not a claim of how TN10 behaves in general.

# Mempool and template timeline, pre-run 35

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Pre-run 17: ready count and ready mass come from the full mempool read up to 10,000 entries and from the node's own figures (getFeeEstimateExperimental, verbose) above that, where the per-class columns stay blank (the node's wRPC replies are capped at 128 MiB, about 12,500 entries). Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs (our heavy lane is its own class, our heavy); its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.

## The run

Step is the runner's step at the minute's start (see TIMELINE.md).

| Minute (UTC) | Step | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Our heavy in mempool / ready | Floor in mempool / ready | Kcc in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: our heavy | Template: floor | Template: kcc | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 3 mempool | Public 7 mempool |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T14:54 | families | 2 | 11 | 12 | 1.04 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 475,319 | 0 | 0 | 0 | 11 | 0 | 0 | 106.8 / 105.0 / 101.6 | 12 | 1 | 1 |
| 2026-11-14T14:55 | BASE | 3 | 5 | 11 | 0.95 | 0 | 0 | - | - | 0 | 0 / 0 | 11 / 11 | 0 / 0 | 11 | 473,755 | 0 | 0 | 0 | 11 | 0 | 0 | 100.0 / 100.0 / 100.0 | 0 | 0 | 1 |
| 2026-11-14T14:56 | BASE | 3 | 11 | 12 | 1.04 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 474,041 | 0 | 0 | 0 | 11 | 0 | 0 | 109.6 / 106.9 / 102.2 | 0 | 0 | 1 |
| 2026-11-14T14:57 | BASE | 3 | 1 | 10 | 0.86 | 0 | 0 | - | - | 0 | 0 / 0 | 10 / 10 | 0 / 0 | 10 | 430,120 | 0 | 0 | 0 | 10 | 0 | 0 | 100.0 / 100.0 / 100.0 | 1 | 0 | 1 |
| 2026-11-14T14:58 | HOLD-1 | 2 | 146 | 152 | 1.60 | 1 | 1 | - | - | 139 | 0 / 0 | 12 / 12 | 0 / 0 | 78 | 387,863 | 0 | 69 | 0 | 9 | 0 | 0 | 202.9 / 151.5 / 111.1 | 512 | 512 | 511 |
| 2026-11-14T14:59 | HOLD-1 | 3 | 70 | 220 | 2.08 | 3 | 3 | - | - | 206 | 0 / 0 | 11 / 11 | 0 / 0 | 52 | 430,177 | 0 | 42 | 0 | 10 | 0 | 0 | 215.9 / 155.3 / 111.5 | 276 | 237 | 194 |
| 2026-11-14T15:00 | HOLD-1 | 3 | 225 | 225 | 1.80 | 0 | 0 | - | - | 206 | 0 / 0 | 12 / 12 | 0 / 0 | 103 | 344,556 | 0 | 95 | 0 | 8 | 0 | 0 | 213.3 / 154.6 / 111.5 | 320 | 509 | 509 |
| 2026-11-14T15:01 | HOLD-1 | 3 | 137 | 213 | 1.60 | 0 | 0 | - | - | 202 | 0 / 0 | 11 / 11 | 0 / 0 | 104 | 343,196 | 0 | 96 | 0 | 8 | 0 | 0 | 201.4 / 151.0 / 111.0 | 229 | 177 | 172 |
| 2026-11-14T15:02 | HOLD-1 | 3 | 31 | 34 | 1.34 | 1 | 1 | - | - | 21 | 0 / 0 | 12 / 12 | 0 / 0 | 28 | 470,788 | 0 | 17 | 0 | 11 | 0 | 0 | 118.0 / 112.5 / 103.7 | 89 | 67 | 76 |
| 2026-11-14T15:03 | HOLD-1 | 3 | 3 | 12 | 1.03 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 471,160 | 0 | 0 | 0 | 11 | 0 | 0 | 100.0 / 100.0 / 100.0 | 1 | 20 | 11 |
| 2026-11-14T15:04 | HOLD-1 | 3 | 12 | 12 | 1.03 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 427,783 | 0 | 0 | 0 | 10 | 0 | 0 | 101.6 / 101.2 / 100.4 | 32 | 32 | 32 |
| 2026-11-14T15:05 | HOLD-1 | 3 | 12 | 12 | 1.02 | 0 | 0 | - | - | 0 | 0 / 0 | 9 / 9 | 0 / 0 | 11 | 385,261 | 0 | 0 | 0 | 9 | 0 | 0 | 100.0 / 100.0 / 100.0 | 33 | 33 | 31 |
| 2026-11-14T15:06 | HOLD-1 | 3 | 12 | 12 | 1.03 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 428,820 | 0 | 0 | 0 | 10 | 0 | 0 | 103.2 / 102.3 / 100.8 | 0 | 46 | 6 |
| 2026-11-14T15:07 | HOLD-1 | 3 | 11 | 51 | 1.15 | 0 | 0 | - | - | 39 | 0 / 0 | 12 / 12 | 0 / 0 | 49 | 426,425 | 0 | 39 | 0 | 10 | 0 | 0 | 138.6 / 124.7 / 106.6 | 39 | 48 | 51 |
| 2026-11-14T15:08 | HOLD-1 | 3 | 50 | 60 | 1.10 | 0 | 0 | 1 | 2,230 | 49 | 0 / 0 | 12 / 12 | 0 / 0 | 29 | 466,157 | 0 | 17 | 0 | 11 | 0 | 0 | 144.3 / 127.7 / 107.2 | 68 | 50 | 51 |
| 2026-11-14T15:09 | HOLD-1 | 3 | 12 | 62 | 1.21 | 1 | 1 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 47 | 423,321 | 0 | 0 | 0 | 10 | 0 | 1 | 127.4 / 118.4 / 105.2 | 64 | 52 | 51 |
| 2026-11-14T15:10 | HOLD-1 | 3 | 12 | 12 | 1.01 | 0 | 0 | - | - | 0 | 0 / 0 | 12 / 12 | 0 / 0 | 11 | 467,649 | 0 | 0 | 0 | 11 | 0 | 0 | 106.2 / 104.5 / 101.5 | 10 | 10 | 2 |
| 2026-11-14T15:11 | HOLD-1 | 3 | 0 | 11 | 0.93 | 0 | 0 | - | - | 0 | 0 / 0 | 11 / 11 | 0 / 0 | 11 | 462,812 | 0 | 0 | 0 | 11 | 0 | 0 | 100.0 / 100.0 / 100.0 | 0 | 0 | 0 |
| 2026-11-14T15:12 | HOLD-1 | 3 | 1 | 1 | 0.08 | 0 | 0 | - | - | 0 | 0 / 0 | 1 / 1 | 0 / 0 | 1 | 42,025 | 0 | 0 | 0 | 1 | 0 | 0 | 100.0 / 100.0 / 100.0 | 1 | 0 | 1 |
| 2026-11-14T15:13 | HOLD-2 | 3 | 17 | 25 | 1.78 | 12 | 12 | - | - | 0 | 0 / 0 | 10 / 10 | 0 / 0 | 21 | 427,573 | 0 | 0 | 0 | 10 | 0 | 8 | 120.9 / 114.4 / 104.2 | 16 | 5 | 4 |
| 2026-11-14T15:14 | HOLD-2 | 3 | 3,951 | 3,290 | 15.69 | 185 | 184 | - | - | 3,756 | 0 / 0 | 10 / 10 | 0 / 0 | 280 | 42,250 | 0 | 261 | 0 | 1 | 0 | 8 | 432.6 / 184.2 / 114.5 | 4,173 | 4,484 | 4,484 |
| 2026-11-14T15:15 | HOLD-2 | 3 (entries skipped: over the read cap) | 11,924 | 4,580 | 22.70 | 259 | 259 | 1 | 8,332 | 8,539 | 0 / 0 | 9 / 9 | 0 / 0 | 282 | 42,393 | 0 | 0 | 0 | 0 | 0 | 0 | 420.8 / 183.5 / 114.4 | 13,117 | 12,657 | 12,177 |
| 2026-11-14T15:16 | HOLD-2 | 3 (entries skipped: over the read cap) | 20,727 | 4,937 | 25.50 | - | - | - | - | - | - / - | - / - | - / - | 256 | 84,444 | 0 | 0 | 0 | 0 | 0 | 0 | 403.4 / 182.3 / 114.3 | 21,586 | 21,514 | 21,037 |
| 2026-11-14T15:17 | HOLD-2 | 3 (entries skipped: over the read cap) | 22,982 | 5,266 | 26.81 | - | - | - | - | - | - / - | - / - | - / - | 281 | 41,883 | 0 | 0 | 0 | 0 | 0 | 0 | 399.8 / 182.1 / 114.3 | 23,542 | 23,790 | 24,047 |
| 2026-11-14T15:18 | HOLD-3 | 3 (entries skipped: over the read cap) | 33,069 | 5,479 | 26.81 | - | - | - | - | - | - / - | - / - | - / - | 257 | 83,856 | 0 | 0 | 0 | 0 | 0 | 0 | 400.2 / 182.1 / 114.3 | 37,164 | 36,826 | 36,776 |
| 2026-11-14T15:19 | HOLD-3 | 3 (entries skipped: over the read cap) | 95,586 | 5,567 | 27.78 | - | - | - | - | - | - / - | - / - | - / - | 281 | 41,846 | 0 | 0 | 0 | 0 | 0 | 0 | 401.2 / 182.2 / 114.3 | 99,830 | 99,141 | 99,141 |
| 2026-11-14T15:20 | HOLD-3 | 3 (entries skipped: over the read cap) | 161,354 | 5,603 | 28.05 | - | - | - | - | - | - / - | - / - | - / - | 306 | 262 | 0 | 0 | 0 | 0 | 0 | 0 | 400.7 / 182.2 / 114.3 | 164,632 | 163,879 | 164,241 |
| 2026-11-14T15:21 | HOLD-3 | 3 (entries skipped: over the read cap) | 218,658 | 5,345 | 27.42 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 397.6 / 181.9 / 114.3 | 221,249 | 220,622 | 221,287 |
| 2026-11-14T15:22 | HOLD-3 | 3 (entries skipped: over the read cap) | 279,570 | 5,294 | 26.21 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 396.3 / 181.8 / 114.3 | 283,825 | 283,177 | 283,172 |
| 2026-11-14T15:23 | HOLD-3 | 3 (entries skipped: over the read cap) | 326,948 | 5,293 | 26.50 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 396.6 / 181.9 / 114.3 | 341,157 | 341,110 | 341,246 |
| 2026-11-14T15:24 | HOLD-3 | 3 (entries skipped: over the read cap) | 355,551 | 5,288 | 27.74 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 396.5 / 181.8 / 114.3 | 397,275 | 396,936 | 396,017 |
| 2026-11-14T15:25 | HOLD-3 | 3 (entries skipped: over the read cap) | 389,986 | 4,976 | 27.92 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 388.7 / 181.3 / 114.2 | 455,276 | 455,212 | 454,688 |
| 2026-11-14T15:26 | HOLD-4 | 3 (entries skipped: over the read cap) | 444,506 | 4,595 | 27.18 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 379.3 / 180.6 / 114.2 | 525,856 | 526,000 | 525,913 |
| 2026-11-14T15:27 | HOLD-4 | 3 (entries skipped: over the read cap) | 546,949 | 4,556 | 26.27 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 377.9 / 180.4 / 114.2 | 653,291 | 652,225 | 652,008 |
| 2026-11-14T15:28 | RETURN | 3 (entries skipped: over the read cap) | 608,191 | 4,550 | 27.40 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 379.4 / 180.6 / 114.2 | 722,868 | 722,636 | 722,636 |
| 2026-11-14T15:29 | RETURN | 3 (entries skipped: over the read cap) | 554,792 | 4,542 | 27.45 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 378.5 / 180.5 / 114.2 | 651,641 | 651,872 | 651,870 |
| 2026-11-14T15:30 | RETURN | 3 (entries skipped: over the read cap) | 484,725 | 4,511 | 26.61 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 377.0 / 180.4 / 114.1 | 570,904 | 570,615 | 570,841 |
| 2026-11-14T15:31 | RETURN | 3 (entries skipped: over the read cap) | 423,457 | 4,495 | 26.94 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 376.7 / 180.3 / 114.1 | 499,476 | 499,106 | 499,448 |
| 2026-11-14T15:32 | RETURN | 3 (entries skipped: over the read cap) | 366,953 | 4,458 | 26.30 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 376.2 / 180.3 / 114.1 | 434,119 | 434,242 | 434,457 |
| 2026-11-14T15:33 | tail | 3 (entries skipped: over the read cap) | 289,310 | 4,340 | 25.15 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 370.2 / 179.8 / 114.1 | 337,374 | 337,188 | 336,960 |
| 2026-11-14T15:34 | tail | 2 (entries skipped: over the read cap) | 206,366 | 3,825 | 23.56 | - | - | - | - | - | - / - | - / - | - / - | - | - | - | - | - | - | - | - | 351.0 / 178.0 / 113.9 | 241,264 | 241,264 | 241,022 |
| 2026-11-14T15:35 | tail | 3 (entries skipped: over the read cap) | 95,749 | 2,552 | 10.43 | - | - | - | - | - | - / - | - / - | - / - | 307 | 131 | 0 | 0 | 0 | 0 | 0 | 0 | 306.3 / 172.9 / 113.5 | 109,360 | 109,359 | 109,360 |
| 2026-11-14T15:36 | tail | 3 (entries skipped: over the read cap) | 2,232 | 155 | 1.50 | 1 | 1 | - | - | 2,231 | 0 / 0 | 0 / 0 | 0 / 0 | 154 | 50 | 0 | 10 | 0 | 0 | 0 | 0 | 100.0 / 100.0 / 100.0 | 2,579 | 2,579 | 2,579 |
| 2026-11-14T15:37 | tail | 3 | 0 | 0 | 0.00 | 0 | 0 | - | - | 0 | 0 / 0 | 0 / 0 | 0 / 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 100.0 / 100.0 / 100.0 | 0 | 0 | 0 |
| 2026-11-14T15:38 | tail | 3 | 0 | 0 | 0.00 | 0 | 0 | - | - | 0 | 0 / 0 | 0 / 0 | 0 / 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 100.0 / 100.0 / 100.0 | 0 | 0 | 0 |
