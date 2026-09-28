# Asset sources

- `assets/options-cost-evidence.svg`: data graphic calculated directly from `yz3639-gif/cushing-wti-research`, [`docs/options-desk/demo-data.json`](https://github.com/yz3639-gif/cushing-wti-research/blob/12309a587094e7e98afc701a37f62a826b969d60/docs/options-desk/demo-data.json). Source SHA-256: `37b218d073690f565f5b8a6f858d2f726ad57efd847f4b2a36376a9d215a5b99`. Exact case: `snapshot_index=0`, `cso_shift=0`, `vanilla_shift_pp=0`, `bundle_id=bundle-4409fb4f564ec2ec9b19`. This is the desk's first displayed snapshot at market volatility, using all 100 original one-day scenarios. For each original strategy and cost multiplier `k ∈ {1,2,4}`, calculate `max(0, -min_s(gross_pnl[s] - k * recorded_ticket_cost))`; quantities and gross P&L stay fixed. No hedge has zero ticket cost. Values are displayed rounded to whole USD. This is a numeric evidence chart, not a screenshot or a forecast.
- `assets/options-desk.jpg`: retained archival interface image, no longer displayed by the site, from `yz3639-gif/cushing-wti-research`, `docs/options-desk/preview.jpg` at `ed9679ad61d242ef3fcd41b0f7c20905baec975a`. Synthetic engineering inputs; original source pixels and historical branding retained.
- `assets/nvda-evidence.png`: `yz3639-gif/Nvda_Quant_Model`, `docs/assets/research_evidence.png` at `a998a85664d1429a3ba98163602f3ebcfb886d50`. Two distinct historical experiments; no live performance claim.
- `assets/cushing-evidence.png`: `yz3639-gif/cushing-wti-research`, `outputs/figures/descriptive_relationship.png` at `ed9679ad61d242ef3fcd41b0f7c20905baec975a`. Historical public-data research.
- `assets/yz.svg`: simple YZ site monogram.

Research figures retain their source pixels. Generated charts must name their source data, exact case and calculation. Interface captures must remain attributable to an actual browser capture.

## Options chart source values

| Fixed strategy | Recorded cost, USD | 1× worst loss, USD | 2× worst loss, USD | 4× worst loss, USD |
|---|---:|---:|---:|---:|
| No hedge | 0 | 22811.528576073 | 22811.528576073 | 22811.528576073 |
| Futures only | 112.500000000 | 8680.959610945 | 8793.459610945 | 9018.459610945 |
| Futures + options | 823.750000000 | 7716.534776595 | 8540.284776595 | 10187.784776595 |

Worst loss is distinct from the engine constraint `max_s(abs(gross_pnl[s])) + scaled_cost <= risk_limit`. The figure reports losses only; Risk Lab displays both measures and recalculates constraint status.
