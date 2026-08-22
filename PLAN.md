# HyderabadNet - Project Plan

## What We Built (Current State — Aug 2026)

A single-page HTML application. Multiple design explorations were done (original clean version + three redesigns with stronger personality). Analysis concluded the right product is a **restrained, high-utility version** that keeps the best engagement features without visual or interaction overkill.

### Core Sections (target production)

| Section | Status | Notes |
|---------|--------|-------|
| Plan Comparison | Done | Speed-tier filterable table, cheapest highlighted |
| ISP Encyclopedia | Done | 7 ISPs, verified plans, expandable cards, direct links |
| Neighborhood flavor | Light | Simple tips / scores for major areas (real data still thin) |
| Router Recommender | Done | Multi-step wizard, ~12 routers, accounts for walls + devices + budget |
| Roast my internet | **New / Keep** | High-engagement diagnostic — the best addition from redesigns |
| Security Audit | Done + upgraded | Interactive score/grade + checklist |
| Glossary | Done | Plain-English definitions |

### Design Direction (locked)

- Base on the warm paper + lime aesthetic from the first redesign (cream background, Space Grotesk + Inter).
- Floating pill nav is good.
- Keep personality and slightly spicy local voice.
- **Remove / avoid:** heavy animated SVG network map, full-screen quiz overlay, hard neo-brutalist shadows everywhere, fake “X reports” numbers, competing design systems, 3+ Google font families.
- Goal: feels like a sharp local tool, not a design showcase.

### ISP Data (Verified Against Websites)

| ISP | Plans Listed | Price Range | Source |
|-----|-------------|-------------|--------|
| ACT Fibernet | 5 (100 Mbps to 1 Gbps) | INR 549 to 2299/mo | actcorp.in |
| Airtel Xstream | 7 (40 Mbps to 1 Gbps) | INR 449 to 3699/mo | airtel.in |
| JioFiber | 4 (30 Mbps to 300 Mbps) | INR 366 to 1399/mo | jio.com |
| Excitel | 4 (200 to 300 Mbps) | INR 466 to 724/mo (12mo) | excitel.com |
| BSNL Bharat Fiber | 3 (40 to 150 Mbps) | INR 366 to 733/mo | plansinfo.com |
| Tata Play Fiber | 4 (50 Mbps to 1 Gbps) | INR 699 to 3266/mo | tataplayfiber.com |
| Hathway | 3 (40 to 150 Mbps) | INR 499 to 849/mo | hathway.com |

### What's Covered

- Plan speeds, monthly/quarterly pricing, FUP, OTT bundles
- Direct links to ISP Hyderabad plans pages
- Router recommendations matched to speed, home size, usage, devices, budget, wall type
- Concrete wall / multi-floor advice
- Interactive “Roast my internet” diagnostic
- Security score + hardening checklist
- Networking glossary
- Strong local voice, “made with love by asmgkr”

### What's Missing (prioritized)

**High priority (do next):**
1. Real locality / area-wise ISP availability & reliability notes (Gachibowli, Madhapur, Kukatpally, etc.)
2. Upload speed comparison (critical for WFH)
3. Installation charges, deposits, hidden fees
4. Affiliate links (Amazon + Flipkart + ISP referrals) so the project can earn
5. SEO meta + Open Graph + basic analytics (Phase 1)

**Medium:**
- Needs calculator (usage → recommended speed tier)
- ISP-specific setup guides (change password, enable WPA3, etc.)
- Share / save comparison results

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
- [ ] Produce single clean production `index.html`
- [ ] Strip overkill (heavy SVG map, quiz overlay, fake report counts)
- [ ] Confirm SEO meta + Open Graph are solid
- [ ] Update this PLAN.md

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
- [ ] Add upload speeds to comparison table
- [ ] Installation charges / deposit notes per ISP

### Phase 3: Interactive Depth

- [ ] Needs calculator (people + streams + devices → recommended speed)
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
