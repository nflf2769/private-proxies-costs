# private proxies: what "private" actually means, how many you need, and what a clean dedicated pool costs

Most people typing "private proxies" into a search bar want one of three things, and they're not the same thing at all. Some want an IP that nobody else is using. Some want an IP that doesn't look like a server rack. Some just want a working proxy without getting scammed. If you buy the wrong category, you'll be back on the same search results page a week later, wondering why your accounts keep asking for verification.

So before pricing anything, it's worth separating those three requirements, because they lead to different products, different price structures, and very different outcomes.

## What the word "private" is actually doing

Private is a description of exclusivity, not of technology. A private proxy is an IP assigned to one customer. The opposite is a shared pool, where hundreds or thousands of users push traffic through the same addresses. Exclusivity is the whole point: you control the reputation of an IP that only you touch.

That's separate from what the IP *is*. An IP can be private and hosted in a datacenter, or private and registered to a residential ISP. Both are exclusive. Only one of them survives contact with a serious anti-bot system.

So "private proxies" usually collapses three questions into one keyword:

1. Is this IP mine alone, or am I sharing it?
2. Does it look like a home connection or a server?
3. How long does it stay the same address?

You can't answer those with a single product category, which is why the market splits into a handful of options that do genuinely different jobs.

## Private vs shared: the part that actually changes your results

Anti-bot systems evaluate IP and ASN reputation early, before they get anywhere near browser fingerprinting. It's the cheapest check they can run, so it runs first. If the address is on a blocklist or belongs to a hosting provider, nothing downstream matters much.

Shared pools have a structural problem here. They get abused — by scraper farms, credential-stuffing crews, whoever bought bandwidth — and every burned address leaves residue on the pool's reputation. A dedicated address sidesteps most of that, because the only person who can ruin it is you.

That's the honest argument for paying more per IP. If you're running one logged-in profile per account, concentration of reputation is the feature you're buying.

## Three kinds of "private" proxy, and the jobs each one fits

| Type | What the IP looks like | Session behaviour | Best fit |
| --- | --- | --- | --- |
| Private datacenter | Hosting/cloud ASN | Static, fast, cheap | Price monitoring, low-protection targets |
| Private ISP ("static residential") | ISP-registered, hosted in a datacenter | Static for weeks or months | Long-lived logged-in sessions, account management |
| Private residential | Real household ISP connection | Hours to ~24h per IP, then it drops | Verification-sensitive work where a rotating-but-exclusive pool is acceptable |

The third row is where things get interesting, and it's also where most of the confusion lives. Residential IPs are not static by nature — the underlying device disconnects, the address changes, and you get a new one. You're renting exclusivity for a window, not a permanent address.

For some workflows that's fine. For a session you need to keep logged in for six months, it isn't, and no marketing copy will change that.

## Where 9Proxy fits into this

9Proxy is a residential proxy platform that sells three things: residential IPs by count, residential bandwidth by gigabyte, and bundles that combine them. The catalog claims 20M+ residential IPs across 90+ countries, HTTP/HTTPS and SOCKS5 support, targeting down to country, state, city, ZIP and ISP level, and 24/7 support.

The relevant piece for anyone hunting private proxies is the IP-based model. Internally, that product is described as one IP per user, one IP counted per forward, with unlimited traffic while the IP is active, and unused IPs that don't expire. In practice that means you're buying exclusive residential addresses rather than traffic — you can push as much data through a working IP as you want.

Two things to know before you assume it's the same as an ISP proxy:

- IP-based access runs through a desktop app with local port forwarding, not just a username and password in a browser extension.
- IP lifespan is residential, which 9Proxy documents as a few hours up to roughly 24 hours per IP. An auto-rotation proxy option lets you rotate on a schedule across selected ports.

If you need a permanent static address bound to one identity, that's a different product category, and 9Proxy doesn't sell it. Being clear about that saves a refund argument later.

## The full price list

9Proxy adjusted pricing on June 1, 2026 — IP packages and bundles went up, GB packages stayed where they were. These are the current published numbers.

**Residential by IP (unlimited bandwidth, unused IPs never expire)**

| Package | Total price | Cost per IP |
| --- | --- | --- |
| 100 IPs | $24 | $0.24 |
| 500 IPs | $72 | $0.144 |
| 1,000 IPs + 500 bonus (1,500 total) | $126 | $0.084 |
| 2,500 IPs | $210 | $0.084 |
| 5,000 IPs | $360 | $0.072 |
| 15,000 IPs | $720 | $0.048 |
| 25,000 IPs | $863 | $0.035 |
| 50,000 IPs | $1,438 | $0.029 |

**Business IP packages**

| Package | Total price | Cost per IP |
| --- | --- | --- |
| 100,000 IPs | $2,300 | $0.023 |
| 200,000 IPs | $4,140 | $0.021 |
| 500,000 IPs | $8,625 | $0.018 |

