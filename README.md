# Gayanara E-commerce Analytics Dashboard 📊

This comprehensive analytics dashboard for **Gayanara**, a rising online fashion brand, addresses data fragmentation issues. It consolidates sales performance, operational logistics, inventory status, and marketing promo effectiveness into a single interactive platform to accelerate strategic business decision-making.

---

## 📑 Table of Contents
1. [Business Understanding](#1-business-understanding)
   * [1.1 Business Background](#11-business-background)
   * [1.2 Business Problem](#12-business-problem)
   * [1.3 Key Business Questions](#13-key-business-questions)
2. [Data Source & Schema](#2-data-source--schema)
3. [Tech Stack & Workflow](#3-tech-stack--workflow)
4. [Data Cleaning](#4-data-cleaning)
5. [Key Findings](#5-key-findings)
6. [Insights & Strategic Recommendations](#6-insights--strategic-recommendations)

---

## 1. Business Understanding

### 1.1 Business Background
Gayanara is experiencing rapid growth in digital transactions. To optimize business expansion, management requires comprehensive, real-time visibility into product sales performance, logistics supply chain efficiency, and the ROI of active marketing promotions.

### 1.2 Business Problem
*   **Data Fragmentation:** Transaction, inventory, shipping, and payment data are stored in separate silos, hindering real-time business monitoring.
*   **Inventory Risk:** Lack of clear mapping between high-demand (*fast-moving*) products and current warehouse stock levels leads to stockout and deadstock risks.
*   **Fulfillment & Return Bottlenecks:** High variance in return rates among different courier partners requires a deep logistics audit.

### 1.3 Key Business Questions
1.  What is the overall sales performance (Total Units Sold, Gross/Net Revenue, and AOV)?
2.  Which product categories and specific items constitute the top-performing and fast-moving segments?
3.  What is the success rate of order fulfillment, and how are courier partners performing?
4.  Which payment channels and promotional strategies are dominant and yield the best ROI?
5.  Which cities and regions contribute the highest revenue to focus market expansion?

---

## 2. Data Source & Schema

The project utilizes several relational tables to build the data model:

| Table Name | Description | Key Columns |
| :--- | :--- | :--- |
| `customers` | Customer profile and demographic data | `customer_id` (PK) |
| `orders` | Order transaction summaries and status | `order_id` (PK), `customer_id` (FK) |
| `order_items` | Item-level details per transaction | `item_id` (PK), `order_id` (FK), `product_id` (FK) |
| `products` | Product catalog and fashion categories | `product_id` (PK) |
| `reviews` | Customer ratings and feedback | `review_id` (PK), `order_id` (FK), `product_id` (FK), `customer_id` (FK) |

---

## 3. Tech Stack & Workflow

*   **Data Extraction & Transformation:**Power Query for initial cleaning and ETL.
*   **Data Modeling & Visualization:** Power BI.
*   **Workflow/Analysis Path:**
    ```text
    Raw Data              ──> ETL & Transformation (Excel Power Query) 
                          ──> Relational Data Modeling (Power BI) 
                          ──> Interactive Dashboard & DAX Measures 
                          ──> Business Insights & Actionable Recommendations
    ```

---

## 4. Data Cleaning

* **Customer Deduplication:** Cleanse the `customers` table by removing duplicate email entries to guarantee unique customer identifiers and accurate user metrics.
* **Text Formatting & Capitalization:** Standardized text cases in the `category` column of the `products` table (Proper Case/Capitalization) to maintain visual consistency in Power BI slicers.
* **Category Harmonization & Taxonomy Cleaning:** Standardized mixed/bilingual category terminology (e.g., mapping *celana* to *pants*, *kaos* to *shirt/t-shirt*, *aksesoris* to *accessories*, *jaket* to *jacket*) and resolved overlapping spelling variations to build a clean, unified product hierarchy.
---

## 5. Key Findings

*   **Overall Sales:** Gayanara achieved **Rp1.5bn** Gross Revenue and **Rp1.11bn** Net Revenue from **6.44K** units sold, with an Average Order Value (AOV) of **Rp498.17K**.
*   **Product Performance:** *Kaos*, *Jaket*, and *Celana* represent the top-performing categories by volume, with demand peaking in 2023–2024.
*   **Logistics & Fulfillment:** **59.2%** of total orders were successfully *delivered*. J&T and JNE handle the highest volume but also record return rates that require evaluation.
*   **Payment Preferences:** *Bank Transfer* (**30.23%**) and *E-Wallets* (*GoPay* & *OVO*) are the dominant payment channels used by customers.
*   **Geographic Spread:** Semarang, Tangerang, Pontianak, Surabaya, and Yogyakarta constitute the Top 5 revenue-generating cities.

---

## 6. Insights & Strategic Recommendations

| Analysis Area | Key Insight | Strategic Recommendation |
| :--- | :--- | :--- |
| **1. Sales & AOV** | Stable sales with solid net revenue contribution across thousands of transactions. | Continuously boost AOV through strategic product bundling and cross-selling complementary fashion items. |
| **2. Product Categories** | *Jaket* and *Celana* categories dominate market demand consistently. | Prioritize inventory procurement and marketing budgets for top-performing categories to prevent stockouts. |
| **3. Order Fulfillment** | Portions of orders still encounter cancellations and returns. | Strengthen pre-shipment Quality Control and audit logistics bottlenecks of specific courier partners. |
| **4. Payment Methods** | *Bank Transfer* and *E-Wallet* handle the vast majority of daily shopping transactions. | Launch exclusive promotion campaigns or cashback discounts in partnership with preferred payment gateway providers. |
| **5. Regional Expansion** | The highest revenue concentration is centered around Top 5 cities in and outside Java. | Optimize geo-targeted digital marketing campaigns and streamline regional delivery routes in these key markets. |

---

<p align="center">
  <i>Presented by 💻 by M. Zenna Arta Caessar</i>
</p>
