# HyderabadNet - Project Plan

## What We Built (Current State — Oct 2026)

A single-page HTML application. Multiple design explorations were done (original clean version + three redesigns with stronger personality). Analysis concluded the right product is a **restrained, high-utility version** that keeps the best engagement features without visual or interaction overkill.

### Core Sections (target production)

| Section | Status | Notes |
|---------|--------|-------|
| Speed Calculator | Done (Oct 2026) | Peak-hour usage → recommended tier, links into Compare + Router Finder |
| Plan Comparison | Done | Min-speed / provider / bundle / data-cap filters, sortable, GST toggle, upload + ₹/Mbps + billing columns, fees table, mobile card layout |
| ISP Encyclopedia | Done | 6 ISPs, 40 plans, fees, upload, pros/cons, tenure pricing, source per ISP |
| Neighborhood flavor | Not started | Real locality data still needed |
| Router Recommender | Done | 12 routers, WAN-port ceiling, budget-aware ranking with reasons, Amazon/Flipkart price links |
| Roast my internet | Not started | High-engagement diagnostic idea from redesigns |
| Security Audit | Done | Interactive weighted checklist, A–F grade, saved in localStorage |
| Glossary | Done | 35 terms, searchable |

### Design Direction (locked)

- Base on the warm paper + lime aesthetic from the first redesign (cream background, Space Grotesk + Inter).
- Floating pill nav is good.
- Keep personality and slightly spicy local voice.
- **Remove / avoid:** heavy animated SVG network map, full-screen quiz overlay, hard neo-brutalist shadows everywhere, fake “X reports” numbers, competing design systems, 3+ Google font families.
- Goal: feels like a sharp local tool, not a design showcase.

### ISP Data (Re-verified October 2026)

All prices are listed monthly price excluding GST. Data lives in the `ISPS` array in `index.html`; every view is derived from it.

| ISP | Plans Listed | Price Range | Upload | Source |
|-----|-------------|-------------|--------|--------|
| ACT Fibernet | 11 (50 Mbps to 1 Gbps, incl. OTT packs) | ₹575 to ₹3,199 | Symmetric | actcorp.in Hyderabad plan grid |
| Airtel Xstream | 8 (40 Mbps to 1 Gbps) | ₹499 to ₹3,999 | Not published | airtel.in/plans/broadband/hyderabad |
| JioFiber | 4 prepaid (30 to 300 Mbps) | ₹399 to ₹1,499 | Symmetric | jio.com Hyderabad page |
| Excitel | 4 (200/300 Mbps, 3/6/9/12-mo prices) | ₹466 to ₹724 (12-mo) | Not published | excitel.com Hyderabad + T&C |
| BSNL Bharat Fibre | 7 (50 to 300 Mbps, all with FUP) | ₹449 to ₹1,799 | Not published | BSNL Telangana circle FTTH tariff, Aug 2026 |
| Hathway | 6 (40 to 300 Mbps) | ₹524 to ₹824 (12-mo effective) | ~30% of download | hathway.com Hyderabad + speed disclosure |

**Corrections made in the Oct 2026 refresh:**
- ACT: old prices (₹599/100 Mbps etc.) came from stale SEO text on actcorp.in; the live plan grid is ₹575/50 Mbps to ₹2,999/1 Gbps, with 400 and 600 Mbps tiers and no 300 Mbps.
- Airtel: added the new ₹1,199 100 Mbps + TV + Netflix plan. Removed invented "quarterly" prices.
- BSNL: ₹399/40 Mbps is rural-only. Replaced with the Telangana urban line-up (Spark ₹449 to Ultra OTT ₹1,799) with FUP and post-FUP speeds.
- Hathway: Hyderabad line-up is now 40–300 Mbps at ₹524–₹824 effective; Hathway publishes typical upload at ~30% of plan speed.
- Tata Play Fiber: removed. Hyderabad isn't in its 18 serviceable cities and its Hyderabad plans URL returns 404.
- Removed unsourced star ratings in favour of sourced "Good for / Watch out" notes.
- Routers: Deco X55 corrected to AX3000; speed estimates now account for 1G WAN ports capping real throughput at ~940 Mbps.