**Residential by GB (unlimited endpoint generation, 180-day validity)**

| Package | Price per GB | Total | Validity |
| --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days |
| 50 GB (+5 GB bonus) | $2.10 | $105 | 180 days |
| 100 GB | $1.50 | $150 | 180 days |
| 200 GB | $1.00 | $200 | 180 days |
| 1,000 GB | $0.80 | $800 | 180 days |
| 2,000 GB | $0.75 | $1,500 | 180 days |

Larger GB tiers continue down to $0.68/GB at the 10,000 GB mark.

**Bundle packages (IPs + bandwidth)**

| Package | What's included | Price |
| --- | --- | --- |
| Starter Bundle | 100 IPs + 5 GB | $30 |
| Popular Bundle | 1,500 IPs + 50 GB | $180 |
| Pro Bundle | 5,000 IPs + 500 GB | $720 |

**Enterprise** — unlimited data validity, one owner plus up to five team members, per-member traffic controls, activity logs, VIP pricing and dedicated support. Price is quoted on request.

You can compare the current tiers and buy any of them here: 👉 [see 9Proxy's current IP and GB packages](https://bit.ly/9-Proxy)

## IP-based or GB-based: the decision that costs people the most

This is where budgets quietly go wrong, and it has nothing to do with which product is "better."

IP-based billing wins when each request is heavy. One IP, unlimited data, a fixed cost. If you're pulling large pages, running sustained sessions, or doing work where bandwidth per request is unpredictable, metering is a trap.

GB-based billing wins when you need many distinct addresses but very little data each. Rotating through thousands of IPs to check geo-specific prices, verify ad placement, or poll an API consumes kilobytes per request. Paying per IP for that is like renting a car to drive to the mailbox.

Bundle packages exist for teams doing both, and the 180-day traffic validity means unused balance doesn't evaporate on a monthly clock.

## How many private IPs do you actually need

Vendors love volume tiers because they encourage overbuying. Here's a rough way to size it without guessing:

- **One IP per logged-in identity.** This is the rule people break first. Two accounts sharing an address is the classic re-verification trigger, and it's the reason some users report problems that the IP quality alone doesn't explain.
- **Add concurrency, not just accounts.** If five scraping jobs run simultaneously and each needs a distinct address, that's five IPs in rotation, not one.
- **Then check the tier math.** At 9Proxy's current prices, the jump from 100 IPs to 1,000+500 bonus IPs is $24 to $126 — a 15x increase in IPs for roughly 5x the money. If you're anywhere near the boundary, stepping up is arithmetic, not ambition.
- **Don't stockpile past your use case.** The per-IP price keeps falling, but only for people who will actually route traffic through them.

For a single operator running a handful of profiles, 100 IPs is a legitimate starting point. For an agency managing client accounts, the 1,500-IP entry tier is usually the more honest comparison.

## Coupons, invite codes, and the small print

9Proxy's sign-up runs on an invite-code model, which is standard for this part of the market — not a warning sign, just a referral mechanism. Referred accounts typically get a discount on their order, though the exact percentage moves with whatever promotion is live, so the number that matters is the one on your checkout summary.

The platform also runs short-window promos. Two recent examples: a Lunar New Year code (LNY2026) that took 8% off regular IP and GB packages, and an April 2026 GB sale where your first paid GB order auto-issued a personal 9% coupon — retrievable under Dashboard → My Account → My Coupons, valid for GB orders only, not stackable with other codes or applicable to bundles or IP plans. Coupons issued through that campaign expired June 30, 2026.

If you're buying, check the coupon field before you pay rather than after: 👉 [check active 9Proxy discounts and current pricing](https://bit.ly/9-Proxy)

## Limits worth knowing before you spend

**No self-serve free trial.** Testing access exists through community channels and promotion codes, but there's no obvious one-click trial on the site. That friction matters, because several public reviews trace back to people who bought the wrong plan type and then hit a firm refund policy. The proxy infrastructure itself isn't what the complaints describe — plan-fit mistakes are.

**90+ countries, not 195.** US, UK, Europe and Southeast Asia coverage is the strong part. If your target geography is niche, verify availability for that country before buying a large package.

**It's residential-only.** No ISP/static product, no datacenter catalog. If you need a permanently static private IP for a long-lived session, look at a provider that sells one.

**Independent performance data is thin but not empty.** One 2026 review ran a 300-request test against Cloudflare-protected targets and reported a 97.7% success rate, with the handful of CAPTCHA challenges traced to a single IP range that rotated clean. That's a single test on a specific target mix, not a general benchmark — treat it as a data point, not a promise.

## The short version

If "private" means *an IP nobody else is touching*, 9Proxy's IP-based packages are a straightforward way to buy exclusive residential addresses with unlimited bandwidth, starting at $24 for 100. If "private" means *a static address that never changes for six months*, this isn't the product, and no discount makes it one. Match the definition to the job first — the pricing table is much easier to read once you have.
