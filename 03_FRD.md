# Functional Requirements Document (FRD)
### Customer Retention & Personalization Initiative

This FRD translates the business requirements (BR-1 through BR-6, see [02_BRD.md](02_BRD.md)) into system/feature-level functional specifications — the "how" the solution will behave, independent of a specific technology stack.

## 1. Functional Requirements

| ID | Functional Requirement | Maps to BR |
|---|---|---|
| FR-1 | System shall generate customer segments using Age, Gender, Category, Frequency of Purchases, Previous Purchases, and Subscription Status as inputs. | BR-1 |
| FR-2 | System shall allow a marketing user to create a promo/discount rule scoped to one or more segments (not all customers by default). | BR-2 |
| FR-3 | System shall flag a customer as "at-risk" when Frequency of Purchases exceeds the customer's historical average interval by a configurable threshold. | BR-3 |
| FR-4 | System shall trigger an automated win-back message (email/promo) when a customer is flagged at-risk. | BR-3 |
| FR-5 | System shall present a dashboard showing subscription rate, discount usage, category mix, and average review rating, refreshed at least daily. | BR-4 |
| FR-6 | System shall allow drill-down on the dashboard by Category, Location, Season, and Subscription Status. | BR-4 |
| FR-7 | System shall aggregate Review Rating by product Category and surface low-rated categories to the merchandising queue. | BR-5 |
| FR-8 | System shall display a subscription prompt at three journey points: product browse, cart, and post-purchase — not checkout only. | BR-6 |
| FR-9 | System shall log every discount/promo issuance with the segment it targeted, for later ROI analysis. | BR-2 |
| FR-10 | System shall support role-based access: Marketing/Analyst (segment & campaign config), Store Ops (catalog & fulfillment), read-only dashboard for Executives. | BR-1–BR-4 |

## 2. Non-Functional Requirements

| ID | Category | Requirement |
|---|---|---|
| NFR-1 | Performance | Dashboard queries shall return results within 3 seconds for datasets up to 100,000 transaction records. |
| NFR-2 | Availability | Segmentation and campaign engine shall be available 99.5% of business hours. |
| NFR-3 | Data Privacy | Customer demographic data used for segmentation shall be access-controlled and comply with applicable data protection regulation. |
| NFR-4 | Usability | Dashboard shall be usable by non-technical marketing staff without SQL/reporting-tool expertise. |
| NFR-5 | Auditability | All discount rule changes and campaign triggers shall be logged with user, timestamp, and rule scope. |
| NFR-6 | Scalability | Solution shall support growth from the current ~3,900 customer records to 10x volume without redesign. |

## 3. Data Requirements
Functional behavior depends on the following data attributes, all present in the current dataset and required as system inputs:

- **Customer ID, Age, Gender** — segmentation inputs
- **Item Purchased, Category, Purchase Amount, Season, Color, Size** — product & merchandising inputs
- **Review Rating** — feedback loop input
- **Subscription Status, Discount Applied, Promo Code Used** — retention/discount engine inputs
- **Previous Purchases, Frequency of Purchases** — churn-risk / at-risk scoring inputs
- **Payment Method, Shipping Type, Location** — operational/fulfillment context (reporting only, not decisioning, per current scope)

## 4. System Interfaces (Conceptual)
- Segmentation & Rules Engine ↔ Campaign/Promo Delivery (email, on-site banner, checkout)
- Transaction Data Store → Analytics Dashboard (daily refresh, read-only)
- Review Rating Store → Merchandising Queue (threshold-based alert)
- Payment Gateway — external system, called at checkout, out of scope for modification
