> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is a pre-run. Pre-run 35.** It is not the Wednesday run. It is not the Tuesday run. It is not pre-run 1 to 34, and it does not edit their repos. A read does not start a runner.

# tn10-storm-2026-11-11-prerun-35

**Pre-run 35: the same fee as pre-run 34, run again so the 3,040 step and RETURN are actually submitted.** The neuron stays [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). This repo does not edit that repo.

> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What these pages report is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

| Field | Value |
|---|---|
| Target | The three lines stay up while simple payments are offered at 1,013, then 2,027, then 3,040, then one minute at 4,053, then 1,013 again. At least one hop, one mint and one guest carrier land in the open window. The run names the first line that falls behind |
| The change | Same knob as pre-run 34: floor families 1–12 pay 200 sompi per gram. Payments stay at 150. What changes is our sender, not the fee. Pre-run 34's payment pool dropped coins it had not spent, and the run stopped before RETURN was scored |
| Met or not met | **met** on the combined three-part target (23,781 floor hops, 120 mints, 8 of 8 guest carriers, window 14:53:11Z–15:39:04Z). HOLD-1 did not meet on payment submit-OK. That miss is our sender's coin line, and those minutes are not the 1,013 reading. HOLD-2 met. At 3,040, submit-OK stayed near the offer and same-minute inclusion of our payments is the payment line behind (118,500–126,056). HOLD-4 is an observation (242,003 of 243,180). RETURN met on submit-OK (60,433–61,292). Inclusion in those minutes stayed 126,402–135,121 and floor hops stayed 365–384, against quiet 957 and 917. A payment sender logged usable 17,999 at 15:33:12Z. The runner stopped at 15:33:25Z on return-closed |
| Retry count | 0. The next attempt is a new repo. This one is not resumed |
| Core tags | 1. Rotation log: 39 samples, 0 still listed in every sample. The published 1,520 is the sum of those checks. Each sample checked at most 40 ids |
| Status | done (HOLD-1 not met). Closed from the published step files |

Plan, lock, and the prediction are in [plan/PLAN.md](plan/PLAN.md), [locks/LOCKED.md](locks/LOCKED.md), and [plan/PREDICTIONS.md](plan/PREDICTIONS.md). Written before any submit.
