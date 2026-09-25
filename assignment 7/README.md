# Business Application: Scenario Planing tool:

## Project Overview

This project focuses on building an interactive **Scenario Planning Tool in Microsoft Excel** to help a Sales Manager evaluate the impact of different customer discount, COGS and Average Net Invoice Price (Avg NIP) assumptions on sales and profitability.

The objective is to make the discount approval process faster by allowing the Sales Manager to compare **Best Case, Realistic Case, and Worst Case** scenarios before making a decision.

> **Note:** The festival-season demand and production/logistics constraints used in this project are assumptions created specifically for this scenario-planning exercise. They are not presented as actual events or facts about AtliQ.

---

## Business Problem

Mr. Haryali, a Sales Manager at AtliQ, receives customer discount requests.

Before approving a discount, he needs to evaluate its impact on:

* Net Invoice Sales
* Post Discount
* Net Sales
* COGS
* Gross Margin
* Gross Margin Target

Manually checking these calculations for different discount and cost assumptions can take considerable time.

The goal of this Excel tool is to allow the Sales Manager to quickly evaluate different scenarios and understand their potential impact on profitability.

---

## Business Scenario

For this project, I assumed that AtliQ is entering a **festival season**.

During the festival season, major customers such as **Croma, Amazon, and Flipkart** may request higher discounts to support increased sales.

I also assumed a **production and logistics constraint** where products need to be shipped faster. This may require additional logistics resources and result in a higher COGS assumption.

This creates a business trade-off:

> **Higher Discount → Lower Net Sales**

> **Higher COGS → Lower Gross Margin**

The Scenario Planning Tool helps the Sales Manager evaluate these effects before approving a discount or COGS (freight cost + manufacturing cost + transportation cost).

---

## Objective

The tool is designed to help answer:

1. What is the impact of a proposed discount on Net Sales?
2. How does a change in COGS affect Gross Margin?
3. Does the scenario achieve the required Gross Margin Target?
4. How do the Best Case, Realistic Case, and Worst Case scenarios differ?
5. Can the Sales Manager quickly evaluate a discount request?

---

## Scenario Planning

The Excel model contains three scenarios:

| Scenario           | Description                                 |
| ------------------ | ------------------------------------------- |
| **Best Case**      | Favorable discount and COGS assumptions     |
| **Realistic Case** | Expected business conditions                |
| **Worst Case**     | Higher discount and higher COGS assumptions |

These scenarios are used to understand how changes in business assumptions can affect profitability.

---

## Key Parameters

The tool allows the user to adjust:

* **Average Net Invoice Price (Avg NIP)**
* **Discount %**
* **COGS %**
* **Gross Margin Target**

### Average Net Invoice Price

For example, suppose five products have the following Net Invoice Prices:

```text
12, 10, 3, 9, 1
```

Average NIP:

```text
(12 + 10 + 3 + 9 + 1) / 5 = 7
```

---

## Calculation Logic

The model uses the following calculation flow:

### 1. Net Invoice Sales

```text
Avg NIP × Sales Units
```

### 2. Post Discount

```text
Net Invoice Sales × Discount %
```

### 3. Net Sales

```text
Net Invoice Sales − Post Discount
```

### 4. COGS

```text
Net Sales × COGS %
```

### 5. Gross Margin

```text
Net Sales − COGS
```

### 6. vs Target

```text
Gross Margin − GM Target
```

---

## Scenario Example

The following example illustrates how the scenario calculations work.

### Assumptions

| Parameter   |     Value |
| ----------- | --------: |
| Average NIP |        $6 |
| Discount    |       50% |
| COGS        |       20% |
| GM Target   | $1,00,000 |

### Scenario Results

| Metric            |     Best Case | Realistic Case |   Worst Case |
| ----------------- | ------------: | -------------: | -----------: |
| Sales Units       |       100,000 |         50,000 |       25,000 |
| Net Invoice Sales |     $6,00,000 |      $3,00,000 |    $1,50,000 |
| Post Discount     |     $3,00,000 |      $1,50,000 |      $75,000 |
| Net Sales         |     $3,00,000 |      $1,50,000 |      $75,000 |
| COGS              |       $60,000 |        $30,000 |      $15,000 |
| Gross Margin      |     $2,40,000 |      $1,20,000 |      $60,000 |
| GM Target         |     $1,00,000 |      $1,00,000 |    $1,00,000 |
| **Vs Target**     | **$1,40,000** |    **$20,000** | **-$40,000** |

The table shows how the same business assumptions can produce different profitability outcomes under different sales scenarios.

---

## Filters / Selection

The model can be analyzed based on:

* **Customer**
* **Product**
* **Date**

This allows the Sales Manager to evaluate the scenario for different business selections.

---

## Decision-Making Flow

```text
Customer Discount Request
          ↓
Select Customer / Product / Date
          ↓
Set Discount %
          ↓
Set COGS %
          ↓
Calculate Net Sales
          ↓
Calculate Gross Margin
          ↓
Compare with GM Target
          ↓
Compare Best / Realistic / Worst Case
          ↓
Evaluate the Discount Request
```

---

## Business Insight

The scenario analysis demonstrates that discount decisions should not be evaluated only from a sales perspective.

A higher discount can reduce Net Sales, while higher COGS can further reduce Gross Margin.

In the assumed festival-season scenario, the Sales Manager therefore needs to consider both **customer discount requirements and cost conditions** before approving a discount.

---

## Skills Demonstrated

* Microsoft Excel
* Scenario Planning
* Excel Formulas
* Conditional Formatting
* Business Analysis
* Decision Support

---

## Project Outcome

The final Excel tool provides a simple way to test different business assumptions and understand their potential impact on sales and profitability.

Instead of manually checking each discount request, the Sales Manager can change the relevant assumptions and compare the **Best Case, Realistic Case, and Worst Case** scenarios.

This demonstrates how Excel can be used not only for reporting and calculations, but also as a **business decision-support tool**.

---

## Author

**Galib Mulani**

Aspiring Data Analyst | Excel | Power BI | SQL | Python

[LinkedIn](https://www.linkedin.com/in/galib-mulani-5005aa184/)

