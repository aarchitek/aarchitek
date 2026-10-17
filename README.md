# Architekture

**Data tooling studio.** I build web scrapers and data pipelines that hold up in production — and I ship them as products people pay to use.

**12 production actors live on the [Apify Store](https://apify.com/architekture)** — grocery price intelligence across NZ / AU / UK, people-search exports, job market data, transcript pipelines — each one recon-verified, billing-audited, and heartbeat-monitored. Used via API, MCP, and scheduled runs by data teams and AI agents.

---

### Flagship work

| Actor | What it does | Proof |
|---|---|---|
| [New World NZ Scraper](https://apify.com/architekture/new-world-nz-scraper) | Store-by-store grocery prices across ~149 NZ stores, Clubcard pricing, barcode + nutrition detail mode | Zero-supply category created from a recorded gap; store price variation proven with 4-store × 39-product evidence before a line of marketing copy was written |
| [Tesco UK Scraper](https://apify.com/architekture/tesco-uk-scraper) | Tesco prices with resolved Clubcard & multibuy strings, GTIN barcodes, full category crawls | Akamai-fronted target solved with session warm-up + embedded-state parsing; validated runs published in README |
| [Pak'nSave NZ Scraper](https://apify.com/architekture/paknsave-nz-scraper) | Foodstuffs NZ prices, specials, store context | Cloudflare clearance path reversed and replayed through the site's own edge API |

Actor source is intentionally private — buyers pay for the hosted, monitored product, not a repo to self-host.

---

### How I build

1. **Recon before code.** Every target gets a bounded recon run with explicit kill criteria (login walls, anti-bot ceilings, demand re-verification). Builds that fail the recon get parked, not shipped.
2. **Evidence-driven READMEs.** Performance claims in my docs are measured on validation runs with run IDs, never estimated.
3. **Billing you can audit.** Pay-per-event actors charge only for delivered rows; failed requests and empty runs cost nothing. Charge counts are checked against delivered rows after every deploy.
4. **Monitored in production.** Canary runs with two-consecutive-failure alerting; a double-charge crash window found by review was patched across the catalog before it ever billed a customer wrong.

### Stack

Python · Playwright · Apify platform (PPE billing, canaries, GitHub-connected builds) · REST API design · data normalization · NZ/AU/UK retail platforms (Foodstuffs, Woolworths, Tesco/Akamai, Coles)

### Also

Web developer with a BFA in graphic design — the designer-turned-builder combination behind scrapers whose deliverables arrive clean and documented, not as terminal dumps.

**Hire me for scraping, data pipelines, and API work:** north@architek.earth · [Apify Store profile](https://apify.com/architekture)
