> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine. Pre-run 35. Not Wednesday. Not Tuesday. Not pre-runs 1 to 34.

# Targets

**Question.** Pre-run 34 asked this with floor hops at 200 sompi per gram and payments at 150. On our desk, at 1,013 payments a second the floor stayed at 709–778 a minute (quiet 796 and 833). At 2,027 the floor fell to 315–381 while payment submit-OK stayed near the offer. The 3,040 step did not submit the offer: our payment pool fell to 7–19 coins and submit-OK sat near 7,000 a minute, while 5,408 payment coins were still free. RETURN was not scored. The runner stopped because usable funds on the family key went under 18,000 tKAS. This run asks the same fee question again, with the sender keeping coins it did not spend, so the 3,040 step and RETURN are readings of the offer.

**Target.** Between `PRE-RUN-OPEN` and the end of RETURN, at least one covenant hop, one KCC-20 mint and one tic-tac-toe carrier are accepted on our desk node. Each scored payment step is three clean minutes of submit-OK within 10 percent, or `NOT MET` after one repair. The 4,053 minute is an observation. The run names the first component that falls behind. Retry count 0.

## The one knob, written before the arm

**The floor-family fee stays 200.** Families 1–12 pay 200 sompi per gram of node mass, as in pre-run 34. The payment offer is unchanged: 1,013, then 2,027, then 3,040, then one minute at 4,053, then 1,013 again, at 150 sompi per gram, to the kept public TN10 nodes. The families, the mint line and the guest stay on the desk node.

What stays put, so it is not a second knob:

- Twelve covenant families, 1.2 hops a second, one sender, one builder.
- The KCC-20 family stays at 100.
- No heavy lane. The desk node is not restarted. We do not stop it for this send.

Tool fixes, recorded here, not a second network knob:

- A payment submit that is not known to have spent the coin puts the coin back. Pre-run 34 classed those submits as other and dropped the coin. The repair then dealt only the handed-off pool. This run's repair also deals free coins the handoff does not already hold.
- The mint accept cap is 120 and the try cap passed to the process is 140. Pre-run 34's process accepted 90 and stopped because the try cap was 90.
- One tic-tac-toe match. A carrier counts only when its id is among the desk node's accepted ids.
- The family-key budget uses 500 tKAS a minute for the planned minutes. Pre-run 34's check used 760 for 24 minutes and the families ran about 35. The large drop that time was coins falling under 3 tKAS, which usable does not count. Those coins are packed into large coins before the hashes. The payment sender still stops every sender when usable funds fall under 18,000 tKAS.

Two recorded facts that are not a second knob:

- The Mini is not reachable from this desk. This run has one counter, the desk node. [logs/MINI-NOT-REACHABLE.md](../logs/MINI-NOT-REACHABLE.md) is on origin before the arm. We do not write a Mini-armed file.
- Keys 1 and 2 are not used. One distinct key per family. The payment pile is a different key and is not split for this run.

## What we are checking in our own earlier pages

- Pre-run 33, hops at 100: payment submit-OK stayed near the offer through 3,040, and same-minute inclusion plateaued near 123,000–133,000 a minute there. Floor hops were about 60–160 a minute once the payments were up.
- Pre-run 34, hops at 200: the 1,013 and 2,027 minutes are the fee reading we trust. The 3,040 payment numbers are our pool. We do not read either run as a correction of finding 1.

## Order

1. Disk floor written. Desk free space at 2026-11-14T14:41:04Z: 333.19 GB. Abort under 150 GB. The desk node is not restarted.
2. Free check, read-only, committed before any submit. Names that do not answer are logged and dropped. A raw address found by a scan is not a send target.
3. Family-key dust under 3 tKAS packed into large coins, logged, before the hashes. Family top-up only if a key has no coin of at least 15 tKAS. The new coins are left until their block DAA is behind the tip. The payment pile is reused if it still has at least 4,500 coins over 10 tKAS.
4. Hashes first. Thirteen rows in [hashes/SIXTEEN.md](../hashes/README.md) (the file keeps that name). The offline check builds them and does not submit.
5. `PRE-RUN-OPEN`, then genesis of the thirteen covenants, then the lines, then the ladder.

| Order | File | Payments | What else runs |
|---:|---|---|---|
| 1 | BASE | none | families, mint line, one guest match. 2 whole minutes. Not scored |
| 2 | HOLD-1 | 1,013 tx/s | the three lines stay up |
| 3 | HOLD-2 | 2,027 tx/s | the same |
| 4 | HOLD-3 | 3,040 tx/s | the same |
| 5 | HOLD-4 | 4,053 tx/s | one pinned minute. Not scored |
| 6 | RETURN | 1,013 tx/s | the same, to see whether the lines come back |
| 7 | tail | stopped | the counter reads on for 5 minutes |

The knob is the floor fee, and it is the same fee as pre-run 34. It does not change during the run. One repair per scored step, and that repair keeps free coins the handoff dropped.

## Cohorts

| Cohort | Families | Rate, sompi/gram of node mass | Where |
|---|---|---:|---|
| floor | 1–12 | 200 | desk node |
| kcc | 13 | 100 | desk node, the mint line |
| payments | — | 150 sompi/gram, on the payment's own mass | kept public TN10 nodes |

Finding 1 is still the capacity line we are using for the offer sizes: about 304–308 simple payments in a full block, about 3,040–3,080 a second at 10 blocks a second. 1,013, 2,027, 3,040 and 4,053 are one third, two thirds, three thirds and four thirds of the low edge. We may be dividing it wrong. The count files will say what the node did.
