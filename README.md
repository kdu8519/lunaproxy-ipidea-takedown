# lunaproxy review: What the IPIDEA takedown means for your account, and the $1/GB residential proxy worth switching to

If you searched "lunaproxy review" this month, there's a decent chance you weren't comparison shopping. You were opening a dashboard that wouldn't load, or trying to work out why a proxy pool that seemed fine last quarter suddenly stopped returning usable IPs. That's a different question than "is LunaProxy any good," and it deserves a different answer.

So here's the honest split: LunaProxy was a real proxy provider with real customers and real pricing, and in January 2026 it got caught up in the largest residential proxy takedown the industry has seen. What you do next depends on whether you still have traffic sitting in an account, or whether you're just looking for a cheap residential pool that isn't tied to a shuttered network.

## The short version

- LunaProxy advertised a 200M+ residential pool across 195 locations, with pay-as-you-go traffic and entry pricing that undercut almost everyone.
- On January 28, 2026, Google's Threat Intelligence Group took court-ordered action against IPIDEA, a China-based residential proxy backend. Google named Luna Proxy publicly as one of several brands running on that infrastructure.
- Independent reporting since then says the brand's domains stopped resolving. A July 2026 DNS check published on dev.to found `lunaproxy.com` returning NXDOMAIN.
- If you want a residential pool with transparent sourcing, non-expiring traffic, and a $5 entry point, DataImpulse is the provider I'd point you to — with one real caveat about targeting surcharges that's worth reading before you scale.

## What LunaProxy actually sold

Strip away the affiliate blog posts and the advertised product was straightforward. Rotating residential proxies billed by traffic, sticky sessions you could hold for up to 90 minutes, HTTP(S) and SOCKS5 support, country and city-level targeting, no concurrency limit on the rotating pool, and traffic that could be extended to 60 or 90 days with rollover if you renewed in time.

Alongside that it sold static ISP proxies billed per IP, dedicated datacenter proxies sold both per IP and by traffic, an unlimited residential plan charged by time rather than volume, rotating ISP proxies, and a Universal Scraping API. The headline number was always the same: 200 million residential IPs across 195 locations. Independent reviewers largely accepted that the pool was genuinely large, though the geographic mix leaned heavily toward Brazil and India, with thinner depth in the US and EU than the headline implied.

The prices, though, never quite agreed with each other. Depending on which directory or review you read, entry residential ran anywhere from $0.65/GB to $2.10/GB, unlimited residential was either $60/month or hundreds of dollars per day, and static ISP was quoted both as $3/week and as $0.17/day. Some of that is promotion versus list price. Some of it is affiliates copying each other. Either way, it's a reminder that a published rate card is only worth as much as the provider's willingness to keep it accurate.

## January 2026: the part most reviews haven't caught up with

On January 29, 2026, Google published findings from its Threat Intelligence Group describing a coordinated disruption of IPIDEA, which Google assessed as one of the largest residential proxy networks in the world. The action followed a US federal court order issued the previous day and covered dozens of domains used for both device control and marketing.

The technical story is uncomfortable reading if you've ever bought cheap residential IPs. Google's report describes SDKs — Castar, Earn, Hex and Packet — embedded in apps, enrolling consumer devices as proxy exit nodes without clear disclosure. Play Protect enforcement was set to remove apps containing that code from Android devices, with roughly nine million devices expected to drop out of the pool. In a single week of January 2026, Google observed more than 550 tracked threat groups routing traffic through IPIDEA exit nodes.

What matters for a proxy buyer is the brand list. Google stated that a number of apparently independent services were controlled by the same operators behind IPIDEA, and named 360 Proxy, Luna Proxy, PIA S5, Radish VPN and others. Subsequent coverage — including reporting from SecurityAffairs, Decodo and Korean security outlet Boannews — repeated the same list, and added 922 Proxy, ABC Proxy, IP2World, PY Proxy, Galleon VPN and Tab Proxy.

