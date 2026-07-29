# Agile User Stories
### Customer Retention & Personalization Initiative

User stories translate the FRD (see [03_FRD.md](03_FRD.md)) into implementable, Agile-ready units of work, each with acceptance criteria for the development and QA teams.

## 1. Customer-Facing Stories

| ID | User Story | Acceptance Criteria | Priority |
|---|---|---|---|
| US-1 | As a returning customer, I want to see offers relevant to what I usually buy, so that I feel the retailer understands my preferences. | Given a logged-in customer with purchase history, when they browse, then at least one recommended offer matches their top purchase category. | High |
| US-2 | As a customer who is not yet a subscriber, I want to see the subscription benefit while browsing (not only at checkout), so that I can decide to join earlier in my journey. | Given a non-subscribed customer, when they view a product or cart, then a subscription prompt with a stated benefit is displayed. | Medium |
| US-3 | As a lapsing customer, I want to receive a relevant reminder or offer if I haven't purchased in a while, so that I don't drift away without the retailer noticing. | Given a customer flagged at-risk, when the nightly job runs, then a win-back email/promo is sent within 24 hours. | High |
| US-4 | As a customer, I want my review rating to actually influence what's shown to me, so that low-quality items are less likely to be recommended to me. | Given a category with average rating below a set threshold, when recommendations are generated, then that category's weighting is reduced. | Low |

## 2. Marketing / Analyst Stories

| ID | User Story | Acceptance Criteria | Priority |
|---|---|---|---|
| US-5 | As a marketing analyst, I want to create a discount rule scoped to a specific segment, so that I don't have to discount every customer to reach the ones I'm targeting. | Given segment criteria (e.g., Category = Footwear, Subscription = No), when I publish a rule, then only matching customers receive the promo code. | High |
| US-6 | As a marketing analyst, I want to see subscription conversion and discount ROI on one dashboard, so that I can decide where to invest promotional budget. | Given published campaigns, when I open the dashboard, then conversion rate and discount spend are shown per segment, refreshed daily. | High |
| US-7 | As a marketing analyst, I want to be alerted when a product category's average review rating drops below a threshold, so that I can flag it before it affects sales. | Given category average rating < 3.0, when the daily aggregation runs, then an alert appears in the merchandising queue. | Medium |

## 3. Store Operations / Executive Stories

| ID | User Story | Acceptance Criteria | Priority |
|---|---|---|---|
| US-8 | As a store operations manager, I want a single view of sales, category mix, and shipping preference, so that I can plan inventory and fulfillment capacity. | Given current transaction data, when I open the ops dashboard, then category mix and shipping-type distribution are shown for the selected date range. | Medium |
| US-9 | As an executive, I want a read-only summary of retention KPIs, so that I can track progress against subscription and repeat-purchase targets without needing raw data access. | Given executive role login, when the dashboard loads, then KPI summary tiles (subscription rate, repeat purchase rate) are visible with trend arrows. | Medium |
| US-10 | As a system administrator, I want every discount rule change logged, so that we can audit who targeted which segment and when. | Given any rule create/edit/delete action, when it is saved, then user ID, timestamp, and rule scope are written to an audit log. | Low |
