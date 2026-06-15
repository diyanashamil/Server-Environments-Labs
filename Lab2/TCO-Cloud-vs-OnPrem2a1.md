# 2a-1 Total Cost of Ownership (TCO) — Cloud vs On-Premise

**Unit:** Introduction to Server Environments and Architectures
**Deliverable file:** `Cloud_vs_OnPrem_TCO.xlsx`

This analysis applies the **Total Cost of Ownership** methodology to compare
running a single server workload (≈2 vCPU / 8GB RAM / 100GB storage, 24×7) across
three options — **on-premise hardware, AWS (EC2), and Microsoft Azure** — over a
3-year period, including monthly and yearly costs, a break-even point, and a
3-year projection.

---

## 1. Workload & Assumptions

| Assumption | Value |
|---|---|
| Projection period | 3 years (36 months) |
| Workload | 1 server: ~2 vCPU / 8GB RAM / 100GB / 24×7 |

---

## 2. Cost Components

**On-Premise (own hardware)**
- *Upfront (CapEx):* server hardware, software / OS licensing, installation & setup
- *Monthly (OpEx):* power & cooling, maintenance / support, IT admin time, facilities / network

**AWS (EC2)**
- *Monthly:* EC2 instance (24×7), EBS storage, data transfer, support plan
- No upfront cost (on-demand)

**Azure (Virtual Machine)**
- *Monthly:* VM (24×7), managed disk, bandwidth, support plan
- No upfront cost (pay-as-you-go)

---

## 3. Results (example figures)

| Metric | On-Premise | AWS | Azure |
|---|---|---|---|
| Upfront cost | $8,000 | $0 | $0 |
| Monthly cost | $120 | $300 | $310 |
| Yearly cost | $1,440 | $3,600 | $3,720 |
| **3-Year TCO** | **$12,320** | **$10,800** | **$11,160** |

- **Lowest 3-year TCO:** AWS
- **Break-even (On-Premise vs AWS):** ~44 months
- **Break-even (On-Premise vs Azure):** ~42 months

*(Replace the yellow input cells with real figures from the AWS Pricing
Calculator, Azure Pricing Calculator, and a real server quote.)*

---

## 4. Break-even & Projection

On-premise carries a large **upfront** cost but a **lower monthly** cost, while
cloud has **zero upfront** but higher recurring cost. The cumulative-cost chart
shows the on-premise line starting high and rising slowly, and the cloud lines
starting at zero and rising faster.

With the example figures the lines **cross at around 42–44 months**, meaning:
- For a **3-year horizon**, cloud (AWS) is cheapest.
- **Beyond ~3.7 years**, on-premise becomes the cheaper option.

---

## 5. Reflection

**Which option has the lowest TCO and why?**
Over the 3-year period, **AWS** has the lowest TCO. Cloud avoids the large upfront
hardware and setup cost, so even though its monthly cost is higher, the absence of
capital expenditure keeps it ahead within this time frame.

**When would on-premise win?**
On-premise has a lower monthly running cost, so the longer the server is kept, the
more its upfront cost is offset. Past the break-even point (~3.7 years here), it
becomes the cheaper option — which is why long-lived, stable workloads can favour
on-premise.

**Cloud vs on-premise — key trade-offs.**
Cloud offers no upfront cost, fast scaling, and no hardware maintenance, but costs
more per month and continues indefinitely. On-premise offers control and lower
long-term running cost, but requires capital, physical space, and in-house
maintenance, and scales slowly.

**AWS vs Azure.**
The two cloud providers are closely matched; the choice often comes down to
existing ecosystem, specific service pricing, support tier, and regional
availability rather than raw compute cost.

**Non-financial factors.**
Scalability, reliability/uptime SLAs, security and compliance, disaster recovery,
and the availability of in-house skills all influence the decision beyond cost
alone.

---

## Files in this folder
- `Cloud_vs_OnPrem_TCO.xlsx` — the TCO model (On-Prem / AWS / Azure)
- This `README.md` — analysis and reflection