Two things followed. First, Google explicitly warned that because proxy operators share device pools through reseller agreements, the disruption could have downstream impact on affiliated entities. Second, users started losing access. ProxyStats' tracking page states that 922 Proxy, PIA S5, LunaProxy and others stopped working at the end of January 2026, and a dev.to write-up of registry and DNS checks in July 2026 reported NXDOMAIN for `lunaproxy.com`, `pyproxy.com` and `abcproxy.com` alike.

Worth being precise here: Google did not say every affiliated brand was permanently dead, and it's entirely possible some reappear under new infrastructure. What the public record does show is that the backend behind LunaProxy's pool was targeted, the storefront went dark, and the companies sharing that pool fell together.

> If your LunaProxy account still holds prepaid traffic, treat recovery as unlikely and don't spend more money on the assumption that it comes back. Historical evidence from the 911 S5 shutdown points the same way.

## A second problem: the clone sites

When a brand goes dark, the demand doesn't. Searches keep coming, which is exactly the environment clone operators like.

Scamadviser's record for `lunaproxy.online` — note the TLD — shows a domain registered in May 2026, a trust score of 1, and flags for phishing and suspicious activity from IPQS. That is not the LunaProxy you may have bought from in 2023. It's a domain that didn't exist until after the takedown, carrying a recycled brand name.

The practical rule: before trusting any "revived" provider, check the registration date through a WHOIS or RDAP lookup. A provider claiming years of history on a domain registered a few months ago is not the provider you remember.

## What users were saying before the shutdown

LunaProxy's Trustpilot page sits at 3.6 out of 5 across roughly 105 reviews, and the pattern in the complaints is consistent and specific rather than vague anger.

Recurring themes:

- IPs flagged as high-risk by third-party checkers, or recognised as datacenter/hosting ranges rather than residential connections. One reviewer noted the ISP showed as "Medium Risk" on Scamalytics and as a hosting provider on Ping0.cc.
- Geographic mismatch. A customer reported buying a Turkish residential proxy that resolved to Singapore, with no refund offered.
- Refunds. Multiple reviewers described requests being refused, with the provider replying that IPinfo is the accepted detection standard for disputes.
- Slow connections on some packages. One complaint measured below 1 Mbit on most addresses.
- Support responsiveness. Some customers described Telegram responses taking twelve hours or longer.

There's a countervailing pattern too. A cluster of five-star reviews landed within days of each other in September 2024, many using the same marketing phrase — "game-changer" — which is worth noting when you're weighing a star average. Independent reviewers were measured rather than hostile: ProxyLook graded pricing and pool size highly but gave ethics a B, citing minimal disclosure around IP sourcing, infrastructure and KYC, and characterising the business as a reseller rather than a network operator.

## What you actually need now

Once you set aside the brand question, the requirements don't change much. You want residential IPs that don't get flagged on sight, per-GB pricing that doesn't require a monthly commitment, sessions that behave predictably, and a provider whose IP sourcing you can at least describe out loud. And after watching an entire cluster of cheap providers vanish in a single week, you probably want to buy in small increments rather than prepay a terabyte.

## Why DataImpulse is the provider I'd start with

DataImpulse runs a residential network of 90M+ IPs across 195+ countries, sold on a pure pay-as-you-go model with no subscription. The two features that matter most in a post-IPIDEA market:

**Traffic doesn't expire.** Buy 5 GB, use 2 GB, come back in four months — the balance is still there. Most of the budget segment expires your bandwidth after a set period. TechRadar's review singled this out as the provider's defining differentiator, and it's also the feature that softens the risk of a provider going dark: you're not locked into a monthly renewal cycle that keeps charging for capacity you can't reach.

**The entry price is $5.** Five dollars for 5 GB at $1/GB is the honest floor here. Country-level targeting is included in that base rate across all 195 covered regions with no activation fee, and the pool is described by the provider as ethically sourced — the claim TechRadar's reviewer also leaned on when noting the IPs' cleaner reputation scores.

