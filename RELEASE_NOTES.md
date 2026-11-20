## Energy API endpoints, snapshot 15 Nov 2026

- 72,606 endpoints passed a keyless data call, tested 14–15 Nov 2026 (IST)
- 5,304 services · 251 country codes · 51,239 keyless JSON rows

### Download

- `Energy_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz`: the full list, 72,606 rows, 2.5 MB gzipped (20.6 MB as CSV), SHA-256 `566d691b6595b39f16d12dcdf2e0492f844ee0a159aae64e467aa429ca593d3f`
- `SHA256SUMS.txt`: the checksum of that file

Check the download in the folder that holds both files:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
shasum -a 256 -c SHA256SUMS.txt      # macOS
certutil -hashfile Energy_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz SHA256   # Windows: compare with SHA256SUMS.txt
```

Then `gunzip Energy_API_Endpoints_AgentPopulation_Snapshot_2026-11-15.csv.gz` and pass the CSV path to the examples or to `node tools/test-endpoints.mjs`. The repository itself holds a 1,000-row sample and the services list.

### What's in it for you

- 🤖 Agent tools: 418 · Wrap one URL pattern as a get_power_mix or get_power_price tool: pass a country, bidding zone or region, return generation by source, the price or the carbon intensity with its timestamp; add a timeout.
- 📱 App features: 9,067 · Show power plants, solar and wind sites, substations, chargers or fuel stations near a place on a map; each layer query returns features with names, capacities or fuel types.
- 🧠 Grounding and data pipelines: 23,852 · Load energy balances, generation, consumption and price series on a schedule into your own store, so answers about a country's energy cite a dated source.
- 🧪 Evals and testing: 72,606 · Run your energy tool against a fixed set of URLs across formats; check that units (MW, MWh, price per MWh, gCO2/kWh), timestamps and country codes parse, and keep last_tested as the baseline for your own re-tests.

### Changes

- First release
- Left out: 635 rows whose URL carried a credential-looking parameter or a login.
- Left out: 402 ArcGIS Survey123 layers (they can hold people's form answers).
- Left out: 3 layers marked editable in the title (they can hold entries that people added).
- Left out: 50 ArcGIS layers that keep a form's default service name (they can hold people's form answers).
- Left out: 263 ArcGIS class or coursework layers (lab, assignment, exam, quiz, lesson, exercise, tutorial and final-project layers, copies of class layers, layers named for a person or a person's home, and layers whose name ends in a person's name or holds a student number).
- Left out: 7 ArcGIS layers that hold reports, comments, submissions or form responses sent in by the public.
- Left out: 580 rows whose title is about COVID-19 or vaccination (map layers filed under energy, not about energy).
- Overlap: 2,642 of these URLs are also in 190k-weather-apis-for-agents.
- Overlap: 132 of these URLs are also in 270k-transit-apis-for-agents.
- Overlap: 195 of these URLs are also in 270k-water-apis-for-agents.
- Overlap: 1,446 of these URLs are also in 130k-finance-economy-apis-for-agents.
- Overlap: 63 of these URLs are also in 130k-india-apis-for-agents.
- Overlap: 66 of these URLs are also in 86k-oceans-apis-for-agents.
- Overlap: 117 of these URLs are also in 20k-air-quality-apis-for-agents.
- Overlap: 51,239 of these URLs are also in 2.5m-agent-ready-apis.
- Overlap: 1 of these URLs is also in 6.5k-wildfire-apis-for-agents.
- Overlap: 15 of these URLs are also in 24k-traffic-apis-for-agents.
- Overlap: 1 of these URLs is also in 10k-earthquake-apis-for-agents.

On the date in last_tested (IST), one GET to the URL, sent with no key, returned HTTP 2xx and a non-empty data body. HTML pages and empty results did not pass. The format column records what came back. This is a test result for that date, not a promise that the URL answers today. Licences, terms, rate limits, accuracy and freshness were not reviewed. Endpoints are URLs, not separate APIs; many share one service. This pack was tested 14–15 Nov 2026; snapshot 15 Nov 2026.

For the latest tested endpoints, search agentpopulation.com/apis. This pack is a snapshot from 15 Nov 2026.

Credit: Energy API endpoints by AgentPopulation (https://agentpopulation.com), CC BY 4.0, snapshot 15 Nov 2026.

Compiled by [AgentPopulation](https://agentpopulation.com) with [AP Desk](https://github.com/agentpopulation/apdesk) · corrections: [@agentpopulation](https://x.com/agentpopulation) on X
