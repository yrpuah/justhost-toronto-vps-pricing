# Toronto VPS: What It Costs, Which Plan Size You Need, and Whether JustHost's $1.77/mo NVMe Plans Fit (Full Price Table + Refund Rules)

A Toronto VPS from a provider with a verifiable facility in the city starts at **$3.75 to $5 per month** for the smallest plan, and four providers I checked all publish that number instead of hiding it behind a quote form. JustHost.asia undercuts every one of them: KVM plans with NVMe storage start at **$2.21/mo month-to-month, or $1.77/mo when you pay for 12 months**. The catch is worth stating in the first paragraph rather than the last. JustHost's public pages don't list datacenter cities, so Toronto is something you confirm in the order flow, not something you can assume from the plan table.

Below: every plan on JustHost's tariff page with both price columns, a sizing guide for the workloads people actually run on a Toronto box, what a Toronto address changes about latency and Canadian data residency, and the billing terms that decide whether the cheap price stays cheap.

> **Quick pick:** Alpha Centauri, 2 cores / 2 GB RAM / 40 GB NVMe / 400 Mbit unmetered port, **$5.21/mo** or **$4.17/mo on a 12-month term**. It's the smallest JustHost plan that runs WordPress with MySQL plus a container or two without swapping. Running only a static site, a WireGuard endpoint or a build runner? New Star at **$2.21/mo** is enough. 👉 [Check the current JustHost VPS plans and confirm your location at checkout](https://justhost.asia/en/services/vps/tariffs?ref=196392)

## The full JustHost VPS lineup, both price columns

The tariff page splits the range into two groups. The "special offers" (New Star, Double Star, Bright Star) carry a three-month minimum order and take 20% off when you prepay a year. The IPv4 + IPv6 line is the KVM group, and it's the one to buy if you need a routed /64 or a dual-stack setup out of the box. Every plan in both groups includes NVMe storage, built-in DDoS filtering, root access and a control panel, and every plan sells bandwidth as an unmetered fair-share port rather than a monthly terabyte cap.

