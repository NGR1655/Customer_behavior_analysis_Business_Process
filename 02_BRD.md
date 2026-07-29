# Business Requirements Document (BRD)
### Customer Retention & Personalization Initiative

## 1. Document Purpose
This BRD defines the business-level "what" and "why" for the Customer Retention & Personalization Initiative. It is the contract between business stakeholders and the delivery team on the problem being solved and the value expected, independent of how it will be built.

## 2. Business Problem Statement
Only 27% of the retailer's customers are enrolled in the subscription/loyalty program, and discounting is applied broadly rather than as a targeted lever to convert the remaining 73%. Combined with a lack of segmentation (by age, gender, category affinity, or purchase frequency) and reporting that lags a full month behind activity, the business cannot identify which customers are at risk of churning or which are ready to convert to loyalty members — resulting in lost repeat-purchase revenue and inefficient discount spend.

## 3. Business Objectives

| ID | Objective | Target Metric |
|---|---|---|
| BO-1 | Increase subscription/loyalty enrollment | Raise subscription rate from 27% to 40%+ within 2 quarters |
| BO-2 | Improve discount efficiency | Reduce blanket discounting; increase discount-to-conversion rate by 15% |
| BO-3 | Increase repeat purchase rate | Grow average previous-purchases-per-customer trend quarter over quarter |
| BO-4 | Enable data-driven decisions | Move from monthly manual reporting to a real-time, self-service dashboard |
| BO-5 | Grow cross-category sales | Increase Footwear & Outerwear share of basket by 5 percentage points |

## 4. Scope

### In Scope
- Customer segmentation based on existing attributes (age, gender, category, frequency, previous purchases, review rating).
- Targeted discount/promo-code rules engine tied to segment and subscription status.
- Subscription conversion workflow (in-session and post-purchase prompts, win-back campaigns).
- Real-time analytics dashboard for retention, discount performance, and category mix.
- Review-rating feedback loop into merchandising/catalog decisions.

### Out of Scope
- Changes to physical store operations, payment gateway providers, or shipping carriers.
- New product categories or supplier/catalog sourcing changes.
- Loyalty program tiering/rewards redesign beyond enrollment conversion (future phase).

## 5. Assumptions & Constraints
- **Assumption:** Existing dataset fields (18 attributes) are available in a live, queryable system of record.
- **Assumption:** Marketing has the ability to send targeted email/promo campaigns.
- **Constraint:** Solution must not increase average discount depth beyond current levels — the goal is better targeting, not deeper discounting.
- **Constraint:** Any customer segmentation must comply with data privacy regulations relevant to the retailer's operating regions.

## 6. Business Requirements

| ID | Requirement | Priority |
|---|---|---|
| BR-1 | The business shall be able to segment customers by demographic and behavioral attributes. | High |
| BR-2 | The business shall be able to target discounts/promotions to specific segments rather than all customers. | High |
| BR-3 | The business shall be able to identify customers likely to churn or lapse and trigger a retention action. | High |
| BR-4 | The business shall be able to view retention, subscription, and sales performance in real time. | High |
| BR-5 | The business shall use product review ratings to inform merchandising and personalization. | Medium |
| BR-6 | The business shall increase visibility of subscription benefits at multiple points in the customer journey, not only at checkout. | Medium |

## 7. Success Metrics / KPIs
- Subscription enrollment rate (target: 27% → 40%+)
- Discount-to-purchase conversion rate for targeted vs. blanket campaigns
- Repeat purchase rate / average previous purchases per active customer
- Category mix shift (Footwear + Outerwear share of total purchases)
- Time-to-insight (monthly manual reporting → real-time dashboard availability)

## 8. Stakeholders & Sign-off

| Role | Interest | Sign-off Required |
|---|---|---|
| VP of Marketing | Campaign targeting, discount ROI | Yes |
| Head of Store Operations | Operational feasibility | Yes |
| Customer Experience Lead | Customer journey impact | Yes |
| Data / Analytics Manager | Data availability & governance | Yes |
