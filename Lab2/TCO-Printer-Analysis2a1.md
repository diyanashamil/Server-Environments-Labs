# 2a-1 Total Cost of Ownership (TCO) — Printer Comparison

**Unit:** Introduction to Server Environments and Architectures
**Deliverable file:** `TCO_Printer_Comparison.xlsx`

This analysis applies the **Total Cost of Ownership** methodology to compare two
printers over a 5-year period, accounting for both fixed and variable costs, to
support a cost-based procurement decision.

---

## 1. Printers Chosen (Deliverable 1)

| | Printer A | Printer B |
|---|---|---|
| **Type** | Inkjet (entry-level / home) | Laser (office-class) |
| **Model (example)** | HP DeskJet | Brother HL-L2350DW |
| **Use case** | Personal / low volume | Workgroup / high volume |

*(Replace with your two researched models.)*

---

## 2. Cost Assumptions (Deliverable 2)

| Assumption | Value |
|---|---|
| Comparison period | 5 years |
| Pages printed per week | 750 |
| Weeks per year | 52 |
| **Total pages over period** | **195,000** |
| Printer power-on time | 40 hrs/week |
| Electricity rate | $0.30 / kWh |
| Paper cost (ream of 500) | $6.00 |

---

## 3. Expense Items — Fixed vs Variable (Deliverable 3)

| Cost | Type |
|---|---|
| Printer (hardware) | **Fixed** |
| Ink / toner cartridges | **Variable** |
| Paper | **Variable** |
| Electricity | **Variable** |

**Units consumed** are calculated automatically:
- Cartridges = Total pages ÷ cartridge yield
- Paper reams = Total pages ÷ 500
- Electricity (kWh) = (watts ÷ 1000) × hours/week × weeks × years

---

## 4. Unit Costs Sourced (Deliverable 4)

Replace the example prices in the spreadsheet's **yellow cells** with real
sourced figures and list the links here, e.g.:

- Printer price — *[source URL]*
- Ink / toner cost per cartridge — *[source URL]*
- Cartridge page yield — *[manufacturer spec URL]*
- Paper ream price — *[source URL]*
- Electricity rate — *[local provider URL]*

---

## 5. TCO Spreadsheet Model (Deliverables 5 & 6)

The spreadsheet (`TCO_Printer_Comparison.xlsx`) contains separate sheets for each
printer with the structure **Item → Type → Unit Price → Units Consumed → Total**,
plus separate Fixed and Variable subtotals, a Grand Total (TCO), and Cost per Page.

**Results with the example assumptions:**

| Metric | Inkjet (A) | Laser (B) |
|---|---|---|
| Total fixed | $80 | $150 |
| Total variable | ~$41,434 | ~$13,212 |
| **5-Year TCO** | **~$41,514** | **~$13,362** |
| **Cost per page** | **~$0.213** | **~$0.069** |

---

## 7. Break-even (Deliverable 7)

The laser costs more upfront ($150 vs $80) but far less per page. Break-even in
pages is roughly:

```
(Laser price − Inkjet price) ÷ (Inkjet cost/page − Laser cost/page)
= (150 − 80) ÷ (0.213 − 0.069)
≈ 486 pages
```

At 750 pages/week, the laser pays for its higher purchase price in **under one
week**. For a light home user printing ~5 pages/week, the same 486 pages takes
roughly **1.9 years** to reach.

---

## 8. Reflection (Deliverable 8)

**Which printer has lower TCO and why?**
The **laser** has the much lower TCO at 750 pages/week. Although it costs more to
buy, its high cartridge yield and low cost-per-page mean consumables (the largest
cost driver) are far cheaper over high volume. Inkjet ink is expensive per page,
which dominates its total cost.

**Would the choice change at only 5 pages/week?**
Yes, it could. At very low volume the total page count is tiny (about 1,300 pages
over 5 years), so consumable savings barely matter and the laser's higher purchase
price is harder to justify. For a light home user, a cheap inkjet may be the more
sensible choice.

**Other qualitative / intangible factors?**
Print speed (pages per minute), print quality (laser is sharper for text, inkjet
better for photos/colour), reliability and duty cycle, warranty and brand support,
physical size and noise, energy efficiency, and connectivity (Wi-Fi, duplex).

**For a large workgroup printer, what to prioritise?**
Pages-per-minute, monthly duty cycle, toner yield and cost-per-page, paper-tray
capacity, network features, and reliability/uptime — performance and running cost
matter more than purchase price at scale.

**Estimated break-even.**
Roughly **486 pages** — under a week at 750 pages/week, or about 1.9 years at
5 pages/week.

---

## 9. Sensitivity Analysis (Optional — Deliverable 9)

Because every input is a formula linked to the Assumptions sheet, sensitivity
testing is simple: change pages/week, cartridge price, or the electricity rate in
the yellow cells, and every total and the break-even update automatically.
For example, increasing pages/week widens the laser's advantage; lowering it
narrows or reverses it.

---

## Files in this folder
- `TCO_Printer_Comparison.xlsx` — the TCO model
- `assumptions.txt` — cost assumptions and source links (optional)
- This `README.md` — analysis and reflection
