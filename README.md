# Cheap VPS: real year-one costs, renewal traps to avoid, and when RackNerd's $1.92/month KVM plan makes sense

A usable Linux VPS now starts under $2 a month. That's the short answer most people want from a "cheap VPS" search, but the two catches that decide whether a deal is actually cheap rarely make it into the headline: almost everything at that price bills a full year upfront, and most providers at the very bottom won't refund you. This guide puts verified numbers on both catches, runs the year-one math that headline prices hide, and takes a close look at RackNerd's entry KVM plan, the cheapest RackNerd deal we could confirm at current prices.

> **Quick picks**
> - **Cheapest verified deal:** RackNerd's 512 MB KVM VPS in Los Angeles, 1 vCPU and 30 GB SSD, at **$1.92/mo billed yearly** — $23.04 for the whole year. Right size for learning Linux and running light side projects. 👉 [see RackNerd's current VPS lineup and prices](https://bit.ly/my-rn)
> - **Fewest surprises near the bottom:** InterServer, $3/mo with the price locked for life.
> - **Refund safety net:** IONOS's VPS line, 30-day money-back, intro pricing from $2/mo.

## What cheap VPS pricing actually looks like right now

Cheap VPS deals cluster into three bands, and knowing which band you're shopping in prevents most bad purchases. Under roughly $2.10 a month you're in true budget territory: smaller providers, KVM virtualization, modest specs, and annual prepayment on most plans. From $3 to $5, the extra dollars buy locked pricing, more RAM, or a managed layer. Above that, you're mostly paying for support and headroom.

The sub-$2.10 tier, with figures as currently listed:

| Provider | Entry specs | Location(s) | Price & billing | Refund listed |
| --- | --- | --- | --- | --- |
| CloudCone | 1 vCPU, 1 GB RAM, 14 GB SSD | Los Angeles | $1.66/mo, billed yearly | No |
| IONOS (VPS Linux XS) | 1 vCPU, 1 GB RAM, 10 GB NVMe | global | $2.00/mo | Yes |
| BuyVM | 0.5 GB RAM, 10 GB NVMe (Ryzen KVM) | Las Vegas, Miami, New York, Luxembourg | $2.00/mo | No |
| GreenCloudVPS | 2 vCPU, 4 GB RAM, 35 GB NVMe | Los Angeles, Amsterdam, Utah, Vietnam | $2.08/mo, billed yearly | No |

GreenCloudVPS's row deserves a second look: 4 GB of RAM at $2.08 is the strongest memory-per-dollar of the plans in this table, and the location list includes Amsterdam and two Vietnamese cities, which is uncommon at this price. BuyVM bills monthly at the bottom of the market, which lowers the commitment if you just want to try something out.

Two details in that table matter more than they first appear. Only IONOS offers a refund. And several listings tag IPv6 in the specs without mentioning a dedicated IPv4 address, which affects what you can actually host (more on that below).

## RackNerd's entry KVM plan in plain numbers

RackNerd's cheapest plan we could verify is a 512 MB KVM VPS hosted in Los Angeles: 1 vCPU, 30 GB SSD, listed at $1.92/mo when you pay for 12 months up front. That's $23.04 for the year, charged once.

| Plan | Specs | Location | Billing | Price | Order |
| --- | --- | --- | --- | --- | --- |
| KVM VPS 512 MB | 1 vCPU, 0.5 GB RAM, 30 GB SSD | Los Angeles | 12 months prepaid | $1.92/mo ($23.04/yr) | [order this plan](https://bit.ly/my-rn) |

What 512 MB actually runs: more than you'd expect, as long as you stay light. A personal proxy or tunnel, a small static site, cron jobs, a status bot, a lightweight monitoring node — all realistic. You'll want a swap file and a lean distro, because RAM is the wall you hit first at half a gigabyte. What it won't do: databases under real load, Node or Java apps with actual traffic, or a Docker host running several containers at once.

Three caveats before prepaying a year. The comparison index we pulled these figures from (dataset last refreshed in late January) lists this plan as **non-refundable**, so treat the $23.04 as spent once you click. The spec listing tags IPv6 without a dedicated IPv4 address, and if you plan to host anything reachable from the regular internet — a website, mail, most self-hosted services — confirm the address allocation at checkout before committing. And budget hosts reshuffle promotions often enough that the order page is the only number worth trusting on the day you buy; RackNerd keeps larger KVM configurations on its order pages as well, so 👉 [check RackNerd's current configurations and pricing](https://bit.ly/my-rn) for whatever's available now.

## The year-one math most roundups skip

A headline monthly price is really a statement about billing terms, and two providers can advertise similar numbers while costing very different amounts over twelve months. Here's the arithmetic on the plans above:

| Plan | Headline price | What year one costs | After that |
| --- | --- | --- | --- |
| RackNerd KVM 512 MB | $1.92/mo | $23.04, prepaid | confirm at checkout |
| CloudCone SSD VPS 1 | $1.66/mo | $19.92, prepaid | confirm at checkout |
| IONOS VPS S+ | $2/mo intro | $60 (3 months at $2, then 9 at $6) | $72/yr at $6/mo |
| InterServer | $3/mo | $36 | stays $3/mo, locked |
| Contabo 8 GB | $4.73/mo | $56.76 | no renewal increase, per listing |
| Hostinger KVM 1 | $4.99/mo | $119.76, 24 months prepaid | $11.99/mo ($143.88/yr) |

A few things jump out. IONOS's $2 is a three-month teaser on a 1-year term; the regular $6/mo rate kicks in for the remaining nine months, so year one runs $60 and every year after runs $72. Hostinger has the steepest gap in this comparison — the renewal more than doubles to $11.99/mo, and the $4.99 rate requires a 24-month commitment. InterServer's lifetime lock is what makes $3 genuinely cheap in years two and three, and Contabo's no-hike pricing explains why it keeps appearing in budget roundups despite being fully unmanaged.

For the annual-prepay deals, the tradeoff is simple: lowest possible price, money committed up front, no refund at RackNerd or CloudCone. If that trade works for you, 👉 [grab RackNerd's 512 MB KVM plan at $23.04 for the year](https://bit.ly/my-rn) and you're done paying for twelve months.

## Refunds: the fine print that splits the cheap tier

Below $3 a month, most providers keep your money once the invoice clears, so the refund column is where the real differences live.

- **30-day money-back:** IONOS across its VPS line, Hostinger, and hosting-cheap — a KVM provider whose entry plan costs more ($13.52/mo for 1 core and 1 GB, London or Dallas) but bundles daily backups, a free managed migration, and optional cPanel.
- **30 days free:** Kamatera's cloud VPS, per HowToHosting's April listing.
- **No refund listed:** RackNerd's 512 MB plan, CloudCone, BuyVM, and GreenCloudVPS in the sub-$2.10 tier. InterServer states plainly that its VPS plans carry no money-back guarantee.

The practical rule: with non-refundable providers, start with the smallest plan and scale up after you've seen real performance. InterServer's slice model is built for exactly that — each added slice brings 1 CPU, 2 GB RAM, and 40 GB SSD — though HostingAdvice's review flags a dated dashboard and no built-in terminal (SSH only), so go in comfortable with a command line.

## The $3–5 tier: paying a little more for fewer surprises

A few dollars more per month buys three different things depending on the provider: locked pricing, more RAM, or someone else handling the server.

| Provider | What you get | Price | The catch |
| --- | --- | --- | --- |
| InterServer | 1 CPU, 2 GB RAM, 40 GB SSD per slice; Linux or Windows; 450+ supported scripts | $3/mo, locked for life | dated dashboard, SSH-only access, no VPS money-back |
| Kamatera | auto-scaling cloud VPS across 24 data centers | from $4/mo | entry RAM sits around 1 GB at this price, per HowToHosting's comparison |
| Contabo | 8 GB RAM, unmanaged | $4.73/mo, no setup fee | fully unmanaged; the same roundup quotes $4.95 in its summary, so treat it as "about five dollars" |
| Ultahost | 1 GB RAM, 30 GB NVMe, fully managed | $4.80/mo | 1 GB is entry-level; you're paying for the management |
| Hostinger | 1 vCPU (AMD EPYC), 4 GB RAM, 50 GB NVMe, 4 TB traffic, AI-assisted panel | $4.99/mo on a 24-month term | renews at $11.99/mo; no phone support |

Ultahost is the rare managed option under $5 with no renewal increase — what you pay at signup is what you pay at renewal, which is genuinely uncommon at this end of the market. Hostinger's 4 GB at $4.99 is the standout RAM-to-price ratio in its band (HowToHosting calls it the best in the price range), but the 24-month commitment and the doubling renewal mean it stays cheap only if you're willing to migrate or renegotiate after two years. Kamatera fits apps that need to grow or shrink with traffic rather than sit at a fixed size.

## When a cheap VPS is the wrong tool

Four situations call for something other than a budget VPS. Self-hosted email is the first: budget IP ranges carry reputation problems that low prices can't fix, and deliverability suffers for reasons unrelated to your server's specs. Second, if you want someone handling updates, security, and troubleshooting, an unmanaged $2 box will leave you entirely on your own — Ultahost's managed plan and hosting-cheap's migration-and-backup bundle exist for that reason. Third, workloads that scale with demand fit Kamatera's auto-scaling model better than any fixed-size plan. Fourth, automation stacks that need more than a gigabyte: IONOS positions its VPS+ line at exactly this use case, with 1-click installs for tools like n8n, 2 GB of RAM at the entry tier, and unlimited traffic on a 1 Gbps connection backed by a 99.99% uptime target.

## Five checks before you order

Run through this list before paying for any budget VPS; the first item catches most people.

1. **Renewal price.** The checkout page shows what year two costs. Hostinger's KVM 1 jumps from $4.99 to $11.99; InterServer's stays at $3.
2. **Billing term and upfront total.** A "$1.92/mo" plan is really a $23.04 charge today.
3. **Refund policy.** At the bottom of the market, assume no unless it's explicitly stated.
4. **IPv4 vs IPv6.** Several sub-$2.10 listings tag IPv6 only, and anything reachable from the open internet needs an IPv4 address — confirm the allocation before paying.
5. **Performance expectations.** Shared CPU means a neighbor's spike can become your latency. InterServer caps its servers at 50% capacity to counter exactly this, and it's a fair question to ask of any provider.

## Cheap VPS FAQ

**Is a 512 MB VPS actually good for anything?**
Yes, for low-memory jobs: a personal tunnel, a small static site, cron jobs, a lightweight bot or monitoring node. Add a swap file and run a lean distro. It's the wrong size for databases, busy web applications, or multi-container Docker setups.

**Why do the cheapest plans bill yearly?**
Because annual prepayment is how those prices get that low. RackNerd's $1.92/mo and CloudCone's $1.66/mo both mean a single charge covering 12 months. Monthly billing exists at this level — BuyVM and IONOS's XS plan — but usually brings fewer resources per dollar.

**Will the price go up at renewal?**
Depends entirely on the provider. InterServer locks its price for life and Contabo's listing shows no renewal increase, while Hostinger's KVM 1 renews at $11.99 against a $4.99 signup price and IONOS's $2 teaser lasts three months. The checkout page is where the renewal figure actually appears, so read it before paying.

**Do I need to be a sysadmin to run one of these?**
For most sub-$5 plans, yes to some degree — they're unmanaged, and InterServer doesn't even ship a browser terminal. The exceptions: Hostinger's visual panel with its built-in AI assistant softens the learning curve considerably, and managed options like Ultahost handle administration for you.

## Which plan should you actually buy?

- **Lowest possible spend, light workload, comfortable in a terminal:** RackNerd's 512 MB KVM at $23.04/year is the cheapest verified deal in this entire comparison. 👉 [order RackNerd's 512 MB KVM plan](https://bit.ly/my-rn)
- **Want a refund window while you test:** IONOS, with a 30-day money-back guarantee and intro pricing from $2/mo.
- **Want pricing you can forget about for years:** InterServer at $3/mo, locked.
- **Need RAM for a real application:** Contabo's 8 GB at roughly $4.75, or Hostinger's 4 GB at $4.99 if you've accepted the renewal math.
- **Want it managed:** Ultahost at $4.80 with no renewal increase.

One last thing before you click order on any of these: confirm three items on the checkout page itself — the renewal price, the refund policy, and the IPv4 allocation. Those are the three places where budget VPS deals hide their real cost. If the RackNerd plan passes all three for your use case, it's about as cheap as a working server gets.
