# Method, pre-run 35

> This is our own Kaspa Testnet-10 testing. What follows is what we observed in this run, on our own nodes; it is not a claim of how TN10 or Kaspa behave in general.

> Counts only. Desk side. Submit-OK is the desk sender log; included is the desk counter's read of what the desk's private TN10 node accepted on chain. Mini's files are a second read.

Steps (our own heavy lane on one absolute timeline): BASE = mix 2 min; HOLD-1 = mix 3 min; HOLD-2 = mix 3 min; HOLD-3 = mix 3 min; then N0-drain through the HOLD-4 minute and RETURN 3 min, then a 5-minute counter tail.

Our heavy lane's totals were not read.

Accepted hops per cohort, as the desk's coordinator read them: floor 23,781, kcc 120.

Per step (all OBSERVATION, families plus our own heavy lane, no payment of ours):

- BASE: OBSERVATION, submit-OK 0 / 0; our payments included 0 / 0; hops included floor/kcc 1874/8; counter minutes not kept-pace 0 of 2.
- HOLD-1: NOT MET, submit-OK 34,681 / 34,082 / 11,293 / 6,407 / 6,328 / 6,284 / 9,322 / 9,320 / 0 / 0 / 0 / 0; our payments included 34,335 / 33,995 / 11,427 / 6,362 / 6,362 / 6,328 / 9,430 / 9,318 / 1,147 / 0 / 0 / 0; hops included floor/kcc 10900/46; counter minutes not kept-pace 0 of 12.
- HOLD-2: MET on submit-OK, submit-OK 122,618 / 120,916 / 121,518 / 121,479; our payments included 114,950 / 112,803 / 118,474 / 116,378; hops included floor/kcc 1467/10; counter minutes not kept-pace 0 of 4.
- HOLD-3: MET on submit-OK, submit-OK 182,242 / 181,475 / 183,542 / 181,944; our payments included 118,500 / 124,352 / 122,557 / 126,056; hops included floor/kcc 1332/10; counter minutes not kept-pace 0 of 4.
- HOLD-4: OBSERVATION, submit-OK 242,003; our payments included 124,792; hops included floor/kcc 340/1; counter minutes not kept-pace 0 of 1.
- RETURN: MET on submit-OK, submit-OK 61,292 / 60,433 / 60,532 / 61,184; our payments included 132,285 / 135,121 / 132,780 / 126,402; hops included floor/kcc 1494/11; counter minutes not kept-pace 0 of 4.

Decent on the desk side: every step file reached origin.

## Selection rule, read before the run

The desk node and the kept public kaspads answered serverVersion 2.1.0 at the preflight. In rusty-kaspa tag v2.1.0 (commit 01b532e8b553523216471682649693af92f0fd16), `mining/src/mempool/model/frontier.rs` `build_selector` takes every ready transaction best-first while the ready set's mass fits one block, and otherwise samples at random with weight (fee/mass)^3 (`ALPHA = 3` in `mining/src/mempool/model/frontier/selectors.rs`, weight in `mining/src/mempool/model/frontier/feerate_key.rs`): `sample_inplace` above four blocks' mass, `MutatingTreeSelector` between one and four. Only a transaction with no parent in the mempool is in the ready set (`mining/src/mempool/model/transactions_pool.rs`), so a chained hop is not a candidate until its parent is out of the mempool. Against an outside stream at 100, the weights are 1.00 (100), 3.38 (150), 27.0 (300) and 91.1 (450), per unit of mass. In the duel our two lanes move between 100 and 2,000 (logs/duel.log, published after the run). A higher fee raises the odds; it does not buy a place in a queue. This is the source's rule, read from the code; the run does not see a miner's template.

Hop rates per hop, one builder: floor (families 1–12) 200 sompi/gram on the desk's private node, kcc (families 13–13) 100 sompi/gram on the desk's private node. Payments 150. The funding coins were not one size, so the fee is not called the whole cause. Every tier was read and submitted on the desk's private TN10 node, which also ran the counter. No payment sender was started; 3 unique public kaspads were read for sync only.

## Misses

- HOLD-1 NOT MET.


## Fixes

- 2026-11-14T15:06:12Z HOLD-1: restarted the payment senders with their pools handed off and dealt again (one try for this reason; 9 of 9 running again after the restart, pools 601 / 601 / 601 / 601 / 601 / 601 / 601 / 601 / 600 coins, fair; deal 5408 of a 5408-coin pile, handoff plus free set, capped at the pile).

## On origin

- counts/desk/BASE.md: 2026-11-14T14:58:22Z
- counts/desk/HOLD-1.md: 2026-11-14T15:13:22Z
- counts/desk/HOLD-2.md: 2026-11-14T15:18:22Z
- counts/desk/HOLD-3.md: 2026-11-14T15:23:22Z
- counts/desk/HOLD-4.md: 2026-11-14T15:28:22Z
- counts/desk/RETURN.md: 2026-11-14T15:33:22Z
- counts/chain/TIMELINE.md: 2026-11-14T15:38:59Z
- counts/chain/MEMPOOL.md: 2026-11-14T15:39:02Z
