> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Lock (pre-run 35)

Locked before the first submit.

- Network: Testnet-10. The desk node is not restarted and it is not stopped.
- One knob, the same one as pre-run 34: floor families 1–12 pay 200 sompi per gram of node mass. Payments stay at 150, offered at 1,013, then 2,027, then 3,040, then one minute at 4,053, then 1,013. Those payments go to the kept public TN10 nodes.
- Families stay at 12, 1.2 hops a second, on the desk node. The KCC-20 family stays at 100. The mint line stays one at a time. The accept cap is 120 and the try cap passed to the process is 140. One guest match, on the desk node.
- No heavy lane.
- One counter: the desk node. The Mini is not reachable. No Mini-armed file.
- Keys 1 and 2 are not used. One distinct key per family. The payment sender stops on usable funds under 18,000 tKAS, not on a coin count. A submit that is not known to have spent the coin puts the coin back.
- Disk line: abort if the desk is under 150 GB free. It was 333.19 GB at 2026-11-14T14:41:04Z.
- A miss is a retry with the fix written first. This page is not rewritten to match the result.
