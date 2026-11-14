> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.

# Target, pre-run 35 (desk's own read)

Open window: from logs/PRE-RUN-OPEN.md on origin (2026-11-14T14:53:11Z) to this file (2026-11-14T15:39:04Z). Accepted = the desk node's own read (coordinator accepting-header time for the family hops; next minter seen for the mints).

| Line | Accepted on the desk node in the window | Met |
|---|---:|---|
| Covenant hop (families 1–12, floor) | 23,781 | met |
| KCC-20 mint (family 13, one at a time, cap 30) | 120 | met |
| Tic-tac-toe guest carrier (one match, one carrier at a time) | 8 of 8 logged (8 submit-OK per ttflow) | met |

The combined three-part target is **met** in this run (twelve covenant families, the KCC-20 mint line and the tic-tac-toe guest, held up while simple payments step through 1,013, 2,027, 3,040 and one minute at 4,053 tx/s; which component fell behind first is in counts/chain/FIRST-BEHIND.md).

Guest carriers counted only when the id ttflow logged is among the desk node's own accepted transaction ids (its virtual chain since the guest started); ttflow's "accepted" alone means the node took the submit. Steps accepted: m1 Step 1 (Init), m1 Step 2 (Deposit Player A), m1 Step 3 (Deposit Player B), m1 Step 4 (CreateGame), m1 Step 5 (JoinGame), m1 Step 6 (Turn Player A), m1 Step 7 (Turn Player B), m1 Step 8 (Withdraw). Steps logged but not seen accepted: -. Gate: gate ok. DA read at RETURN: open 0; playing 0; finished 1.

Issue #1146 rotation sample (rot24.mjs, our own accepted ids, 60 s or more after acceptance, asked one at a time on the same node): 39 samples, 1520 ids checked, 0 still listed in the mempool.