BSNL's own sites were unreachable when re-verifying; recheck against bsnl.co.in when possible.

### What's Covered

- Plan speeds, upload speeds, monthly / tenure pricing, billing basis, FUP + post-FUP speed, OTT bundles
- Installation fees, deposits and router terms per ISP; GST toggle
- Direct links to ISP Hyderabad plans pages, with source + verification date per ISP
- Speed calculator (peak-hour usage → recommended tier)
- Router recommendations matched to speed, home size, usage, devices, budget, wall type, with reasons
- Concrete wall / multi-floor advice
- Security score + hardening checklist
- Searchable networking glossary
- Strong local voice, “made with love by asmgkr”

### What's Missing (prioritized)

**High priority (do next):**
1. Real locality / area-wise ISP availability & reliability notes (Gachibowli, Madhapur, Kukatpally, etc.)
2. ~~Upload speed comparison~~ Done (Oct 2026), shows "Not published" where the ISP doesn't disclose it
3. ~~Installation charges, deposits, hidden fees~~ Done (Oct 2026), fees table + per-ISP facts
4. Affiliate links: Amazon/Flipkart search links are on router cards; swap in affiliate tags once approved
5. ~~SEO meta + Open Graph~~ Done; basic analytics still to add (Phase 1)

**Medium:**
- ~~Needs calculator (usage → recommended speed tier)~~ Done (Oct 2026)
- ISP-specific setup guides (change password, enable WPA3, etc.)
- Share / save comparison results (filters in URL)
- Upload speeds for Airtel / Excitel / BSNL once published or measured

**Later:**
- User-submitted speed data by area
- Newsletter / feedback
- LCO listings

---

## Hosting Plan

### Recommended: GitHub Pages (Free)

**Why:**
- Static HTML file, no server needed
- Free hosting with automatic HTTPS
- Custom domain support
- Deploy by pushing to a GitHub repo

**Steps:**
1. Create a GitHub repo (e.g., `hyderabadnet`)
2. Push the `hyderabad-internet-guide/` folder contents
3. Enable GitHub Pages in repo settings (Settings > Pages > Source: main branch)
4. Site goes live at `https://yourusername.github.io/hyderabadnet/`
5. Optional: Buy a domain (INR 500-800/year on Namecheap/GoDaddy) and point it to GitHub Pages

**Alternative: Cloudflare Pages**
- Better performance (global CDN)
- Unlimited bandwidth
- Same static file deployment

### Security on Free Hosting

- All static hosts provide automatic SSL/HTTPS
- No server-side code means no server to hack
- The only risk is if you add forms or user data later (then use Netlify Forms or a backend)
- For a static informational site, security is handled by the host

---

## Monetization: Affiliate Links

### Amazon Associates (India)

**Setup:**
1. Sign up at affiliate-program.amazon.in
2. Get approved (usually instant for India)
3. Generate text links for specific router ASINs
4. Place them on router recommendation cards

**Commission:** 1-10% on electronics (typically 2-4% for routers)

**Example earnings:**
- Archer AX73 (INR 8,000) x 2% = INR 160 per sale
- Archer BE230 (INR 9,000) x 2% = INR 180 per sale
- RT-AX86U Pro (INR 23,000) x 2% = INR 460 per sale

**Placement:**
- Each router recommendation card gets "Buy on Amazon" button
- Comparison section gets affiliate links for top routers

### Flipkart Affiliate

**Setup:**
1. Sign up at affiliate.flipkart.com
2. Similar to Amazon, sometimes better prices on Indian electronics
3. Worth having both and showing the better deal

### ISP Referral Programs

- Airtel: Partner program pays per installation
- Jio: Jio Partner program for fiber referrals
- ACT: Local partner/referral programs in Hyderabad
- These require business registration in some cases but pay INR 100-500 per installation

---

## Roadmap: From HTML to Real Product

### Phase 0: Consolidate (NOW — in progress)

**Goal:** Ship one strong production file instead of four competing versions.

