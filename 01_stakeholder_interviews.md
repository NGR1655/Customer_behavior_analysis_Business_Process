# Stakeholder Interviews & Requirement Gathering

> **Note:** This document simulates stakeholder interviews. In the absence of live interview transcripts, statements below are constructed as reasonable, evidence-based assumptions derived from patterns observed in the transaction dataset — following standard BA practice of triangulating requirements from data when direct stakeholder access is limited.

## 1. Interview Summaries

### VP of Marketing — *Simulated Stakeholder*
- "We run the same seasonal promo codes for everyone. We don't know if we're discounting customers who would have bought anyway."
- "Our subscription program has been flat for two quarters. We need to know who to target and why they aren't converting."
- "I want a monthly view turned into a real-time view — by the time I see the report, the season has already changed."

### Head of Store Operations — *Simulated Stakeholder*
- "Shipping and payment options are already broad — customers aren't complaining there. My concern is repeat visits."
- "We collect a review rating on every order, but nothing happens with that data once it's stored."

### Customer Experience Lead — *Simulated Stakeholder*
- "A 20-year-old and a 65-year-old currently see the exact same discount banner. That doesn't feel right."
- "We have almost 4,000 customers and 25 average past purchases each — these are loyal-ish people we're at risk of losing quietly."

### Data / Analytics Manager — *Simulated Stakeholder*
- "The raw data (age, gender, category, discount flag, subscription flag, review rating, frequency) is all there — it's just never been operationalized into segments or triggers."

## 2. Requirement-Gathering Approach

Requirements were derived using a blended approach appropriate for a data-first engagement:

1. **Document/data analysis** — profiling the 18-column transaction dataset to identify behavioral patterns (subscription vs. discount correlation, category mix, purchase frequency distribution).
2. **Simulated structured interviews** — role-based statements above, framed around the top business pain points a retailer with this data profile would realistically raise.
3. **Assumption validation workshops** *(simulated)* — cross-checking each assumption against the dataset before writing it into a requirement, to avoid requirements the data cannot support.

## 3. Key Assumptions Carried Forward

- The dataset represents a representative sample of the retailer's active customer base and current operating process.
- "Subscription Status" reflects enrollment in a loyalty/subscription program that the business wants to grow.
- "Discount Applied" / "Promo Code Used" reflect a currently undifferentiated, rules-light discounting process (they move together in 100% of subscribed-customer records, suggesting the two are bundled rather than independently targeted).
- "Review Rating" is collected post-purchase but is not currently fed back into merchandising or personalization decisions.
- The business goal is to increase repeat purchase rate and subscription conversion without degrading the customer experience or increasing operational shipping/payment complexity.