The mechanics are standard but worth spelling out because they affect how you configure things. Rotating sessions assign a new IP per request. Sticky sessions hold an IP for 1 to 120 minutes, with 30 minutes as the default when you don't specify an interval, and they run on ports 10000–20000. Both HTTP(S) and SOCKS5 are supported, and you can target by country, or by city, state, ZIP and ASN for an additional cost. The gateway is `gw.dataimpulse.com:823` if you're wiring credentials into a scraper or an antidetect browser.

Independent benchmark data is also more favourable than LunaProxy's was. ProxyStats, which probes providers live rather than collecting affiliate copy, currently ranks DataImpulse first with a composite score of 85/100. Over a trailing 30-day window it logged 7,634 probes at a 92.8% success rate with a 520 ms median response, and session reliability — whether a sticky session keeps its IP without silently rotating — at 93/100. Its measured strength was latency percentiles and success rates on Google and Amazon targets; its measured weakness was 30-day uptime, landing in the bottom 20% of the benchmark set.

That uptime figure is the one number I'd keep in your head. It's not fatal — it's a percentile, not an outage report — but if you're running pipelines where downtime costs real money, budget for a fallback route rather than assuming one provider covers you.

👉 [Start with the 5 GB residential package](https://bit.ly/dataimPulse)

## All DataImpulse plans compared

DataImpulse doesn't sell tiered monthly subscriptions. Every line is billed by traffic, per gigabyte, with the balance staying valid until you use it. There are four proxy products on the site:

| Plan | What you get | Price | Billing cycle | Buy |
| --- | --- | --- | --- | --- |
| **Residential** | 90M+ IPs, 195+ countries (214 locations listed), rotating + sticky sessions, HTTP(S)/SOCKS5, free country targeting, traffic never expires, advanced targeting at 2× rate | From $1/GB — $5 for 5 GB entry; $0.80/GB at the $800/1 TB volume tier | Pay-as-you-go, no subscription | [Get the residential proxy package](https://bit.ly/dataimPulse) |
| **Premium Residential** | Faster, higher-trust residential traffic, dedicated account manager, all targeting options included at no surcharge, 210 locations | From $5/GB — $5 for 1 GB, $50 for 10 GB; custom pricing from $20,000 at 5 TB+ | Pay-as-you-go, no subscription | [Compare premium residential pricing](https://bit.ly/dataimPulse) |
| **Mobile** | Mobile carrier IPs, 191 locations, volume discounts from the 1 TB tier | From $2/GB | Pay-as-you-go, no subscription | [Check mobile proxy rates](https://bit.ly/dataimPulse) |
| **Datacenter** | 123 locations, state/city/ZIP/ASN targeting available without the residential surcharge | Listed from $0.50/GB | Pay-as-you-go, no subscription | [See datacenter proxy pricing](https://bit.ly/dataimPulse) |

One footnote on that table: per-GB rates scale with volume, and the lowest published tier is the $800/1 TB package at $0.80/GB on standard residential. Don't buy at that level on day one. Buy the $5 entry package, run it against your actual targets, and only then decide whether the volume tier is worth committing to.

## Where DataImpulse isn't the cheapest option

Three things to know before you treat it as the default answer.

**Advanced targeting costs double on residential.** City, state, ZIP and ASN selection is billed at 2× the standard per-GB rate. If your workflow depends on ZIP-level precision, your real cost is $2/GB, not $1/GB. Datacenter proxies appear to include those filters without the surcharge, which may make them the better choice for some targeted jobs. Confirm current billing treatment with support before you build a budget around it — this is the kind of policy that changes quietly.

**Mobile and premium residential volume discounts only start at 1 TB.** Below that, you're paying the list rate.

**There's no free trial.** What there is instead is a 7-day refund policy for new users, which is not the same thing but covers the "does this actually work on my targets" question if you test immediately.

And to be fair about the comparison: LunaProxy's advertised entry price of $0.65–$0.77/GB was lower than DataImpulse's $1/GB. But that price was attached to a pool whose backend Google dismantled in a single week, sourced through SDKs installed on consumer devices without clear disclosure. If your cost calculation ignores where the IPs come from, you'll keep finding the same deal — right up until it disappears again.

## How to switch without repeating the mistake

1. **Verify the domain before you pay.** Pull the registration date on any provider you're considering. Anything less than six months old and claiming a long track record deserves suspicion.
2. **Buy the smallest package.** At DataImpulse that's $5 for 5 GB. There's no reason to prepay a terabyte on a first purchase, especially when the balance doesn't expire.
3. **Test against your real targets, not a demo site.** Success rates on Google and Amazon tell you less than your own hardest target does.
4. **Sample the IP quality yourself.** Run a handful of IPs through a reputation checker and confirm they read as residential rather than hosting ranges. This is the single most common complaint about the budget segment.
5. **Keep a second provider in your config.** Treating provider death as routine rather than exceptional is the actual lesson of January 2026.
6. **Save the targeting cost into your budget.** If you need city or ZIP level, work out the doubled rate first.

👉 [Run your first 5 GB test for $5](https://bit.ly/dataimPulse)

## FAQ

**Is LunaProxy still working?**

Reporting from ProxyStats says the service stopped working at the end of January 2026, and a July 2026 DNS check found `lunaproxy.com` no longer resolving. Google's January 2026 report named Luna Proxy among the brands running on the IPIDEA backend it disrupted. Some directories still publish LunaProxy pricing as if the service were live, but directory pages lag reality by months. If you still need access, treat any site currently offering "LunaProxy" as unverified.

**Was LunaProxy a scam?**

That's the wrong frame for what happened. It sold a working product to paying customers for years and had a 3.6/5 Trustpilot average with both hostile and positive reviews. The documented problems were IP quality, geographic accuracy, refund refusals and support responsiveness. The bigger issue was structural: the network its IPs came from was operating on infrastructure Google assessed as enrolling consumer devices without clear consent.

**Why is DataImpulse the recommendation rather than a bigger name?**

Price and exposure. Bright Data and Oxylabs offer more enterprise tooling, but a $1/GB entry point with non-expiring traffic and no subscription is a much smaller bet to place while you're evaluating. TechRadar's review was positive, ProxyStats' live benchmark ranks it first at 85/100 with a 92.8% success rate, and the pay-as-you-go model means a provider problem costs you a balance rather than a contract.

**Does DataImpulse have a free trial?**

Not one that's currently advertised. The provider lists a 7-day refund policy for new users, so the practical approach is to buy the $5 entry package, test it against real targets within the first week, and decide from there.

**What's the cheapest legitimate residential entry price right now?**

$1/GB pay-as-you-go is roughly the floor for a provider with published sourcing policies — DataImpulse's 5 GB package at $5 is the concrete example. Rates below that, and especially below $0.80/GB, generally mean either a large volume commitment or a network you can't audit.

## Bottom line

LunaProxy was a real budget option with a genuinely large pool, and its pricing genuinely undercut most of the market. It also sat on infrastructure that Google's Threat Intelligence Group dismantled in January 2026 alongside a dozen other brands, and the storefront appears to have gone with it. The IP quality complaints that predated the takedown — flagged ranges, geographic mismatches, contested refunds — were already visible on Trustpilot at 3.6/5.

If you need a residential pool this month, buy five dollars' worth somewhere you can verify, test it against the sites you actually scrape, and keep a backup route configured. DataImpulse's $1/GB pay-as-you-go line is the most sensible starting point for that test, as long as you go in knowing that city and ZIP targeting doubles the rate and that its benchmark uptime is the weakest of its measured metrics.

👉 [Test DataImpulse's residential proxies with the $5 starter package](https://bit.ly/dataimPulse)
