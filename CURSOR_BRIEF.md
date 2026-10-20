# Cursor Brief — ewsol.au Tasmania Rebuild

**Repo:** `PhoenixRisen2468/ewsol.au` (GitHub Pages → `ewsol.au`)  
**Stack:** static HTML/CSS/JS only. No React, no framework migration.  
**Working copy:** prefer the deploy folder already used for pushes (`Engineered Water Soluton WWW/.deploy-tmp`), then `git push origin main`.

---

## Goal (one line)

Make ewsol.au read like a bloke from up the road who knows water inside out — not a Sydney consultancy pitch deck.

A Midlands farmer, a TasWater PM, and a Hydro Tas contractor should all land and think: *yeah, this fella can sort it.*

---

## Truth table (do not invent)

| Item | Current / confirmed |
|------|---------------------|
| Phone | `0475 212 468` (`tel:+61475212468`) — confirm it still rings Mitchell |
| Email | `mitchell@ewsol.au` (plain `mailto:`, no Cloudflare obfuscation in source) |
| Hobart | 85 Murray Street, Hobart TAS 7000 — if not a staffed office, label **by appointment** |
| Launceston | 63 St John Street, Launceston TAS 7250 — same rule |
| Mail | PO Box 76, Kings Meadows TAS 7249 |
| Profile photo | `mitchell-jacques.jpg` (cache-bust query OK) |
| Formerly | Meyjor Industries Pty Ltd · Est. 2011 — reconcile with bio “Meyjor 2012–2023” |
| Clients (real, mainland track record) | Urban Utilities, Sydney Water, Seqwater, Thiess, John Holland, Abergeldie, BMA — logos only with written OK |
| Clients (do **not** invent) | TasWater, Hydro Tasmania, “Tasmania Growers”, “Farm Irrigation” |

If TasWater / Hydro work is real (direct or as sub), list with a one-line project note. Otherwise use the **Built for Tassie infrastructure** framing below — never fake the client strip.

---

## Fix first (credibility — before polish)

Do these before any visual redesign:

1. **Delete “Sarah Montana — Client”.** Template filler. Real quote (name + farm/company + town) or remove the section.
2. **Strip fake client cells** (“Tasmania Growers”, “Farm Irrigation”). Categories ≠ clients.
3. **No TasWater / Hydro logos or client claims** unless paid work is real (ACL s18 + logo permission).
4. **Reconcile dates** (Est. 2011 vs Meyjor 2012–2023), phone, and address labelling.
5. **Merge duplicate services** — “Our Services” + “Specialist Services” are the same idea twice. Contact must be last, not mid-page.

---

## Voice

- Short sentences. First person where it fits (“I’ll come out and have a look”).
- Plain words: pump, dam, pivot, blocked nozzles, power bill, shed.
- **Ban:** solutions-driven, seamless, stakeholder, end-to-end, best-in-class, transformed our approach, exceeded expectations.
- Dry / lightly cheeky OK. Not try-hard bogan. Honest tradie quote, not a beer ad.
- “Tassie” in casual copy; “Tasmania” in headings / meta.
- Every section answers one of: what do you do · where do you go · who turns up · how do I start · how do I ring you.

### Hero (adapt)

- **H1:** Farm water that keeps running.  
  *(alts: “Water work, done properly.” / “When the pivot stops, ring me.”)*
- **Sub:** Pivots, pumps, dams and filtration across Tasmania. Thirty-odd years in water — mines, councils, big city utilities — now working Tassie paddocks and infrastructure. You deal with me, not a call centre.
- **Buttons:** Ring Mitchell (`tel:`) primary · What I do (anchor)

---

## Target `index.html` structure

1. **Hero** — real photo (pivot / pump shed / Mitchell on site). Sticky “Ring Mitchell” on mobile. No stock skyline.
2. **What I do** — 4–6 plain cards, **no emoji icons**:
   - Centre pivots & irrigation  
   - Pump stations & boosters  
   - Dam, river & bore filtration  
   - Off-grid & solar water (Mitchell’s lived off-grid on solar ~10 years — say so)  
   - Water & wastewater infrastructure (heavy stuff)  
   - Contractor support for utilities & hydro works  
3. **Where I go** — simple SVG map of Tassie regions + “Based in Tassie. If it’s on the island, I’ll get there.”
4. **Built for Tassie infrastructure** — honest positioning without fake clients:
   - Tasmania’s water and power run on TasWater, Hydro Tasmania, and a lot of contractors. I’ve done this at scale for Sydney Water, Urban Utilities, Seqwater, Thiess and John Holland. Same standards, available here.
   - Capability: pump stations, rising mains, treatment mechanical, clarifiers, dewatering, dam/intake, tunnelling-adjacent mechanical, mine water.
   - CTA: head contractor bidding Tassie water/hydro who needs a mechanical/water lead → talk.