- [x] Analyze original vs redesigns — identify what sits right vs overkill
- [x] Lock design direction (restrained warm paper + lime + personality + Roast)
- [x] Produce single clean production `index.html`
- [x] Strip overkill (heavy SVG map, quiz overlay, fake report counts, unsourced ratings)
- [x] Confirm SEO meta + Open Graph are solid
- [x] Update this PLAN.md

### Phase 1: Deploy and Share (next)

**Goal:** Get the site live and gather real feedback.

- [x] GitHub repo exists (`abhishekSF/asmgkr-internet-guide`)
- [ ] Push consolidated `index.html` + updated PLAN
- [ ] Enable GitHub Pages
- [ ] Add Google Analytics (or Plausible / Umami)
- [ ] Share with 10–15 friends in Hyderabad
- [ ] Post in r/hyderabad + local WhatsApp/Telegram tech groups

**Effort:** 1 day once file is ready

### Phase 2: Monetize + Data Depth (parallel)

**Goal:** Make it earn and make locality advice trustworthy.

- [ ] Amazon Associates India + Flipkart Affiliate → “Buy on Amazon” on router cards
- [ ] ISP referral links where available
- [ ] Real locality notes for 10–15 major areas (availability + common complaints)
- [x] Add upload speeds to comparison table
- [x] Installation charges / deposit notes per ISP

### Phase 3: Interactive Depth

- [x] Needs calculator (people + streams + devices → recommended speed)
- [ ] Better share results (roast score, security grade, comparison)
- [ ] Inline jargon tooltips
- [ ] ISP-specific setup guides (ACT / Airtel / Jio password + WPA3)

### Phase 4+: Advanced

- User-submitted speed data by area
- Performance / support quality notes
- Newsletter for plan price changes
- Consider Astro/Next only if traffic and update frequency justify it

---

## Revenue Projections (Conservative)

| Source | Monthly Estimate | Notes |
|--------|-----------------|-------|
| Amazon Affiliates | INR 2,000-5,000 | 10-25 router sales/month at INR 200 avg |
| Flipkart Affiliates | INR 1,000-3,000 | 5-15 sales/month |
| ISP Referrals | INR 2,000-8,000 | 10-40 installations/month at INR 200 avg |
| **Total** | **INR 5,000-16,000** | Growing with traffic and SEO |

**Break-even on time:** If you spend 20 hours/month on updates, and earn INR 5,000+, that's INR 250/hour. Worth it if the site grows.

---

## SEO Strategy

**Target keywords (long-tail):**
- "best router for 1 Gbps ACT Hyderabad"
- "Airtel vs Jio vs ACT Hyderabad 2026"
- "wifi for 2 BHK Hyderabad concrete walls"
- "cheapest 300 Mbps plan Hyderabad"
- "how to change ACT router password"
- "WPA3 setup for JioFiber"

**Content strategy:**
- Each ISP card targets "ISP name Hyderabad plans" queries
- Router finder targets "best router for [speed] Mbps" queries
- Security section targets "how to secure home wifi India" queries
- Glossary targets "what is [term]" queries

---

## Tech Stack (Current and Future)

| Phase | Stack | Why |
|-------|-------|-----|
| Now | Single HTML file | Simple, fast, no dependencies |
| Phase 3+ | Same HTML, maybe split into files | Still static, easier to maintain |
| Phase 6+ | Next.js or Astro | If you need CMS, forms, user accounts |
| If needed | Vercel/Netlify hosting | Free tier still works, adds serverless functions |

---

## Key Metrics to Track

1. **Page views** (Google Analytics)
2. **Most clicked ISP cards** (which ISPs people care about)
3. **Router finder usage** (how many people use it, what inputs)
4. **Affiliate click-through rate** (are people clicking buy buttons)
5. **Bounce rate** (are people leaving immediately)
6. **Search queries** (what keywords bring people in)

---

## Summary

We have a solid foundation: verified ISP data, a working router recommender, security guidance, and glossary. The main gaps are locality data, monetization, SEO, and interactive features. The project can be deployed to GitHub Pages for free in under an hour, and affiliate links can start generating revenue immediately.

The real differentiator is accuracy and completeness. If every plan is verified, every recommendation makes sense, and the whole thing actually helps someone make a decision, this fills a real gap in the Hyderabad market.
