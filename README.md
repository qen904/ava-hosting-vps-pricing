# ava.hosting: €5 VPS or €2 app hosting? Full plan tables, real first-year cost, and the limits to check before you order

ava.hosting sells two product lines that sit on the same price ladder and suit different people. The KVM VPS line starts at **€5.00/month**. The self-hosted Cloud Apps line starts at **€2.00/month**. If your goal is to run n8n, a small database, or anything else from the app catalog without configuring a server, read the €2 line first. If you need root, a custom kernel, your own control panel or a Windows image, you want the VPS.

The company behind the domain is AvaHost, headquartered in Chișinău, Moldova, operating since 2002, with a single data center and 24/7 engineer support in English, Russian and Romanian. Its published first-response benchmark is 30 minutes. Everything below comes from the live plan pages and the official deployment guide, including the parts most listings skip: which billing period each price refers to, what the 99.9% SLA actually covers, and where the cheap entry points have strings attached.

> **Quick pick:** one app on one server, no shell access needed: **Self-hosted Start, €2.00/month** (1 vCPU, 1 GB RAM, 15 GB NVMe). Root access, custom stack or Windows: **VPS One, €5.00/month** (1 vCPU, 2 GB RAM, 25 GB NVMe, 1 Gbps port).
> 👉 [Check both plan lines and current prices on ava.hosting](https://my.ava.hosting/aff.php?aff=15562)

## KVM VPS plans: seven tiers, one annual outlier

Every VPS tier runs on Intel Xeon E5 with ECC RAM and NVMe storage, unlimited bandwidth, free DDoS protection, weekly backups included, full root access, a control panel, the 99.9% SLA and 24/7 support. Six of the seven are monthly prices. The seventh, VPS Nano, is priced per year and shows **0 Available**.

| Plan | vCPU | RAM | NVMe | Price and billing | Order |
| --- | --- | --- | --- | --- | --- |
| VPS Nano | 1 | 512 MB | 20 GB | €11.00 / year | [Order VPS Nano](https://my.ava.hosting/aff.php?aff=15562) |
| VPS One | 1 | 2 GB | 25 GB | €5.00 / month | [Order VPS One](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Basic | 2 | 4 GB | 50 GB | €10.00 / month | [Order VPS Basic](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Lucky | 2 | 6 GB | 70 GB | €15.00 / month | [Order VPS Lucky](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Power | 4 | 8 GB | 90 GB | €20.00 / month | [Order VPS Power](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Extra | 6 | 12 GB | 120 GB | €30.00 / month | [Order VPS Extra](https://my.ava.hosting/aff.php?aff=15562) |
| VPS Ultra | 8 | 16 GB | 160 GB | €40.00 / month | [Order VPS Ultra](https://my.ava.hosting/aff.php?aff=15562) |

Three details that matter more than the spec sheet:

- **VPS Nano is €11.00 per year, not per month.** It is also the only plan whose card lists a limit in red: **port 25 is closed**, so it cannot send outbound mail directly. At the time of writing the card reads 0 Available, so confirm stock before you plan around it.
- **Port speed splits at the bottom.** Nano runs a 100 Mbps port. Every other tier gets 1 Gbps.
- **The jump from Basic to Lucky is RAM-heavy, not CPU-heavy.** Both give 2 vCPU; Lucky adds 2 GB RAM and 20 GB disk for €5 more. If your workload is a Java app or a busy database, that €5 buys more than a core would.

AvaHost runs KVM with a fixed vCPU allocation and dedicated RAM per instance, and gives each VPS its own IPv4 address. Root access means you can load Plesk, cPanel, ispmanager or DirectAdmin as a paid panel, install any free panel yourself, or ask support to install one. Windows VPS uses the same KVM base and supports .NET, MSSQL and MetaTrader.

## Self-hosted Cloud Apps plans: six tiers, more disk per euro

This is the line built for the catalog at ava.hosting/cloud-apps. You buy a plan, it becomes a capacity pool in your dashboard, and you carve that pool into one or more app deployments. All six tiers include unlimited transfer.

| Plan | vCPU | RAM | NVMe | Price and billing | Order |
| --- | --- | --- | --- | --- | --- |
| Self-hosted Start | 1 | 1 GB | 15 GB | €2.00 / month | [Order Self-hosted Start](https://my.ava.hosting/aff.php?aff=15562) |
| Mini | 1 | 2 GB | 25 GB | €5.00 / month | [Order Mini](https://my.ava.hosting/aff.php?aff=15562) |
| Basic | 2 | 4 GB | 50 GB | €10.00 / month | [Order Basic](https://my.ava.hosting/aff.php?aff=15562) |
| Pro | 4 | 8 GB | 100 GB | €20.00 / month | [Order Pro](https://my.ava.hosting/aff.php?aff=15562) |
| Business | 6 | 12 GB | 150 GB | €30.00 / month | [Order Business](https://my.ava.hosting/aff.php?aff=15562) |
| Power | 8 | 16 GB | 200 GB | €40.00 / month | [Order Power](https://my.ava.hosting/aff.php?aff=15562) |

The Start card carries a "Free Trial" label, but the plan pages do not state a trial length, conditions or whether a card is required, so treat it as a label rather than a promise and check at checkout.

## Which line to buy at the same price

At four overlapping price points the Cloud Apps line gives you more disk:

| Price | VPS line | Cloud Apps line |
| --- | --- | --- |
| €20/month | VPS Power, 4 vCPU / 8 GB / 90 GB | Pro, 4 vCPU / 8 GB / 100 GB |
| €30/month | VPS Extra, 6 vCPU / 12 GB / 120 GB | Business, 6 vCPU / 12 GB / 150 GB |
| €40/month | VPS Ultra, 8 vCPU / 16 GB / 160 GB | Power, 8 vCPU / 16 GB / 200 GB |

At €10 the two are identical on paper: 2 vCPU, 4 GB RAM, 50 GB NVMe. The VPS card adds the 1 Gbps port, root access and control panel items; the Cloud Apps card adds unlimited transfer and nothing else.

Buy the VPS if you need to install packages at the system level, run a mail server, compile your own kernel modules, or use an operating system the catalog does not cover. Buy Cloud Apps if your plan is "deploy n8n, then maybe a second small app later" and you would rather not patch a server. The plan pages do not say whether both lines share identical virtualisation underneath, and the deployment guide describes Cloud Apps as allocating from a capacity pool, so treat them as separate products that happen to overlap in price.

## What the first year actually costs

The cheapest Cloud Apps entry is **€2.00/month, which is €24 for twelve months** on monthly billing. The official deployment guide, published 15 September 2026, shows a worked example where the Start plan costs **EUR 12 for the entire year** under the annual offer displayed at that time. That is half the monthly price for the same plan. Annual billing is the first thing to check at checkout, and the discount is not guaranteed to stay.

The VPS line's cheapest entry is **VPS Nano at €11.00/year**, which undercuts even the promotional Start price. Two catches: 0 Available when checked, and port 25 closed. If you need outbound mail from that box, Nano is not an option at any price.

Set against that, the difference between a €2 plan and a €5 plan is €36 a year. If the app page says your application needs 2 GB of RAM, paying €24/year for a 1 GB plan you cannot use is the expensive choice.

> Prices and discounts change. The official guidance is to use the amount shown in your configuration summary as the price for your order, so verify before paying rather than trusting a figure from an earlier article.
> 👉 [Start a Cloud Apps order and compare monthly against annual billing](https://my.ava.hosting/aff.php?aff=15562)

## Buying and deploying a Cloud App: the steps that go wrong

The official walkthrough uses n8n as the example and states the same flow applies to other catalog apps. Compressed to what you actually have to decide:

1. **Pick the app from the catalog.** Each card shows a starting price. Open the app page and read the minimum disk and memory figures, because those drive which plan is pre-selected.
2. **Accept or change the pre-selected plan.** The system defaults to the minimum recommended tier. An app with heavier requirements will show a higher starting price. For a small n8n instance the guide's example uses the Start plan.
3. **Choose the billing cycle.** This is where the annual offer appears, if there is one.
4. **Enter the promotion code on the Review & Checkout page.** That is the only place the guide puts it: confirm product and period, validate the code, then create or sign into the account, accept the terms and place the order.
5. **Open the dashboard.** You will see counts for deployed apps, running apps, and your capacity pools. Click "Deploy your first app" or "Deploy app".
6. **Work through App, then Size it, then Review.** In Size it you select the capacity pool from step 1, pick a location (leave **Best available** or choose from the list when one is offered), then allocate CPU cores, RAM and disk. The usage bars show what this deployment takes and what stays free for other apps. You also name the instance and pick a subdomain under **avahost.app**, for example `my-app.avahost.app`.
7. **Deploy, then read the email before opening the app.** The confirmation email carries the app URL and app-specific setup instructions. There is no second payment at deployment; the guide is explicit that deployment draws on capacity you already bought.

Two things people get wrong here. The resource numbers in the guide (1 vCPU, 2 GB RAM, 5 GB disk for n8n) are example values from the deployment screen, not universal minimums, so follow the app page and the dashboard validation instead. And for n8n specifically, **the first visitor has to create the owner account**: email, first name, last name, password. Until that is done, the instance is open. Open it promptly.

After deployment the app page shows status, address, assigned capacity and live usage, with stop, restart and delete controls. Depending on the app and account, tabs also cover credentials, console, logs and files, snapshots, environment variables, domains and access. Account failures go to a support ticket; the Feedback board is for suggesting apps.

> 👉 [Open the Cloud Apps order flow on ava.hosting](https://my.ava.hosting/aff.php?aff=15562)

## Limits to check before you pay

**The SLA covers power and network, not your application.** AvaHost publishes 99.9% uptime covering the core power and network layers at the Chișinău data center, plus DDoS protection on all plans. The official FAQ says plainly that it does not cover downtime caused by your own apps or software. Ask support for the full SLA document if you need the credit calculation and measurement intervals for procurement.

**DDoS mitigation is network-layer.** It filters volumetric UDP and TCP floods before they reach the host. That is the common attack type; it is not a promise about application-layer attacks.

**One location.** All data sits in the Chișinău facility. The company's argument is that Moldova's position serves both EU and CIS users from one origin, and that Moldovan data protection law is modelled on GDPR principles. No latency figures are published for other regions, and no list of alternative locations appears in the deployment guide, only the option to choose "Best available" or a listed location when available. Test latency from where your users are before committing.

**Dedicated servers need a stock check.** Bare metal starts at **€85.00/month** and tops out at **€149.00/month**, with no hypervisor layer. AvaHost states that hardware availability varies and asks you to contact pre-sales with your workload profile to confirm stock and provisioning timelines. The documented upgrade trigger is a VPS that runs out of CPU, RAM or disk speed under normal load.

**Payment and currency.** Cards (Visa, Mastercard), PayPal, bank transfer, WebMoney and 20+ cryptocurrencies including BTC, ETH and USDT. Prices are in EUR and monthly by default; you pick the billing period at checkout.

> 👉 [Confirm current plan availability and pricing before ordering](https://my.ava.hosting/aff.php?aff=15562)

## Pick by workload

- **One self-hosted app, small team, no shell needed:** Self-hosted Start at €2/month, or Mini at €5 if the app page asks for 2 GB RAM.
- **Several light apps on one bill:** Pro at €20 gives 4 vCPU, 8 GB and 100 GB to split across deployments, with the usage bars telling you what is left.
- **You need root, a panel, Windows or a mail stack:** VPS One at €5, VPS Basic at €10 for 4 GB, and only go above Basic if CPU or disk is the bottleneck rather than RAM.
- **Sustained load that a VPS cannot hold:** the dedicated range at €85 to €149, after a conversation with pre-sales.
- **Absolute lowest annual spend, no mail:** VPS Nano at €11/year, once stock exists.

Two things to confirm on the order page itself: the billing period attached to the price you are looking at, and whether the plan you want is in stock. Both change without notice, and both decide what you actually pay.

> 👉 [Compare the plans and place your order on ava.hosting](https://my.ava.hosting/aff.php?aff=15562)