5. **Who turns up** — Mitchell photo + 4–5 lines. Lead: 30+ years, zero OH&S career-wide, mines → farms. Degrees in a small “the paperwork” disclosure. Keep: “I read the contract so you don’t have to.”
6. **Who I’ve worked for** — real names only; greyscale logos only with permission. Caption: “Big jobs on the mainland. Same standards on your farm.”
7. **Jobs** — 3 cards → `projects.html`: photo, location, problem → done → result. Real jobs only; label mainland locations clearly if no Tassie jobs yet.
8. **How it works** — Ring/text → site look (say if free/charged) → fixed quote, no surprise extras.
9. **Contact** — bottom. Phone big. “Text is fine — I’m often in a paddock.” Form: name, phone, town, what’s broken. Service-area line.
10. **Footer** — ABN, Formerly Meyjor, postal, links.

---

## Visual direction

**CSS tokens (`:root`):**

| Token | Hex | Role |
|-------|-----|------|
| `--dolerite` | `#3b3f42` | main text / dark |
| `--button-grass` | `#6b7a3a` | primary accent |
| `--eucalypt` | `#8fa39a` | secondary |
| `--rust` | `#a5522d` | CTA / highlights |
| `--cream` | `#f3efe6` | background |
| `--bass-strait` | `#2f5566` | links / water |

- Dark mode via `prefers-color-scheme`.
- Type: chunky slab/grotesque headings (e.g. Archivo Black, Zilla Slab) + readable body (Source Sans 3). **No italic agency hero.**
- Real photos > everything. No stock “engineer with tablet”.
- Kill emoji icons. Kill most scroll animations (one subtle fade max; honour `prefers-reduced-motion`).
- Buttons: square-ish, solid, high contrast.

> Note: current live site is dark/teal industrial. The cream/Highlands palette above is the **rebuild target** — don’t half-migrate; either finish the new system or keep the old one coherent until cutover.

---

## Sub-pages

| Page | Action |
|------|--------|
| `farm-irrigation-tasmania.html` | Keep; rewrite in new voice; crops + “common problems I fix” |
| `water-wastewater-bowen-basin.html` | Rename → `infrastructure.html`; Bowen Basin = track record for Tassie contractors; **301** old URL |
| `off-grid-water.html` | **New** — bores, tanks, solar pumping, rainwater (lifestyle blocks / shacks) |
| `projects.html` | Same card language as homepage Jobs |

Also present: `coal-clarifiers-bowen-basin.html`, `wastewater-treatment-mackay.html` — fold into infrastructure track record or 301; don’t leave orphan SEO pages with Mackay-as-home messaging.

---

## SEO / technical

- Title: `Engineered Water Solutions | Farm Irrigation, Pumps & Water Engineering — Tasmania`
- Meta ~150 chars, new voice.
- JSON-LD `LocalBusiness` + `Service` — real phone, correct address type, Tassie service areas.
- Keywords natural: Launceston, Hobart, Midlands, North West Coast, Central Highlands, Devonport, Burnie.
- WebP images, lazy-load below fold, honest `alt` text.
- Mobile-first: ≥16px gutters, tap targets ≥44px, `tel:` everywhere.
- Form → Mitchell’s email (Formspree or Cloudflare Worker), honeypot, no CAPTCHA wall.

---

## Don’t

- Don’t claim clients, jobs, or numbers that aren’t real.
- Don’t use logos without written permission.
- Don’t add chatbot, empty blog, or “Our Values”.
- Don’t Squarespace-trades cliché (clip-art ute) — competence comes from photos, plain words, track record.

---

## Deliverable checklist

- [ ] Credibility fixes (testimonial, clients, dates, phone, addresses)
- [ ] New `index.html` structure
- [ ] CSS tokens + type + dark mode (full cutover)
- [ ] Tasmania region SVG map
- [ ] Infrastructure section (honest TasWater/Hydro framing)
- [ ] Rewrite + rename sub-pages + 301s
- [ ] New `off-grid-water.html`
- [ ] Schema, meta, image optimisation
- [ ] Mobile 375px check; Lighthouse ≥90

---

## Agent execution notes

1. Work in the static files already on GitHub Pages — no new framework.
2. Push only when the user asks (or when they say “push it”).
3. Prefer small, reviewable commits: credibility → structure/copy → visuals → SEO.
4. When unsure if a client/job is real — **ask**, don’t invent.
