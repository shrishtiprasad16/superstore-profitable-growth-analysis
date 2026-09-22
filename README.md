# Superstore — Profitable Growth Analysis

## Business Question

**Where should the business focus its efforts to increase revenue while protecting profitability?**

This analysis looks beyond sales growth to understand where revenue is translating into profit and where the business is losing value through low-margin products, discounting, and unprofitable customer relationships.

---

## What I Analyzed

The analysis covers:

- Sales and profit growth over time
- Category and subcategory profitability
- Regional and state-level performance
- Discounting and profit leakage
- Customer-level profitability
- Loss-making products
- Returns

I used **Excel, Python, and Power BI**, with each tool serving a different purpose rather than repeating the same analysis across all three.

### Tools

**Excel**
- Overall business performance
- Category, region, segment and subcategory analysis
- Discount analysis
- Product profitability
- Returns analysis

**Python**
- Growth decomposition
- Customer profitability risk
- Product-level loss analysis
- High-discount profitability analysis

**Power BI**
- Executive dashboard
- KPI monitoring
- Growth and profitability visualization
- Customer and subcategory risk views

---

## Business Snapshot

| Metric | Result |
|---|---:|
| Sales | **$2.33M** |
| Profit | **$292.30K** |
| Profit Margin | **12.56%** |
| Orders | **5,111** |
| Customers | **804** |

The dataset contains **10,194 transaction records** covering 2023–2026.

---

## Key Findings

### Sales growth accelerated after 2024

Sales declined **4.26% in 2024**, before increasing:

- **29.80% in 2025**
- **21.44% in 2026**

Profit also increased during this period, although profit growth slowed from **33.29% in 2025 to 16.04% in 2026**.

This made profitability an important part of evaluating the quality of the recent sales growth.

---

### Furniture generates revenue but weak profit

| Category | Sales | Profit | Margin |
|---|---:|---:|---:|
| Technology | $839.89K | $146.54K | 17.45% |
| Office Supplies | $731.89K | $126.02K | 17.22% |
| Furniture | $754.75K | $19.73K | 2.61% |

Furniture accounts for significant sales but produces a much lower margin than Technology and Office Supplies.

---

### Tables are the largest subcategory-level loss area

Tables generated:

- **$208.02K in sales**
- **-$17.75K in profit**
- **-8.53% margin**

Bookcases and Supplies also recorded negative profit.

This points to a more specific problem than simply saying Furniture is underperforming: **the business can drill down to the products and economics behind the losses.**

---

### Some high-revenue customers are not profitable

For the customer analysis, I defined:

- **High revenue:** sales of at least $5,000
- **Profitability risk:** profit margin below 10%

This identified **33 customers** generating approximately:

- **$254.25K in sales**
- **-$20.74K in profit**

Within this group, **17 customers had negative profit margins**, representing approximately **$138.79K in sales and $26.36K in losses**.

The analysis therefore looks at customer value in terms of both revenue and profitability.

---

### Higher discounts are associated with weaker profitability

Transactions with discounts above 30% generated approximately:

- **$91.8K in sales**
- **-$37.7K in profit**

The analysis uses this as a **theoretical break-even gap**, rather than assuming that the entire amount could actually be recovered.

The relationship between discounting and profitability is treated as an association, not proof of causation.

---

### Recent growth is driven more by customer and order activity

The Python analysis shows that recent sales growth is associated with:

- More customers
- More orders
- Higher orders per customer

while average order value declined.

This suggests that revenue growth should be evaluated alongside customer behavior and order economics rather than sales volume alone.

---

### Regional performance also varies

The West recorded the highest regional margin at approximately **14.98%**, while Central recorded approximately **7.92%**.

The state-level analysis identified additional loss-making markets, including Texas, Ohio, Pennsylvania and Illinois.

These areas require further investigation into the underlying product, pricing and discount mix.

---

## Recommendations

Based on the analysis, the main areas for management attention are:

1. **Protect profitable growth** rather than optimizing for revenue alone.
2. **Review Furniture profitability**, particularly Tables and other loss-making subcategories.
3. **Investigate loss-making products** to understand pricing, discounting and cost drivers.
4. **Review high-revenue, low-margin customer relationships** before prioritizing them purely based on sales.
5. **Reassess high-discount transactions** and understand where discounts are not translating into profitable sales.
6. **Investigate loss-making states** at a more granular product and customer level.
7. Use the Power BI dashboard to monitor these areas as performance changes.

---

## Dashboard

![Superstore Profitable Growth Dashboard](screenshots/dashboard.png)

The Power BI dashboard brings the main findings into one management view, including:

- Sales and profit growth
- Category profitability
- Subcategory profit leakage
- High-value customer profitability risk
- Overall business KPIs

---

## Project Structure

```text
superstore-profitable-growth-analysis/
│
├── README.md
│
├── notebooks/
│   └── Superstore_Growth_Analysis.ipynb
│
├── excel/
│   └── Superstore_Analysis.xlsx
│
├── powerbi/
│   └── Superstore_Profitable_Growth.pbix
│
└── screenshots/
    └── dashboard.png
