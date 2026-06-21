# FallSeed Mortgage Broker

> **A Progressive Web App (PWA) seed for UK Mortgage firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-mortgage/

## What this is

`fallseed-mortgage` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Mortgage wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

Mortgage broking · intermediary (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`fallmortgage`](https://sjgant80-hub.github.io/fallmortgage/) | Client register · application tracker · ESIS · affordability records · KFI / ESIS storage · 12-pt compliance · proc fee log |
| onboard | [`fallmortgageonboard`](https://sjgant80-hub.github.io/fallmortgageonboard/) | Client onboarding · fact-find · objectives · vulnerability check · CDD / KYC · source of deposit · consent capture |
| paper | [`fallmortgagepaper`](https://sjgant80-hub.github.io/fallmortgagepaper/) | Suitability letter · IDD / Initial Disclosure · ESIS · TOBA · Mortgage Promise pack · Consumer Duty fair-value templates |
| practice | [`fallmortgagepractice`](https://sjgant80-hub.github.io/fallmortgagepractice/) | Pipeline · case tracker · file reviews · proc fee reconciliation · CPD log · vulnerable-customer log · complaints register |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-mortgage-v2`) on your device
- **BroadcastChannel mesh** — `fall-mortgage` for cross-tool sync; `fall-signal` for global hello
- **P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1097**, spine-clean mod 127. Mesh channel **`fall-mortgage`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.
