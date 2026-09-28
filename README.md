# Nostradamus Intellect — the public record

**Every sealed forecast, as data, under version control.** A mirror of the public record of
[nostradamusintellect.com](https://nostradamusintellect.com): the sixteen hash-sealed ledger entries, the sealed
statements of public figures, the live projections, the engine's model card, and the OpenTimestamps manifest.

Why it is here as well as on the site: **a second, independent witness.** Every commit to this repository is dated by
GitHub, so each batch of seals has a timestamp nobody at Nostradamus Intellect controls — in addition to the Bitcoin
anchor. If a number on the site ever differed from the one committed here, anyone could see it.

> Status: 0 sealed cards graded. The first public verdict is **2027-02-28**. On the sixteen ledger seals a perfectly
> calibrated forecaster would still expect about five misses (see `record.json` → `ledger_arithmetic`).

## Files

| File | What it holds |
|---|---|
| [`record.json`](record.json) | The whole record in summary, the resolution calendar, the ledger arithmetic, the contract — as served at `/engine/record.json` |
| [`ledger-seals.json`](ledger-seals.json) | The 16 graded ledger seals, whole: probability, dates, resolution criterion, the `sealed` fields, SHA-256, ledger root, timestamp-proof URL |
| [`sealed-statements.json`](sealed-statements.json) | Public figures' dated claims, quoted exactly with receipts, sealed and graded on the same terms |
| [`projections.json`](projections.json) | The live projections (narrative windows, not scored) |
| [`model-card.json`](model-card.json) | The engine's published constants, formulas and versions |
| [`checksums.json`](checksums.json) | Checksums of the engine artefacts |
| [`ots-manifest.json`](ots-manifest.json) | The OpenTimestamps manifest: every seal's SHA-256 and the ledger root. The `.ots` proofs are at `https://nostradamusintellect.com/ots/<id>.ots` |

## Verify it

```bash
npx -y nostradamus-intellect verify all
```

or with [`verify.mjs`](https://github.com/NostradamusIntellect/nostradamus-intellect-protocol/blob/main/verify.mjs) from
the protocol repository. A seal's hash is SHA-256 of `JSON.stringify(sealed)`; the ledger root is SHA-256 of the list
of sealed objects in ledger order. Both are in `ledger-seals.json`.

## How it is kept

A snapshot is committed whenever the record changes: a new seal batch, a new sealed statement, a verdict. A sealed
probability is never rewritten — so in this history, a sealed number only ever appears once.

## Work with us

Built in the open by one founder. We are looking for people:

- **Researchers and forecasters:** use the record, reproduce the arithmetic, critique the criteria. Seal your own numbers
  through the [Observer Protocol](https://nostradamusintellect.com/observers).
- **Builders:** the [`ni` CLI and MCP server](https://github.com/NostradamusIntellect/nostradamus-intellect-mcp) —
  [where we need help](https://github.com/NostradamusIntellect/nostradamus-intellect-mcp/blob/main/CONTRIBUTING.md).
  We are open to people who want to join the founding team.
- **Newsrooms, platforms, institutions and AI-evaluation teams:** the record as data, commissioned questions graded in
  public, calibration training.
- **Investors, donors and supporters:** the record is free to read forever, with no ads — write to us if you want to
  back that.
- Everyone: [nostradamusintellect@proton.me](mailto:nostradamusintellect@proton.me) ·
  [X @Nostradamusmind](https://x.com/Nostradamusmind)

Nothing can be bought: partnerships, sponsorship, donations and investment never change a probability, a date or a
criterion.

## Licence

The record is published under CC BY 4.0. Quote a card with its code, the probability, the resolution date and the URL.

<sub>Not financial, medical, legal or safety advice. Forward-looking content is probabilistic simulation. Nothing here is
a reading of Michel de Nostredame.</sub>