| Plan | vCPU / RAM / NVMe | Port (unmetered, fair-share) | Monthly | 12-month term | Order |
| --- | --- | --- | --- | --- | --- |
| New Star | 1 core / 1 GB / 10 GB | 100 Mbit (~31 TB) | $2.21 | $1.77 | [Order New Star](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Double Star | 2 cores / 2 GB / 20 GB | 200 Mbit (~62 TB) | $4.11 | $3.28 | [Order Double Star](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Bright Star | 4 cores / 4 GB / 30 GB | 300 Mbit (~93 TB) | $5.68 | $4.54 | [Order Bright Star](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Sirius | 1 core / 1 GB / 20 GB | 300 Mbit (~93 TB) | $2.81 | $2.25 | [Order Sirius](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Arcturus | 1 core / 2 GB / 30 GB | 300 Mbit (~93 TB) | $4.01 | $3.21 | [Order Arcturus](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Alpha Centauri | 2 cores / 2 GB / 40 GB | 400 Mbit (~124 TB) | $5.21 | $4.17 | [Order Alpha Centauri](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Vega | 2 cores / 4 GB / 80 GB | 500 Mbit (~155 TB) | $7.79 | $6.23 | [Order Vega](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Capella | 4 cores / 4 GB / 120 GB | 750 Mbit (~232 TB) | $10.61 | $8.49 | [Order Capella](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Rigel | 4 cores / 8 GB / 200 GB | 750 Mbit (~232 TB) | $16.20 | $12.96 | [Order Rigel](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Antares | 5 cores / 8 GB / 300 GB | 750 Mbit (~232 TB) | $19.20 | $15.36 | [Order Antares](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Betelgeuse | 6 cores / 12 GB / 400 GB | 750 Mbit (~232 TB) | $26.40 | $21.12 | [Order Betelgeuse](https://justhost.asia/en/services/vps/tariffs?ref=196392) |

Four things about that table that the page itself doesn't spell out:

**The headline price isn't a named plan.** The section header advertises the IPv4 + IPv6 line "from $1.40" and the homepage banner says "from $1.99", while the cheapest plan in the actual list is Sirius at $2.81. Those sub-$2 entry numbers come from the config constructor, where you build a smaller machine than any preset. If a $1.40 sticker is the reason you clicked, check what it buys before you compare it to Sirius.

**The top of the range is Spica** (8 cores / 16 GB RAM / 500 GB NVMe), priced on the same tariff page just above Betelgeuse.

**The terabyte figures are JustHost's own conversion** of an unmetered port into a monthly volume, and the port is explicitly fair-share. You get the port speed when the host has capacity, not a guaranteed 750 Mbit at 3 a.m. on a busy node.

**The currency isn't printed on the prices.** Confirm it in the cart before you line these numbers up against the USD prices in the comparison table further down.

## What a Toronto address actually buys you

Two things, and only one of them is about speed.

The speed case is real but narrower than the marketing suggests. Toronto sits close to the US East Coast and the Canadian corridor. torontovps.com publishes latency figures for its own network: under 1 ms inside Toronto, roughly 12 ms to New York, 18 ms to Chicago, 20 ms to Montreal, 65 ms to Los Angeles and 82 ms to London. Those are vendor numbers rather than independent measurements, so treat them as an order of magnitude and ask any provider for a test IP or looking glass before you commit. What they describe is a location that works for Ontario, Quebec and the US Northeast, and is a poor fit for users in Asia or South America.

The second reason is residency. If you handle personal data governed by PIPEDA or provincial privacy law, keeping the workload in Canada removes a category of cross-border transfer questions. Sucura Networks puts it plainly on its Toronto page: Canadian data residency without an enterprise price tag. Kamatera lists "compliance with Canadian regulations is a concern" among the reasons to pick its Toronto region. For a Canadian SaaS, an e-commerce store with customer records, or an internal tool holding employee data, that argument carries more weight than 10 ms of latency.

"Toronto" in a plan name usually means one of a handful of carrier hotels. OliveVPS runs out of 151 Front Street West downtown, Tier III certified with Cogent, Lumen, Bell, Rogers and Telia on the transit list. Sucura operates its own hardware at 245 Consumers Road in North York under AS398999. Ask for the street address, not the city name; a "Toronto" node that turns out to sit in Montreal or Buffalo is a different compliance conversation.

Which brings back the JustHost question. The company's own profile describes 45 server locations worldwide, and its VPS pages describe KVM virtualisation, NVMe storage, built-in DDoS filtering and 24/7 support, but the tariff page doesn't enumerate cities. Toronto may well be in the picker. I couldn't verify it from published pages, so treat location as the first thing you check rather than the last. 👉 [Open the plan page and check the location list before paying](https://justhost.asia/en/services/vps/tariffs?ref=196392)

## Matching a plan to what you're running

**Static site, VPN endpoint, uptime monitor, cron box.** 1 core and 1 GB covers it. New Star at $2.21 gives you 10 GB of disk and a 100 Mbit port; Sirius at $2.81 gives you 20 GB, a 300 Mbit port and IPv6. The extra 60 cents triples the port speed and doubles the disk, which is the better buy unless the absolute minimum monthly number is the point.

**WordPress with MySQL, a small Laravel or Node app, a single-site Ghost install.** Start at 2 GB. Arcturus ($4.01, 1 core, 30 GB) handles a low-traffic site; Alpha Centauri ($5.21, 2 cores, 40 GB) is $1.20 more for a second core, which matters the moment a plugin or a backup job pins one CPU.

**Docker, K3s, three to five sites, a staging copy.** Vega at $7.79 gets 4 GB and 80 GB. KVM means containers and custom kernels run natively, so there's no nested-virtualisation workaround to fight.

**Databases and I/O-heavy work.** Capella ($10.61) gives 4 cores and 120 GB but stays at 4 GB of RAM, which is an odd pairing. If the workload is memory-hungry, jump to Rigel ($16.20) for 8 GB and 200 GB rather than adding cores you won't use.

**Windows, RDP or MT4/MT5.** JustHost's VPS pages describe root access and a control panel but don't publish an OS list I could verify, so confirm Windows availability with support before ordering. It's a common place to get caught: OliveVPS sells its $3.99 Starter as Linux-only, with Windows starting on the $7.99 Pro plan and carrying a licensing surcharge, and torontovps.com gates Windows to its $7 Niagara plan and above. Cheap tiers and Windows rarely coexist.

**Bandwidth-heavy work.** 750 Mbit is JustHost's ceiling. If you need a 10 Gbps port, this isn't the product; Cloudnium, Sucura and torontovps all list 10 Gbps on their Toronto plans.

One JustHost feature worth knowing if you expect to grow: the company says you can add CPU cores, RAM or disk to an existing VPS without migrating your data to another server, with minimal downtime. That's cheaper than a rebuild, though it means the plan you buy today doesn't have to be sized for next year.

## Three billing details that decide the real price

**The discount is prepayment, not a lower list price.** New Star costs $26.52 over a year at the monthly rate versus $21.24 on the 12-month term, a saving of $5.28. Vega saves $18.72 ($93.48 versus $74.76). Alpha Centauri saves $12.48. That's a real 20%, and it's the entire reason the "$1.77" number exists. The trade is that a year of prepaid service is a year of exposure if the node or the location turns out wrong.

**The cheap tier can't be bought for one month.** The three special-offer plans require an order of at least three months, so testing New Star for 30 days isn't an option. Sirius, Arcturus and the rest of the IPv4 + IPv6 line have no stated minimum on the tariff page.

**The refund policy is a calculation, not a window.** JustHost publishes a refund and cancellation article that works through pro-rata charges for services rendered, deductions for expenses actually incurred, and refunds back through the original payment channel. There's no "30-day money-back guarantee" line to point at, which is different from OliveVPS's 7-day guarantee or torontovps.com's 24-hour window (itself excluded for promotional plans, crypto payments and annual billing). Before you prepay a year, get the refund terms for your specific plan in writing from support. Public review pages for the JustHosting brand include complaints from users whose servers were suspended over abuse flags and who say refunds were refused; I can't tie those orders to this domain, but it's another argument for a short first payment. 👉 [Start on the monthly rate and check the terms yourself](https://justhost.asia/en/services/vps/tariffs?ref=196392)

## How the Toronto providers line up

Pure reference, since the entry prices people compare are rarely the same machine.

| Provider | Entry plan | Storage / port | Entry price | Billing and refund |
| --- | --- | --- | --- | --- |
| Cloudnium | 2 vCPU / 2 GB / 20 GB | Ceph distributed SSD, 10 Gbps-ready | $3.99/mo | Monthly; no refund window published |
| OliveVPS | 1 vCPU / 1 GB / 25 GB | Local NVMe, 1 Gbps, 1 TB | $3.99/mo | Monthly; 7-day money-back; Linux only at this tier |
| Sucura Networks | 1 vCPU / 2 GB / 55 GB | Local NVMe, 10 Gbps, 5 TB | $3.75/mo or $0.005/hr | Hourly, no minimum term, no setup fee; prices in USD |
| torontovps.com | 1 vCPU / 1 GB / 15 GB | Local NVMe, 10 Gbps, 2 TB | $5/mo | 24-hour window; excludes promos, crypto and annual |
| JustHost.asia | 1 core / 1 GB / 10 GB | NVMe, 100 Mbit unmetered | $2.21/mo ($1.77 at 12 months) | Pro-rata policy; Toronto location unconfirmed |

Read the configs, not the prices. Sucura's $3.75 buys 2 GB of RAM, 55 GB of disk and 5 TB of traffic on a 10 Gbps port. JustHost's $2.21 buys 1 GB, 10 GB and a 100 Mbit port. Per gigabyte of RAM, JustHost is roughly half the price; per megabit of port, it's an order of magnitude behind. If your workload is bandwidth-bound, the extra $1.50 to $2.80 at a Toronto-native provider is money well spent. If it's a small site or a VPN endpoint where cost is the constraint, JustHost wins on arithmetic.

The storage architecture is the other fork. Cloudnium runs distributed Ceph, which replicates blocks across nodes and self-heals when hardware fails. OliveVPS, Sucura and torontovps all use local NVMe, which is faster per operation but tied to one host. Neither is universally better; pick redundancy if a lost node would hurt, local disk if you need the IOPS and keep your own backups.

## FAQ

**How much does a Toronto VPS cost?** Between $3.75 and $5 per month for the smallest plan at the four Toronto-based providers above. JustHost starts lower at $2.21 monthly, but confirm the Canadian location before you treat it as a Toronto price.

**Does JustHost.asia have a Toronto datacenter?** Not documented on the pages I read. The brand advertises dozens of locations worldwide without listing them on the tariff page. Pick your location during checkout and get written confirmation if residency matters.

**Which plan do I need for WordPress?** Alpha Centauri at $5.21 ($4.17 on a 12-month term) for a normal site with a database. Drop to Arcturus at $4.01 if traffic is genuinely low and you keep plugins lean.

**Can I run Windows?** Not confirmed for JustHost. Ask support. Budget hosts usually restrict Windows to mid-tier plans and add a licensing fee, as OliveVPS and torontovps.com both do.

**Can I get a refund?** JustHost's policy calculates a pro-rata refund with documented deductions rather than offering a fixed money-back period. Get your plan's terms confirmed in writing before a long prepayment.

**Do I need a Canadian server for PIPEDA?** If you hold personal data covered by PIPEDA or provincial law, hosting in-country removes cross-border transfer questions from the picture. That's the strongest reason to pay Toronto prices instead of Ashburn prices.

**Will Docker and Kubernetes work?** Yes on the KVM plans. JustHost's IPv4 + IPv6 line is KVM, so Docker, Compose and K3s run natively, and the top plans ship with enough disk for a small cluster.

## Before you order

Pick by workload rather than by the lowest number. A static site or VPN endpoint: New Star at $2.21, or Sirius at $2.81 if you want IPv6 and the faster port. A WordPress site or a small app: Alpha Centauri at $5.21. Containers and multiple sites: Vega at $7.79. Memory-hungry services: Rigel at $16.20. Anything that needs a 10 Gbps port or a confirmed Toronto street address belongs with a provider that publishes both.

Four checks before you pay: whether the location picker actually offers Canada, whether the price you're looking at is the monthly or the 12-month rate, what the refund terms are for the billing period you chose, and whether 100 to 750 Mbit of fair-share port covers your traffic. Answer those and the decision takes about two minutes.

👉 [Compare the JustHost VPS plans and confirm your location before checkout](https://justhost.asia/en/services/vps/tariffs?ref=196392)
