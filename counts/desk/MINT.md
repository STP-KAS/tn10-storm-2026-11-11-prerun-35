> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value. Counts only. No id, txid or address in this file.

# KCC-20 mint line, pre-run 35

One fresh KCC-20 public-mint launch (family 13 in the hash file; a launch name not used before). One mint at a time: the line builds one mint at the floor rate on the node's own mass, submits it to the desk's private node, and waits until the node shows the next minter (the mint accepted on the virtual chain) before the next one, then 15 s. Cap 30 accepted mints. A reject is kept with the node's text; the fee is not raised.

- Mints submitted OK: 120; accepted (next minter seen on the desk node): 120; rejected: 0; accept timeouts (120 s): 0; build failures: 0.
- Accept time, submit to next minter seen: min 507 ms, median 1027 ms, max 29276 ms.
- Node rate (fee / node mass): 100–100.31; node mass 40381–42086; fees 4.9362 tKAS in all.
- Accepted mints by step: BASE 12, HOLD-1 56, HOLD-2 13, HOLD-3 19, HOLD-4 4, RETURN 14, tail 2.
- End state: cap.

No reject text.

