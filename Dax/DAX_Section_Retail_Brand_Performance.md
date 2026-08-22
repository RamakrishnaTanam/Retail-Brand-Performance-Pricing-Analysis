# DAX — Retail Brand Performance & Pricing Analytics

This project uses DAX in Power BI to create analytical fields and support brand-level pricing and profitability analysis.

## 1. Discount Percentage

Calculates the percentage discount from the marked price to the sale price.

```DAX
Discount Percentage =
DIVIDE(
    'Men+Tshirt'[Marked_Price] - 'Men+Tshirt'[Sale_Price],
    'Men+Tshirt'[Marked_Price],
    0
) * 100
```

**Purpose:** Measures the discount offered on each product.

---

## 2. Profit Percentage

Calculates profit percentage based on sale price and cost price.

```DAX
Profit % =
DIVIDE(
    'Men+Tshirt'[Sale_Price] - 'Men+Tshirt'[Cost_Price],
    'Men+Tshirt'[Sale_Price],
    0
) * 100
```

**Purpose:** Measures product-level profitability and enables brand-level profit comparisons.

---

## 3. Cost Price

Where cost price is derived from sale price and the available profit percentage:

```DAX
Cost Price =
'Men+Tshirt'[Sale_Price] *
(1 - DIVIDE('Men+Tshirt'[Profit %], 100, 0))
```

**Purpose:** Estimates the product cost from its sale price and profit percentage.

---

## 4. Average Discount %

Used in the dashboard to compare discount levels across brands.

```DAX
Average Discount % =
AVERAGE('Men+Tshirt'[Discount Percentage])
```

---

## 5. Average Profit %

Used to compare brand-level profitability.

```DAX
Average Profit % =
AVERAGE('Men+Tshirt'[Profit %])
```

---

## 6. Average Sale Price

Used to compare the average selling price of products across brands.

```DAX
Average Sale Price =
AVERAGE('Men+Tshirt'[Sale_Price])
```

---

## 7. Product Variety

Counts the number of products associated with each brand.

```DAX
Product Variety =
DISTINCTCOUNT('Men+Tshirt'[Title])
```

## DAX Skills Demonstrated

- Calculated columns
- Measures
- `DIVIDE()`
- `AVERAGE()`
- `DISTINCTCOUNT()`
- Percentage calculations
- Brand-level aggregation
- Pricing and profitability analysis

> **Note:** Update column names/formulas if your final Power BI model uses different field names or business definitions. The formulas above document the analytical logic used for this portfolio project.
