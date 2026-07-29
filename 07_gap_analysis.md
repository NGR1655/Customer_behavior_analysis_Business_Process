# Gap Analysis
### Customer Retention & Personalization Initiative

The gap analysis below compares the current state to the desired future state across key capability dimensions, and identifies what must be built or changed to close each gap. See [06_process_maps_as_is_to_be.md](06_process_maps_as_is_to_be.md) for the corresponding process flows.

| Dimension | As-Is (Current) | To-Be (Desired) | Gap / Action Needed |
|---|---|---|---|
| Segmentation | None — all customers treated the same | Segments by age, category, frequency, subscription status | Build segmentation engine (FR-1) |
| Discounting | Blanket promo codes to ~43% of customers regardless of fit | Targeted rules scoped to segments | Build rules engine + retire blanket codes (FR-2, FR-9) |
| Subscription conversion | Pitched once, at checkout only (27% enrolled) | Pitched at 3 journey points using a propensity score | Add prompts + predictive scoring (FR-8) |
| Churn / retention | No detection of lapsing customers | At-risk flag + automated win-back trigger | Build at-risk scoring + campaign automation (FR-3, FR-4) |
| Reporting | Manual, monthly, retrospective | Real-time, self-service dashboard | Build dashboard with daily refresh (FR-5, FR-6) |
| Review feedback loop | Ratings collected, unused | Ratings aggregated and surfaced to merchandising | Build alerting on low-rated categories (FR-7) |
| Governance / audit | No tracking of who changed discount rules | Full audit log of rule changes | Build audit logging (NFR-5) |

## Overall Gap Summary
The retailer already captures the data needed (demographics, purchase history, review ratings, subscription and discount flags) to close every gap above — the shortfall is entirely in **how that data is used** (segmentation, automation, and real-time reporting), not in **what is collected**. This significantly de-risks delivery, since no new data-collection process is required.
